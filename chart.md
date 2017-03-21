# Objeto: **chart**
- define una gráfica

## Parámetros
##### id
- identificador de la gráfica

##### type
- define el [tipo de gráfica](chart-type.md) por omisión.

##### argumentField
- especifica el campo que proporciona argumentos para los puntos de la serie.

##### title
- título de la gráfica

##### subTitle
- sub título de la gráfica

##### tooltip
- muestra una pequeña ventana mostrando el valor del punto de la gráfica.

##### valueAxisTitle
- Especifica el título para el eje de valores.

##### palette
- se puede definir opcionalmente otra [paleta de colores](pallete.md) a utilizar.

##### animated (true, false)
- con esta opción se puede apagar la animación.
- por omisión es `true`.

##### compactValues (true, false)
- en el caso de una sola serie, con esta opción se eliminan los datos vacíos o nulos.

## Sub objetos

##### [legend](chart-legend.md)
- información de las series

##### [tooltip](chart-tooltip.md)
- configuración de la ayuda que aparece al estar sobre un punto de la gráfica.

##### [serie](chart-serie.md)
- define una serie de la gráfica

## Ejemplo
````
{{#chart id="barras" type="bar" argumentField="category" title="Ventas" subTitle="(de la empresa)" tooltip="true" valueAxisTitle="en miles"}}
  {{legend verticalAlignment="top" horizontalAlignment="center" itemTextPosition="right"}}
  {{serie valueField="cantidad" name="Cantidad"}}
  {{serie valueField="importe" name="Importe"}}
{{/chart}}
````