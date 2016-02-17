# Objeto: **survey**
- define una encuesta
- **Nota: por el momento el audio unicamente funciona en "Google Chrome".**

## Parámetros
##### id
- identificador de la encuesta

##### type
- `oral` encuesta oral.

##### source
- tipo de documento que contiene la encuesta a aplicar.

##### vista
- vista del tipo documento que contiene la encuesta a aplicar.
- necesitamos mapear mínimo el nombre y las preguntas.

##### width
- ancho de la ventana de la encuesta
- puede ser en pixeles o en porcentaje

##### height
- alto de la ventana de la encuesta
- puede ser en pixeles o en porcentaje

##### itemHeight
- alto del espacio para cada pregunta 
- puede ser en pixeles o en porcentaje

##### itemTemplate
- [template](template.md) a mostrar para cada pregunta.
- el contexto es el de cada pregunta de la vista.
- adicionalmente se agregan los campos calculados por `itemMap` ademas de: `_index`, `_length` y `_position`.

##### title
- título a mostrar en la ventana.

##### showTitle (true, false)
- es posible controlar si se muestra o no el título.
- por omisión es `true`.

##### loop (true, false)
- con esta opción el cuestionario cicla, hasta que el usuario cierra la ventana.
- por omisión es `false`.

##### animationEnabled (true, false)
- genera una animación al momento de cambiar la pregunta del cuestionario.
- por omisión es `true`.

##### swipeEnabled (true, false)
- permite que el usuario cambie las preguntas al hacer un swipe (touch).
- por omisión es `false`.

##### closeOnBackButton (true, false)
- se cierra el cuestionario al oprimir el botón de regresar.
- por omisión es `false`.

##### closeOnOutsideClick (true, false)
- se cierra el cuestionario al hacer un click fuera del cuestionario.
- por omisión es `false`.

##### showCloseButton (true, false)
- muestra un botón para cerrar manualmente el cuestionario.
- por omisión es `false`.

## Sub objetos

##### [param](param.md)
- para mandar parámetros a la vista.

##### [map](set.md)
- es necesario mapear: `name`y `items`.

##### [itemMap](set.md)
- es necesario mapear: `isQuestion`, `isFirst` y `isLast`.

##### [onChange](on-change.md)
- dispara el evento cuando cambia un `item`.

##### [onPlay](on-play.md)
- dispara el evento cuando inicia la reproducción del audio.

##### [onRecord](on-record.md)
- dispara el evento cuando inicia la grabación.

##### [onEnd](on-end.md)
- dispara el evento al terminar la encuesta.

## Ejemplo
````
{{#survey id="encuesta" type="oral" source="encuesta" view="todo" width="80%" height="70%" itemHeight="500" itemTemplate="encuesta" loop="false" animationEnabled="true" swipeEnabled="false" closeOnBackButton="false" closeOnOutsideClick="false" showCloseButton="false" showTitle="false"}}
  {{param codigo="'MX-GCP-00001'"}}
  {{map name="base.nombre"}}
  {{map items="preguntas"}}
  {{itemMap isQuestion="type=='question'"}}
  {{itemMap isFirst="_index==0"}}
  {{itemMap isLast="_index==_length-1"}}
  {{onChange playAudio="audio"}}
  {{#onPlay}}
    {{#jQuery find=".survey-mic"}}
      {{set type="addClass" key="btn-grey"}}
      {{set type="removeClass" key="btn-green"}}
    {{/jQuery}}
  {{/onPlay}}
  {{#onRecord notify="Gravando..." notifyTimeOut="25000"}}
    {{#jQuery find=".survey-mic"}}
      {{set type="addClass" key="btn-green"}}
      {{set type="removeClass" key="btn-grey"}}
    {{/jQuery}}
  {{/onRecord}}
  {{onEnd type="success" message="Cuestinario enviado con exito, gracias por participar." displayTime="5000" createNew="true"}}
{{/survey}}
````
Template:
````
{{#template id="encuesta"}}
<div>
  <span style="font-size: 20px;">{{header}}</span></br>
  <span style="font-size: 40px;">{{name}}</span></br></br>
  <span style="font-size: 15px;">{{footer}}</span></br>
  {{#if isQuestion}}
    <span style="position: absolute;left: 45%;bottom: 10%;" class="btn btn-floating x2 btn-grey btn-ripple survey-mic"><span class="ion-mic-a"></span></span>
  {{/if}}
</div>
{{/template}}
````