# Generate a dataset to plot Karel's figure in each time

Karel is drawn with 6 squares (body, feet, eyes and mouth) using
geom_rect(), so we need arguments xmin, xmax, ymin and ymax for each of
them. So this function takes Karel's current position (x, y) and
direction (1 east, 2 north, 3 west, 4 south) and generates the
corresponding values of xmin, xmax, ymin and ymax.

## Uso

``` r
draw_karel_df(x, y, direction, moment)
```

## Valor

A 6x7 tibble. First row is for the body, 2nd for the left foot, then
right foot, left eye, right eye and finally the mouth. Columns are xmin,
xmax, ymin, ymax, moment (time), a color (for fill) and a transparency
value (alpha)

## Detalles

This function is called repeatedly for each position of Karel through
time.
