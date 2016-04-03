# Objeto: **onChange**
- sirve para controlar las acciones cuando un campo cambia de valor

## Parámetros

##### refresh (true, false)
- se refresca el modal de captura
- sirve para cuando necesitamos que cambie la presentación o las ayuda de captura de la forma.

##### clearFields
- con esta opción es posible borrar los valores de otros campos de la misma sección y que estén visibles en ese momento en la forma de captura.
- lista de campos separados por comas.

##### getSourceDoc (true, false)
- esta opción lee el documento completo y se tiene disponible en el contexto para hacer expresiones.

##### getSourceDocAs
- es posible cambiar el nombre del objeto obtenido, por omisión es `_source`.

##### playAudio (url)
- en el caso de las encuestas orales, es posible lanzar un audio.

## Sub objetos
##### [set](set.md)
- para asignar a nuevo valor a otro campo de la misma sección
- se pueden usar como contexto todo el documento remoto como el documento local (cuando se usa ayudas en captura tipo `lookup`, `select` o `autocomplete`).
- Nota: el campo debe estar visible en la forma para que funcione.

##### [jQuery](jquery.md)
- ejecuta una acción en el DOM

##### [log](log.md)
- muestra en la consola un mensaje

## Ejemplo:
````
{{#onChange}}
    {{set nombre="=base.nombre"}}
{{/onChange}}

{{onChange refresh="true"}}
````