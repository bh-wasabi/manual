# Markup: **page**
- diseño HTML de una página (o tab) del documento.

## Parámetros

#### id
- identificador de la página
- opcional

#### name
- nombre a desplegar
- se ve cuando hay más de una sola página

#### icon
- icono a desplegar
- [lista de iconos](ion-icons.md).

#### saveHtml (true, false)
- guarda el `HTML` en el documento.
- puede usar el `id` de la página como llave.

#### render
- se puede ligar con un [template](template.md) especifico.
- esto sirve cuando queremos "pintar" un página basado en algo más abierto que no este representado por las secciones del documento.

#### hide (true, false)
- oculta la página
- se puede usar una [expresión](expr.md).

#### show o condition (true, false)
- muestra la página
- se puede usar una [expresión](expr.md).

#### readOnly (true, false)
- con esta opción podemos controlar la edición de toda la página completa.
- se puede usar una [expresión](expr.md).

#### attachSection 
- es posible cambiar la sección del documento al momento de generar un adjunto cuando se esta seleccionada la página.

#### attachLabel
- es posible modificar el título de la ventana de adjuntos cuando se esta seleccionada la página.

#### blockAttach (true, false)
- con esta opción se puede bloquear la acción de adjuntar de esta página.

#### [form](form.md)
- identificador de la forma a usar en esta página.
- cuando se usa esta opción se ignora todo el contenido adicional de la página.
- puede ser una expresión.

## Facilitadores
- los objetos de tipo Markup pueden contener HTML abiertamente y sin ninguna restricción.
- [lista de facilitadores](helpers.md).

