# Turn on Karel's superpowers

After running `load_super_karel()`, Karel can also turn right and turn
around with
[`turn_right()`](https://docs.ropensci.org/karel/reference/actions.md)
and
[`turn_around()`](https://docs.ropensci.org/karel/reference/actions.md).
If these superpowers aren't loaded, then these functions won't be
available and Karel can't use them.

## Uso

``` r
load_super_karel()
```

## Valor

It doesn't return anything but attaches to the global environment the
functions
[`turn_right()`](https://docs.ropensci.org/karel/reference/actions.md)
and
[`turn_around()`](https://docs.ropensci.org/karel/reference/actions.md).

## Ver también

[`actions`](https://docs.ropensci.org/karel/reference/actions.md)
[`generate_world`](https://docs.ropensci.org/karel/reference/generate_world.md)
[`run_actions`](https://docs.ropensci.org/karel/reference/run_actions.md)

## Ejemplos

``` r
generate_world("mundo001")

load_super_karel()
turn_around()
turn_right()
if (interactive()) run_actions()
```
