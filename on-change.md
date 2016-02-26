# Objeto: **onChange**
- sirve para controlar las acciones cuando un campo cambia de valor

## Parámetros

##### refresh (true, false)
- se refresca el modal de captura
- sirve para cuando necesitamos que cambie la presentación o las ayuda de captura de la forma.

##### clearFields
- con esta opción es posible borrar los valores de otros campos de la misma sección y que estén visibles en ese momento en la forma de captura.
- lista de campos separados por comas.

##### playAudio (url)
- en el caso de las encuestas orales, es posible lanzar un audio.

## Sub objetos
##### [set](set.md)
- para asignar a nuevo valor a otro campo de la misma sección
- el contexto incluye la información de la ayuda en captura

##### [update](update.md)
- es posible afectar otros campos de otras secciones.

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