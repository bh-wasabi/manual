# Manual
#### Versión 1.0.0

## Objetos principales
#### [app](app.md)
- aplicación

#### [cfg](cfg.md)
- configuración

#### [doc](doc.md)
- tipo de documento

## Directivas de Compilación
- Es posible usar estas directivas para hacer cambios al código a un nivel superior.
- para esto se usa `[.` y `.]` en lugar de `{{` y `}}`.

Ejemplo
```
[.#if pruebas.]
{{#define type="doc" id="cte" name="Pruebas"}}
[.else.]
{{#define type="doc" id="cte" name="Producción"}}
[./if.]
```