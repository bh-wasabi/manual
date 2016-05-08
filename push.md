# Objeto: **push**
- inserta manualmente un objeto a una sección tipo arreglo.

## Parámetros
#### value
- con esta opción es posible asignar todo el objeto junto.

##### condition
- con esta opción es posible condicionar la acción.

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
  {{push value="{articulo: 'A3', cantidad: 3, precio: 1500}"}}
{{/create}}
`````