# Create dataset about beepers

Given the elements provided in the world, this function generates a
dataset with info about the beepers present in the world. This function
is called from
[`generar_mundo()`](https://docs.ropensci.org/karel/reference/generar_mundo.md).

## Uso

``` r
create_beepers(nx = NULL, pos_x = NULL, pos_y = NULL, n = NULL, moment = 1)
```

## Argumentos

- nx:

  horizontal size of the world

- pos_x, :

  pos_y vectors of coordinates of cells with non-zero amount of beepers

- n:

  number of beepers in each cell indicated by coordinates in `pos_x` and
  `pos_y`

- moment:

  time

## Valor

A tibble with as many rows as cells with beepers in the world and 5
columns: `x` and `y` for the coordinates of the cell, `cell` is the
number of the cell counting as cell number 1 the cell in the bottom left
corner and going upwards by row (meaning cell number 2 would be the cell
in coordinates x=2 and y=1), `n` the number of beepers in this cell and
`moment` the moment in which this state of the world corresponds to.
