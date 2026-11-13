# Ejecutar acciones

Esta función produce la animación que muestra todas las acciones
realizadas por Karel desde que su mundo fue generado con
`generar_mundo`.

## Uso

``` r
ejecutar_acciones(repetir = FALSE)
```

## Argumentos

- repetir:

  Valor lógico TRUE o FALSE que indica si la animación debe repetirse
  una y otra vez luego de finalizada (por defecto: FALSE).

## Valor

Produce una animación con `gganimate`.

## Ver también

[`generar_mundo`](https://docs.ropensci.org/karel/reference/generar_mundo.md)

## Ejemplos

``` r
generar_mundo("mundo001")

avanzar()
juntar_coso()
girar_izquierda()
poner_coso()
if (interactive()) ejecutar_acciones()
```
