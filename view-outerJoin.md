# Objeto: **outerJoin**
- es posible unir el resultado de la vista con un preset y así poder obtener todos los registros del preset, junto con el documento que le corresponde.

## Parámetros
#### preset
- tipo de documento a unir.

#### as
- con este nombre va a quedar anexada la información que vamos a leer.

## Sub objetos

#### [param](param.md)
- parámetros para usar en la sub vista.

## Ejemplo:
````
{{#view id="lista"}}
  {{#find}}
    {{include field="base.nombre"}}
    {{include field="base.tipo"}}
    {{include field="base.estatus"}}
    {{include field="base.fechaAlta"}}
    {{include field="base.central"}}
    {{sort field="base.nombre"}}
    {{search field="base.nombre"}}
  {{/find}}
  {{#outerJoin preset="app.centrales" as="central"}}
    {{param id="base.central"}}
  {{/outerJoin}}
  {{editor display="base.nombre"}}
{{/view}}
```