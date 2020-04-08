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

#### before
- validaciones previas al inicio del flujo de trabajo.
- Nota: se usa con BPMN.

#### skipIsAffected (true, false)
- con esta opción podemos controlar que el flujo no modifique la bandera `isAffected` del documento.

#### bpmn
- nombre del archivo XML que contiene el diagrama BPMN

#### autoEmail (true, false)
- genera un correo electrónico al usuario que le llega la tarea de forma automática.

#### autoEmailFrom
- emisor del correo electrónico.
- lo puede leer del perfil.
- puede ser una [expresión](expr.md).

#### autoEmailProfile
- busca un perfil de correo de la configuración del servidor.

#### autoEmailTemplate
- identificador del `template` a usar.

## Sub objetos

#### [step](step.md)
- un paso a ejecutar en el flujo de trabajo
