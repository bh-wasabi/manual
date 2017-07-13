# Objeto: **range** (gauge)
- configura un rango de valores en la gráfica tipo gauge.

## Parámetros
#### startValue (#)
- valor inicial del rango

#### endValue (#)
- valor final del rango

#### color (#)
- es posible definir el color especifico de este rango.


## Ejemplos:
````
{{#gauge id="gauge" view="gauge" startValue="0" endValue="100" tickInterval="10" valueField="valor"}}
  {{range startValue="0" endValue="30" color="#bb626a"}}
  {{range startValue="30" endValue="70" color="#dac599"}}
  {{range startValue="70" endValue="100" color="#70b3a1"}}
{{/gauge}}
````

