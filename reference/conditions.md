# Conditions that Karel can test

These group of functions return a logical value `TRUE` or `FALSE`
according to Karel's evaluation of her world.

## Uso

``` r
front_is_clear()

front_is_blocked()

left_is_clear()

left_is_blocked()

right_is_clear()

right_is_blocked()

beepers_present()

no_beepers_present()

karel_has_beepers()

karel_has_no_beepers()

facing_east()

facing_west()

facing_north()

facing_south()
```

## Valor

Logical value TRUE or FALSE.

## Detalles

The functions `front_is_clear()`, `front_is_blocked()`,
`left_is_clear()`, `left_is_blocked()`, `right_is_clear()` y
`right_is_blocked()` test if there is a wall in front of Karel, to her
left or to her right, respectively. The functions `beepers_present()`
and `no_beepers_present()` test whether there are any `beepers` at
Karel's current position. The functions `karel_has_beepers()` and
`karel_has_no_beepers()` test if Karel has any `beepers` in her bag (not
visible in the plot). The functions `facing_east()`, `facing_west()`,
`facing_north()` and `facing_south()` test the direction to which Karel
is facing right now.

## Ver también

[`generate_world`](https://docs.ropensci.org/karel/reference/generate_world.md)

## Ejemplos

``` r
generate_world("mundo001")

front_is_clear()
#> [1] TRUE
front_is_blocked()
#> [1] FALSE
left_is_clear()
#> [1] TRUE
left_is_blocked()
#> [1] FALSE
right_is_clear()
#> [1] FALSE
right_is_blocked()
#> [1] TRUE
beepers_present()
#> [1] FALSE
no_beepers_present()
#> [1] TRUE
karel_has_beepers()
#> [1] TRUE
karel_has_no_beepers()
#> [1] FALSE
facing_east()
#> [1] TRUE
facing_west()
#> [1] FALSE
facing_north()
#> [1] FALSE
facing_south()
#> [1] FALSE
```
