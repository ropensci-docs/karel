# Get Karel's environment

This function returns the environment called pkg_env created by the
package. It's useful for debugging and checking. It's an internal
function.

## Uso

``` r
.get_pkg_env()
```

## Valor

An enviroment with objects that represent Karel's world.

## Detalles

`pkg_env` is an environment created inside the package to store and
share between functions all the objects related to Karel's world and its
state. Since the functions that will be used by the students should be
simple and without arguments (for example,
[`move()`](https://docs.ropensci.org/karel/reference/actions.md)), these
functions modify internally `pkg_env`.

The components of this environment are:

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

5.  `open_moves`: a nx x ny x 4 array of TRUE/FALSE values indicating if
    Karel can move to each direction from a given position. For example,
    if Karel is in the bottom left corner, which is cell \[1, 1\], it
    can't go south or left, so we have both open_moves\[1, 1, 3\] and
    open_moves\[1, 1, 4\] set to FALSE. Depending on the existing walls
    it could move south or north, so open_moves\[1, 1, 1\] and
    open_moves\[1, 1, 2\] could be TRUE or FALSE. Taking into account
    the size of the world and the walls, this array is created by the
    internal function
    [`generate_open_moves`](https://docs.ropensci.org/karel/reference/generate_open_moves.md).

6.  `karel`: a data.frame with a row for each moment, in which each
    state of Karel is recorded throughout the execution of its actions.
    It has 4 columns: karel_x (Karel's x-axis coordinate), karel_y
    (Karel's y-axis coordinate), karel_dir (the direction Karel is
    facing, 1 east, 2 north, 3 west, or 4 south), and moment (integer
    value indicating each moment).

7.  `dir_now`: current Karel's facing direction.

8.  `x_now`: x-axis coordinate of Karel's current position.

9.  `y_now`: y-axis coordinate of Karel's current position.

10. `moment`: current moment (integer value).

11. `beepers_any`: total amount of beepers present in the world at this
    moment.

12. `beepers_bag`: number of beepers that Karel has available in its bag
    at the moment. Karel can put beepers if it has beepers in its bag.
    It can take the value Inf.

13. `beepers_now`: a data.frame with as many rows as cells with beepers
    in the world and 5 columns: `x` and `y` for the coordinates of the
    cell, `cell` is the number of the cell counting as cell number 1 the
    cell in the bottom left corner and going upwards by row (meaning
    cell number 2 would be the cell in coordinates x=2 and y=1), `n` the
    number of beepers in this cell and `moment` the moment in which this
    state of the world corresponds to. It is created by the internal
    function
    [`create_beepers`](https://docs.ropensci.org/karel/reference/create_beepers.md).

14. `beepers_all`: a data.frame with the same structure as
    `beepers_now`. While `beepers_now` only has current state of
    beepers, `beepers_all` acummulates all states for the animation,
    binding the rows of `beepers_now` and `beepers_all` after each
    action.

15. `base_plot`: the initial plot of the world, with its size and all
    the walls if there are any. It doesn't show Karel or the beepers,
    since those things can change with time. This is the base plot that
    is used later to produce the animation. This plot is created by the
    internal function
    [`plot_base_world`](https://docs.ropensci.org/karel/reference/plot_base_world.md).
