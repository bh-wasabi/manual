# Objeto: **transform**
- genera una o varias transformaciones en el documento

## Parámetros
#### id
- identificador

## Sub objetos

#### [update](update.md)
- actualiza una sección del documento

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