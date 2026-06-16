# Objeto: **transform**
- genera una o varias transformaciones en el documento

## Parámetros
#### id
- identificador

#### items
- es posible transformar un arreglo
- el resultado va a ser también un arreglo
- puede ser una expresión


#### type
- `json`
- `edi`

#### ediDetailSegments
- en caso de `type="edi"` es posible tener segmentos múltiples e incluso Sub segmentos múltiples.
- lista de segmentos que contiene el detalle, pueden estar anidados, separados por comas.
- por ejemplo: `ediDetailSegments="OBR,OBX"`, en este caso hay un detalle `OBR` que contiene un subDetalle `OBX`.


#### readOnly
- puede generar el nuevo documento con la bandera _readOnly

## Sub objetos

#### [set](set.md)
- guarda un dato directamente.

#### [push](push.md)
- inserta un dato a un arreglo

#### [update](update.md)
- actualiza una sección del documento
- es posible hacer transformaciones recursivas usando nuevamente `transform` en el `update`, por ejemplo:
````
{{update section="contacto" transform="contacto"}}
````

## Ejemplo:
````
{{#transform id="resumen"}}
    {{#update sourcePath="/articulos" groupBy="alias, descripcion, unidad, precio" sum="cantidad,importe" sortBy="cantidad"}}
        {{set clave="alias"}}
        {{set descripcion="descripcion"}}
        {{set cantidad="cantidad"}}
        {{set unidad="unidad"}}
        {{set precio="precio"}}
        {{set importe="importe"}}
    {{/update}}        
{{/transform}}
````

## Ejemplo Complejo FHIR:
````
{{#transform id="contact"}}
  {{set relationship="=fn('CodeableConcept', base._extra.relacion)"}}
  {{set references="=fn('Reference', base._extra.referencias)"}}
  {{set period="=fn('Period', base.desde, base.hasta)"}}      
{{/transform}}

{{#transform id="birthGeneral"}}
  {{set linkId="'birthGeneral'"}}
  {{set text="'General Information'"}}
  {{push item="=fn('Item', 'CodeableConcept', 'nameOfChild', 'Name of child', base._extra.relacion)"}}
  {{push item="=fn('Item', 'CodeableConcept', 'sex',         'Sex',           base._extra.relacion)"}}
{{/transform}}

{{#transform id="neonatalInformation"}}
  {{set linkId="'neonatalInformation'"}}
  {{set text="'Neonatal Information'"}}
  {{push item="=fn('Item', 'CodeableConcept', 'birthWeight', 'Birth weight (kg)', base._extra.relacion)"}}
  {{push item="=fn('Item', 'CodeableConcept', 'birthLength', 'Birth length (cm)', base._extra.relacion)"}}
{{/transform}}

{{#transform id="birthDetails"}}
  {{set linkId="'birthDetails'"}}
  {{set text="'Birth details - To be completed by health professional'"}}
  {{update section="item" type="array" transform="birthGeneral"}}
  {{update section="item" type="array" transform="neonatalInformation"}}
{{/transform}}

{{#transform id="healtDetails-1-1"}}
  {{set linkId="'1.1'"}}
  {{set text="'General Information'"}}
  {{push item="=fn('Item', 'String',  '1.1.1', 'Name',                   _name,        'http://loinc.org/fhir/DataElement/54125-0')"}}
  {{push item="=fn('Item', 'String',  '1.1.2', 'Gender',                 'Female',     'http://loinc.org/fhir/DataElement/54131-8')"}}
  {{push item="=fn('Item', 'Date',    '1.1.3', 'Date of Birth',          '1966-04-04', 'http://loinc.org/fhir/DataElement/21112-8')"}}
  {{push item="=fn('Item', 'String',  '1.1.4', 'Were you born a twin?',  'No',         'http://loinc.org/fhir/DataElement/54132-6')"}}
  {{push item="=fn('Item', 'String',  '1.1.5', 'Were you adopted?',      'No',         'http://loinc.org/fhir/DataElement/54128-4')"}}
  {{push item="=fn('Item', 'Decimal', '1.1.6', 'Weight (kg)',             70,          'http://loinc.org/fhir/DataElement/29463-7')"}}
  {{push item="=fn('Item', 'Decimal', '1.1.7', 'Height (cm)',             1.65,        'http://loinc.org/fhir/DataElement/8302-2')"}}
  {{push item="=fn('Item', 'Decimal', '1.1.8', 'Body mass index (BMI)',   22.5,        'http://loinc.org/fhir/DataElement/39156-5')"}}
{{/transform}}

{{#transform id="healtDetails-1-2"}}
  {{set linkId="'1.2'"}}
  {{set text="'Family Information'"}}
  {{push item="=fn('Item', 'String', '1.1.1', 'Name',                   'Susan')"}}
  {{push item="=fn('Item', 'String', '1.1.3', 'Relationship to you',    'Daughter')"}}
  {{push item="=fn('Item', 'String', '1.1.2', 'Gender',                 'Female')"}}
  {{push item="=fn('Item', 'Date',   '1.1.4', 'Date of Birth',          '1999-01-06')"}}
{{/transform}}

{{#transform id="healtDetails" items="base._extra.referencias"}}
  {{set linkId="'1'"}}
  {{set definition="'http://loinc.org/fhir/DataElement/54126-8'"}}
  {{set text="'Your health information'"}}
  {{update section="item" type="array" transform="healtDetails-1-1"}}
  {{update section="item" type="array" transform="healtDetails-1-2"}}
{{/transform}}

{{#transform id="fhir"}}
  {{set resourceType="'Patient'"}}
  {{set id="_id"}}
  {{set language="'es'"}}
  {{set active="fn('isActive', base.estatus)"}}
  {{set text="fn('Narrative', _html.resumen)"}}
  {{set name="=fn('HumanName', base.nombres)"}}
  {{set telecom="=fn('ContactPoint', base.telecom)"}}
  {{set address="=fn('Address', base.direcciones)"}}
  {{set maritalStatus="=fn('CodeableConcept', base._extra.estadoCivil)"}}
  {{set reference="=fn('Reference', base._extra.asegurado)"}}
  {{set gender="=base.genero"}}
  {{set bundleType="=fn('CodeableConcept', base._extra.tipoPaquete)"}}
  {{set contentType="=fn('CodeableConcept', base._extra.tipoContenido)"}}
  {{update section="contact" transform="contact"}}
  {{update section="item" type="array" transform="birthDetails"}}
  {{update section="item" type="array" transform="healtDetails"}}
{{/transform}}
````

