# Available actions for Karel

`move()`, `turn_left()`, `pick_beeper()` y `put_beeper()` are the four
basic activities that Karel can perform. If you turn on Karel's
superpowers with
[`load_super_karel()`](https://docs.ropensci.org/karel/reference/load_super_karel.md),
then she can also `turn_right()` y `turn_around()`.

## Uso

``` r
move()

turn_left()

put_beeper()

pick_beeper()

turn_right()

turn_around()
```

## Valor

These functions don't return anything, but make changes in Karel's world
that are visible when all the actions are run through
[`run_actions()`](https://docs.ropensci.org/karel/reference/run_actions.md).

## Ver también

[`load_super_karel`](https://docs.ropensci.org/karel/reference/load_super_karel.md)
[`generate_world`](https://docs.ropensci.org/karel/reference/generate_world.md)
[`run_actions`](https://docs.ropensci.org/karel/reference/run_actions.md)

## Ejemplos

``` r
generate_world("mundo001")

move()
pick_beeper()
turn_left()
put_beeper()
if (interactive()) run_actions()
```
