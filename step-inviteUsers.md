# Objeto: **inviteUsers** (step)
- invita a una lista de usuarios, crea los que no exista y les genera un correo electrónico con la invitación.

## Parámetros
#### users
- arreglo que contiene la lista de usuarios.

#### subject
- es el asunto del correo electrónico a enviar.

#### from
- es posible especificar directamente el emisor del correo electrónico.

#### profile
- es posible especificar un perfil de correo electrónico de envío diferente.

#### template
- template a usar para mandar el correo a nuevos usuarios
- se tiene como `scope` el documento del nuevo usuario.
- requiere que este configurado por lo menos un perfil de correo electrónico en `wasabi-cfg`.

#### templateExistingUsers
- es posible cambiar de template para cuando son usuarios existentes.
- por omisión usa el `template`.

#### alwaysResetPassword (true, false)
- con esta opción siempre se genera una nueva contraseña y le pide al usuario que la cambie.

## Sub objetos

#### set
- asigna una propiedad especifica
- es necesario especificar: `email`, `name`.
- opcionalmente: `password`, `proyect`y `_proyect`.

Ejemplo:
````
{{#inviteUsers users="usuarios"}}
  {{set email="correo"}} 
  {{set name="nombre"}}
  {{set password="codigo"}}
  {{set proyect="_id.toString()"}}
  {{set _proyect="base.nombre"}}
  {{set level="admin"}}
  {{set roles="rol1"}}
{{/inviteUsers}}      
````