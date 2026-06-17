# calc

## disponibles todo el tiempo
#### _ (underscore)
- https://underscorejs.org

#### $ (jquery)
- https://jquery.com

#### moment
- https://momentjs.com

#### numeral
- http://numeraljs.com

## funciones predefinidas

#### fn (id, parámetros...)
- ejecuta una función configurable.
- debe existir el identificador en la configuración (`_cfg`).
- puede tener algunos parámetros múltiples.
- Nota: esta función también se puede ejecutar directamente sin el prefijo `calc.`

#### log (parámetros...)
- despliega en la consola los parámetros indicados.

#### in (valor, arreglo)
- busca sí existe un valor en un arreglo.

#### notIn (valor, arreglo)
- busca no existe un valor en un arreglo.

#### inForce (desde, hasta, [fecha])
- checa si está vigente.
- la fecha es opcional, si no se define se usa `moment().format()`.

#### arrayInArray (valores, arreglo)
- busca sí existe alguno de los valores en un arreglo.

#### text (valor)
- forza el resultado como texto.

#### normalize (valor)
- normalize el resultado como texto.

#### tpl (templateId, datos, [seccionId])
- ejecuta un templateId de la configuración `_app` de Handlebars.
- datos puede ser un arreglo de documentos, y se puede poner el nombre de la sección a extraer.

#### hbs (plantilla, datos)
- ejecuta una plantilla de forma manual con Handlebars y regresa el HTML o XML ya parseado.

#### if (expresion, verdadero, falso)
- ejecuta una expresión, si el resutaldo es verdadero devuelve el primer valor en caso contrario regresa el segundo valor, por ejemplo: `calc.if(1==2, 2*2, 3*3)`. genera 9.

#### removeEmptyRows (arreglo, campo)
- elimina los renglones que no tienen valor en el campo indicado.

#### substr (texto, inicio, tamaño)
- obtiene el `substr` del texto indicado.

#### leftStr (texto, posicion)
- obtiene los caracteres a la izquierda de la posición en el texto.
- por ejemplo `calc.leftStr('hola mundo!', 6)` devuelve `'hola m'`.

#### rightStr (texto, posicion)
- obtiene los caracteres a la izquierda de la posición en el texto.
- por ejemplo `calc.rightStr('hola mundo!', 6)` devuelve `' mundo!'`.

#### posStr (texto1, texto2)
- obtiene la poisición si existe el texto2 dentro del texto1
- por ejemplo `calc.posStr('hola como estas', 'como')` devuelve `5`.

#### delStr (texto, posicion, tamaño)
- elimina dentro de un texto a partir de una posición, un tamaño de caracteres.
- por ejemplo `calc.delStr('hola como estas', 5, 3)` devuelve `'hola o estas'`.

#### insStr (texto1, texto2, posicion)
- inserta el texto2 dentro del texto1 a partir de la posición indicada.
- por ejemplo `calc.insStr('hola mundo!', ' como estas', 10)` devuelve `'hola mundo como estas!'`.

#### alignLeft (texto, ancho, relleno)
- alinea el texto a la izquierda y le rellena todo el ancho sobrante con un caracter.
- por omisión el relleno es un espacio.
- por ejemplo `calc.alignLeft('hola', 10, '*')` devuelve `'hola******'`.

#### alignRight (texto, ancho, relleno)
- alinea el texto a la derecha y le rellena todo el ancho sobrante con un caracter.
- por omisión el relleno es un espacio.
- por ejemplo `calc.alignRight('hola', 10, '*')` devuelve `'******hola'`.

#### alignCenter (texto, ancho, relleno)
- alinea el texto centrado y le rellena todo el ancho sobrante con un caracter.
- por omisión el relleno es un espacio.
- por ejemplo `calc.alignCenter('hola', 10, '*')` devuelve `'***hola***'`.

#### netDiscount (argumentos)
- calcula un descuento neto en cascada usando cada parametro como un descuento adicional.
- por ejemplo `calc.netDiscount(10,20,30)` devuelve `49.6`.

#### promoDiscount
- calcula los descuentos usando las promociones aplicadas
  
#### promoId
- devuelve el id de la promoción aplicada

#### promoName
- devuelve el nombre de la promoción aplicada

#### cut (texto, llave)
- busca la llave en el texto y si existe corta el texto hasta ese punto.
- por ejemplo `calc.cut('hola mundo!', 'mundo')` regresa `' hola'`.

#### cut2 (texto, llave)
- parecedio a `cut` pero regresa el texto que sigue a ese punto.
- por ejemplo `calc.cut2('hola mundo!', 'mundo')` regresa `'undo!'`.

#### keys (obj)
- obtiene la lista de llaves

#### names (obj)
- obtiene la lista de nombres

#### values (obj)
- obtiene la lista de valores

#### concat (valor1, valor2, valorN)
- concatena varios valores, agregando un espacio entre los valores.
- es posible agregar comas para separar estos valores, por ejemplo: `calc.concat(@apellidoPaterno,',', @nombre)`. genera "Perez, Juan".

#### concat2 (valor1, valor2, valorN)
- concatena varios valores, sin agregar espacio entre los valores.
- es posible agregar comas para separar estos valores, por ejemplo: `calc.concatCompact(@apellidoPaterno,'/', @nombre)`. genera "Perez/Juan".

#### concat3 (valor1, valor2, valorN)
- concatena varios valores, agregando comas entre los valores.

#### concat4 (valor1, valor2, valorN)
- concatena varios valores, agregando / entre los valores.

#### concat5 (valor1, valor2, valorN)
- concatena varios valores, agregando ^ entre los valores sin espacios.

#### concat6 (valor1, valor2, valorN)
- concatena varios valores, agregando > entre los valores sin espacios.

#### arrayWithItems (valor)
- checa que exista y que sea un arreglo con elementos

#### concatValueKey  (valor1, valor2)
- concatena 2 valores descripción y clave entre paréntesis.

#### concatPoint  (valor1, valor2, valorN)
- concatena varios valores, agregando ´.´ entre los valores sin espacios.

#### concatPairs  (valor1, valor2, valor3, valor4, valorN)
- concatena varios valores en pares, separados por comas.

#### concatTab  (valor1, valor2, valorN)
- concatena varios valores, agregando ´tab´ entre los valores sin espacios.

#### concatEnter  (valor1, valor2, valorN)
- concatena varios valores, agregando ´enter´ entre los valores sin espacios.

#### concatItemsEnter  (items, key, value, prefix, sufix)
- genera un texto separado por Enter del campo valor con prefijo o sufijos opcionales

#### concatPath  (valor1, valor2, valorN)
- concatena varios valores, agregando ´/´ entre los valores sin espacios.

#### concatPipe  (valor1, valor2, valorN)
- concatena varios valores, agregando ´|´ entre los valores sin espacios.

#### concatHost  (valor1, valor2, valorN)
- es parecido a ´concatPath´, pero agrega de prefijo el Host

#### concatCommaDot  (valor1, valor2, valorN)
- concatena varios valores, agregando comas entre los valores, al final pone un '.' si es más de 1 valor.

#### maxStringLength (texto, max)
- limita el texto a un máximo.

#### length (texto)
- número de carácteres en texto

#### pair (campo, valor, valor2, valor3)
- concatena un campo/valor si tiene valor
- puede concatenar hasta 3 valores
- por ejemplo: `calc.pair('nombre','juan','perez','lopez')`. genera 'nombre: juan perez lopez'.

#### pairIf (condicion, campo, valor, valor2, valor3)
- similar a la función calc.pair con la opción de agregar una condicion al principio.

#### toArray (valor1, valor2, valorN)
- convierte los parámetros a un arreglo.

#### prorrate (arreglo, campo, valor, tipo)
- `arreglo` arreglo a usar
- `campo` campo a modificar
- `valor` valor numérico a prorratear
- `tipo` por omisión `div` (hace una división del importe entre la cantidad de elementos del arreglo).

#### repeat (valor, veces)
- genera un texto con el texto repetido la veces indicadas.

#### int (valor)
- forza el resultado como integro.

#### integer (valor)
- funciona igual que `int`.

#### number (valor)
- forza el resultado como numérico.

#### objectId ()
- regresa un ObjectID de mongo nuevo.
- regresa un texto

#### forceObjectId (valor)
- funciona igual que `objectId`.

#### round(importe, decimales)
- redondea el importe a la decimales indicadas

#### isTrue (valor)
- evalúa si el valor es verdadero.

#### isAllTrueFalse (valor1, valor2, valorN)
- evalúa todos los argumentos y regresa un `true` si todos los valores son verdaderos o falsos.

#### isFalse (valor)
- evalúa si el valor es `false`.

#### notFalse (valor)
- evalúa si el valor no es `false`, `'no'`, `'false'`, `'falso'`.

#### isEmpty (valor)
- checa que el valor tenga datos o no sea un objeto o arreglo vacio.

#### isNotEmpty (valor)
- nega al isEmpty

#### ifEmpty (valor1, valor2)
- si el valor1 esta vacio regresa el valor2

#### isJson (valor)
- checa si el JSON válido

#### isNull (valor, valorPorOmision)
- checa si el valor es nulo, devuelve el valor por omisión.
- otra forma de lograr es poner la variable entre paréntesis y hacer un "or" contra el valor por omisión, por ejemplo: `(@valor||'')`.

#### nullIf (valor1, valor2)
- si el valor1 es igual al valor2 devuelve un `null`.

#### hasValue (valor)
- devuelve `true` o `false` si tiene o no valor.

#### hasValues (arreglo)
- devuelve `true` o `false` todos los elementos del arreglo tienen valor.

#### hasValueRef (doc, arregloReferencias)
- devuelve `true` o `false` si todas las referencias indicadas tienen valor.

#### pesos (valor)
- imprime un importe en texto (pesos).

#### numberInText (valor)
- imprime un importe en texto.

#### strToNumber (texto)
- convierte un texto a numerico, incluso forzando el valor si tiene comas.
- por ejemplo `calc.strToNumber('123,456.78')` devuelve `123456.78`

#### strToDateFormat (valor, formato)
- convierte un texto a fecha usando momentjs para que tenga mucho mas tolerancia en el valor que llega.
- el formato puede ayudar a definir en que formato llega la fecha y en que formato se devuelve el resultado.

#### strToDateTimeFormat (fechaStr, horaStr, formato)
- convierte una fecha y hora por separando en una fecha y hora juntos
- puede tener un formato específico la fecha.
- por ejemplo `calc.strToDateTimeFormat('2026-12-31','19:20')` devuelve `'2026-12-31T19:20:00-06:00'`

#### formatDate (valor, formato)
- convierte un valor a fecha usando un formato opcional.

#### dateToStrFormat (valor, formato)
- funciona igual que `formatDate`

#### strToItems (texto, separador)
- desglosa una lista de un texto, en el fondo usa la función `splitAndTrim`.
- por omisión usa la coma como separador.
- por ejemplo `calc.strToItems('a,b,c,d,e')` devuelve un arreglo de textos `['a','b','c','d','e']`.

#### strToItemsQuotes (texto, separador, comilla)
- hace algo similar a `strToItems` pero adicionalmente le agrega comillas al resultado.
- por ejemplo `calc.strToItemsQuotes('1,2,3,4',',','"')` regresa `['"1"', '"2"', '"3"', '"4"']`.

#### booleanToBit (valor)
- convierte un valor logico `true` o `false` a `1` o `0`.

#### formatCurrency (valor)
- imprime un importe en texto con formato monetario.

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

#### getPresetAll (preset)
- devuelve el arreglo completo del preset.

#### getPresetPersona (preset, id, personaId)
- devuelve el objeto del preset con un `id` especifico y con la posibilidad de que exista a nivel persona (como primera opción).

#### joinPreset (items, preset, itemKey, presetKey)
- une una lista con un preset, usando las llaves para encontrar los id.

#### arrayToItems (items, key)
- convierte un arreglo simple en una lista de objetos

#### arrayToLines (arreglo)
- separa un arreglo en lineas por enter.

#### presetName (preset, id)
- devuelve el nombre de un `preset` especifico con un `id` especifico.

#### presetInfo (preset, id)
- devuelve los datos de un `preset` especifico con un `id` especifico.

#### presetToArray (preset, key)
- convierte un preset a un arreglo donde `key` es el nombre del `id`.

#### presetNotIn (preset, excluir, separadoComas)
- devuelve un arreglo con la lista o separado por Comas de la lista excluyendo la lista

#### presetIdWhere (preset, filtro)
- devuelve la lista de id, del preset que corresponde al filtro.

#### tagsToArray (preset, key)
- convierte un arreglo simple donde `key` es el nombre del `id`.

#### stringify (objeto)
- convierte un objeto a una cadena de texto JSON.

#### sha1 (texto)
- genera un hash.

#### splitAndTrim (texto, separador) 
- convierte un texto a un arreglo
- por omisión usa la coma como separador
- si lo valores tienen espacios el aplica un `trim`.

#### split (texto, separador) 
- hace lo mismo que `splitAndTrim`.

#### splitAndTrimFirst (texto, separador) 
- es igual que `splitAndTrim` pero devulve unicamente el primer valor del arreglo.

#### format (tipo, valor, formato)
- tipo (number/date) 
- aplica el formato según el tipo de datos del valor.

#### split (texto, separador)
- convierte un text (separado por comas) a un arreglo
- por omisión el separador es `,`

#### join (arreglo, control)
- convierte un arreglo a un texto separado por comas
- el control es un segundo arreglo opcional que nos indica si generar el elemento o no.

#### joinItems (arreglo, separador)
- convierte un arreglo a un texto con un separador especial.

#### joinAndTrimItems (arreglo, separador)
- hace lo mismo que `joinItems` pero le aplica un `trim` a cada valor.

#### joinArraysByKey (arreglo1, arreglo2, llave)
- une 2 arreglos usando una campo llave en común.

#### joinArraysById (arreglo1, arreglo2, arregloN)
- une n arreglos usando el campo `id` como llave.

#### unique (arreglo)
- regresa un arreglo con valores únicos.

#### expireColor (fecha, cantidad, unidad)
- devuelve el los colores `green`, `yellow`, `red` o `grey`, en base al vencimiento de la fecha.
- en el momento que esta vencido sale en rojo.
- es posible controlar el periodo amarillo con (cantidad y unidad), por omisión es `cantidad=1`, `unidad=d`, es decir el ultimo día aparece en amarillo el color.

#### map (arreglo, expr)
- recorre un arreglo y evalúa la expresión para cada elemento del arreglo.
- al final queda un arreglo con todos los valores calculados. 

#### mapKeyValue (arreglo, keyValue)
- para un arreglo ejecuta una transformacion de una llave en particular
- el valor puede ser una expresion usando el contexto del elemento del arreglo.
- key value es un objeto tipo `{"campo":"valor"}`.

#### extractToList (arreglo, campo, filtros)
- extrae un campo de un arreglo y lo convierte a un texto separado por comas.
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.

#### extractToKeyValue (arreglo, campoLlave, campoValor)
- extrae objetos de un arreglo.

#### first (arreglo, filtros)
- devuelve el primer elemento del arreglo.
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- si no hay resultados devuelve un objeto vacio `{}`.

#### firstValidSchedule (arreglo, campoHorario)
- devuleve el primer objeto del arreglo que tiene un horario valido

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

#### lookupConfigException (type, field)
- busca una excepción de la configuración (_app), que corresponde a un tipo/campo especifico
- estas excepciones son relativas a la fecha hoy.

#### pluck (arreglo, llave)
- genera un nuevo arreglo con las puras llaves.

#### pluckRef (arreglo, llave)
- genera un nuevo arreglo con las puras llaves. 
- buscando en el objeto la referencia.

#### pluckRefKeys (arreglo, llaves[, nombres, tipoDatos])
- genera un nuevo arreglo con múltiples referencias con la opción de cambiar de nombre la llave.

#### pluckRefHasValue (arreglo[, llave])
- busca sí en los resultados existe alguno `true` o si tiene la llave opcional.

#### pluckExpr (arreglo, llave)
- genera un nuevo arreglo con las puras llaves. 
- la llave puede ser una expresión.

#### pluckExprHasValue (arreglo, llave)
- busca sí en los resultados existe alguno `true`.

#### itemsToLines (arreglo)
- genera un texto separado por Enter para cada línea.

#### deleteRef (objeto, llave)
- elimina una campo del objeto

#### deleteRefInArray (arreglo, llave)
- elimina una campo del objeto en el arreglo

#### itemsInArray (arreglo1, llave, arreglo2)
- extrae una sub lista del arreglo1 donde exista la llave (del arreglo1) en en arreglo2
- el arreglo2 debe ser un arreglo simple.

Ejemplo:
````
calc.itemsInArray([{id:1, nombre:'uno'}, {id:4, nombre: 'cuatro'}], 'id', [1,2,3])
````
#### tax (amount, percent[, decimales])
- calcula el impuesto directo de un porcentaje en enteros
- opcionalmente se puede redondear el resultado

#### addTax (amount, percent[, decimales])
- calcula el importe Total directo de un porcentaje en enteros
- opcionalmente se puede redondear el resultado

#### addTaxRetention (amount, percent, retention1, retention2, [, decimales])
- calcula el importe Total directo de un porcentaje en enteros, quitando retenciones
- opcionalmente se puede redondear el resultado

#### taxExcluded (amount, percent[, decimales])
- calcula el importe sin el impuesto incluido
- opcionalmente se puede redondear el resultado

#### taxIncluded (amount, percent[, decimales])
- calcula el impuesto incluido de un precio que incluye impuestos
- opcionalmente se puede redondear el resultado

#### taxAmount (preset, taxTypes, amount, filter)
- Esta función regresa el importe de impuestos a nivel línea.

#### taxBreakdown (preset, items, grandTotal, action)
- Esta función regresa el desglose de los impuestos totales de un movimiento.

#### deductible (amount, type, percent, top)
- determina la parte deducible de un importe, ya sea por porcentaje o tope

#### notDeductible (amount, type, percent, top)
- determina la parte no deducible de un importe, ya sea por porcentaje o tope

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

#### sortArray(arreglo, campos)
- ordena un arreglo de objetos
- lista de campos separados por comas.

#### findDuplicates (arreglo, agrupadores)
- `arreglo`
- `agrupadores` lista de campos separados por comas

#### preset (id)
- devuelve el preset completo.

#### duration (desde, hasta)
- calcula la duración del rango de tiempos.

#### fromYear (año)
- pone el primer momento de un año especifico.

#### toYear (año)
- pone el ultimo momento de un año especifico.

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

#### fromNowMinutes (fecha[, desde])
- devuelve la cantidad de minutos de una fecha a hoy.
- desde es opcional

#### fromNowHours (fecha[, desde])
- devuelve la cantidad de horas de una fecha a hoy.
- desde es opcional

#### fromNowDays (fecha[, desde])
- devuelve la cantidad de días de una fecha a hoy.
- desde es opcional

#### fromNowMonths (fecha[, desde])
- devuelve la cantidad de meses de una fecha a hoy.
- desde es opcional

#### fromNowYears (fecha[, desde])
- devuelve la cantidad de años de una fecha a hoy.
- desde es opcional

#### fromNowFloat (fecha, hora)
- devuelve las horas de una fecha a hoy en numérico flotante
- hora opcional 

#### findWhere (arreglo, attributos)
- devuelve el primer elemento de la lista, con los atributos que coincidan.

#### findWhere2 (arreglo, attributos)
- es similar al anterior, pero si no encuentra nada devuelve un objeto vacío.

#### findWhereOptional (arreglo, atributos)
- busca el primer elemento de un arreglo que cumpla con los atributos indicados
- en este caso se eliminan los atributos falsos o vacios antes de hacer la busqueda.

#### findWhereRef (arreglo, referencia, valor [, referencia2, valor2])
- devuelve el primer elemento de la lista, usando la referencia y que el valor corresponda.
- puede tener 2 referencias (opcional).

#### findWhereNotFalse (arreglo, llave)
- devuelve el primer elemento de la lista donde el campo llave no sea falso.

#### firstLike (arreglo, llave, prefijo)
- devuelve el primer elemento de la lista donde el campo llave coincide con el prefijo indicado.

#### where (arreglo, attributos)
- devuelve una lista, con los atributos que coincidan.

#### whereExists (arreglo, llave, valor)
- devuelve una lista, con los valores que existan dentro del texto
- puede ser una arreglo de valores

#### whereExpr (arreglo, expr)
- devuelve una lista donde se cumplen las expresiones en cada uno de los elementos.

#### whereRefIn (arreglo, ref, values)
- devuelve la lista con los valores múltiples que existan en la referencia.

#### notWhere (arreglo, attributos)
- devuelve una lista, con los atributos que no coincidan.

#### whereGreaterThan (arreglo, llave, valor)
- devuelve una lista de los elementos que tienen el valor superior.

#### whereLessThan (arreglo, llave, valor)
- devuelve una lista de los elementos que tienen el valor inferior.

#### whereNotValue (arreglo, llave, valor)
- devuelve la lista de todos los elementos que no corresponde el valor con la llave indicada.

#### whereHasValue (arreglo, llave)
- devuelve una lista, con los registros que tienen valor en ese campo

#### whereIsFalse (arreglo, llave)
- devuelve una lista, con los registros que tienen un valor falso en ese campo

#### whereNotHasValue (arreglo, llave)
- devuelve una lista, con los registros que no tienen valor en ese campo

#### tagsWherePresetHas (tags, preset, attributos)
- devuelve los tags que cumplen con los attributos indicadas.

#### updateArray (arreglo, llave, valor, condicion)
- actualiza un arreglo y pone en un campo especifico un valor especifico
- es posible indicar una condición opcional.

#### updateArrayExpr (arreglo, llave, expr, condicion)
- actualiza un arreglo y pone en un campo especifico un valor especifico
- es posible indicar una condición opcional.

#### getRef (objeto, referencia)
- obtiene un valor de un objeto
- la referencia es la llave pero puede contener sub campos separados con punto, por ejemplo: `getRef({base: {nombre: 'hola'}}, 'base.nombre')` va a devolver `hola`.

#### existsKeys (objeto, campos)
- checa sí todos los campos tienen valor.

#### existsRef (objeto, referencia)
- checa sí existe una referencia.

#### getRefLength (objeto, referencia)
- cantidad de elementos en un arreglo que se obtiene con `getRef`.

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

#### countItems (arreglo)
- cuenta todos los elementos del arreglo

#### countDiff (arreglo, llave)
- cuenta todos los elementos del arreglo que tienen la llave especificada.

#### sum (arreglo, campo)
- suma un campo del arreglo o los campos de un objeto numéricos

#### sumArgs (argumentos)
- suma todos los argumentos
- por ejemplo: `calc.sumArgs(1,2,3,'4')` devuelve `10`

#### sumItems (arreglo)
- suma la lista de todos los elementos del arreglo
- por ejemplo: `calc.sumItems([1,2,3,'4'])` devuelve `10`

#### sumRef (arreglo, referencia)
- suma las referencias del arreglo

#### sumRefWhere (arreglo, referencia, filtro)
- suma las referencias del arreglo, aplicando un filtro previo

#### sumExpr (arreglo, expresión)
- suma las expresiones del arreglo

#### avgArgs (argumentos)
- hace un promedio de todos los argumentos
- por ejemplo: `calc.avgArgs(1,2,3,'4')` devuelve `2.5`

#### avgItems (argumentos)
- hace un promedio de todos los elementos del arreglo
- por ejemplo: `calc.avgItems([1,2,3,'4'])` devuelve `2.5`

#### union (arreglo1, arreglo2, arregloN)
- une todos los arreglos

#### hasRole (roles)
- checa que el usuario actual tenga alguno de los roles, separados por comas.

#### mergeMasterDetail (mater, detalle, campos, mapeo, usarDetalle)
- sirve para generar un resultado uniforme, devuelve un arreglo.
- master es el encabezado (objeto)
- detalle (opcional) es un arreglo
- mapeo (opcional) lista de campos separados por comas, y es posible renombrar el campo, por ejemplo `importe,referencia` o `importe,referencia=ref`.
- usarDetalle (opcional), es un valor tipo `Boolean` para controlar si se usa o no el detalle, por omisión es verdadero.

#### mergeArraysByKey (arreglo1, arreglo2, llaves, opciones)
- puede hacer un `merge` entre 2 arreglos usando una o varias llaves separadas por comas.

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

#### sha512 (texto)
- genera un hash tipo `sha512` del texto indicado.

#### newUuid ()
- genera un uuid nuevo.
- es similar a usar `calc.newId('uuid')`

#### newDoc (doc o docs, [tipo, deleteRef, untilRef])
- genera un nuevo ID, y pone la sección `_created`.

#### printIf (condicion, texto)
- si la condiciones es verdadera imprime el texto, 
- si no devuelve ''

#### isNumeric (valor)
- evalua el valor para ver si puede ser un numérico, incluso si es un texto busca si es completamente númerico.
- regresa true o false.

#### quotes (texto, comilla)
- pone el texto entre comillas dobles por omisión

#### zeroFill (numero, dígitos)
- pone un numero relleno de ceros, por ejemplo `calc.zeroFill(123,6)` devuelve `000123`.

#### zeroFillCode (code, dígitos)
- pone un código relleno de ceros en las partes numéricas
- esta función es muy util para convertir cuentas contables a un texto que se pueda ordenar con seguridad
- por ejemplo: `calc.zeroFillCode('100-01-001',5)` devuelve: `'00100-00001-00001'`.

#### mask (texto)
- convierte un texto en asteriscos según su longitud.

#### matchIfPattern (regex, texto)
- valida el texto con una expresión regular

#### prefixIf (texto, prefijo)
- si tiene un valor en `texto` retorna el `prefijo`+`texto`

#### addIf (texto, prefijo)
- similar a la función `calc.prefixIf`

#### enter (texto, titulo)
 - genera un texto con el enter `\n` como prefijo.
 - por ejemplo `calc.enter('juan','hola')` genera `'\nhola juan'`
 
#### userName
- devuelve el nombre del usuario actual.
 
#### userTurn 
- devuelve el turno del usuario actual.

#### max (valor, maximo)
- limita al máximo el resultado

#### min (valor, minimo)
- limita al mínimo el resultado

#### safeDiv (valor, división)
- divide de manera segura

#### arrayToFlags (arreglo)
- convierte un arreglo plano en un objeto (true, false).

#### trim (valor)
- quita los espacios previos y posteriores del texto.

#### trimArray (lista)
- quita los espacios previos y posteriores de la lista 
- quita lineas vacías.

#### trimTextArea (valor)
- quita los espacios previos y posteriores del texto.
- quita lineas vacías.

#### forceDataType (valor[, tipo, formato])
- regresa el valor el tipo de datos especifico y puede incluir un formato

#### appParam y getAppParam (param, tipo, formato)
- es posible leer un parámetro de la configuración _app y regresarlo en un tipo y formato especifico.

#### number (#)
- forza el valor como numérico.

#### forceNumber (#)
- forza el valor como numérico.

#### forceNumber2 (#)
- igual que `forceNumber`, pero tiene tolerancia a las comas.

#### string (valor)
- forza el valor como texto.

#### forceString (valor)
- hace lo mismo `string`.

#### forceArray (valor)
- forza el valor como un arreglo.

#### forceObject (valor)
- forza el valor como un objecto.
- si es un arreglo respeta el valor
- si no es un objeto regresa `null`.

#### forceJoin (arreglo, separador)
- separa un arreglo a un texto usando el separador indicado.
- por ejemplo `calc.forceJoin(['a','b','c'],'|')` regresa `'a|b|c'`.

#### forceJson (valor)
- forza el valor ya sea texto u objeto a regresarlo como un objeto.

#### forceId (id)
- checa sí llega un valor y en caso de vacío genera un `ObjectID` nuevo como `string`.

#### sortSimple (arreglo [, direccion, limite])
- ordena un arreglo simple de valores, no de objetos.
- la dirección puede ser `asc` (por omisión) o `desc`.
- se puede limitar la cantidad de elementos del resultado.

#### curp (nombres, apellidoPaterno, apellidoMaterno, genero, entidad, fechaNacimiento, anchoMaximo, noRemoverMalasPalabras)
- genera el CURP con los datos del objeto
- el `anchoMaximo` limita los caracteres del resultado, el CURP mide 18 digitos, pero tal vez se quiere sugerir todo menos el digito verificador en ese caso se pone 17.
- el parámetro `noRemoverMalasPalabras` es un `true` o `false` para modificar el CURP con la lista de palabras que se especifica en la RENAPO, por omision es `true`.

#### contieneMalaPalabra (texto)
- devuelte un `true` o `false` si el texto indicado coincide con la lista de malas palabras de la RENAPO.
  
#### curpOk (curp)
- valida que sea un CURP válido

#### curp2Ok (curp)
- valida que sea un CURP válido (con menos detalles)

#### curp3Ok (curp)
- valida que sea un CURP válido (con letras y números, de 12 a 18 letras, sin validar más detalles).

#### rutOk (rut)
- valida que sea un RUT válido

#### uuidOk (uuid)
- valida que sea un UUID válido

#### mergeObj (obj1, obj2)
- plancha los valores existentes en el objeto2 al objeto1.

#### mapArray (items, mapeo)
- recorre un arreglo y mapea los elementos a los nuevos key=value del mapeo.

````
calc.mapArray([{_id:1,_name:'hola'}], {id:'_id',nombre:'_name'})
````

#### profileMatch (obj1, obj2, propiedades)
- genera un % de macheo de los objetos en el arreglo de propiedades definido

#### errorInSequence (lista, inicia, error)
- revisa una lista para ver que no existan hoyos, regresa el primer problema

#### filterRef (items, key, value)
- devuelve la lista de lo que corresponde a esa referencia

#### filterInRef (items, key, values)
- devuelve la lista de lo que corresponde a esa referencia y valores

#### filterNotRef (items, key, value)
- devuelve la lista de lo que no corresponde a esa referencia

#### filterIfRef (items, key)
- devuelve la lista sí existe referencia.

#### itemsSetRef (items, key, value)
- asigna el valor a la lista en la referencia indicada.

#### itemsSetRefIfNotExists (items, key, value)
- asigna el valor a la lista en la referencia indicada si no tiene valor.

#### itemsSetExpr (items, key, expr)
- asigna el valor de la expresión a la lista en la referencia indicada.
- usa el scope del mismo registro

#### setIndication (type, lastIndication, startHour, requests)
- cambia los estatus, elimina los suspendidos o cancelados, genera nuevos id.

#### addTimeUnit (fecha, cantidad, unidad)
- calcula una nueva fecha incrementado la cantidad y unidad

#### semaphore (vencimiento, [horas, ahora, esVigenciaVerde])
- regresa un color green, yellow o red, si ya esta vencido
- también se pueden definir las horas de amarillo, por omisión 24.
- opcional mente se puede definir cuál es el día base por omisión es "ahora".
- si esVerde todo el periodo de vigencia es Verde, de la otra forma es azul hasta 1 día antes del vencimiento

#### semaphore2 (vencimiento, [horas, ahora, esVigenciaVerde])
- es la misma rutina que `semaphore` antes le agrega un dia al vencimiento.

#### semaforo (vencimiento, [horas, ahora])
- es la misma rutina que `semaphore` pero devuelve los colores en español.

#### addTimeZone (fecha)
- a una fecha hora sin la zona horaria le pone la zona horaria.
- por ejemplo: 2013-04-01T00:00:00, lo pone 2013-04-01T00:00:00-06:00

#### setTime (fecha, hora, minutos)
- pone una hora y minutos específicos a una fecha otorgada.

#### setTimeStr (fecha, tiempo)
- pone una hora (formato fecha) específico a una fecha otorgada.

#### findDuplicatesWhereRefIn (items, ref, key, values, key2, values2, key3, values3)
- obtiene una lista con diferentes criterios de filtrado

#### getRange (desde, hasta)
- devuelve una lista de fechas

#### explodeRange (fromDate, toDate, expr)
- explosiona un rango de fechas ejecutando la expresión con el scope 

#### explodeRangePreset (fromDate, toDate, preset, expr)
- explosiona un preset en un rango de fechas ejecutando la expresión con el scope 

#### isBetween (value, from, to)
- checa si esta en el rango

#### isBetweenDateTime (value, from, to)
- checa si esta en el rango convirtiendo a fechas

#### isBetweenDateAndTime (value, from, to, fromTime, toTime)
- checa si esta en el rango convirtiendo a fechas y checando el rango de horas

#### translate (value)
- traduce un texto usando el idioma del usuario

#### clearFields (items, fields)
- elimina los campos separados por comas de la lista

#### clearFieldsWhen (items, fields, attrs)
- elimina los campos separados por comas de la lista, cuando cumple la condición 

#### itemsToIdName (items)
- regresa una arreglo en una lista de objetos id y nombre.

#### paymentPlan (prestamo)
- regresa una arreglo con la tabla de amortización

#### paymentApply (prestamo, saldos, cobro)
- aplica un pago al préstamo
- regresa un objeto con 2 arreglos

#### checkList (preset, nombres)
- regresa una arreglo el check list palomeado

#### checkListMerge (checkList, vistosBuenos, vistosRegulares, vistosMalos, estaCompleto)
- regresa una arreglo el check list para ver el estatus en la solicitud

#### valueMap (items, key, value)
- regresa un objeto con las llaves y valores mapeados

#### meetsSexLimit (limiteSexo, genero)
- verifica que el genero especificado cumpla con los limites aceptables

#### meetsSexLimitSeul (limiteSexo, genero)
- verifica que el genero especificado cumpla con los limites aceptables para la guia Seul

#### meetsAgeLimit (valor, desde, fechaNacimiento, checarInferior, hoy, edadDesconocida)
- verifica que la edad especificada cumpla con los limites aceptables

#### recalcLimiteEdadDiagnostico (arreglo, fechaNacimiento, hoy, edadDesconocida)
- recalcula las edades en los diagnosticos
  
#### recalcLimitesDiagnostico (arreglo, fechaNacimiento, genero, hoy, edadDesconocida)
- recalcula los limites en los diagnosticos

#### hasDecimals (numero)
- verifica si el número indicado tiene decimales

#### hasDuplicates (arreglo, excepciones, valorARevisar)
- verifica si tiene duplicados en el arreglo
- se puede incluir una lista de excepciones

#### whereRef (arreglo, referencia, valor)
- devuelve los elementos del arreglo que tienen una referencia con un valor específico.

#### whereRefIn (arreglo, referencia, valores)
-  similar a `whereRef` con la diferencia que puede aceptar múltiples valores.
-  los valores es un arreglo
  
#### findDuplicatesWhereRefIn (arreglo, referencia, llave, valores, llave2, valores2, llave3, valores3)
- devuelve la lista de duplicados en un arreglo usando una referencia y llave.
- puede soportar una segunda y tercera llave y referencia opcional.

#### findDuplicates (arreglo, llaves)
- devuelve la lista de duplicados en un arreglo usando lista de llaves.

#### getDuplicates (arreglo)
- devuelve la lista de duplicados en un arreglo.

#### findDuplicatesMultiple (arreglo, llaves)
- devuelve la lista de duplicados en un arreglo unicamente en la lista de llaves.

#### forceNumberCurrency (texto)
- convierte a numerico un campo que tiene formato de moneda.

#### removeKeys (arreglo, llaves)
- elimina la lista de llaves del arreglo.

#### removeEnters (texto)
- elimina todos los enter `\n` de un texto.
  
#### removePrefix (texto, prefijo)
- elimina el prefijo del texto indicado.

#### removeSuffix (texto, sufijo)
- elimina el sufijo del texto indicado.

#### itemsLength (arreglo)
- obtiene el tamaño del arreglo y devuelve un cero.
  
#### getFolioFromReference (texto)
- extrae el folio de una referencia compuesta.
- por ejemplo `Pedido 1234` devuelve `1234`.

#### getAccount (cuenta, separador, nivel)
- devuelve el nivel de la cuenta contable.
- por omisión el separador es `.`.

#### isWorkingDay (fecha)
- devuelve `true` o `false` si el dia es habil tomando en cuenta la configuración general de Días Festivos.

#### getTermName (vencimiento, fecha)
- devuelve si el plazo es `Hoy`, `24 Horas` o `48 Horas`.

#### getNextLaborDay (fecha, duracion)
- devuelve la fecha del siguiete día habil tomando en cuenta la configuración general de Días Festivos.

#### rangeTable (tabla, valor)
- devuelve todos los elementos de la configuración general `app.tablaRango` que cumplen con la tabla y valor indicado que corresponde al rango del valor.

#### taxTable (tabla, importe)
- devuelve todos los elementos de la configuración general `app.tablaImpuestos` que cumplen con la tabla y valor indicado que corresponde al rango del importe.

#### taxTablePyramidal (tabla, importe, importe2)
- hace un calculo piramidal (inverso) para buscar cual es el valor que corresponde.

#### inflation (tabla, desde, ajusteInflacion, mensualidad)
- calcula el % de inflación usando alguna de las tablas de la configuración general como el INPC.

#### setInflation (arreglo, campo, inflacion)
- devulve en arreglo con la inflación aplicada al campo.

#### searchItemsInItems (arreglo1, arreglo2, prefijo)
- busca si alguno de los elementos del arreglo2 existen en el arreglo1
- se puede usar un prefijo opcional.

#### factor (valor, factor)
- multiplica un valor por el factor.
- por omisión usa el factor `1`.

#### subItemsMap (arreglo, referenciaSubItem, exprId, exprNombre)
- genera un arreglo usando una sub referencia.

#### getFilterDateRange (parametro)
- devuelve un objeto `{from, to}` usando la fecha actual y un parametro de filtro de fechas.
- parametros válidos: `all,specific,last60,last30,last15,last7,last3,yesterday,today,todayAndTomorrow,tomorrow,next3,next7,next15,next30,lastWeek,thisWeek,nextWeek,lastMonth,thisMonth,nextMonth,lastYear,thisYear,nextYear`.

#### getFilterDateRangeFrom (parametro)
- devuelve unicamente `from` usando `getFilterDateRange`.

#### getFilterDateRangeTo (parametro)
- devuelve unicamente `to` usando `getFilterDateRange`.

#### getUrlParameter (parametro)
- busca un parámetro de la url y devuelve el valor.

#### urlFromBucket (req, nombreArchivo)
- devuelve la url completa que corresponde al archivo y usando el bucket que esta configurado en ese servidor.

#### eq (valor1, valor2)
- devuelve `true` o `false` si los valores son iguales.

#### eq2 (valor1, valor2)
- es similar a `eq`, pero tiene mas tolerancia con los vacios, falsos, nulos, etc.

#### gt (valor1, valor2)
- devuelve `true` o `false` si los valor1 es mayor que valor2.
- tienen que tener valor ambos parámetros.

#### major (valor1, valor2)
- es igual que `gt`.

#### lt (valor1, valor2)
- devuelve `true` o `false` si los valor1 es menor que valor2.
- tienen que tener valor ambos parámetros.
  
#### minor (valor1, valor2)
- es igual que `lt`.
  
#### abs (numero)
- devuelve el valor absoluto númerico.

#### arrayLength (argumentos)
- suma la cantidad de elementos de los todos los arreglos especificados.

#### isArrayLength (arreglo)
- devuelve `true` o `false` si el arreglo tiene o no elementos.

#### isPositive (valor, factor)
- devuelve `true` o `false` si el valor es positivo.
- puede tener un factor adicional.

#### isNegative (valor, factor)
- devuelve `true` o `false` si el valor es negativo.
- puede tener un factor adicional.

#### r3 (cantidad1, total, cantidad2)
- calcula una regla de tres, asi `cantidad2*total/cantidad1`
- debe tener valor en los 3 valores.

#### dimensionsToVolume (dimensiones)
- calcula el volumen usando el texto largo x ancho x alto.
- por ejemplo `10x20x3` = `600`.

#### dimensionsToLengthWidthHeight (dimensiones)
- devuelve un objeto `{length, width, height}`
- leyendo las dimensiones del texto largo x ancho x alto.

#### ledgerCurrency (mayor, moneda)
- devuelve una leyenda con la cuenta y mayor en minusculas usando `/` como división.

#### isHiddenTenant ()
- devuelve `true` o `false` si en la configuración del servidor esta especificado este parámetro.

#### topKeyValue (datos)
- devuelve el valor máximo de un objeto tipo campo valor.

#### replaceAll (buscar, reemplazar, texto)
- devuelve el texto con todas las coincidencias reemplazadas.

#### proyectDate (fecha, hora, unidadTiempo, fechaMaxima, hora, diasHabiles)
- proyecta una fecha a futuro con algunas restricciones como la fecha máxima o días habiles.

#### translate (valor)
- traduce algunos valores que estan definidos en el preset.

#### nextDate (fecha, dias)
- calcula la siguiente fecha aumentado los dias y lo devuelve en moment.

#### addTimeZone (fecha)
- a un texto tipo fecha con el formato YYYY-MM-DDTHH:mm:ss el agrega la zona horaria.
- por ejemplo `calc.addTimeZone('2026-05-15T19:36:12')` regresa `'2026-05-15T19:36:12-06:00'`

#### concatDash (argumentos)
- devuelve un texto concatenando los argumentos con `' - '`

#### concatSlash (argumentos)
- devuelve un texto concatenando los argumentos con `' / '`

#### concatSlash2 (argumentos)
- devuelve un texto concatenando los argumentos con `'/'`

#### concatLodash (argumentos)
- devuelve un texto concatenando los argumentos con `'_'`
   
#### concatPairs (argumentos)
- devuelve un texto concatenando los argumentos por pares separando `campo: valor` y comas entre pares.

#### concatPairsEnter (argumentos)
- similar a `concatPairs` pero en lugar de comas le pone enter `\n`.

#### concatItemsEnter (arreglo, campo, valor, prefijo, sufijo)
- similar a `concatPairsEnter` usando un arrelgo donde se define el `campo` y `valor`.

#### concatPipe (argumentos)
- devuelve un texto concatenando los argumentos con `'|'`

#### concatDot (argumentos)
- devuelve un texto concatenando los argumentos con `'.'`
  
#### concatTab (argumentos)
- devuelve un texto concatenando los argumentos con tabs `\t`

#### concatProductName (codigo, descripcion, modelo, talla, color, estilo)
- devuelve una descripcion de un producto tomando en cuenta posibles campos extras.

#### breadCrumb (arreglo)
- devuelve un texto concatenando los argumentos con `' > '`
  
#### validarCurp (curp)
- devuelve `true` o `false` si el curp indicado cubre con las validaciones simples de tamaño y bloques de letras o números.

#### curpDate (fecha)
- devuelve la fecha con el formato que pide el CURP.

#### mergeScanner (arreglo, textoScanner)
- esta función sirve para agregar al detalle de una operación tipo artículos, un texto que contiene lo scaneado con las herramientas del sistema.
- hay una logica especial para el scanner que se usa para surtir o recibir productos en el almacén.

#### mergeArrays (argumentos)
- esta función concatena múltiples arreglos que se pueden pasar como parámetros.

#### mergeArraysByKey (arreglo1, arreglo2, llave, opciones)
- esta función une 2 arreglos que tienen una llave en común.
- la llave puede ser una referencia con puntos entre las secciones y campos.

#### existsRefIn (datos, referencia, valores)
- devuelve `true` o `false` si los valores existen en los datos usando la referencia indicada.
  
#### min (valor, minimo)
- si el valor indicado es menor que el minímo devuelve el valor en caso contrario el devuelve el mínimo.
  
#### minLimit (valor, limite)
- funciona igual que `min`.
  
#### minArgs (argumentos)
- analiza todos los argumentos y devuelve el valor minímo encontrado.

#### minItems (arreglo)
- analiza todos los elementos del arreglo y devuelve el valor minímo encontrado.

#### getMin (valor1, valor2)
- devuelve el valor menor de los 2 indicados.

#### max (valor, maximo)
- si el valor indicado es mayor que el máximo devuelve el valor en caso contrario el devuelve el máximo.

#### maxLimit (valor, limite)
- funciona igual que `max`.

#### maxArgs (argumentos)
- analiza todos los argumentos y devuelve el valor máximo encontrado.

#### maxItems (arreglo)
- analiza todos los elementos del arreglo y devuelve el valor máximo encontrado.

#### getMax (valor1, valor2)
- devuelve el valor mayor de los 2 indicados.

#### missingOver (valor)
- si el valor en menor a cero regresa el valor absoluto.

#### leftOver (valor)
- si el valor en mayor a cero regresa el valor absoluto.

#### safeDivCeil (valor1, valor2)
- ejecuta una división segura (si el valor2 es cero no falla).
- redondea un número hacia arriba hasta el siguiente número entero mayor o más cercano.

#### safeDivTrunc (valor1, valor2)
- ejecuta una división segura (si el valor2 es cero no falla).
- eliminar los decimales de un número, conservando únicamente la parte entera.

#### safeDivRound (valor1, valor2, decimales)
- ejecuta una división segura (si el valor2 es cero no falla).
- redondea el resultado usando las decimales indicadas.

#### differenceError (arreglo1, arreglo2, mensajeError)
- analiza 2 arreglos y si encuentra diferencias devuelve el mensaje error indicado.

#### forceUpperCase (texto)
- conviere un texto a mayúsculas.

#### forceLowerCase (texto)
- conviere un texto a minúsculas.

#### addDuration (fecha, duracion, opciones)
- a una fecha se le agrega una duración
- la duración se puede definir así: `8h`, `2d`, `5d`, `1w`, `2m`, `1y`, etc.

#### addDurationFormat (fecha, duracion, formato, opciones)
- simular `addDuration` pero se puede agregar un formato específico a la fecha resultado.

#### rangeFromYearMonth (año, mes)
- devuelve `{from, to}` a una fecha en un mes en particular, dando el principio y fin de mes.
- por ejemplo `calc.rangeFromYearMonth(2026, 6)` regresa `{from: '2026-06-01', to: '2026-06-30'}`.

#### fromYearMonthDay (año, mes, dia)
- regresa la fecha en formato `YYYY-MM-DD`.

#### fromYearMonth (año, mes)
- regresa la fecha inicio de mes
- por ejemplo `calc.fromYearMonth(2026, 6)` regresa `2026-06-01T00:00:00-06:00`

#### toYearMonth (año, mes)
- regresa la fecha fin de mes
- por ejemplo `calc.toYearMonth(2026, 6)` regresa `2026-06-30T23:59:59-06:00`

#### reconcileMarketSales (renglones, ventas)
- una función interna para reconciliar la ventas del sistema vs las ventas de un Marketplace.

#### blowInt (integro)
- genera una explosión de un número.
- por ejemplo `calc.blowInt(10)` regresa `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`

#### blowLot (cantidad, lote, tolerancia)
- genera una explosión de una cantidad por el tamaño del lote indicado
- por ejemplo `calc.blowLot(100, 30)` regresa `[30, 30, 30]`
- puede tener un % tolerancia para redondear.

#### inList (arreglo, llave, lista)
- analiza un campo llave de un arreglo y devuelve todos los elementos que estan en la lista.

#### notInList (arreglo, llave, lista)
- analiza un campo llave de un arreglo y devuelve todos los elementos que no estan en la lista.

#### itemsToCode (arreglo)
- convierte un arreglo de valores a un arreglo de objetos `[{id, nombre}]`.
- por ejemplo `calc.itemsToCode(['A','B','C'])` regresa `[{"id":"A","nombre":"A"},{"id":"B","nombre":"B"},{"id":"C","nombre":"C"}]`.

#### itemsToUrlKeyValue (arreglo, llave, valor)

#### urlKeyValueToItems (texto, llave, valor, opciones)

#### tipoServicioSis (tipoServicioSis, tipoPersonalNom, genero, rangoEdad, tipoCode)

#### rfcPhysicalPerson (nombre, apellidoPaterno, apellidoMaterno, fechaNacimiento)
- calcula el RFC de una persona física.

#### nom50Ok (texto)
- valida un texto siguendo las reglas de la NOM y que no exceda 50 carácteres.

#### nomEspecialesOk (texto)
- valida un texto que sigula las reglas de la NOM considerando carácteres especiales.

#### nomEspeciales2Ok (texto)
- valida un texto que sigula las reglas de la NOM considerando carácteres especiales y tienen mas consideranciones.

#### nomNoEspecialesOk (texto)
- valida un texto que sigula las reglas de la NOM sin tomar en cuenta carácteres especiales.

#### nomNoEspeciales2Ok (texto)
- valida un texto que sigula las reglas de la NOM sin tomar en cuenta carácteres especiales y otras consideraciones.

#### nomNoEspeciales3Ok (texto)
- valida un texto que sigula las reglas de la NOM sin tomar en cuenta carácteres especiales y otras consideraciones.

#### round2 (numerico)
- rendondea un importe a 2 decimales.

#### amountDiff (numero1, numero2)
- regresa la diferencia absoluta entre 2 números.

#### trunc (valor)
- eliminar los decimales de un número, conservando únicamente la parte entera.

#### preset (preset)
- devuelte un arreglo con el preset establecido.
- por ejemplo `calc.getPresetFromName('month')` regresa `{"1":"Enero","2":"Febrero","3":"Marzo","4":"Abril","5":"Mayo","6":"Junio","7":"Julio","8":"Agosto","9":"Septiembre","10":"Octubre","11":"Noviembre","12":"Diciembre"}`

#### momentName (id)
- devuelve el nombre de un momento especifico
- los momentos se configuran como un `code`.
- por ejemplo `calc.momentName('enEjecucion')` devuelve `'En Ejecución'`.

#### momentDefinition (id)
- devuelve la definición del momento si esta configurada.

#### momentInfo (id)
- devuelve toda la información del momento
- por ejemplo `calc.momentInfo('enEjecucion')` devuelve `{"partOf":"activo","nombre":"En Ejecución","id":"enEjecucion"}`

#### presetNames (preset, arreglo)
- devuelve la lista de nombres del preset pudiendo considerar el arreglo como filtro
- por ejemplo `calc.presetNames('cfg.diaSemana', ['1','2','3'])` devuelve `'Lunes, Martes, Miércoles.'`.

#### presetNamesList (preset, arreglo)
- similar a `presetNames` pero regresa un arreglo con la lista de nombres
- por ejemplo `calc.presetNamesList('cfg.diaSemana', ['1','2','3'])` devuelve `["Lunes","Martes","Miércoles"]`.

#### presetDefinition (preset, id)
- devuelve toda la información del preset.

#### setValueInArray (arreglo, campo, valor)
- a un arreglo le asigna un campo adicional con el valor específico.

#### setFactorInArray (arreglo, llaves, factor)
- en un arreglo a la lista de campos (llaves) les aplica un factor.

#### validateCfdiTotals (base, importes, descuentos, subTotal, descuento, impuestos, retenciones, total)
- valida si los totales del CFDI corresponden con todos los campos calculados.

#### getLayoutInfo (tipo)
- devuelve la definición de un layout del metadata.

#### case (objeto, filtro, default)
- ejecuta una simple función para determinar un valor de un objeto usando un filtro
- en caso de no encontrar un valor regresa el valor por omisión.

#### bigger (valor1, valor2)
- devuelve el valor mayor.

#### smaller (valor1, valor2)
- devuelve el valor menor.

#### addDays (fecha, dias, formato)
- agrega una cantidad de días (positivo o negativo) a una fecha específica.
- se puede especificar un formato opcional.

#### addMonths (fecha, meses, formato)
- agrega una cantidad de meses (positivo o negativo) a una fecha específica.
- se puede especificar un formato opcional.

#### year (fecha)
-  devuelve el año de la fecha específica.

#### years (desde, hasta)
- calcula los años entre las 2 fechas.

#### yearsToDate (fecha, ahora)
- calcula los años a hoy.
- se puede especificar el ahora para cambiar las fechas.

#### month (fecha)
- devuelve el número de mes de una fecha específica, considerando 1 = enero y 12 = diciembre.

#### monthName (fecha, verCorto)
- devuelve el nombre del mes de una fecha específica.
- se puede solicitar un nombre corto.

#### nextMonth (fecha, dia)
- agrega un mes y lo pone en un dia en particular.

#### elapsedTime (desde, hasta, unidad)
- calcula un tiempo entre 2 fechas y lo pone en la unidad especificada.

#### diffDays (desde, hasta)
- calcula la diferencia de dias entre 2 fechas

#### diffHours (desde, hasta)
- calcula la diferencia de horas entre 2 fechas

#### diffMinutes (desde, hasta)
- calcula la diferencia de minutos entre 2 fechas

#### day (fecha)
- devuelve el número de día de una fecha específica.

#### days (desde, hasta)
- calcula la diferencia de dias entre 2 fechas
  
#### dayName (fecha)
- devuelve del nombre del día de la semana que corresponde esa fecha.

#### isoWeek (fecha)
-  devuelve el número de semana segun la ISO.
  
#### isLeapYear (fecha)
- devuelve `true` o `false` si la fecha corresponde a un año bisiesto.

#### isBimester (fecha)
- devuelve `true` o `false` si la fecha corresponde a un mes que sea fin de bimestre, los meses `2,4,6,8,10,12`.

#### bimester (fecha)
- regresa el número de bimestre al que corresponde esa fecha.
- por ejemplo el bimestre 1 corresponde a los meses de enero y febrero.

#### nextBimester (fecha, dia)
- regresa la fecha en el día específico del siguiente bimestre.

#### bimesterDays (fecha)
- regresa la cantidad de dias que hay en el bimestre de la fecha específica.

#### lastDayBimester (fecha)
- regresa el último día del bimestre de la fecha específica.

#### isAnniversary (fecha, desde, hasta)

#### firstDayOfMonth (fecha)
- regresa el primer día del la fecha específica.

#### firstDayOfPeriod (año, mes)
- regresa el primer día del año y mes específico.
  
#### lastDayOfMonth (fecha)
- regresa el último día del la fecha específica.

#### lastDayOfPeriod (año, mes)
- regresa el último día del año y mes específico.
  
#### firstDayOfYear (fecha)
- regresa el primer día del año del la fecha específica.
  
#### lastDayOfYear (fecha)
- regresa el último día del año del la fecha específica.
  
#### dateDMY (fecha)
- regresa la fecha en formato DD-MM-YYYY

#### dateMDY (fecha)
- regresa la fecha en formato MM-DD-YYYY

#### dateYMD (fecha)
- regresa la fecha en formato YYYY-MM-DD

#### getDate (fecha)
- extrae la fecha sin hora de la fecha específica.

#### getTime (fecha)
- extrae la hora de la fecha específica.

#### incDatetime (fecha, cantidad, unidad)
- incrementa la fecha en la cantidad y unidad específica.

#### retention (importe, retencion1, retencion2, decimales)
- calcula el % retención usando las 2 retenciones juntas
- se puede definir el rendondeo con las decimales opcionales.

#### setRef (objeto, llave, valor)
- devuelve el objeto modificando un valor en una llave (o referencia con puntos).

#### getPresetKeyValue (preset, nombreCampo, presetPartOf, nombrePartOf) 

#### prefixItems (prefijo, arreglo) 

#### pluckWhere (arreglo, llave, atributos) 

#### pluckWhereIsEmpty (arreglo, llave, atributos) 

#### pluckEq (arreglo, llave, valor)

#### pluckUniq (arreglo, llave)

#### pluckRefMerge (arreglo, referencia)

#### pluckRefs (arreglo, llaves)

#### pluckRefKeys (arreglo, llaves, nombres, tiposDatos) 

#### pluckRef2 (doc, llave1, llave2) 

#### compareArrays (arreglo1, arreglo2, llaves) 

#### itemsSet (arreglo, llave, valor)

#### setPlan (tipo, ultimoPlan, seRepite, horaInicial, solicitudes)

#### itemsToLines (arreglo)

#### deleteFieldsFromArray (arreglo, campos)

#### unDeleteFieldsFromArray (arreglo, campos)

#### first (arreglo, filtros)

#### firstValue (arreglo)

#### firstObj (arreglo)

#### firstDef (arreglo, valorPorOmision)

#### firstSeparator (texto, separador)

#### firstValidSchedule (arreglo, campo, fecha)

#### rest (arreglo)

#### expireColor (fecha, periodo, unidad)

#### cat (importe, enganche, importePago, numPagos, periodicidad)

#### catArray (importe, enganche, pagos, periodicidad)

#### dueTimes (servicio, subTipoSolicitud, motivo, momentoDieta, criticidadZona, tiempos)

#### dueDate (vencimientoActual, tipoVencimiento, tiempo)

#### dueText (fechaVencimiento)

#### addPct (valor, pct)

#### addMargin (valor, pct)

#### subtractMargin (valor, pct)

#### amountPct (valor, pct)

#### decPct (valor, pct)

#### incPct (valor, pct)

#### globalVariable (llave, valorPorOmision)

#### globalVariableIsTrue (llave, valorPorOmision)

#### globalVariableIsFalse (llave, valorPorOmision)

#### globalVariableToArray (llave, valorPorOmision)

#### globalVariableToNumber (llave, valorPorOmision)

#### globalVariableIn (llave, valor)

#### globalVariableWhereValue (llaves, valor)

#### consecutiveType (llave, valor)

#### alertDate (vencimientoActual, tipoVencimiento, tiempo)

#### paymentPlan (operacion, opciones)

#### paymentApply (operacion, tabla, abono, recalcular)

#### paymentPlanSchool (doc, articulos)

#### scholarshipSchool (base, precioUnitario, cantidad, beca, subsidio, prestacion, precioAjustado)

#### subsidySchool (base, precioUnitario, cantidad, subsidio)

#### benefitSchool (base, precioUnitario, cantidad, prestacion)

#### paletMove (arreglo, posicionOrigen, posicionDestino)

#### saveAsText (arreglo, nombreArchivo, encoding)

#### saveAsTextFromText (texto, nombreArchivo, encoding)

#### saveFieldsAsCsv (arreglo, campos, textos, nombreArchivo, encoding)

#### saveLayoutAsText (arreglo, tipo, nombreArchivo, encoding)

#### periodFrom (tipo, periodo, ejercicio)

#### periodTo (tipo, periodo, ejercicio)

#### isPair (numero)

#### isOdd (numero)

#### validarFechaEventoAtencion (fechaEvento, fechaAtencion, conHoras)

#### inc (numero, valor)

#### incLetter (texto)

#### dec (numero, valor)

#### decLetter (texto)

#### now (formato)

#### today (formato)

#### time (formato)

#### factorial (numero)

#### random (factor, decimales)

#### error (mensaje)

#### warning (mensaje)

#### info (mensaje)

#### success (mensaje)

#### breakdownDenoms (importe, denominaciones)

#### mdPrecioSucio (parametros) 

#### serieToDate (serie)

#### cubage (tiposCajas, articulos)

#### docToTokens (doc, campos)

#### jsonValuesToText (obj)

#### itemPassFilter (elemento, filtro)

#### itemsPassFilter (arreglo, filtro)

#### scapeRegExp (texto)