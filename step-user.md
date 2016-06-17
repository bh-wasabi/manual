# Objeto: **user** (step)
- define una acción que debe hacer el usuario
- a los usuarios les aparecerá en su bandeja de entrada el pendiente.

## Parámetros
##### subject
- se define el asunto del mensaje que le va aparecer al usuario en us bandeja de entrada.

##### icon
- el icono que deseamos que aparezca.
- [ion-icons](ion-icons.md)

##### color
- el color del icono

##### role
- el rol del usuario al que se le va asignar la tarea.
- es importante configurar correctamente `_user.hbs` para que tenga el control por roles.

##### duration
- el tiempo en el que expira la tarea.
- `1d` equivale a 1 día.
- `6h` equivale a 6 horas.
- `30m` equivale a 30 minutos.

## Sub objetos

##### [validate](step-validate.md)
- se pueden configurar validaciones adicionales, al momento de que el usuario le oprime afectar.
