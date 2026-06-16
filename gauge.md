# Objeto: **gauge**
- define una gráfica de tipo gauge

## Parámetros
#### id
- identificador de la gráfica

#### type
- `circular` por omisión.
- `linear`

#### startValue (#)
- valor inicial
- puede ser una [expresión](expr.md).

#### endValue (#)
- valor final
- puede ser una [expresión](expr.md).

#### tickInterval (#)
- intervalo entre puntos
- puede ser una [expresión](expr.md).

#### value
- valor a mostrar con la aguja.

#### valueField
- campo que contiene el valor a mostrar con la aguja.

#### title
- título opcional.

#### subTitle
- sub título opcional.

#### palette
- se puede definir opcionalmente otra [paleta de colores](pallete.md) a utilizar.

#### showPct (true, false)
- muestra el % en la escala.

#### textCloud (true, false)
- muestra el indicador con el dato exacto.

#### textCloudColor
- es posible cambiar el color cuando se usa la opción `textCloud`.

#### animated (true, false)
- con esta opción se puede apagar la animación.
- por omisión es `true`.

## Sub objetos

#### [range](gauge-range.md)
- define un rango de colores

## Ejemplo
````
{{#gauge id="indice" type="circular" value="105" startValue="50" endValue="150" tickInterval="10" pallete="pastel" title="Satisfacción de clientes"}}
  {{range startValue="50" endValue="90"}}
  {{range startValue="90" endValue="130"}}
  {{range startValue="130" endValue="150"}}
{{/gauge}}
````
