# Markup: **table**
- dibuja una tabla en la página

## Contexto
- identificador de la sección 
- debe ser tipo arreglo

## Parámetros
##### cols
- lista de columnas (separadas por comas)
- podemos poner el nombre de otra columna entre corchetes para indicar que hay una liga automática.

## Ejemplo:
````
{{#row class="invoice-body"}}
    {{#col medium="100%"}}
        {{#zone id="articulos" modal="articulo" modalGrid="articulos"}}
            {{table articulos cols="articulo, nombre[articulo], descripcion[factura], cantidad, precio, promociones, descuentoPct, importe"}}
        {{/zone}}
    {{/col}}
{{/row}}
````