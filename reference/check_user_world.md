# Check user's own world

This function analyzes if a world provided by the user satisfies all
requirements.

## Uso

``` r
check_user_world(world, lang)
```

## Argumentos

- world:

  The world provided by the user. It's a list. See details in
  [`generar_mundo`](https://docs.ropensci.org/karel/reference/generar_mundo.md).

## Valor

If a misespecification is found, this function produces a stop and
provides a descriptive error message.

## Detalles

This function is called by
[`.generate_world`](https://docs.ropensci.org/karel/reference/dot-generate_world.md).
