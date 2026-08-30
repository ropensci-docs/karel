# Generate array which shows moves that Karel can and can't make

This function creates `open_moves`, a nx x ny x 4 array of TRUE/FALSE
values indicating if Karel can move to each direction from a given
position. For example, if Karel is in the bottom left corner, which is
cell \[1, 1\], it can't go south or left, so we have both open_moves\[1,
1, 3\] and open_moves\[1, 1, 4\] set to FALSE. Depending on the existing
walls it could move south or north, so open_moves\[1, 1, 1\] and
open_moves\[1, 1, 2\] could be TRUE or FALSE.

## Uso

``` r
generate_open_moves(nx, ny, hor_walls, ver_walls)
```

## Argumentos

- nx, :

  ny size of the world

- hor_walls, :

  ver_walls dataset of horizontal and vertical walls as described in the
  details for the function
  [`.generate_world`](https://docs.ropensci.org/karel/reference/dot-generate_world.md).

## Valor

A 6nx x ny x 4 array of TRUE/FALSE values

## Detalles

Taking into account the size of the world and the walls, this function
properly defines the array open_moves.
