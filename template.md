# Markup: **template**
- definición de una plantilla re-utilizable
- se puede usar para producir XML como HTML.

## Parámetros
##### id
- identificador de la plantilla

##### type
- `html`
- `xml`

## Facilitadores especiales
- los objetos de tipo Markup pueden contener HTML abiertamente y sin ninguna restricción.
- Nota: en las plantillas NO funciona la lista de facilitadores que tenemos en otros objetos como [page](page.md), [modal](modal.md) o [report](report.md).

##### campos directos
- en el caso de las plantillas se usan los campos directamente
- por ejemplo: `{{empresa.rfc}}`

##### if
- podemos condicionar un bloque si el contexto tiene valor

##### unless
- es el contrario del `if`, la condición es que no tenga valor.

##### with
- para tener un contexto a partir de un objeto del documento

##### each
- podemos hacer iteraciones
- en el contexto va el campo tipo arreglo.

##### date
- sirve para poner formato a un campo tipo fecha.
- tiene 2 contextos: el campo y el formato, el formato debe ir entre comillas dobles.
- se usa [Moment.js](http://momentjs.com) para formatear las fechas
- ejemplo: `{{date base.fechaAlta "DD/MMM/YYYY"}}`

##### number
- sirve para poner formato a un campo numérico.
- tiene 2 contextos: el campo y el formato, el formato debe ir entre comillas dobles.
- se usa [Numeral.js](http://numeraljs.com) para formatear los números.
- ejemplo: `{{date importe "#,.##"}}`

##### display
- es otra forma de formatear un numero o una fecha.
- ejemplos: `{{display importe type="number" format="#,.##"}}`, `{{display fecha type="date" format="DD/MMM/YYYY"}}`


## Ejemplo:
````
{{#template id="cfdi" type="xml"}}
<?xml version="1.0" encoding="UTF-8" ?>
<cfdi:Comprobante xmlns:cfdi="http://www.sat.gob.mx/cfd/3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.sat.gob.mx/cfd/3 http://www.sat.gob.mx/sitio_internet/cfd/3/cfdv32.xsd" version="3.2" tipoDeComprobante="ingreso" folio="{{movimiento.folio}}" fecha="{{movimiento.fecha}}" sello="" formaDePago="{{movimiento.formaPago}}" noCertificado="" certificado="" subTotal="{{totales.subTotal}}" TipoCambio="{{movimiento.tipoCambio}}" Moneda="{{movimiento.moneda}}" total="{{totales.total}}" metodoDePago="{{movimiento.metodoDePago}}" LugarExpedicion="{{movimiento.lugarExpedicion}}" NumCtaPago="">
    <cfdi:Emisor rfc="{{empresa.rfc}}" nombre="{{empresa.nombre}}">
        <cfdi:DomicilioFiscal calle="{{empresa.calle}}" noExterior="{{empresa.noExterior}}" colonia="{{empresa.colonia}}" municipio="{{empresa.municipio}}" estado="{{empresa.estado}}" pais="{{empresa.pais}}" codigoPostal="{{empresa.codigoPostal}}" />
        <cfdi:ExpedidoEn calle="{{expedidoEn.calle}}" noExterior="{{expedidoEn.noExterior}}" colonia="{{expedidoEn.colonia}}" municipio="{{expedidoEn.municipio}}" estado="{{expedidoEn.estado}}" pais="{{expedidoEn.pais}}" codigoPostal="{{expedidoEn.codigoPostal}}" />
        <cfdi:RegimenFiscal Regimen="{{empresa.regimenFiscal}}" />
    </cfdi:Emisor>
    <cfdi:Receptor rfc="{{cliente.rfc}}" nombre="{{cliente.nombre}}">
        <cfdi:Domicilio calle="{{cliente.domicilio.calle}}" noExterior="{{cliente.domicilio.noExterior}}" colonia="{{cliente.domicilio.colonia}}" municipio="{{cliente.domicilio.municipio}}" estado="{{cliente.domicilio.estado}}" pais="{{cliente.domicilio.pais}}" codigoPostal="{{cliente.domicilio.codigoPostal}}" />
    </cfdi:Receptor>
    <cfdi:Conceptos>
    {{#each articulos}}
        <cfdi:Concepto cantidad="{{cantidad}}" unidad="{{unidad}}" descripcion="{{descripcion}}" valorUnitario="{{valorUnitario}}" importe="{{subTotal}}" />
    {{/each}}
    </cfdi:Conceptos>
    <cfdi:Impuestos totalImpuestosTrasladados="{{totales.impuestos}}">
        <cfdi:Traslados>
        {{#each totales.desgloseImpuestos}}
            <cfdi:Traslado impuesto="{{impuesto}}" tasa="{{tasa}}" importe="{{importe}}" />
        {{/each}}
        </cfdi:Traslados>
    </cfdi:Impuestos>
    <cfdi:Complemento>
    </cfdi:Complemento>
</cfdi:Comprobante>
{{/template}}
````