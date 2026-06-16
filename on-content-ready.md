# Objeto: **onContentReady**
- sirve para controlar las acciones cuando se crea un campo

## Sub objetos

#### [get](get.md)
- es posible leer el tipo de cambio o una tabla DMN antes de ejecutar el `set`.

#### [set](set.md)
- para asignar a nuevo valor a otro campo de la misma sección
- se pueden usar como contexto la sección actual, el documento remoto (cuando se usa ayudas en captura tipo `lookup`, `select` o `autocomplete`), y el documento local.
- Nota: el campo debe estar visible en la forma para que funcione.

#### [update](on-change-update.md)
- es posible actualizar una sección completa del documento.
- se tiene el documento remoto dentro del contexto.

#### [jQuery](jquery.md)
- ejecuta una acción en el DOM

#### [log](log.md)
- muestra en la consola un mensaje


