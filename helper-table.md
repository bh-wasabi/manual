# Markup: **table**
- dibuja una tabla en la página

## Contexto
- identificador de la sección 
- debe ser tipo arreglo

## Parámetros
#### cols
- lista de columnas (separadas por comas)
- podemos poner el nombre de otra columna entre corchetes para indicar que hay una liga automática.

#### xsmall
- lista de anchos (separadas por comas)

#### small
- lista de anchos (separadas por comas)

#### medium
- lista de anchos (separadas por comas)

#### large
- lista de anchos (separadas por comas)

#### limit (#)
- con esta opción es posible limitar la cantidad de registros a desplegar.

#### unlink (true, false)
- con esta opción es posible eliminar los `links` de los valores de la tabla.

#### filter
- es posible seleccionar indicar un filtro adicional.
- por ejemplo: `filter="tipo=foto"`.
- es posible tener multiples filtros separados por el símbolo `&`.

#### removeEmptyCols (true, false)
- elimina las columnas que no tienen datos automáticamente.

#### checkList (true, false)
- permite cambiar la clase el en la tabla dependiendo del valor de un campo.

#### checkListField
- campo a usar, debe de ser tipo `boolean`.

#### checkListTrueClass
- clase que se pone a nivel renglón de la tabla cuando el valor en `true`.

#### checkListFalseClass
- clase que se pone a nivel renglón de la tabla cuando el valor en `false`.

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