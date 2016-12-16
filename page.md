# Markup: **page**
- diseño HTML de una página (o tab) del documento.

## Parámetros
##### name
- nombre a desplegar
- se ve cuando hay más de una sola página

##### icon
- icono a desplegar
- [lista de iconos](ion-icons.md).

##### render
- se puede ligar con un [template](template.md) especifico.
- esto sirve cuando queremos "pintar" un página basado en algo más abierto que no este representado por las secciones del documento.

##### hide (true, false)
- oculta la página
- se puede usar una [expresión](expr.md).

##### show (true, false)
- muestra la página
- se puede usar una [expresión](expr.md).

##### readOnly (true, false)
- con esta opción podemos controlar la edición de toda la página completa.
- se puede usar una [expresión](expr.md).

##### [form](form.md)
- identificador de la forma a usar en esta página.
- cuando se usa esta opción se ignora todo el contenido adicional de la página.
- puede ser una expresión.

## Facilitadores
- los objetos de tipo Markup pueden contener HTML abiertamente y sin ninguna restricción.
- [lista de facilitadores](helpers.md).
