# Objeto: **graph**
- configura las relaciones para afectar la base de datos GraphDB.
- el nodo que genera este tipo de documento y como se relaciona con otros tipos de documentos.

## Parámetros
- no tiene parámetros

## Sub objetos

#### node
- se definen todos los campos (importantes del documento) que queremos tener en el nodo, usando el comando [set](set.md).

#### [relation](graph-relation.md)
- descripcion

# Ejemplo:
````
{{#graph}}
    {{#node}}
        {{set nombre="movimiento.nombre"}}
        {{set fecha="movimiento.fecha"}}
        {{set moneda="movimiento.moneda"}}
        {{set total="totales.total"}}
    {{/node}}
    {{#relation from="cliente" name="VENDIDO" section="cliente" field="cliente"}}
        {{set fecha="movimiento.fecha"}}
    {{/relation}}
    {{#relation to="articulo" name="CONTIENE" section="articulos" field="articulo"}}
        {{set fecha="movimiento.fecha"}}
        {{set cantidad="cantidad"}}
    {{/relation}}
{{/graph}}
````
