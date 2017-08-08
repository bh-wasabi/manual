# Objeto: **show**

## Parámetros
#### id
- identificador del `show`

#### name
- nombre

#### template
- identificador del template a usar.

#### view
- identificador de la vista a usar
- si no hay vista, lee el documento completo de la colección, si viene el `id` en la url.
- se pueden pasar parámetros adicionales para la vista a travez de la url.

#### first (true, false)
- en el caso de una vista, extrae el primer documento y lo usa como contexto de la plantilla.

#### as
- es posible cambiar el contexto a usar cuando regresa una vista con multiples resultados.
- por omisión es `_items`.

#### transform
- se puede generar una [transformación](transform.md) antes de ejecutar la plantilla.
- puede ser una expresión.

#### registerVisit (true, false)
- se registran las visitas a esta `url`.
- todos los parámetros se guardan como campos.

#### uniqueVisit (true, false)
- se registra únicamente la primera visita.


## Sintaxis
````
https://<sitio>/show/<showId>/<docType>
https://<sitio>/show/<showId>/<docType>/<id>
````