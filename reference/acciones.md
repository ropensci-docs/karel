# Acciones que Karel puede realizar

`avanzar()`, `girar_izquierda()`, `juntar_coso()` y `poner_coso()` son
las cuatro actividades básicas que Karel sabe realizar. Si se habilitan
los superpoderes de Karel con
[`cargar_super_karel()`](https://docs.ropensci.org/karel/reference/cargar_super_karel.md),
entonces también puede `girar_derecha()` y `darse_vuelta()`.

## Uso

``` r
avanzar()

girar_izquierda()

poner_coso()

juntar_coso()

girar_derecha()

darse_vuelta()
```

## Valor

Estas funciones no devuelven nada, pero realizan cambios en el mundo de
Karel que se ven cuando se ejecutan todas las acciones con
[`ejecutar_acciones()`](https://docs.ropensci.org/karel/reference/ejecutar_acciones.md).

## Ver también

[`cargar_super_karel`](https://docs.ropensci.org/karel/reference/cargar_super_karel.md)
[`generar_mundo`](https://docs.ropensci.org/karel/reference/generar_mundo.md)
[`ejecutar_acciones`](https://docs.ropensci.org/karel/reference/ejecutar_acciones.md)

## Ejemplos

``` r
generar_mundo("mundo001")

avanzar()
juntar_coso()
girar_izquierda()
poner_coso()
if (interactive()) ejecutar_acciones()
```
