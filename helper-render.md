# Markup: **render**
- llena un [template](template.md) para incrustarlo en alguna posición de la página.

## Contexto
- no tiene

## Parámetros
#### template
- identificador del template a usar.

#### source
- es posible llenar el template usando una colección remota.
- parámetro opcional

#### view
- identificador de la vista, local o remota.

## Sub objetos

#### [param](helper-param.md)
- es posible asignar valores a los parámetros que necesita la vista.

## Ejemplo:
````
{{#render source="_company" view="lista" template="empresas"}}
  {{param tipo="base.tipo"}}
{{/render}}

{{#template id="empresas"}}
<div>
  <h5>Empresas</h5>
  {{#each this}}
    <strong>{{base.nombre}}</strong></br>
    {{sat.rfc}}</br>
    Grupo: {{base._grupo}}</br>
    Estatus: {{base._estatus}}</br>
  {{/each}}
</div>
{{/template}}
````