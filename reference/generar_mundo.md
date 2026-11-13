# Generar el mundo de Karel

Esta función toma un "mundo" (es decir, una lista con información acerca
de su tamaño, paredes, "cosos" presentes y la ubicación y dirección de
Karel), lo grafica y prepara todo para que Karel pueda realizar sus
acciones. Siempre debe ser evaluada antes de que Karel empiece a cumplir
sus objetivos, en especial, si en algún momento hemos cometido un error,
debemos comenzar de nuevo corriendo primero esta función.

## Uso

``` r
generar_mundo(mundo)
```

## Argumentos

- mundo:

  Un carácter de largo 1 indicando el nombre de uno de los mundos que ya
  vienen en el paquete o un objeto de tipo lista con todos los
  componentes que debe tener un mundo (ver más abajo en Detalles).

## Valor

Dibuja el estado inicial del mundo de Karel y deja todo preparado para
comenzar a registrar sus acciones.

## Detalles

Luego de correr `generar_mundo()`, se ejecutan las acciones de Karel y
se pueden visualizar con la función
[`ejecutar_acciones()`](https://docs.ropensci.org/karel/reference/ejecutar_acciones.md).

El argumento `mundo` puede consistir de un mundo creado (es decir,
inventado) por cualquiera. En este caso, `mundo` debe ser una lista con
los siguientes componentes:

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

5.  `karel_x`: coordenada en el eje x para la posición inicial de Karel.

6.  `karel_y`: coordenada en el eje y para la posición inicial de Karel.

7.  `karel_dir`: dirección inicial de Karel: 1 (mira al oeste), 2 (mira
    al norte), 3 (mira al oeste) o 4 (mira al sur).

8.  `beepers_x`: vector numérico con las coordenadas en el eje x de las
    celdas donde hay cosos inicialmente. El largo de los vectores
    beepers_x, beepers_y y beepers_n debe coincidir. Si no se desea que
    haya cosos en el mundo, proveer el valor NULL.

9.  `beepers_y`: vector numérico con las coordenadas en el eje y de las
    celdas donde hay cosos inicialmente. El largo de los vectores
    beepers_x, beepers_y y beepers_n debe coincidir. Si no se desea que
    haya cosos en el mundo, proveer el valor NULL.

10. `beepers_n`: vector numérico con la cantidad de cosos que hay
    inicialmente en cada una de las posiciones determinadas por los
    valores de beepers_x y beepers_y. El largo de los vectores
    beepers_x, beepers_y y beepers_n debe coincidir. Si no se desea que
    haya cosos en el mundo, proveer el valor NULL.

11. `beepers_bag`: número de cosos que Karel tienen a disposición en su
    muchila al inicio. Karel puede poner cosos si es que tiene cosos en
    su mochila. Puede tomar el valor Inf.

## Ver también

[`acciones`](https://docs.ropensci.org/karel/reference/acciones.md)
[`ejecutar_acciones`](https://docs.ropensci.org/karel/reference/ejecutar_acciones.md)

## Ejemplos

``` r
generar_mundo("mundo001")

```
