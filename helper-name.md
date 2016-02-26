# Markup: **name**
- imprime el valor visible del campo
- si tiene algún formato definido lo usa automáticamente.
- hace una liga (`link`) automáticamente (en los casos que aplica).
- para imprimir el valor literal del campo hay que usar [value](helper-value.md).

## Contexto
- campo

## Parámetros
#### unlink (true, false)
- con esta opción es posible desactivar el `link` automático.


## Ejemplo:
````
{{name base.estatus}}
````