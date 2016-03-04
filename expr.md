# expresiones

## javascript
- la expresión debe estar en el lenguaje javascript.

## contexto evaluación
- hay que tomar en cuenta cual es el contexto de evaluación, varia en cada caso.
- normalmente se tiene acceso al documento completo

## contextos adiciones
- `moment` basado en la libreria de [Moment.js](http://momentjs.com).
- `numeral` basado en la libreria de [Numeral.js](http://numeraljs.com/).
- `functions` [lista de funciones](functions.md).

## otras consideraciones importantes
- si se agrega un "=" previo, se forza a que el evaluador considere que es una expresión.
- si se usa @ para es equivalente a usar "this".
- Nota: cuando no es seguro al 100% que exista una propiedad de un objeto (directa) es muy recomendable usar el prefijo `this.` o `@`, si se usa el prefijo de la sección no hay este problema.
- Nota: cuando la expresión puede regresar multiples resultados, hay que poner la palabra reservada "return" antes, por ejemplo: `=if (a>b) {return a} else {return b}`
 

## contextos especiales
- en el documento pueden existir algunos parámetros adiciones bajo la sección `_options`.
- `isVertical` es verdadero si la forma se abrió en forma vertical.
- `isSubDoc`  es verdadero si el documento se abrió como sub-documento de otro.
- `browserId` identificador del `browser` actual que esta abriendo el documento.
- `inbox` sección de la colección `_inbox` con información del inbox actual. 
- `workflow` sección de la colección `_inbox` con información del workflow actual.