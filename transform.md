# Objeto: **transform**
- genera una o varias transformaciones en el documento

## Parámetros
#### id
- identificador

## Sub objetos

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