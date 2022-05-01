# Objeto: **join**
- al resultado de una vista, se le puede unir información de otras vistas

## Parámetros
#### source
- tipo de documento a unir.

#### view
- nombre de la vista a unir.

#### as
- con este nombre va a quedar anexada la información que vamos a leer.

#### first (true, false)
- devuelve el primer registro del arreglo, cuando son múltiples.

#### id
- se puede definir el parámetro _id directamente para que el `join` sea más directo.

#### filter
- en algunos casos es posible poner un filtro adicional, tipo campo=valor,campo2=valor2

## Sub objetos

#### [param](param.md)
- parámetros para usar en la sub vista.

## Ejemplo:
Vista que se quiere jalar:
````
{{#view id="sub-conteo"}}
  {{define type="param" id="parentType"}}
  {{define type="param" id="parentId"}}
  {{#pipeline}}
    {{filter field="_parent.type" eq="parentType"}}
    {{filter field="_parent.id" eq="parentId"}}      
    {{group type="count" as="conteo"}}
  {{/pipeline}}  
{{/view}}
````

Vista principal con el `join`:
````
{{#view id="lista"}}
  {{#find}}
    {{include field="base.nombre"}}
    {{include field="base.tipo"}}
    {{include field="base.estatus"}}
    {{include field="base.fechaAlta"}}
    {{sort field="base.nombre"}}
    {{search field="base.nombre"}}
  {{/find}}
  {{#join source="contacto" view="sub-conteo" as="contactos" first="true"}}
    {{param parentType="_type"}}
    {{param parentId="_id"}}
  {{/join}}
  {{editor display="base.nombre"}}
{{/view}}
```