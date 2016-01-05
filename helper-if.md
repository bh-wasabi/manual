# Markup: **if**
- condiciona un bloque a si el contexto tiene valor

## Contexto
- se indica el campo u objeto a analizar si tiene valor

## Ejemplo:
En este caso si el campo "esTarjeta" tiene es verdadero, despliega todo el bloque en la pantalla.
````
{{#if esTarjeta}}
  {{label tarjetaTipo}}
  {{br}}{{label tarjetaNumero}}
  {{br}}{{label tarjetaNombre}}
  {{br}}Vencimiento:
  {{br}}{{label tarjetaCodigo}}
  {{hairline}}
  {{label tarjetaDireccion}}
  {{br}}
  {{br}}{{label tarjetaCodigoPostal}}
  {{br}}{{label tarjetaEstado}}
  {{br}}{{label tarjetaPais}}
{{/if}}
````