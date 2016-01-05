# Objeto: **queue** (step)
- genera una acción por procesar en alguna cola.

## Parámetros
##### type
- `workflow` cola de flujos de trabajo.
- `api` cola para otras funciones avanzadas del API.

##### action
- identificador de la acción a ejecutar.

##### queueType
- sirve para re-encolar otra acción al terminar de procesar la cola actual.

##### queueAction
- funciona junto con `queueType`, aquí se define la acción a re-encolar.

## Sub objetos

##### [param](param.md)
- se definen todos los parámetros a agregar a la cola.
