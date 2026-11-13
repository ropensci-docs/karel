# Create Karel's world

This function takes a "world" (i.e. a list with data about its size,
walls, beepers and Karel's position and direction), plots it and
prepares everything so that Karel can start performing actions in it. It
must be run always before Karel starts working on her goals, especially
if we have made a mistake, we must start all over again by first running
this function.

## Uso

``` r
generate_world(world)
```

## Argumentos

- world:

  Character vector of length 1 with the name of one of the provided
  worlds in the package or a list provided by the user with all the
  components that a world needs (see more below in details).

## Valor

Plots the initial state of Karel's world and prepares everything to
start recording her actions.

## Detalles

After running `generate_world()`, we can run Karel's actions and finally
visualize it all with the function
[`run_actions()`](https://docs.ropensci.org/karel/reference/run_actions.md).

Argument `world` can be create by the user. In this case, it must be a
list with the following components:

1.  `nx`: size of Karel's world, number of cells in x-axis.

2.  `ny`: size of Karel's world, number of cells in y-axis.

3.  `hor_walls`: a data.frame with a row for each horizontal wall in
    Karel's world and 3 columns: x (coordinate of the start of the wall
    in the x axis), y (coordinate of the start of the wall in the y
    axis), lgth (length of the wall, in number of cells it covers). If
    it is NULL, there are no horizontal walls in the world.

4.  `ver_walls`: a data.frame with a row for each vertical wall in
    Karel's world and 3 columns: x (coordinate of the start of the wall
    in the x axis), y (coordinate of the start of the wall in the y
    axis), lgth (length of the wall, in number of cells it covers). If
    it takes the value NULL, there are no vertical walls in the world.

5.  `karel_x`: x-coordinate for Karel's initial position.

6.  `karel_y`: y-coordinate for Karel's initial position.

7.  `karel_dir`: Karel's starting direction: 1 (facing west), 2 (facing
    north), 3 (facing west), or 4 (facing south).

8.  `beepers_x`: Numeric vector with the x-axis coordinates of the cells
    where there are beepers initially. The length of the vectors
    beepers_x, beepers_y and beepers_n must match. If you don't want
    beepers in the world, supply the value NULL.

9.  `beepers_y`: Numeric vector with the coordinates in the y-axis of
    the cells where there are beepers initially. The length of the
    vectors beepers_x, beepers_y and beepers_n must match. If you don't
    want beepers in the world, supply the value NULL.

10. `beepers_n`: numeric vector with the number of beepers that are
    initially in each of the positions determined by the values of
    beepers_x and beepers_y. The length of the vectors beepers_x,
    beepers_y and beepers_n must match. If you don't want beepers in the
    world, supply the value NULL.

11. `beepers_bag`: number of beepers that Karel has available in its bag
    at the beginning. Karel can put beepers if it has beepers in its
    bag. It can take the value Inf.

## Ver también

[`actions`](https://docs.ropensci.org/karel/reference/actions.md)
[`run_actions`](https://docs.ropensci.org/karel/reference/run_actions.md)

## Ejemplos

``` r
generate_world("mundo001")

```
