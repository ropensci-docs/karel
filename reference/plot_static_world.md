# Plot the world at a given time

This function plots Karel'w wort at the requested time. Initially, time
is 1 and with each action that Karel performs, time is incremented by
one. Current time is stored in `pkg_env$moment`. This function is useful
for debugging and to get static images to be used in the examples in the
handouts for students. It's an internal function, not thought to be used
by students, but can be used with karel:::plot_static_world().

## Uso

``` r
plot_static_world(time)
```

## Argumentos

- time:

  The requested time

## Valor

Prints the plot.

## Ejemplos

``` r
if (interactive()) karel:::plot_static_world(1)
```
