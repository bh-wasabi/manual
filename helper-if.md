# Markup: **if**
- condiciona un bloque a si el contexto tiene valor

## Contexto
- se indica el campo u objeto a analizar si tiene valor

## Parametros
#### context
- es posible indicar un contexto diferente de otra sección del documento.

#### context="contexto"
- si se quiere forzar un contexto especifico se puede hacer con este parámetro.
- muy útil para cuando se esta dentro de un `with`
- también se puede usar el prefijo `@root.` para evitar las rutas.

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

````
{{#if context="../esTarjeta"}}
{{/if}}

{{#if context="@root.pago.esTarjeta"}}
{{/if}}

````