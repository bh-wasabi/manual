# Objeto: **timeline**
- define una línea del tiempo
- esta pensado en presentar una lista de sub documentos.

## Parámetros
##### id
- identificador

##### view
- identificador de la vista a usar

##### start
- fecha inicial

##### end
- fecha final

##### min
- fecha mínima

##### max
- fecha máxima

##### zoomable (true, false)
- permite hacer zoom.

##### moveable (true, false)
- permite mover las fechas del visor.

##### selectable (true, false)
- permite seleccionar un elemento.

##### editable (true, false)
- permite editar un elemento.

##### showDoc (true, false)
- a hacer click muestra el documento.

## Sub objetos

##### [map](map.md)
- mapea el resultado de la vista a los campos que necesita la línea del tiempo.

##### Campos a mapear:
- content (name/label), nombre a presentar.
- start (date), fecha inicial.
- end, fecha final.
- type (box, point, range, background).

## Ejemplo
````
{{#timeline id="linea-tiempo" view="sub-lista" showDoc="true"}}
  {{map name="'Revisión '+moment(base.fechaAlta).format('D MMM')"}}
  {{map date="=base.fechaAlta"}}
{{/timeline}}
````
