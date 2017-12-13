# Objeto: **workflow**
- define un flujo de trabajo

## Parámetros
#### id
- identificador del flujo de trabajo

#### name
- nombre del flujo de trabajo

#### stages
- Lista (separada por comas) de fases del proceso.

#### start
- identificador de paso donde inicia el flujo de trabajo.
- Nota: cuando se usa BPMN no es necesario indicar `start`.

#### skipIsAffected (true, false)
- con esta opción podemos controlar que el flujo no modifique la bandera `isAffected` del documento.

#### bpmn
- identificador del XML que contiene el diagrama BPMN

## Sub objetos

#### [step](step.md)
- un paso a ejecutar en el flujo de trabajo
