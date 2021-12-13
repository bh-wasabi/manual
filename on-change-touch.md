# Objeto: **touch** (onChange)
- actualiza una sección tipo arreglo

## Parámetros
#### section
- sección del documento a actualizar.

## Sub objetos

#### [set](set.md)
- actualiza el valor de uno o varios campos.

## Ejemplos:
`````
{#touch section="alimentacionPacientesLote"}}
  {{set alimentacionDia="=fn('alimentacionDia', calc.findWhere(_remoteScope.menuDia, {regimenAlimenticio: regimenAlimenticio}))"}}
{{/touch}}
`````