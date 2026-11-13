# Put horizontal walls (streets)

Helper function for
[`generate_open_moves()`](https://docs.ropensci.org/karel/reference/generate_open_moves.md).
It takes the available data for a piece of horizontal wall (x and y
coordinates of its beginning point and its length) and produces a
dataset with the positions and directions of prohibited moves for Karel
because of this wall.

## Uso

``` r
put_hor_walls(x, y, lgth)
```

## Argumentos

- x, :

  y x and y coordinates of the beginning point of the wall

- lgth:

  length of the wall

## Valor

A lgth x 3 dataset with coordinates where Karel can't move and the
direction (side) towards it can't move because of this piece of
horizontal wall.
