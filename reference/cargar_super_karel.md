# Habilitar los superpoderes de Karel

Luego de correr `cargar_super_karel()`, Karel también puede girar a la
derecha y darse vuelta, a través de las acciones
[`girar_derecha()`](https://docs.ropensci.org/karel/reference/acciones.md)
y
[`darse_vuelta()`](https://docs.ropensci.org/karel/reference/acciones.md).
Si no se cargan los superpoderes, estas dos funciones no están
disponibles.

## Uso

``` r
cargar_super_karel()
```

## Valor

No devuelve ningún valor, pero adjuntan al Global Environment las
funciones
[`girar_derecha()`](https://docs.ropensci.org/karel/reference/acciones.md)
y
[`darse_vuelta()`](https://docs.ropensci.org/karel/reference/acciones.md).

## Ver también

[`acciones`](https://docs.ropensci.org/karel/reference/acciones.md)
[`generar_mundo`](https://docs.ropensci.org/karel/reference/generar_mundo.md)
[`ejecutar_acciones`](https://docs.ropensci.org/karel/reference/ejecutar_acciones.md)

## Ejemplos

``` r
generar_mundo("mundo001")

cargar_super_karel()
darse_vuelta()
girar_derecha()
if (interactive()) ejecutar_acciones()
```
