# Manual
#### Versión 2.0.0

## Objetos principales
#### [app](app.md)
- aplicación

#### [cfg](cfg.md)
- configuración

#### [doc](doc.md)
- tipo de documento

#### [metadata](metadata.md)
- metadata que ayuda a crear el código de forma automática

#### [wasabiCfg](wasabiCfg.md)
- configuración del servidor de Wasabi

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
