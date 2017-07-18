# Objeto: **chart**
- define una gráfica

## Parámetros

#### id
- identificador de la gráfica

#### type
- define el [tipo de gráfica](chart-type.md) por omisión.

#### argumentField
- especifica el campo que proporciona argumentos para los puntos de la serie.

#### title
- título de la gráfica

#### subTitle
- sub título de la gráfica

#### section
- la gráfica puede basarse en una sección del documento.

#### view
- vista de donde sale la información

#### source
- si la fuente de la vista es diferente

#### tooltip
- muestra una pequeña ventana mostrando el valor del punto de la gráfica.

#### valueAxisTitle
- Especifica el título para el eje de valores.

#### palette
- se puede definir opcionalmente otra [paleta de colores](pallete.md) a utilizar.

#### animated (true, false)
- con esta opción se puede apagar la animación.
- por omisión es `true`.

#### compactValues (true, false)
- en el caso de una sola serie, con esta opción se eliminan los datos vacíos o nulos.

#### saveImage (true, false)
- guarda la gráfica en el documento
- esto sirve para poder imprimir en PDF la gráfica
- esto tiene algunas restricciones, y por el momento funciona únicamente al guardar el documento y se tienen que visitar previamente las secciones donde hay gráficos.

#### imageWidth (#)
- ancho de la gráfica guardada en pixeles
- por omisión es 500

#### imageHeight (#)
- alto de la gráfica guardada en pixeles
- por omisión es 500

## Sub objetos

#### [legend](chart-legend.md)
- información de las series

#### [tooltip](chart-tooltip.md)
- configuración de la ayuda que aparece al estar sobre un punto de la gráfica.

#### [serie](chart-serie.md)
- define una serie de la gráfica

## Ejemplo
````
{{#chart id="barras" type="bar" argumentField="category" title="Ventas" subTitle="(de la empresa)" tooltip="true" valueAxisTitle="en miles"}}
  {{legend verticalAlignment="top" horizontalAlignment="center" itemTextPosition="right"}}
  {{serie valueField="cantidad" name="Cantidad"}}
  {{serie valueField="importe" name="Importe"}}
{{/chart}}
````