# Objeto: **push**
- inserta manualmente un objeto a una sección tipo arreglo.

## Parámetros
- no tiene parámetros

## Sub objetos

##### [set](set.md)
- asigna los valores del objeto.

## Ejemplo:
`````
{{#create section="articulos"}}              
  {{#push}}
    {{set articulo="A1" cantidad="1" precio="=500*2"}}
  {{/push}}
  {{#push}}
    {{set articulo="A2" cantidad="2" precio="=600*2"}}
  {{/push}}
{{/create}}
`````