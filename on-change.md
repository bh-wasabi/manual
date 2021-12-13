# Objeto: **onChange**
- sirve para controlar las acciones cuando un campo cambia de valor

## Parámetros

#### refresh (true, false)
- se refresca el modal de captura
- sirve para cuando necesitamos que cambie la presentación o las ayuda de captura de la forma.

#### clearFields
- con esta opción es posible borrar los valores de otros campos de la misma sección y que estén visibles en ese momento en la forma de captura.
- lista de campos separados por comas.

#### clearFieldsCondition
- es posible establecer una condición para que borre los valores.
- actualmente únicamente funciona en los `grids`.

#### getSourceDoc (true, false)
- esta opción lee el documento completo y se tiene disponible en el contexto para hacer expresiones.

#### getSourceDocAs
- es posible cambiar el nombre del objeto obtenido, por omisión es `_source`.

#### playAudio (url)
- en el caso de las encuestas orales, es posible lanzar un audio.

#### refreshApplyStatus (true, false)
- debe ser el mismo campo que tenga `applyTo` en el `grid`, para que actualice los totales.

#### forceRecalc (true, false)
- forzar el recálculo de la sección en algunos casos.

#### forceRecalcSection
- nombre de la sección a recalcular sí es otra sección.

#### action
- identificador de la acción a ejecutar.

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

#### [touch](on-change-touch.md)
- es posible actualizar una sección tipo arreglo.

#### [jQuery](jquery.md)
- ejecuta una acción en el DOM

#### [log](log.md)
- muestra en la consola un mensaje

## Ejemplos:
````
{{#onChange}}
    {{set nombre="=base.nombre"}}
{{/onChange}}

{{#onChange}}
  {{#get rate="=moneda" as="_rate"}}
    {{set tipoCambio="=_rate.value"}}
  {{/get}}
{{/onChange}}

{{onChange refresh="true"}}
````