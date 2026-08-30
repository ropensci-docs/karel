# Producir un gráfico del mundo de Karel en un momento dado

Esta función grafica el mundo de Karel en el momento pedido.
Inicialmente, momento toma el valor 1 y con cada acción que Karel
realiza se incrementa en 1. El momento actual está guardado en
`pkg_env$moment`. Esta función es útil para revisar el código y para
obtener imágenes estáticas que pueden usarse al crear ejemplos y
ejercicios en los materiales de estudio para los estudiantes. Es una
función interna, no está pensada para ser usada por estudiantes, pero se
puede usar con karel:::graficar_mundo_estatico().

## Uso

``` r
graficar_mundo_estatico(momento)
```

## Argumentos

- momento:

  El momento que se desea graficar.

## Valor

Imprime el gráfico.

## Ejemplos

``` r
if (interactive()) karel:::graficar_mundo_estatico(1)
```
