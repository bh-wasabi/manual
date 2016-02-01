# Objeto: **map**
- define un mapa a desplegar en en documento
- para desplegarlas hay que usar un [widget](helper-widget.md).

## Parámetros
##### id
- identificador del mapa

##### type
- `roadmap` por omisión.
- `satellite`
- `hybrid`

##### provider
- `bing`
- `google` por omisión.
- `googleStatic`

##### controls (true, false)
- despliega los controles nativos del mapa.

##### autoAdjust (true, false)
- con esta opción se ajusta automáticamente al centro y al nivel del zoom.
- por omisión es `true`.

##### zoom (#)
- nivel de zoom 

##### center
- coordenada o dirección donde se va centrar el mapa.
- por ejemplo: `center="19.4326068,-99.1353936"`

##### markerIconSrc (url)
- es posible especificar la dirección url de símbolo a usar como marcador.
- esta dirección debe ser publica y accesible desde otros servidores (Google o Bing).

##### height
- alto del mapa a mostrar
- puede ser en pixeles o en porcentaje.

##### width
- ancho del mapa a mostrar
- puede ser en pixeles o en porcentaje.

## Sub objetos

##### [marker](map-marker.md)
- define los marcadores en el mapa.

##### [route](map-route.md)
- define la ruta en el mapa.

## Ejemplo
````
{{#map id="mapa" provider="google" type="roadmap" zoom="14" height="600" controls="true"}}
  {{marker section="direcciones" location="calle+' '+codigoPostal+' '+ciudad+' '+estado+' '+pais" tooltip="_tipo"}}
  {{route section="direcciones" location="calle+' '+codigoPostal+' '+ciudad+' '+estado+' '+pais"}}
{{/map}}
  ````
