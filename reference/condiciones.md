# Condiciones que Karel puede verificar

Este conjunto de funciones devuelven un valor lógico `TRUE` o `FALSE`
según la evaluación que Karel puede hacer de su mundo.

## Uso

``` r
frente_abierto()

frente_cerrado()

izquierda_abierto()

izquierda_cerrado()

derecha_abierto()

derecha_cerrado()

hay_cosos()

no_hay_cosos()

karel_tiene_cosos()

karel_no_tiene_cosos()

mira_al_este()

mira_al_oeste()

mira_al_norte()

mira_al_sur()
```

## Valor

Valor lógico TRUE o FALSE.

## Detalles

Las funciones `frente_abierto()`, `frente_cerrado()`,
`izquierda_abierto()`, `izquierda_cerrado()`, `derecha_abierto()` y
`derecha_cerrado()` analizan si hay paredes al frente, a la izquierda o
a la derecha de Karel. Las funciones `hay_cosos()` y `no_hay_cosos()`
analizan si hay `cosos` en la posición actual de Karel. Las funciones
`karel_tiene_cosos()` y `karel_no_tiene_cosos()` analizan si Karel tiene
`cosos` en su mochila (no visibles en la representación gráfica). Las
funciones `mira_al_este()`, `mira_al_oeste()`, `mira_al_norte()` y
`mira_al_sur()` analizan la dirección hacia la cual Karel está mirando.

## Ver también

[`generar_mundo`](https://docs.ropensci.org/karel/reference/generar_mundo.md)

## Ejemplos

``` r
generar_mundo("mundo001")

frente_abierto()
#> [1] TRUE
frente_cerrado()
#> [1] FALSE
izquierda_abierto()
#> [1] TRUE
izquierda_cerrado()
#> [1] FALSE
derecha_abierto()
#> [1] FALSE
derecha_cerrado()
#> [1] TRUE
hay_cosos()
#> [1] FALSE
no_hay_cosos()
#> [1] TRUE
karel_tiene_cosos()
#> [1] TRUE
karel_no_tiene_cosos()
#> [1] FALSE
mira_al_este()
#> [1] TRUE
mira_al_oeste()
#> [1] FALSE
mira_al_norte()
#> [1] FALSE
mira_al_sur()
#> [1] FALSE
```
