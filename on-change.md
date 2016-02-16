# Objeto: **onChange**
- sirve para controlar las acciones cuando un campo cambia de valor

## Parámetros

##### refresh (true, false)
- se refresca el modal de captura
- sirve para cuando necesitamos que cambie la presentación o las ayuda de captura de la forma.

##### playAudio (url)
- en el caso de las encuestas orales, es posible lanzar un audio.

## Sub objetos
##### set
- para asignar a nuevo valor a otro campo de la misma sección
- el contexto incluye la información de la ayuda en captura

## Ejemplo:
````
{{#onChange}}
    {{set nombre="=base.nombre"}}
{{/onChange}}

{{onChange refresh="true"}}
````