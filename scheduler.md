# Objeto: **scheduler**
- define una agenda a desplegar en en documento
- para desplegarlas hay que usar un [widget](helper-widget.md).

## Parámetros
#### id
- identificador de la agenda.

#### section
- sección del documento que contiene el arreglo con los campos necesarios.
- si no se indica va usar los datos de la vista del `widget`.

#### views
- lista separada por comas con las posibles vistas de la agenda.
- `day, week, workWeek, month, timelineDay, timelineWeek, timelineWorkWeek`
- por omisión es `day, week`.

#### currentView
- vista por omisión al abrir la agenda.

#### currentDate (YYYY-MM-DD)
- es posible abrir la agenda en una fecha especifica.
- por omisión es la fecha actual.

#### firstDayOfWeek (#)
- `0` domingo (por omisión)
- `1` lunes
- `2` martes
- `3` miércoles
- `4` jueves
- `5` viernes
- `6` sabado

#### startDayHour (#)
- hora inicial de la agenda
- por omisión es a las 9am

#### endDayHour (#)
- hora final de la agenda
- por omisión es a las 8pm

#### height
- alto del mapa a mostrar
- puede ser en pixeles o en porcentaje.
- en la vista del mes es necesario especificar el alto en pixeles.

#### width
- ancho del mapa a mostrar
- puede ser en pixeles o en porcentaje.

#### useDropDownViewSwitcher (true, false)
- otra forma de presentar el menú para cambiar de vista.

#### multiResources (true, false)
- permite mostrar una agenda con multiples recursos al mismo tiempo
- la vista debe regresar una lista de recursos, cada uno con su agenda.

#### resourceLabel
- nombre del recurso

#### resourceName
- campo que contiene el nombre del recurso

#### resourceColor
- campo que contiene el color del recurso

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
