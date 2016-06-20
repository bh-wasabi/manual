# Objeto: **email** (step)
- envia un correo electrónico.

## Parámetros

##### from
- emisor
- puede ser una [expresión](expr.md).

##### to
- destinatario

##### cc
- con copia a

##### bcc
- con copia oculta a

##### subject
- asunto del correo

##### text
- cuerpo del mensaje en texto simple.

##### html
- cuerpo del mensaje en formato HTML.

##### template
- identificador del template a usar
- es posible agregar parámetros al template.

##### s3FilePath
- ruta s3 del archivo a enviar.
- puede ser completa (`https://..`) o partir del `bucket` actual.

##### fileName
- es posible cambiar el nombre del archivo a enviar.

## Ejemplo
````
{{#email from="demo.wasabi@gmail.com" to="calc.email(contacto.correo, contacto.nombre)" subject="base.nombre" template="email"}}
  {{param _step="en Revisión Administrativa"}}
{{/email}}

{{#template id="email"}}
<div>
  Ciudad de Mexico, {{date base.fechaAlta "dddd, D MMMM YYYY"}}</br>
  </br>
  Estimado: <strong>{{contacto.nombre}},</strong>
  </br>
  </br>
  Por medio de la presente le notificamos que su solicitud de <strong>{{base._tipo}}</strong>, esta <strong>{{_step}}</strong>.
  </br>
  </br>
  </br>
  Atentamente,</br>
</div>
{{/template}}  

````