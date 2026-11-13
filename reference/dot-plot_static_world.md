# Plot the world at a given time

This function plots Karel'w wort at the requested time. Initially, time
is 1 and with each action that Karel performs, time is incremented by
one. Current time is stored in `pkg_env$moment`. This function is useful
for debuggint and to get static images to be used in the examples in the
handouts for studentes.

## Uso

``` r
.plot_static_world(time, lang)
```

## Argumentos

- time:

  The requested time

- lang:

  language code (such as "en" or "es") for printing messages

## Valor

Prints the plot.
