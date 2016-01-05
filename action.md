# Objeto: **action**
- define una acción del documento
- esto funciona cuando el documento es editable.

## Parámetros
##### id
- identificador de la acción

##### type
- `open` abre el documento para editarlo.
- `close` guarda los cambios.
- `affect` afecta el documento (tiene que estar en un proceso).
- `add` agrega un detalle, abre la ventana modal asignada.
- `cancel-edit` cancela la edición.
- `geocomplete` herramienta para buscar una dirección o establecimiento y obtener la dirección.
- `menu` podemos tener una acción que invoque a un menú.

##### modal
- identificador de la forma modal a invocar

##### label
- etiqueta a mostrar en el botón

##### menu
- identificador del menú a invocar sobre esta acción

##### hide (true, false)
- oculta la acción

##### country
- identificador del país
- esto sirve únicamente en la acción `geocomplete`

##### center
- latitud y longitud para centrar en el mapa
- esto sirve únicamente en la acción `geocomplete`

## Sub objetos
##### [update](update.md)
- en algunas acciones es posible cambiar los campos del documento.

