# Check the walls user's provided world

This is a helper function to check ver_walls and hor_walls. It's called
by check_user_world twice.

## Uso

``` r
check_walls(dataset, name, nx, ny, lang)
```

## Argumentos

- dataset:

  Either hor_walls or ver_walls

- name:

  Character string: "hor_walls" or "ver_walls"

- nx, :

  ny Size of the world

- lang:

  language code (such as "en" or "es") for printing messages

## Valor

If a misespecification is found, this function produces a stop and
provides a descriptive error message.
