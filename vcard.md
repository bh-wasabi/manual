# Objeto: **vCard**
- estructura del archivo

## Secciones y Campos

#### name (objeto)
- `givenName`
- `familyName`
- `sufix`
- `prefix`
- `fullName`

#### org (texto)
- nombre de la organización

#### title (texto)
- título

#### photo (url)
- url de la foto

#### adr (arreglo)
- `streetAddress`, calle
- `locality`, localidad o ciudad
- `region`, region o estado
- `postalCode`, código postal
- `countryName`, nombre del país

#### tel (arreglo)
- `type`
- `data`

#### email (arreglo)
- `type`
- `data`

#### label (arreglo)
- `type`
- `data`

## Ejemplos
````
{{action id="adjuntar" type="attach" label="Adjuntar..." onVCard="from-vcard"}}

{{#transform id="from-vcard"}}
  {{#update section="base" sourcePath="/"}}
    {{set nombre="name.givenName"}}
    {{set apellidos="name.familyName"}}
  {{/update}}
  {{#update section="telefonos" sourcePath="/tel"}}
    {{set tipo="type"}}
    {{set numero="data"}}
  {{/update}}
{{/transform}}
````
