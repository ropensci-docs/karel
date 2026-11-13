# Obtener el ambiente de Karel

Esta función devuelve un ambiente (R environment) llamado pkg_env, que
es creado por el paquete. Se puede usar para probar el funcionamiento
del paquete. Es una función interna, no está pensada para ser usada por
estudiantes, pero se puede usar con karel:::conseguir_amb().

## Uso

``` r
conseguir_amb()
```

## Valor

Un ambiente de R con objetos que representan al mundo de Karel.

## Detalles

`pkg_env` es un ambiente de R creado dentro del paquete para guardar y
compartir entre las funciones todos los objetos relacionados con el
mundo de Karel y su estado en cada momento. Dado que estas funciones que
usan los estudiantes deben ser simples y no usar argumentos (como, por
ejemplo,
[`avanzar()`](https://docs.ropensci.org/karel/reference/acciones.md))
estas funciones modifican internamente a `pkg_env` para implementar cada
acción.

Los componentes de este ambiente son:

1.  `nx`: tamaño del mundo de Karel, número de celdas en el eje x

2.  `ny`: tamaño del mundo de Karel, número de celdas en el eje x

3.  `hor_walls`: un data.frame con una fila por cada pared horizontal
    que hay en el mundo de Karel y 3 columnas: x (coordenada del inicio
    de la pared en el eje x), y (coordenada del inicio de la pared en el
    eje y), lgth (longitud de la pared, en cantidad de celdas que
    abarca). Si toma el valor NULL, no hay paredes horizontales en el
    mundo.

4.  `ver_walls`: un data.frame con una fila por cada pared vertical que
    hay en el mundo de Karel y 3 columnas: x (coordenada del inicio de
    la pared en el eje x), y (coordenada del inicio de la pared en el
    eje y), lgth (longitud de la pared, en cantidad de celdas que
    abarca). Si toma el valor NULL, no hay paredes verticales en el
    mundo.

5.  `open_moves`: un arreglo de dimensión nx x ny x 4 de valores
    TRUE/FALSE que indica si Karel puede moverse en cada dirección desde
    una posición determinada. Para ejemplo, si Karel está en la esquina
    inferior izquierda, que es la celda \[1, 1\], no puede ir al sur ni
    a la izquierda, por lo que tenemos open_moves\[1, 1, 3\] y
    open_moves\[1, 1, 4\] establecido en FALSO. Dependiendo de las
    paredes existentes podría moverse al sur o al norte, por lo que
    open_moves\[1, 1, 1\] y open_moves\[1, 1, 2\] puede ser VERDADERO o
    FALSO. Teniendo en cuenta el tamaño del mundo y la paredes, este
    arreglo es creado por la función interna
    [`generate_open_moves`](https://docs.ropensci.org/karel/reference/generate_open_moves.md).

6.  `karel`: un data.frame con una fila para cada momento, en el que se
    registra cada estado de Karel a lo largo de la ejecución de sus
    acciones. Tiene 4 columnas: karel_x (coordenada de Karel en el eje
    x), karel_y (coordenada de Karel en el eje y), karel_dir (dirección
    a la que mira Karel, 1 este, 2 norte, 3 oeste o 4 sur), y moment
    (valor entero indicando cada momento).

7.  `dir_now`: dirección en la cual Karel está mirando ahora.

8.  `x_now`: coordenada en el eje x actual de Karel.

9.  `y_now`: coordenada en el eje y actual de Karel.

10. `moment`: momento actual (valor entero).

11. `beepers_any`: cantidad total de cosos presentes en el mundo en este
    momento.

12. `beepers_bag`: número de cosos que Karel tienen a disposición en su
    muchila ahora. Karel puede poner cosos si es que tiene cosos en su
    mochila. Puede tomar el valor Inf.

13. `beepers_now`: un data.frame con tantas filas como celdas con cosos
    haya en el mundo y 5 columnas: `x` y `y` para las coordenadas de la
    celda, `cell` es el número de la celda contando como celda número 1
    la celda en la esquina inferior izquierda y yendo hacia arriba por
    fila (lo que significa que la celda número 2 sería la celda en las
    coordenadas x=2 e y=1), `n` el número de cosos en esta celda y
    `moment` el momento al cual corresponde este estado del mundo. Es
    creado por la función interna
    [`create_beepers`](https://docs.ropensci.org/karel/reference/create_beepers.md).

14. `beepers_all`: un data.frame con la misma estructura que
    `beepers_now`. Mientras que `beepers_now` solo tiene el estado
    actual de cosos, `beepers_all` acumula todos los estados para la
    animación, uniendo las filas de `beepers_now` y `beepers_all`
    después de cada acción.

15. `base_plot`: gráfico inicial del mundo, con su tamaño y todas las
    paredes si las hay. No muestra a Karel ni a los cosos, ya que estos
    pueden cambiar con el tiempo. Este es el gráfico base que es
    utilizado más tarde para producir la animación. Este gráfico es
    creado por la función interna
    [`plot_base_world`](https://docs.ropensci.org/karel/reference/plot_base_world.md).

## Ejemplos

``` r
generar_mundo("mundo001")

if (interactive()) karel:::conseguir_amb()
```
