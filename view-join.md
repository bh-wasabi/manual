# Objeto: **join**
- al resultado de una vista, se le puede unir información de otras vistas

## Parámetros
##### source
- tipo de documento a unir.

##### view
- nombre de la vista a unir.

##### as
- con este nombre va a quedar anexada la información que vamos a leer.

##### first (true, false)
- devuelve el primer registro del arreglo.

## Sub objetos

##### [param](param.md)
- parámetros para usar en la sub vista.

## Ejemplo:
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