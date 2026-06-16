# Objeto: **app**
- define una aplicación

## Parámetros
#### Nota: como `app` también puede ser un `doc`, los parámetros también son los de `doc`.

#### type
- tipo de objeto, en este caso debe ser `app`

#### id
- `_app` únicamente puede ser esta opción.

#### name
- nombre visible de la aplicación 

#### color
- color de fondo de la barra superior de la aplicación
- [lista de colores](colors.md)

#### defaultMenu
- el id del menú por omisión, la idea es que se configuren diferentes menús y que por rol de usuario se puedan acceder.

#### logo
- url (interna o externa)
- es el logotipo opcional que aparece sobre la barra superior de lado derecho.

## Sub objetos
#### [menu](menu.md)
- es el menu principal de la aplicación.

#### [mapPreset](mapPreset.md)
- es posible hacer un mapeo de un `preset` con alguna vista del sistema.

#### [css](http://www.w3schools.com/css/)
- es posible agregar estilos adicionales a la aplicación.

por ejemplo:

````
{{#css}}
.page-header{
  background-color: black;
}

body {
  font-size: 20px;
  color: red;
}
{{/css}}
```` 


#### [doc](doc.md)
- ahora podemos poner una forma que va a tener todos los datos a nivel aplicación `_app`.
- para acceder a esta forma desde el menú la ruta debe ser: `href="/_app"`.
- es un documento único a nivel base de datos de documentos.


