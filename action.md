# Objeto: **action**
- define una acción del documento
- esto funciona cuando el documento es editable.

## Parámetros
##### id
- identificador de la acción

##### type
- `open` abre el documento para editarlo.
- `close` guarda los cambios.
- `affect` guarda y afecta el documento (inicia el flujo de trabajo).
- `affect-direct` afecta y si es correcto guarda el documento, es útil para cuando se quiere validar un documento, funciona únicamente con flujos de 1 paso.
- `cancel` cancela el documento, inicia un flujo de trabajo.
- `add` agrega un detalle, abre la ventana modal asignada.
- `copy` copia el documento.
- `cancel-edit` cancela la edición.
- `geocomplete` herramienta para buscar una dirección o establecimiento y obtener la dirección. [definición del objeto obtenido por google](google-geocomplete.md).
- `menu` podemos tener una acción que invoque a un menú.
- `attach` con esta opción podemos adjuntar archivos al documento.
- `photo` abre la cámara del browser y toma una foto que se convierte en un adjunto automáticamente.
- `subdoc`con esta opción es posible agregar un sub-documento (es necesario especificar `source` para que funcione y definir el botón sobre la forma modal usando `buttonFloat`).
- `refresh` refresca el documento.
- `refresh-widgets` refresca los `widgets` del documento.
- `post` para ejecutar un `request` tipo `post` en el backend.
- `start-workflow` inicia un flujo de trabajo del documento.

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

##### copyTo
- cuando la acción es `type="copy"` aquí se especifica el tipo de documento donde se va a copiar.
- por omisión es al mismo.

##### exclude
- cuando la acción es `type="copy"` aquí se especifica la lista de secciones o la lista de `seccion.campo` a excluir en la copia.
- es una lista separada por comas.

##### visibleMode
- `open` la acción será visible únicamente al abrir el documento.
- `close` la acción será visible únicamente con el documento cerrado.
- `allways` la acción será visible siempre.

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

##### workflow
- flujo de trabajo a afectar.

##### message
- mensaje a desplegar al iniciar el flujo de trabajo.

##### postPath
- la ruta donde se va hacer el `request`
- debe ser una ruta interna.
- esto funcionan únicamente cuando es `type="post"`.

##### confirm (true, false)
- es posible confirmar la acción previo a su ejecución.

##### confirmMessage
- es posible desplegar un mensaje distinto al confirmar.
- puede ser una [expresión](expr.md).

##### confirmTitle
- titulo de la confirmación.
- puede ser una [expresión](expr.md).

##### sendDeviceDataId
- envia deviceDataId al servidor, si la acción el tipo es `affect`, `affect-direct` y `post`.
- esto sirve para poder hacer los cargos automáticos a las tarjetas de crédito.

## Sub objetos
##### [update](update.md)
- en algunas acciones es posible cambiar los campos del documento.

##### [ask](ask.md)
- si la acción es `type="post"` es posible preguntar algunos parámetros manualmente.

##### [param](param.md)
- si la acción es `type="post"` es posible pasar parámetros.

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