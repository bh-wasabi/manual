# Objeto: **transform**
- genera una o varias transformaciones en el documento

## Parámetros
#### id
- identificador

#### items
- es posible transformar un arreglo
- el resultado va a ser también un arreglo
- puede ser una expresión

## Sub objetos

#### [set](set.md)
- guarda un dato directamente.

#### [push](push.md)
- inserta un dato a un arreglo

#### [update](update.md)
- actualiza una sección del documento
- es posible hacer transformaciones recursivas usando nuevamente `transform` en el `update`, por ejemplo:
````
{{update section="contacto" transform="contacto"}}
````

## Ejemplos:
````
{{#transform id="resumen"}}
    {{#update sourcePath="/articulos" groupBy="alias, descripcion, unidad, precio" sum="cantidad,importe" sortBy="cantidad"}}
        {{set clave="alias"}}
        {{set descripcion="descripcion"}}
        {{set cantidad="cantidad"}}
        {{set unidad="unidad"}}
        {{set precio="precio"}}
        {{set importe="importe"}}
    {{/update}}        
{{/transform}}
````