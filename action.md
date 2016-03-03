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
- `geocomplete` herramienta para buscar una dirección o establecimiento y obtener la dirección. [definición del objeto obtenido por google](google-geocomplete.md).
- `menu` podemos tener una acción que invoque a un menú.
- `attach` con esta opción podemos adjuntar archivos al documento.
- `subdoc`con esta opción es posible agregar un sub-documento (es necesario especificar `source` para que funcione y definir el botón sobre la forma modal usando `buttonFloat`).

##### modal
- identificador de la forma modal a invocar

##### label
- etiqueta a mostrar en el botón

##### source
- en el caso de sub-documentos aqui se especifica el tipo de documento a agregar.

##### color
- es posible establecer el color del botón en la acción.
- [lista de colores](colors.md).

##### menu
- identificador del menú a invocar sobre esta acción

##### hide (true, false)
- oculta la acción

##### btnSolid (true, false)
- con esta opción es posible forzar a que el botón tenga un fondo solido y no sea transparente.

##### country
- identificador del país
- esto sirve únicamente en la acción `geocomplete`

##### center
- latitud y longitud para centrar en el mapa
- esto sirve únicamente en la acción `geocomplete`

##### condition
- es una [expresión](expr.md).
- es posible condicionar la acción usando el contexto del documento.

## Sub objetos
##### [update](update.md)
- en algunas acciones es posible cambiar los campos del documento.

## Ejemplo geocomplete
````
{{#action id="cliente-direccion" hide="true" type="geocomplete" county="mx" center="23.634501,-102.552784"}}
    {{#update section="enviar" sourcePath="/"}}
        {{set nombre="@name"}}
        {{set calle="address.street"}}
        {{set colonia="address.substreet"}}
        {{set codigoPostal="address.postal_code"}}
        {{set delegacion="address.sublocality"}}
        {{set estado="address.locality"}}
        {{set pais="address.country"}}
    {{/update}}
{{/action}}
````