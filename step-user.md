# Objeto: **user** (step)
- define una acción que debe hacer el usuario
- a los usuarios les aparecerá en su bandeja de entrada el pendiente.

## Parámetros
#### name
- nombre a desplegar en la bandeja de entrada.

#### topic
- tema de la tarea pendiente, se puede hacer para hacer tableros que vayan por tema en lugar de por usuario.

#### subject
- se define el asunto del mensaje que le va aparecer al usuario en us bandeja de entrada.

#### subject2
- se define el segundo asunto del mensaje que le va aparecer al usuario en us bandeja de entrada.

#### amount
- importe

#### unit
- unidad del importe

#### icon
- el icono que deseamos que aparezca.
- [ion-icons](ion-icons.md)

#### color
- el color del icono

#### role
- el rol del usuario al que se le va asignar la tarea.
- es importante configurar correctamente `_user.hbs` para que tenga el control por roles.
- debe ser un usuario con estatus activo.
- puede ser una expresión.

#### division
- la división del usuario al que se le va asignar la tarea.
- es importante configurar correctamente `_user.hbs` para que tenga divisiones.
- puede ser una expresión.

#### userId
- usuario especifico al que se le asigna la tarea.
- puede ser una expresión.

#### duration
- el tiempo en el que expira la tarea.
- `1d` equivale a 1 día.
- `6h` equivale a 6 horas.
- `30m` equivale a 30 minutos.

#### page (#)
- abre el documento en la página especificada.
- del 1 en adelante.

## Sub objetos

#### [validate](step-validate.md)
- se pueden configurar validaciones adicionales, al momento de que el usuario le oprime afectar.
