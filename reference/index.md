# Índice del paquete

## Referencias en español

### Generar un mundo y ejecutar acciones

Todo programa debe comenzar y terminar con estas funciones.

- [`generar_mundo()`](https://docs.ropensci.org/karel/reference/generar_mundo.md)
  : Generar el mundo de Karel
- [`ejecutar_acciones()`](https://docs.ropensci.org/karel/reference/ejecutar_acciones.md)
  : Ejecutar acciones

### Acciones que Karel puede realizar

Funciones que implementan las cuatro actividades básicas que Karel sabe
realizar (avanzar, girar a la izquierda, poner y juntar “cosos”). Si se
habilitan los superpoderes de Karel, también puede girar a la derecha y
darse vuelta.

- [`avanzar()`](https://docs.ropensci.org/karel/reference/acciones.md)
  [`girar_izquierda()`](https://docs.ropensci.org/karel/reference/acciones.md)
  [`poner_coso()`](https://docs.ropensci.org/karel/reference/acciones.md)
  [`juntar_coso()`](https://docs.ropensci.org/karel/reference/acciones.md)
  [`girar_derecha()`](https://docs.ropensci.org/karel/reference/acciones.md)
  [`darse_vuelta()`](https://docs.ropensci.org/karel/reference/acciones.md)
  : Acciones que Karel puede realizar
- [`cargar_super_karel()`](https://docs.ropensci.org/karel/reference/cargar_super_karel.md)
  : Habilitar los superpoderes de Karel

### Condiciones que Karel puede verificar

Este conjunto de funciones devuelven un valor lógico TRUE o FALSE según
la evaluación que Karel puede hacer de su mundo.

- [`frente_abierto()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`frente_cerrado()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`izquierda_abierto()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`izquierda_cerrado()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`derecha_abierto()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`derecha_cerrado()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`hay_cosos()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`no_hay_cosos()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`karel_tiene_cosos()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`karel_no_tiene_cosos()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`mira_al_este()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`mira_al_oeste()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`mira_al_norte()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  [`mira_al_sur()`](https://docs.ropensci.org/karel/reference/condiciones.md)
  : Condiciones que Karel puede verificar

### Funciones internas

Selección de funciones internas que podrían ser útiles para un uso algo
más avanzado del paquete.

- [`conseguir_amb()`](https://docs.ropensci.org/karel/reference/conseguir_amb.md)
  : Obtener el ambiente de Karel
- [`graficar_mundo_estatico()`](https://docs.ropensci.org/karel/reference/graficar_mundo_estatico.md)
  : Producir un gráfico del mundo de Karel en un momento dado

## Reference in English

### Generate a world and run actions

Every program must start and end with calls to these functions.

- [`generate_world()`](https://docs.ropensci.org/karel/reference/generate_world.md)
  : Create Karel's world
- [`run_actions()`](https://docs.ropensci.org/karel/reference/run_actions.md)
  : Run actions

### Available actions for Karel

These functions implement the four basic actions that Karel can perform
(move, turn left, put and pick beepers). If Karel’s superpowers are
turned on, she can also turn right and turn around.

- [`move()`](https://docs.ropensci.org/karel/reference/actions.md)
  [`turn_left()`](https://docs.ropensci.org/karel/reference/actions.md)
  [`put_beeper()`](https://docs.ropensci.org/karel/reference/actions.md)
  [`pick_beeper()`](https://docs.ropensci.org/karel/reference/actions.md)
  [`turn_right()`](https://docs.ropensci.org/karel/reference/actions.md)
  [`turn_around()`](https://docs.ropensci.org/karel/reference/actions.md)
  : Available actions for Karel
- [`load_super_karel()`](https://docs.ropensci.org/karel/reference/load_super_karel.md)
  : Turn on Karel's superpowers

### Conditions that Karel can test

These group of functions return a logical value TRUE or FALSE according
to Karel’s evaluation of her world.

- [`front_is_clear()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`front_is_blocked()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`left_is_clear()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`left_is_blocked()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`right_is_clear()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`right_is_blocked()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`beepers_present()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`no_beepers_present()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`karel_has_beepers()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`karel_has_no_beepers()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`facing_east()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`facing_west()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`facing_north()`](https://docs.ropensci.org/karel/reference/conditions.md)
  [`facing_south()`](https://docs.ropensci.org/karel/reference/conditions.md)
  : Conditions that Karel can test

### Internal functions

Selected internal functions that could be useful to use the package in a
more advanced way.

- [`get_pkg_env()`](https://docs.ropensci.org/karel/reference/get_pkg_env.md)
  : Get Karel's environment
- [`plot_static_world()`](https://docs.ropensci.org/karel/reference/plot_static_world.md)
  : Plot the world at a given time
