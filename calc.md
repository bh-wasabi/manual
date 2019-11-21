# calc
- funciones predefinidas

#### fn (id, parámetros...)
- ejecuta una función configurable.
- debe existir el identificador en la configuración (`_cfg`).
- puede tener algunos parámetros múltiples.
- Nota: esta función también se puede ejecutar directamente sin el prefijo `calc.`

#### log (parámetros...)
- despliega en la consola los parámetros indicados.

#### in (valor, arreglo)
- busca sí existe un valor en un arreglo.

#### arrayInArray (valores, arreglo)
- busca sí existe alguno de los valores en un arreglo.

#### text (valor)
- forza el resultado como texto.

#### tpl (templateId, datos, [seccionId])
- ejecuta un templateId de la configuración `_app` de Handlebars.
- datos puede ser un arreglo de documentos, y se puede poner el nombre de la sección a extraer.

#### hbsMarkdown (plantilla, datos)
- ejecuta una plantilla de forma manual con Handlebars.

#### removeEmptyRows (arreglo, campo)
- elimina los renglones que no tienen valor en el campo indicado.

#### concat (valor1, valor2, valorN)
- concatena varios valores, agregando un espacio entre los valores.
- es posible agregar comas para separar estos valores, por ejemplo: `calc.concat(@apellidoPaterno,',', @nombre)`. genera "Perez, Juan".

#### concat2 (valor1, valor2, valorN)
- concatena varios valores, sin agregar espacio entre los valores.
- es posible agregar comas para separar estos valores, por ejemplo: `calc.concatCompact(@apellidoPaterno,'/', @nombre)`. genera "Perez/Juan".

#### concat3  (valor1, valor2, valorN)
- concatena varios valores, agregando comas entre los valores.

#### concat4  (valor1, valor2, valorN)
- concatena varios valores, agregando / entre los valores.

#### concat5  (valor1, valor2, valorN)
- concatena varios valores, agregando ^ entre los valores sin espacios.

#### concatValueKey  (valor1, valor2)
- concatena 2 valores descripción y clave entre paréntesis.

#### pair (etiqueta, valor, valor2, valor3)
- concatena un campo/valor si tiene valor

#### toArray (valor1, valor2, valorN)
- convierte los parámetros a un arreglo.

#### arrayToLines (arreglo)
- separa un arreglo en lineas por enter.

#### prorrate (arreglo, campo, valor, tipo)
- `arreglo` arreglo a usar
- `campo` campo a modificar
- `valor` valor numérico a prorratear
- `tipo` por omisión `div` (hace una división del importe entre la cantidad de elementos del arreglo).

#### repeat (valor, veces)
- genera un texto con el texto repetido la veces indicadas.

#### number (valor)
- forza el resultado como numérico.

#### objectId (valor)
- regresa un ObjectID de mongo con el valor opcional.

#### round(importe, decimales)
- redondea el importe a la decimales indicadas

#### isTrue (valor)
- evalúa si el valor es verdadero.

#### isFalse (valor)
- evalúa si el valor es false.

#### isNull (valor, valorPorOmision)
- checa si el valor es nulo, devuelve el valor por omisión.
- otra forma de lograr es poner la variable entre paréntesis y hacer un "or" contra el valor por omisión, por ejemplo: `(@valor||'')`.

#### nullIf (valor1, valor2)
- si el valor1 es igual al valor2 devuelve un `null`.

#### hasValue (valor)
- devuelve `true` o `false` si tiene o no valor.

#### pesos (valor)
- imprime un importe en texto (pesos).

#### numberInText (valor)
- imprime un importe en texto.

#### capitalize (valor)
- forza el resultado a la primera letra mayúsculas y las demás minúsculas (por cada palabra).

#### upperCase (valor)
- forza el resultado a mayúsculas.

#### lowerCase (valor)
- forza el resultado a minúsculas.

#### email (email, nombre, apellido, ...)
- valida que el `email` tenga el formato correcto y concatenan el texto correctamente.

#### rfcOk (rfc)
- valida que el `rfc` tenga el formato correcto.

#### rfcPhysicalPerson (nombre, apellidoPaterno, apellidoMaterno, fechaNacimiento)
- calcula el RFC de la persona Física.

#### parse (texto)
- convierte un texto JSON a objeto.

#### getPreset (preset, id)
- devuelve el objeto del preset con un `id` especifico.

#### getPresetPersona (preset, id, personaId)
- devuelve el objeto del preset con un `id` especifico y con la posibilidad de que exista a nivel persona (como primera opción).

#### presetName (preset, id)
- devuelve el nombre de un `preset` especifico con un `id` especifico.

#### presetToArray (preset, key)
- convierte un preset a un arreglo donde `key` es el nombre del `id`.

#### stringify (objeto)
- convierte un objeto a una cadena de texto JSON.

#### sha1 (texto)
- genera un hash. 

#### format (tipo, valor, formato)
- tipo (number/date) 
- aplica el formato según el tipo de datos del valor.

#### split (texto, separador)
- convierte un text (separado por comas) a un arreglo
- por omisión el separador es `,`

#### join (arreglo, control)
- convierte un arreglo a un texto separado por comas
- el control es un segundo arreglo opcional que nos indica si generar el elemento o no.

#### expireColor (fecha, cantidad, unidad)
- devuelve el los colores `green`, `yellow`, `red` o `grey`, en base al vencimiento de la fecha.
- en el momento que esta vencido sale en rojo.
- es posible controlar el periodo amarillo con (cantidad y unidad), por omisión es `cantidad=1`, `unidad=d`, es decir el ultimo día aparece en amarillo el color.

#### map (arreglo, expr)
- recorre un arreglo y evalúa la expresión para cada elemento del arreglo.
- al final queda un arreglo con todos los valores calculados. 

#### extractToList (arreglo, campo, filtros)
- extrae un campo de un arreglo y lo convierte a un texto separado por comas.
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.

#### extractToKeyValue (arreglo, campoLlave, campoValor)
- extrae objetos de un arreglo.

#### first (arreglo, filtros)
- devuelve el primer elemento del arreglo.
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- si no hay resultados devuelve un objeto vacio `{}`.

#### match (arreglo, filtros) o (arreglo, lista de campos, valores...)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- si no hay resultados devuelve un arreglo vacío `[]`.

#### notMatch (arreglo, filtros) o (arreglo, lista de campos, valores...)
- es igual que `match`, pero devuelve lo que no coincide.

#### lookup (arreglo, filtros) o (arreglo, lista de campos, valores...)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- a diferencia de `match` esta comando regresa el primer registro que coincida con el filtro.
- si no hay resultados devuelve un objeto vacío `{}`.

#### lookupInPreset (preset, filtros) o (preset, lista de campos, valores...)
- obtiene el `preset` (con todos sus campos)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- regresa el primer registro que coincida con el filtro.
- si no hay resultados devuelve un objeto vacío `{}`.

#### lookupAllInPreset (preset, filtros)
- similar a `lookupInPreset` con la diferencia que trae todo los objetos que corresponden al filtro.

Ejemplos: 

Sintaxis 1:
````
calc.lookupInPreset('app.subTipoSujeto', 'tipo='+tipo+'&id='+subTipo).cuenta
````

Sintaxis 2:
````
calc.lookupInPreset('app.subTipoSujeto', 'tipo, id', tipo, subTipo).cuenta
````

#### pluck (arreglo, llave)
- genera un nuevo arreglo con las puras llaves.

#### pluckRef (arreglo, llave)
- genera un nuevo arreglo con las puras llaves. 
- buscando en el objeto la referencia.

#### pluckRefHasValue (arreglo, llave)
- busca sí en los resultados existe alguno `true`.

#### pluckExpr (arreglo, llave)
- genera un nuevo arreglo con las puras llaves. 
- la llave puede ser una expresión.

#### pluckExprHasValue (arreglo, llave)
- busca sí en los resultados existe alguno `true`.

#### itemsInArray (arreglo1, llave, arreglo2)
- extrae una sub lista del arreglo1 donde exista la llave (del arreglo1) en en arreglo2
- el arreglo2 debe ser un arreglo simple.

Ejemplo:
````
calc.itemsInArray([{id:1, nombre:'uno'}, {id:4, nombre: 'cuatro'}], 'id', [1,2,3])
````

#### taxAmount (preset, taxTypes, amount, filter)
- Esta función regresa el importe de impuestos a nivel línea.

#### taxBreakdown (preset, items, grandTotal, action)
- Esta función regresa el desglose de los impuestos totales de un movimiento.

#### getProration (items, action)
- Esta función sirve para extraer los prorrateos de una lista y concentrarlos en una nueva sección.
- supone que en la lista existe un objeto tipo arreglo para cada elemento de la lista.
- la acción es un filtro que se aplica.

#### cat (importe, enganche, importePago, numPagos, periodicidad)
- calcula el CAT (Costo Anual Total), según las reglas del Banco de México.
- periodicidad puede ser `'diaria', 'semanal', 'quincenal', 'mensual', 'trimestal', 'cutrimestral', 'semestral'`, por omisión es `'mensual'`.
- todos los demás campos son numéricos.

#### catArray (importe, enganche, pagos, periodicidad)
- al igual que la función `cat` con la diferencia que en pagos viene un arreglo con todos los pagos específicos.

#### mapReduce (arreglo, agrupadores, sumar)
- `arreglo`
- `agrupadores` lista de campos separados por comas
- `sumar` lista de campos separados por comas

#### sortArray(arreglo, campos)
- lista de campos separados por comas.

#### findDuplicates (arreglo, agrupadores)
- `arreglo`
- `agrupadores` lista de campos separados por comas

#### preset (id)
- devuelve el preset completo.

#### duration (desde, hasta)
- calcula la duración del rango de tiempos.

#### fromYearMonth (año, mes)
- pone el primer momento de un mes especifico.

#### toYearMonth (año, mes)
- pone el ultimo momento de un mes especifico.

#### fromNow (fecha, hora)
- calcula el tiempo desde cierta fecha en español.
- hora opcional 

#### fromNowShort (fecha)
- calcula el tiempo desde cierta fecha en español.
- en la forma mas corta.

#### fromNowShort2 (fecha)
- calcula el tiempo desde cierta fecha en español.
- en la forma mas corta diferente.

#### fromNowTime (fecha)
- devuelve las horas de una fecha a hoy en formato hh:mm

#### fromNowHours (fecha)
- devuelve la cantidad de horas de una fecha a hoy.

#### fromNowDays (fecha)
- devuelve la cantidad de días de una fecha a hoy.

#### fromNowMonths (fecha)
- devuelve la cantidad de meses de una fecha a hoy.

#### fromNowYears (fecha)
- devuelve la cantidad de años de una fecha a hoy.

#### fromNowFloat (fecha, hora)
- devuelve las horas de una fecha a hoy en numérico flotante
- hora opcional 

#### findWhere (arreglo, attributos)
- devuelve el primer elemento de la lista, con los atributos que coincidan.

#### findWhereRef (arreglo, referencia, valor)
- devuelve el primer elemento de la lista, usando la referencia y que el valor corresponda.

#### where (arreglo, attributos)
- devuelve una lista, con los atributos que coincidan.

#### notWhere (arreglo, attributos)
- devuelve una lista, con los atributos que no coincidan.

#### whereGreaterThan (arreglo, llave, valor)
- devuelve una lista de los elementos que tienen el valor superior.

#### whereLessThan (arreglo, llave, valor)
- devuelve una lista de los elementos que tienen el valor inferior.

#### tagsWherePresetHas (tags, preset, attributos)
- devuelve los tags que cumplen con los attributos indicadas.

#### updateArray (arreglo, llave, valor, condicion)
- actualiza un arreglo y pone en un campo especifico un valor especifico
- es posible indicar una condición opcional.

#### getRef (objeto, referencia)
- obtiene un valor de un objeto
- la referencia es la llave pero puede contener sub campos separados con punto, por ejemplo: `getRef({base: {nombre: 'hola'}}, 'base.nombre')` va a devolver `hola`.

#### reconcilePreset (preset, lista, listaCampo, filtro, nombreCampo, camposCopiar)
- concilia un preset con una lista especifica.
- listaCampo es el nombre del campo que contiene el `id` en la lista.
- el filtro usa la sintaxis "campo=valor&campo2=valor2" (opcional).
- regresa la lista conciliada con el nombre del campo especifico, por omisión es `exists`.
- es posible poner una lista de campos separadas por comas de campos adicionales a copiar.
- por ejemplo: `reconcilePreset('app.tipoAdjunto', [{id: 'foto'}], 'id')`

#### getHost ()
- devuelve el host donde esta corriendo la página
- por ejemplo: `https://demo.com`

#### transformImage (url, opciones)
- url de la imágen a transformar.
- las opciones deben ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`, son las opciones de [transformImage](transformImage).

#### count (arreglo, campo)
- suma un los valores o campos de un objeto que tienen valor.

#### countArgs (argumentos)
- cuenta todos los argumentos con valor

#### sum (arreglo, campo)
- suma un campo del arreglo o los campos de un objeto numericos

#### sumArgs (argumentos)
- suma todos los argumentos
- por ejemplo: calc.sumArgs(1,2,3,'4') = 10

#### sumRef (arreglo, referencia)
- suma las referencias del arreglo

#### union (arreglo1, arreglo2, arregloN)
- une todos los arreglos

#### mergeMasterDetail (mater, detalle, campos, mapeo, usarDetalle)
- sirve para generar un resultado uniforme, devuelve un arreglo.
- master es el encabezado (objeto)
- detalle (opcional) es un arreglo
- mapeo (opcional) lista de campos separados por comas, y es posible renombrar el campo, por ejemplo `importe,referencia` o `importe,referencia=ref`.
- usarDetalle (opcional), es un valor tipo `Boolean` para controlar si se usa o no el detalle, por omisión es verdadero.


#### mergeToMaster (original, nuevo, master, llave)
- busca los cambios entre el arreglo nuevo y el original, y los aplica en master, usando el campo llave indicada
- deben ser arreglos de objetos todos.
- devuelve un arreglo que seria el nuevo master con los cambios.

#### clone (obj)
- clona un objeto

#### object (lista, [valores])
- convierte arreglos en objetos.

#### newId (tipo)
- genera un nuevo ID, se pueden usar los siguientes tipos (`uuid`, `shortid`, `shortid32`).

#### printIf (condicion, texto)
- si la condiciones es verdadera imprime el texto, 
- si no devuelve ''

#### quotes (texto, comilla)
- pone el texto entre comillas dobles por omisión

#### zeroFill (numero, dígitos)
- pone un numero relleno de ceros.
