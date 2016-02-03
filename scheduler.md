# Objeto: **scheduler**
- define una agenda a desplegar en en documento
- para desplegarlas hay que usar un [widget](helper-widget.md).

## Parámetros
##### id
- identificador de la agenda.

##### section
- sección del documento que contiene el arreglo con los campos necesarios.

##### views
- lista separada por comas con las posibles vistas de la agenda.
- `day, week, workWeek, month, timelineDay, timelineWeek, timelineWorkWeek`
- por omisión es `day, week`.

##### currentView
- vista por omisión al abrir la agenda.

##### currentDate (YYYY-MM-DD)
- es posible abrir la agenda en una fecha especifica.
- por omisión es la fecha actual.

##### firstDayOfWeek (#)
- `0` domingo (por omisión)
- `1` lunes
- `2` martes
- `3` miércoles
- `4` jueves
- `5` viernes
- `6` sabado

##### startDayHour (#)
- hora inicial de la agenda
- por omisión es a las 9am

##### endDayHour (#)
- hora final de la agenda
- por omisión es a las 8pm

##### height
- alto del mapa a mostrar
- puede ser en pixeles o en porcentaje.

##### width
- ancho del mapa a mostrar
- puede ser en pixeles o en porcentaje.

## Ejemplo
Sección del documento con la agenda:
````
{{#section id="agenda" type="array"}}
  {{field id="text" type="text" label="Texto"}}
  {{field id="description" type="text" label="Descripción"}}
  {{field id="allDay" type="boolean" label="Todo el día"}}    
  {{field id="startDate" type="date" label="Fecha inicio" format="DD/MMM/YYYY H:mm a"}}
  {{field id="endDate" type="date" label="Fecha fin" format="DD/MMM/YYYY H:mm a"}}
  {{field id="recurrenceRule" type="text" label="Reglas recurrencia"}}    
  {{field id="recurrenceException" type="text" label="Excepciones recurrencia"}}        
{{/section}}
````
Definición de una agenda simple:
````
{{scheduler id="agenda" section="agenda" views="month, week, day" currentView="week" firstDayOfWeek="0" startDayHour="9" endDayHour="20"}}
````
