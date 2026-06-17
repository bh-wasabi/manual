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

#### abs (numero)
- devuelve el valor absoluto númerico.

#### addDays (fecha, dias, formato)
- agrega una cantidad de días (positivo o negativo) a una fecha específica.
- se puede especificar un formato opcional.

#### addDuration (fecha, duracion, opciones)
- a una fecha se le agrega una duración
- la duración se puede definir así: `8h`, `2d`, `5d`, `1w`, `2m`, `1y`, etc.

#### addDurationFormat (fecha, duracion, formato, opciones)
- simular `addDuration` pero se puede agregar un formato específico a la fecha resultado.

#### addIf (texto, prefijo)
- similar a la función `calc.prefixIf`

#### addMargin (valor, pct)
- calcula un margen en base a un costo y % utilidad.

#### addMonths (fecha, meses, formato)
- agrega una cantidad de meses (positivo o negativo) a una fecha específica.
- se puede especificar un formato opcional.

#### addPct (valor, pct)
- agrega un % a un valor.

#### addTax (amount, percent[, decimales])
- calcula el importe Total directo de un porcentaje en enteros
- opcionalmente se puede redondear el resultado

#### addTaxRetention (amount, percent, retention1, retention2, [, decimales])
- calcula el importe Total directo de un porcentaje en enteros, quitando retenciones
- opcionalmente se puede redondear el resultado

#### addTimeUnit (fecha, cantidad, unidad)
- calcula una nueva fecha incrementado la cantidad y unidad

#### addTimeZone (fecha)
- a una fecha hora sin la zona horaria le pone la zona horaria.
- por ejemplo: 2013-04-01T00:00:00, lo pone 2013-04-01T00:00:00-06:00

#### addTimeZone (fecha)
- a un texto tipo fecha con el formato YYYY-MM-DDTHH:mm:ss el agrega la zona horaria.
- por ejemplo `calc.addTimeZone('2026-05-15T19:36:12')` regresa `'2026-05-15T19:36:12-06:00'`

#### alertDate (vencimientoActual, tipoVencimiento, tiempo)

#### alignCenter (texto, ancho, relleno)
- alinea el texto centrado y le rellena todo el ancho sobrante con un caracter.
- por omisión el relleno es un espacio.
- por ejemplo `calc.alignCenter('hola', 10, '*')` devuelve `'***hola***'`.

#### alignLeft (texto, ancho, relleno)
- alinea el texto a la izquierda y le rellena todo el ancho sobrante con un caracter.
- por omisión el relleno es un espacio.
- por ejemplo `calc.alignLeft('hola', 10, '*')` devuelve `'hola******'`.

#### alignRight (texto, ancho, relleno)
- alinea el texto a la derecha y le rellena todo el ancho sobrante con un caracter.
- por omisión el relleno es un espacio.
- por ejemplo `calc.alignRight('hola', 10, '*')` devuelve `'******hola'`.

#### amountDiff (numero1, numero2)
- regresa la diferencia absoluta entre 2 números.

#### amountPct (valor, pct)

#### appParam y getAppParam (param, tipo, formato)
- es posible leer un parámetro de la configuración _app y regresarlo en un tipo y formato especifico.

#### arrayInArray (valores, arreglo)
- busca sí existe alguno de los valores en un arreglo.

#### arrayLength (argumentos)
- suma la cantidad de elementos de los todos los arreglos especificados.

#### arrayToFlags (arreglo)
- convierte un arreglo plano en un objeto (true, false).

#### arrayToItems (items, key)
- convierte un arreglo simple en una lista de objetos

#### arrayToLines (arreglo)
- separa un arreglo en lineas por enter.

#### arrayWithItems (valor)
- checa que exista y que sea un arreglo con elementos

#### avgArgs (argumentos)
- hace un promedio de todos los argumentos
- por ejemplo: `calc.avgArgs(1,2,3,'4')` devuelve `2.5`

#### avgItems (argumentos)
- hace un promedio de todos los elementos del arreglo
- por ejemplo: `calc.avgItems([1,2,3,'4'])` devuelve `2.5`

#### benefitSchool (base, precioUnitario, cantidad, prestacion)

#### bigger (valor1, valor2)
- devuelve el valor mayor.

#### bimester (fecha)
- regresa el número de bimestre al que corresponde esa fecha.
- por ejemplo el bimestre 1 corresponde a los meses de enero y febrero.

#### bimesterDays (fecha)
- regresa la cantidad de dias que hay en el bimestre de la fecha específica.

#### blowInt (integro)
- genera una explosión de un número.
- por ejemplo `calc.blowInt(10)` regresa `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`

#### blowLot (cantidad, lote, tolerancia)
- genera una explosión de una cantidad por el tamaño del lote indicado
- por ejemplo `calc.blowLot(100, 30)` regresa `[30, 30, 30]`
- puede tener un % tolerancia para redondear.

#### booleanToBit (valor)
- convierte un valor logico `true` o `false` a `1` o `0`.

#### breadCrumb (arreglo)
- devuelve un texto concatenando los argumentos con `' > '`
  
#### breakdownDenoms (importe, denominaciones)
- genera un arreglo con todas la denominaciones requieridas para el importe especifico.
- por ejemplo `calc.breakdownDenoms(1234, [10, 20, 50, 100])` regresa `[{"denominacion":100,"cantidad":12,"importe":1200},{"denominacion":20,"cantidad":1,"importe":20},{"denominacion":10,"cantidad":1,"importe":10},{"denominacion":0,"cantidad":1,"importe":4}]`.

#### capitalize (valor)
- forza el resultado a la primera letra mayúsculas y las demás minúsculas (por cada palabra).

#### case (objeto, filtro, default)
- ejecuta una simple función para determinar un valor de un objeto usando un filtro
- en caso de no encontrar un valor regresa el valor por omisión.

#### cat (importe, enganche, importePago, numPagos, periodicidad)
- calcula el CAT (Costo Anual Total), según las reglas del Banco de México.
- periodicidad puede ser `'diaria', 'semanal', 'quincenal', 'mensual', 'trimestal', 'cutrimestral', 'semestral'`, por omisión es `'mensual'`.
- todos los demás campos son numéricos.

#### cat (importe, enganche, importePago, numPagos, periodicidad)
- calcula el CAT siguiendo las reglas de Banxico.

#### catArray (importe, enganche, pagos, periodicidad)
- al igual que la función `cat` con la diferencia que en pagos viene un arreglo con todos los pagos específicos.

#### catArray (importe, enganche, pagos, periodicidad)

#### checkList (preset, nombres)
- regresa una arreglo el check list palomeado

#### checkListMerge (checkList, vistosBuenos, vistosRegulares, vistosMalos, estaCompleto)
- regresa una arreglo el check list para ver el estatus en la solicitud

#### clearFields (items, fields)
- elimina los campos separados por comas de la lista

#### clearFieldsWhen (items, fields, attrs)
- elimina los campos separados por comas de la lista, cuando cumple la condición 

#### clone (obj)
- clona un objeto

#### compareArrays (arreglo1, arreglo2, llaves) 
- compara 2 arreglos en las llaves específicas.

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

#### concatCommaDot  (valor1, valor2, valorN)
- concatena varios valores, agregando comas entre los valores, al final pone un '.' si es más de 1 valor.

#### concatDash (argumentos)
- devuelve un texto concatenando los argumentos con `' - '`

#### concatDot (argumentos)
- devuelve un texto concatenando los argumentos con `'.'`
  
#### concatEnter  (valor1, valor2, valorN)
- concatena varios valores, agregando ´enter´ entre los valores sin espacios.

#### concatHost  (valor1, valor2, valorN)
- es parecido a ´concatPath´, pero agrega de prefijo el Host

#### concatItemsEnter  (items, key, value, prefix, sufix)
- genera un texto separado por Enter del campo valor con prefijo o sufijos opcionales

#### concatItemsEnter (arreglo, campo, valor, prefijo, sufijo)
- similar a `concatPairsEnter` usando un arrelgo donde se define el `campo` y `valor`.

#### concatLodash (argumentos)
- devuelve un texto concatenando los argumentos con `'_'`
   
#### concatPairs  (valor1, valor2, valor3, valor4, valorN)
- concatena varios valores en pares, separados por comas.

#### concatPairs (argumentos)
- devuelve un texto concatenando los argumentos por pares separando `campo: valor` y comas entre pares.

#### concatPairsEnter (argumentos)
- similar a `concatPairs` pero en lugar de comas le pone enter `\n`.

#### concatPath  (valor1, valor2, valorN)
- concatena varios valores, agregando ´/´ entre los valores sin espacios.

#### concatPipe  (valor1, valor2, valorN)
- concatena varios valores, agregando ´|´ entre los valores sin espacios.

#### concatPipe (argumentos)
- devuelve un texto concatenando los argumentos con `'|'`

#### concatPoint  (valor1, valor2, valorN)
- concatena varios valores, agregando ´.´ entre los valores sin espacios.

#### concatProductName (codigo, descripcion, modelo, talla, color, estilo)
- devuelve una descripcion de un producto tomando en cuenta posibles campos extras.

#### concatSlash (argumentos)
- devuelve un texto concatenando los argumentos con `' / '`

#### concatSlash2 (argumentos)
- devuelve un texto concatenando los argumentos con `'/'`

#### concatTab  (valor1, valor2, valorN)
- concatena varios valores, agregando ´tab´ entre los valores sin espacios.

#### concatTab (argumentos)
- devuelve un texto concatenando los argumentos con tabs `\t`

#### concatValueKey  (valor1, valor2)
- concatena 2 valores descripción y clave entre paréntesis.

#### consecutiveType (llave, valor)

#### contieneMalaPalabra (texto)
- devuelte un `true` o `false` si el texto indicado coincide con la lista de malas palabras de la RENAPO.
  
#### count (arreglo, campo)
- suma un los valores o campos de un objeto que tienen valor.

#### countArgs (argumentos)
- cuenta todos los argumentos con valor

#### countDiff (arreglo, llave)
- cuenta todos los elementos del arreglo que tienen la llave especificada.

#### countItems (arreglo)
- cuenta todos los elementos del arreglo

#### cubage (tiposCajas, articulos)
- calcula el cubicaje necesario para ese tipo de cajas y la lista de articulos requeridos.

#### curp (nombres, apellidoPaterno, apellidoMaterno, genero, entidad, fechaNacimiento, anchoMaximo, noRemoverMalasPalabras)
- genera el CURP con los datos del objeto
- el `anchoMaximo` limita los caracteres del resultado, el CURP mide 18 digitos, pero tal vez se quiere sugerir todo menos el digito verificador en ese caso se pone 17.
- el parámetro `noRemoverMalasPalabras` es un `true` o `false` para modificar el CURP con la lista de palabras que se especifica en la RENAPO, por omision es `true`.

#### curp2Ok (curp)
- valida que sea un CURP válido (con menos detalles)

#### curp3Ok (curp)
- valida que sea un CURP válido (con letras y números, de 12 a 18 letras, sin validar más detalles).

#### curpDate (fecha)
- devuelve la fecha con el formato que pide el CURP.

#### curpOk (curp)
- valida que sea un CURP válido

#### cut (texto, llave)
- busca la llave en el texto y si existe corta el texto hasta ese punto.
- por ejemplo `calc.cut('hola mundo!', 'mundo')` regresa `' hola'`.

#### cut2 (texto, llave)
- parecedio a `cut` pero regresa el texto que sigue a ese punto.
- por ejemplo `calc.cut2('hola mundo!', 'mundo')` regresa `'undo!'`.

#### dateDMY (fecha)
- regresa la fecha en formato DD-MM-YYYY

#### dateMDY (fecha)
- regresa la fecha en formato MM-DD-YYYY

#### dateToStrFormat (valor, formato)
- funciona igual que `formatDate`

#### dateYMD (fecha)
- regresa la fecha en formato YYYY-MM-DD

#### day (fecha)
- devuelve el número de día de una fecha específica.

#### dayName (fecha)
- devuelve del nombre del día de la semana que corresponde esa fecha.

#### days (desde, hasta)
- calcula la diferencia de dias entre 2 fechas
  
#### dec (numero, valor)
- decrementa un numero
- se puede cambiar el valor del decrementa.

#### decLetter (texto)
- decrementa una letra a la siguiente del abecedario.

#### decPct (valor, pct)
- decrementa un % de un valor

#### deductible (amount, type, percent, top)
- determina la parte deducible de un importe, ya sea por porcentaje o tope

#### deleteFieldsFromArray (arreglo, campos)
- elimina todos los campos especificados de un arreglo.

#### deleteRef (objeto, llave)
- elimina una campo del objeto

#### deleteRefInArray (arreglo, llave)
- elimina una campo del objeto en el arreglo

#### delStr (texto, posicion, tamaño)
- elimina dentro de un texto a partir de una posición, un tamaño de caracteres.
- por ejemplo `calc.delStr('hola como estas', 5, 3)` devuelve `'hola o estas'`.

#### diffDays (desde, hasta)
- calcula la diferencia de dias entre 2 fechas

#### differenceError (arreglo1, arreglo2, mensajeError)
- analiza 2 arreglos y si encuentra diferencias devuelve el mensaje error indicado.

#### diffHours (desde, hasta)
- calcula la diferencia de horas entre 2 fechas

#### diffMinutes (desde, hasta)
- calcula la diferencia de minutos entre 2 fechas

#### dimensionsToLengthWidthHeight (dimensiones)
- devuelve un objeto `{length, width, height}`
- leyendo las dimensiones del texto largo x ancho x alto.

#### dimensionsToVolume (dimensiones)
- calcula el volumen usando el texto largo x ancho x alto.
- por ejemplo `10x20x3` = `600`.

#### docToTokens (doc, campos)
- genera todos los tokens normalizados de un documento
- se puede específicar una lista de campos.

#### dueDate (vencimientoActual, tipoVencimiento, tiempo)
- calcula una fecha vencimiento.

#### dueText (fechaVencimiento)
- calcula un texto que indica el tiempo de vencimiento previo o posterior.

#### dueTimes (servicio, subTipoSolicitud, motivo, momentoDieta, criticidadZona, tiempos)

#### duration (desde, hasta)
- calcula la duración del rango de tiempos.

#### elapsedTime (desde, hasta, unidad)
- calcula un tiempo entre 2 fechas y lo pone en la unidad especificada.

#### email (email, nombre, apellido, ...)
- valida que el `email` tenga el formato correcto y concatenan el texto correctamente.

#### enter (texto, titulo)
 - genera un texto con el enter `\n` como prefijo.
 - por ejemplo `calc.enter('juan','hola')` genera `'\nhola juan'`
 
#### eq (valor1, valor2)
- devuelve `true` o `false` si los valores son iguales.

#### eq2 (valor1, valor2)
- es similar a `eq`, pero tiene mas tolerancia con los vacios, falsos, nulos, etc.

#### error (mensaje)
- manda un mensaje de error (rojo) a la pantalla del usuario.

#### errorInSequence (lista, inicia, error)
- revisa una lista para ver que no existan hoyos, regresa el primer problema

#### existsKeys (objeto, campos)
- checa sí todos los campos tienen valor.

#### existsRef (objeto, referencia)
- checa sí existe una referencia.

#### existsRefIn (datos, referencia, valores)
- devuelve `true` o `false` si los valores existen en los datos usando la referencia indicada.
  
#### expireColor (fecha, cantidad, unidad)
- devuelve el los colores `green`, `yellow`, `red` o `grey`, en base al vencimiento de la fecha.
- en el momento que esta vencido sale en rojo.
- es posible controlar el periodo amarillo con (cantidad y unidad), por omisión es `cantidad=1`, `unidad=d`, es decir el ultimo día aparece en amarillo el color.

#### expireColor (fecha, periodo, unidad)
- calula un color tipo semaforo usando la fecha, periodo y unidad de vencimiento.
- normalmente el verde es que esta vigente mas de 1 día, amarillo es que vence ese día y rojo es vencido.

#### explodeRange (fromDate, toDate, expr)
- explosiona un rango de fechas ejecutando la expresión con el scope 

#### explodeRangePreset (fromDate, toDate, preset, expr)
- explosiona un preset en un rango de fechas ejecutando la expresión con el scope 

#### extractToKeyValue (arreglo, campoLlave, campoValor)
- extrae objetos de un arreglo.

#### extractToList (arreglo, campo, filtros)
- extrae un campo de un arreglo y lo convierte a un texto separado por comas.
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.

#### factor (valor, factor)
- multiplica un valor por el factor.
- por omisión usa el factor `1`.

#### factorial (numero)
- aplica un factorial a un número.
- el producto de todos los números enteros positivos desde 1 hasta n.

#### filterIfRef (items, key)
- devuelve la lista sí existe referencia.

#### filterInRef (items, key, values)
- devuelve la lista de lo que corresponde a esa referencia y valores

#### filterNotRef (items, key, value)
- devuelve la lista de lo que no corresponde a esa referencia

#### filterRef (items, key, value)
- devuelve la lista de lo que corresponde a esa referencia

#### findDuplicates (arreglo, agrupadores)
- `arreglo`
- `agrupadores` lista de campos separados por comas

#### findDuplicates (arreglo, llaves)
- devuelve la lista de duplicados en un arreglo usando lista de llaves.

#### findDuplicatesMultiple (arreglo, llaves)
- devuelve la lista de duplicados en un arreglo unicamente en la lista de llaves.

#### findDuplicatesWhereRefIn (arreglo, referencia, llave, valores, llave2, valores2, llave3, valores3)
- devuelve la lista de duplicados en un arreglo usando una referencia y llave.
- puede soportar una segunda y tercera llave y referencia opcional.

#### findDuplicatesWhereRefIn (items, ref, key, values, key2, values2, key3, values3)
- obtiene una lista con diferentes criterios de filtrado

#### findWhere (arreglo, attributos)
- devuelve el primer elemento de la lista, con los atributos que coincidan.

#### findWhere2 (arreglo, attributos)
- es similar al anterior, pero si no encuentra nada devuelve un objeto vacío.

#### findWhereNotFalse (arreglo, llave)
- devuelve el primer elemento de la lista donde el campo llave no sea falso.

#### findWhereOptional (arreglo, atributos)
- busca el primer elemento de un arreglo que cumpla con los atributos indicados
- en este caso se eliminan los atributos falsos o vacios antes de hacer la busqueda.

#### findWhereRef (arreglo, referencia, valor [, referencia2, valor2])
- devuelve el primer elemento de la lista, usando la referencia y que el valor corresponda.
- puede tener 2 referencias (opcional).

#### first (arreglo, filtros)
- devuelve el primer elemento del arreglo.
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- si no hay resultados devuelve un objeto vacio `{}`.

#### first (arreglo, filtros)
- devuelve el primer elemento de un arreglo
- se puede aplicar un filtro opcional, para que sea el primer elemento que cumple con ese criterio.

#### firstDayOfMonth (fecha)
- regresa el primer día del la fecha específica.

#### firstDayOfPeriod (año, mes)
- regresa el primer día del año y mes específico.
  
#### firstDayOfYear (fecha)
- regresa el primer día del año del la fecha específica.
  
#### firstDef (arreglo, valorPorOmision)
- regresa el primer valor del arreglo con la opción de agregar un valor por omisión en caso de que no exista.

#### firstLike (arreglo, llave, prefijo)
- devuelve el primer elemento de la lista donde el campo llave coincide con el prefijo indicado.

#### firstObj (arreglo)
- funciona parecido a `firstValue`

#### firstSeparator (texto, separador)
- busca el primer bloque del texto usando el separador indicado.

#### firstValidSchedule (arreglo, campo, fecha)

#### firstValidSchedule (arreglo, campoHorario)
- devuleve el primer objeto del arreglo que tiene un horario valido

#### firstValue (arreglo)
- funciona unicamente con arreglos y devuelve el primer valor.

#### fn (id, parámetros...)
- ejecuta una función configurable.
- debe existir el identificador en la configuración (`_cfg`).
- puede tener algunos parámetros múltiples.
- Nota: esta función también se puede ejecutar directamente sin el prefijo `calc.`

#### forceArray (valor)
- forza el valor como un arreglo.

#### forceDataType (valor[, tipo, formato])
- regresa el valor el tipo de datos especifico y puede incluir un formato

#### forceId (id)
- checa sí llega un valor y en caso de vacío genera un `ObjectID` nuevo como `string`.

#### forceJoin (arreglo, separador)
- separa un arreglo a un texto usando el separador indicado.
- por ejemplo `calc.forceJoin(['a','b','c'],'|')` regresa `'a|b|c'`.

#### forceJson (valor)
- forza el valor ya sea texto u objeto a regresarlo como un objeto.

#### forceLowerCase (texto)
- conviere un texto a minúsculas.

#### forceNumber (#)
- forza el valor como numérico.

#### forceNumber2 (#)
- igual que `forceNumber`, pero tiene tolerancia a las comas.

#### forceNumberCurrency (texto)
- convierte a numerico un campo que tiene formato de moneda.

#### forceObject (valor)
- forza el valor como un objecto.
- si es un arreglo respeta el valor
- si no es un objeto regresa `null`.

#### forceObjectId (valor)
- funciona igual que `objectId`.

#### forceString (valor)
- hace lo mismo `string`.

#### forceUpperCase (texto)
- conviere un texto a mayúsculas.

#### format (tipo, valor, formato)
- tipo (number/date) 
- aplica el formato según el tipo de datos del valor.

#### formatCurrency (valor)
- imprime un importe en texto con formato monetario.

#### formatDate (valor, formato)
- convierte un valor a fecha usando un formato opcional.

#### fromNow (fecha, hora)
- calcula el tiempo desde cierta fecha en español.
- hora opcional 

#### fromNowDays (fecha[, desde])
- devuelve la cantidad de días de una fecha a hoy.
- desde es opcional

#### fromNowFloat (fecha, hora)
- devuelve las horas de una fecha a hoy en numérico flotante
- hora opcional 

#### fromNowHours (fecha[, desde])
- devuelve la cantidad de horas de una fecha a hoy.
- desde es opcional

#### fromNowMinutes (fecha[, desde])
- devuelve la cantidad de minutos de una fecha a hoy.
- desde es opcional

#### fromNowMonths (fecha[, desde])
- devuelve la cantidad de meses de una fecha a hoy.
- desde es opcional

#### fromNowShort (fecha)
- calcula el tiempo desde cierta fecha en español.
- en la forma mas corta.

#### fromNowShort2 (fecha)
- calcula el tiempo desde cierta fecha en español.
- en la forma mas corta diferente.

#### fromNowTime (fecha)
- devuelve las horas de una fecha a hoy en formato hh:mm

#### fromNowYears (fecha[, desde])
- devuelve la cantidad de años de una fecha a hoy.
- desde es opcional

#### fromYear (año)
- pone el primer momento de un año especifico.

#### fromYearMonth (año, mes)
- pone el primer momento de un mes especifico.

#### fromYearMonth (año, mes)
- regresa la fecha inicio de mes
- por ejemplo `calc.fromYearMonth(2026, 6)` regresa `2026-06-01T00:00:00-06:00`

#### fromYearMonthDay (año, mes, dia)
- regresa la fecha en formato `YYYY-MM-DD`.

#### getAccount (cuenta, separador, nivel)
- devuelve el nivel de la cuenta contable.
- por omisión el separador es `.`.

#### getDate (fecha)
- extrae la fecha sin hora de la fecha específica.

#### getDuplicates (arreglo)
- devuelve la lista de duplicados en un arreglo.

#### getFilterDateRange (parametro)
- devuelve un objeto `{from, to}` usando la fecha actual y un parametro de filtro de fechas.
- parametros válidos: `all,specific,last60,last30,last15,last7,last3,yesterday,today,todayAndTomorrow,tomorrow,next3,next7,next15,next30,lastWeek,thisWeek,nextWeek,lastMonth,thisMonth,nextMonth,lastYear,thisYear,nextYear`.

#### getFilterDateRangeFrom (parametro)
- devuelve unicamente `from` usando `getFilterDateRange`.

#### getFilterDateRangeTo (parametro)
- devuelve unicamente `to` usando `getFilterDateRange`.

#### getFolioFromReference (texto)
- extrae el folio de una referencia compuesta.
- por ejemplo `Pedido 1234` devuelve `1234`.

#### getHost ()
- devuelve el host donde esta corriendo la página
- por ejemplo: `https://demo.com`

#### getLayoutInfo (tipo)
- devuelve la definición de un layout del metadata.

#### getMax (valor1, valor2)
- devuelve el valor mayor de los 2 indicados.

#### getMin (valor1, valor2)
- devuelve el valor menor de los 2 indicados.

#### getNextLaborDay (fecha, duracion)
- devuelve la fecha del siguiete día habil tomando en cuenta la configuración general de Días Festivos.

#### getPreset (preset, id)
- devuelve el objeto del preset con un `id` especifico.

#### getPresetAll (preset)
- devuelve el arreglo completo del preset.

#### getPresetKeyValue (preset, nombreCampo, presetPartOf, nombrePartOf) 

#### getPresetPersona (preset, id, personaId)
- devuelve el objeto del preset con un `id` especifico y con la posibilidad de que exista a nivel persona (como primera opción).

#### getProration (items, action)
- Esta función sirve para extraer los prorrateos de una lista y concentrarlos en una nueva sección.
- supone que en la lista existe un objeto tipo arreglo para cada elemento de la lista.
- la acción es un filtro que se aplica.

#### getRange (desde, hasta)
- devuelve una lista de fechas

#### getRef (objeto, referencia)
- obtiene un valor de un objeto
- la referencia es la llave pero puede contener sub campos separados con punto, por ejemplo: `getRef({base: {nombre: 'hola'}}, 'base.nombre')` va a devolver `hola`.

#### getRefLength (objeto, referencia)
- cantidad de elementos en un arreglo que se obtiene con `getRef`.

#### getTermName (vencimiento, fecha)
- devuelve si el plazo es `Hoy`, `24 Horas` o `48 Horas`.

#### getTime (fecha)
- extrae la hora de la fecha específica.

#### getUrlParameter (parametro)
- busca un parámetro de la url y devuelve el valor.

#### globalVariable (llave, valorPorOmision)
- regresa el valor especificado en esta variable global.
- puede tener un valor por omisión.

#### globalVariableIn (llave, valores)
- devuelve `true` o `false` si la variable global esta en la lista valores especificados.

#### globalVariableIsFalse (llave, valorPorOmision)
- devuelve `true` o `false` si la variable global tiene algun valor negativo o falso.
- puede tener un valor por omisión.

#### globalVariableIsTrue (llave, valorPorOmision)
- devuelve `true` o `false` si la variable global tiene algun valor positivo o verdadero.
- puede tener un valor por omisión.

#### globalVariableToArray (llave, valorPorOmision)
- convierte una variable global a un arreglo.
- puede tener un valor por omisión.

#### globalVariableToNumber (llave, valorPorOmision)
- convierte una variable global a un numerico.
- puede tener un valor por omisión.

#### globalVariableWhereValue (llaves, valor)
- busca una variable global donde alguna de las llaves contenga el valor indicado.

#### gt (valor1, valor2)
- devuelve `true` o `false` si los valor1 es mayor que valor2.
- tienen que tener valor ambos parámetros.

#### hasDecimals (numero)
- verifica si el número indicado tiene decimales

#### hasDuplicates (arreglo, excepciones, valorARevisar)
- verifica si tiene duplicados en el arreglo
- se puede incluir una lista de excepciones

#### hasRole (roles)
- checa que el usuario actual tenga alguno de los roles, separados por comas.

#### hasValue (valor)
- devuelve `true` o `false` si tiene o no valor.

#### hasValueRef (doc, arregloReferencias)
- devuelve `true` o `false` si todas las referencias indicadas tienen valor.

#### hasValues (arreglo)
- devuelve `true` o `false` todos los elementos del arreglo tienen valor.

#### hbs (plantilla, datos)
- ejecuta una plantilla de forma manual con Handlebars y regresa el HTML o XML ya parseado.

#### if (expresion, verdadero, falso)
- ejecuta una expresión, si el resutaldo es verdadero devuelve el primer valor en caso contrario regresa el segundo valor, por ejemplo: `calc.if(1==2, 2*2, 3*3)`. genera 9.

#### ifEmpty (valor1, valor2)
- si el valor1 esta vacio regresa el valor2

#### in (valor, arreglo)
- busca sí existe un valor en un arreglo.

#### inc (numero, valor)
- incrementa un numero
- se puede cambiar el valor del incremento.

#### incDatetime (fecha, cantidad, unidad)
- incrementa la fecha en la cantidad y unidad específica.

#### incLetter (texto)
- incrementa una letra a la siguiente del abecedario.

#### incPct (valor, pct)
- incrementa un % a un valor.

#### inflation (tabla, desde, ajusteInflacion, mensualidad)
- calcula el % de inflación usando alguna de las tablas de la configuración general como el INPC.

#### info (mensaje)
- manda un mensaje de información (azul) a la pantalla del usuario.
  
#### inForce (desde, hasta, [fecha])
- checa si está vigente.
- la fecha es opcional, si no se define se usa `moment().format()`.

#### inList (arreglo, llave, lista)
- analiza un campo llave de un arreglo y devuelve todos los elementos que estan en la lista.

#### insStr (texto1, texto2, posicion)
- inserta el texto2 dentro del texto1 a partir de la posición indicada.
- por ejemplo `calc.insStr('hola mundo!', ' como estas', 10)` devuelve `'hola mundo como estas!'`.

#### int (valor)
- forza el resultado como integro.

#### integer (valor)
- funciona igual que `int`.

#### isAllTrueFalse (valor1, valor2, valorN)
- evalúa todos los argumentos y regresa un `true` si todos los valores son verdaderos o falsos.

#### isAnniversary (fecha, desde, hasta)

#### isArrayLength (arreglo)
- devuelve `true` o `false` si el arreglo tiene o no elementos.

#### isBetween (value, from, to)
- checa si esta en el rango

#### isBetweenDateAndTime (value, from, to, fromTime, toTime)
- checa si esta en el rango convirtiendo a fechas y checando el rango de horas

#### isBetweenDateTime (value, from, to)
- checa si esta en el rango convirtiendo a fechas

#### isBimester (fecha)
- devuelve `true` o `false` si la fecha corresponde a un mes que sea fin de bimestre, los meses `2,4,6,8,10,12`.

#### isEmpty (valor)
- checa que el valor tenga datos o no sea un objeto o arreglo vacio.

#### isFalse (valor)
- evalúa si el valor es `false`.

#### isHiddenTenant ()
- devuelve `true` o `false` si en la configuración del servidor esta especificado este parámetro.

#### isJson (valor)
- checa si el JSON válido

#### isLeapYear (fecha)
- devuelve `true` o `false` si la fecha corresponde a un año bisiesto.

#### isNegative (valor, factor)
- devuelve `true` o `false` si el valor es negativo.
- puede tener un factor adicional.

#### isNotEmpty (valor)
- nega al isEmpty

#### isNull (valor, valorPorOmision)
- checa si el valor es nulo, devuelve el valor por omisión.
- otra forma de lograr es poner la variable entre paréntesis y hacer un "or" contra el valor por omisión, por ejemplo: `(@valor||'')`.

#### isNumeric (valor)
- evalua el valor para ver si puede ser un numérico, incluso si es un texto busca si es completamente númerico.
- regresa true o false.

#### isOdd (numero)
- valida si el número es inpar.
  
#### isoWeek (fecha)
-  devuelve el número de semana segun la ISO.
  
#### isPair (numero)
- valida si el número es par.

#### isPositive (valor, factor)
- devuelve `true` o `false` si el valor es positivo.
- puede tener un factor adicional.

#### isTrue (valor)
- evalúa si el valor es verdadero.

#### isWorkingDay (fecha)
- devuelve `true` o `false` si el dia es habil tomando en cuenta la configuración general de Días Festivos.

#### itemPassFilter (elemento, filtro)
- determina si un elemento pasa un filtro específico.

#### itemsInArray (arreglo1, llave, arreglo2)
- extrae una sub lista del arreglo1 donde exista la llave (del arreglo1) en en arreglo2
- el arreglo2 debe ser un arreglo simple.

Ejemplo:
````
calc.itemsInArray([{id:1, nombre:'uno'}, {id:4, nombre: 'cuatro'}], 'id', [1,2,3])
````
#### itemsLength (arreglo)
- obtiene el tamaño del arreglo y devuelve un cero.
  
#### itemsPassFilter (arreglo, filtro)
- determina si todo el arreglo pasa un filtro específico.

#### itemsSet (arreglo, llave, valor)
- le asigna un valor en una llave específica en todo el arreglo.

#### itemsSetExpr (items, key, expr)
- asigna el valor de la expresión a la lista en la referencia indicada.
- usa el scope del mismo registro

#### itemsSetRef (items, key, value)
- asigna el valor a la lista en la referencia indicada.

#### itemsSetRefIfNotExists (items, key, value)
- asigna el valor a la lista en la referencia indicada si no tiene valor.

#### itemsToCode (arreglo)
- convierte un arreglo de valores a un arreglo de objetos `[{id, nombre}]`.
- por ejemplo `calc.itemsToCode(['A','B','C'])` regresa `[{"id":"A","nombre":"A"},{"id":"B","nombre":"B"},{"id":"C","nombre":"C"}]`.

#### itemsToIdName (items)
- regresa una arreglo en una lista de objetos id y nombre.

#### itemsToLines (arreglo)
- genera un texto separado por Enter para cada línea.

#### itemsToLines (arreglo)
- genera un texto separado por enter `\n` para todos los elementos.

#### itemsToUrlKeyValue (arreglo, llave, valor)
- convierte un arreglo a URL extrayendo los campos indicados (llave y valor)

#### join (arreglo, control)
- convierte un arreglo a un texto separado por comas
- el control es un segundo arreglo opcional que nos indica si generar el elemento o no.

#### joinAndTrimItems (arreglo, separador)
- hace lo mismo que `joinItems` pero le aplica un `trim` a cada valor.

#### joinArraysById (arreglo1, arreglo2, arregloN)
- une n arreglos usando el campo `id` como llave.

#### joinArraysByKey (arreglo1, arreglo2, llave)
- une 2 arreglos usando una campo llave en común.

#### joinItems (arreglo, separador)
- convierte un arreglo a un texto con un separador especial.

#### joinPreset (items, preset, itemKey, presetKey)
- une una lista con un preset, usando las llaves para encontrar los id.

#### jsonValuesToText (obj)
- extrae todos los valores del objeto y los separa con un espacio.

#### keys (obj)
- obtiene la lista de llaves

#### lastDayBimester (fecha)
- regresa el último día del bimestre de la fecha específica.

#### lastDayOfMonth (fecha)
- regresa el último día del la fecha específica.

#### lastDayOfPeriod (año, mes)
- regresa el último día del año y mes específico.
  
#### lastDayOfYear (fecha)
- regresa el último día del año del la fecha específica.
  
#### ledgerCurrency (mayor, moneda)
- devuelve una leyenda con la cuenta y mayor en minusculas usando `/` como división.

#### leftOver (valor)
- si el valor en mayor a cero regresa el valor absoluto.

#### leftStr (texto, posicion)
- obtiene los caracteres a la izquierda de la posición en el texto.
- por ejemplo `calc.leftStr('hola mundo!', 6)` devuelve `'hola m'`.

#### length (texto)
- número de carácteres en texto

#### log (parámetros...)
- despliega en la consola los parámetros indicados.

#### lookup (arreglo, filtros) o (arreglo, lista de campos, valores...)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- a diferencia de `match` esta comando regresa el primer registro que coincida con el filtro.
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

#### lookupInPreset (preset, filtros) o (preset, lista de campos, valores...)
- obtiene el `preset` (con todos sus campos)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- regresa el primer registro que coincida con el filtro.
- si no hay resultados devuelve un objeto vacío `{}`.

#### lowerCase (valor)
- forza el resultado a minúsculas.

#### lt (valor1, valor2)
- devuelve `true` o `false` si los valor1 es menor que valor2.
- tienen que tener valor ambos parámetros.
  
#### major (valor1, valor2)
- es igual que `gt`.

#### map (arreglo, expr)
- recorre un arreglo y evalúa la expresión para cada elemento del arreglo.
- al final queda un arreglo con todos los valores calculados. 

#### mapArray (items, mapeo)
- recorre un arreglo y mapea los elementos a los nuevos key=value del mapeo.

````
calc.mapArray([{_id:1,_name:'hola'}], {id:'_id',nombre:'_name'})
````

#### mapKeyValue (arreglo, keyValue)
- para un arreglo ejecuta una transformacion de una llave en particular
- el valor puede ser una expresion usando el contexto del elemento del arreglo.
- key value es un objeto tipo `{"campo":"valor"}`.

#### mapReduce (arreglo, agrupadores, sumar)
- `arreglo`
- `agrupadores` lista de campos separados por comas
- `sumar` lista de campos separados por comas

#### mask (texto)
- convierte un texto en asteriscos según su longitud.

#### match (arreglo, filtros) o (arreglo, lista de campos, valores...)
- opcionalmente se puede agregar un filtro, debe ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`.
- también soporta una lista de campos (separada por comas) y los valores como parámetros adicionales.
- si no hay resultados devuelve un arreglo vacío `[]`.

#### matchIfPattern (regex, texto)
- valida el texto con una expresión regular

#### max (valor, maximo)
- limita al máximo el resultado

#### max (valor, maximo)
- si el valor indicado es mayor que el máximo devuelve el valor en caso contrario el devuelve el máximo.

#### maxArgs (argumentos)
- analiza todos los argumentos y devuelve el valor máximo encontrado.

#### maxItems (arreglo)
- analiza todos los elementos del arreglo y devuelve el valor máximo encontrado.

#### maxLimit (valor, limite)
- funciona igual que `max`.

#### maxStringLength (texto, max)
- limita el texto a un máximo.

#### mdPrecioSucio (parametros) 
- regresa un precio sucio para el módulo de mercado de dinero.

#### meetsAgeLimit (valor, desde, fechaNacimiento, checarInferior, hoy, edadDesconocida)
- verifica que la edad especificada cumpla con los limites aceptables

#### meetsSexLimit (limiteSexo, genero)
- verifica que el genero especificado cumpla con los limites aceptables

#### meetsSexLimitSeul (limiteSexo, genero)
- verifica que el genero especificado cumpla con los limites aceptables para la guia Seul

#### mergeArrays (argumentos)
- esta función concatena múltiples arreglos que se pueden pasar como parámetros.

#### mergeArraysByKey (arreglo1, arreglo2, llave, opciones)
- esta función une 2 arreglos que tienen una llave en común.
- la llave puede ser una referencia con puntos entre las secciones y campos.

#### mergeArraysByKey (arreglo1, arreglo2, llaves, opciones)
- puede hacer un `merge` entre 2 arreglos usando una o varias llaves separadas por comas.

#### mergeMasterDetail (mater, detalle, campos, mapeo, usarDetalle)
- sirve para generar un resultado uniforme, devuelve un arreglo.
- master es el encabezado (objeto)
- detalle (opcional) es un arreglo
- mapeo (opcional) lista de campos separados por comas, y es posible renombrar el campo, por ejemplo `importe,referencia` o `importe,referencia=ref`.
- usarDetalle (opcional), es un valor tipo `Boolean` para controlar si se usa o no el detalle, por omisión es verdadero.

#### mergeObj (obj1, obj2)
- plancha los valores existentes en el objeto2 al objeto1.

#### mergeScanner (arreglo, textoScanner)
- esta función sirve para agregar al detalle de una operación tipo artículos, un texto que contiene lo scaneado con las herramientas del sistema.
- hay una logica especial para el scanner que se usa para surtir o recibir productos en el almacén.

#### mergeToMaster (original, nuevo, master, llave)
- busca los cambios entre el arreglo nuevo y el original, y los aplica en master, usando el campo llave indicada
- deben ser arreglos de objetos todos.
- devuelve un arreglo que seria el nuevo master con los cambios.

#### min (valor, minimo)
- limita al mínimo el resultado

#### min (valor, minimo)
- si el valor indicado es menor que el minímo devuelve el valor en caso contrario el devuelve el mínimo.
  
#### minArgs (argumentos)
- analiza todos los argumentos y devuelve el valor minímo encontrado.

#### minItems (arreglo)
- analiza todos los elementos del arreglo y devuelve el valor minímo encontrado.

#### minLimit (valor, limite)
- funciona igual que `min`.
  
#### minor (valor1, valor2)
- es igual que `lt`.
  
#### missingOver (valor)
- si el valor en menor a cero regresa el valor absoluto.

#### momentDefinition (id)
- devuelve la definición del momento si esta configurada.

#### momentInfo (id)
- devuelve toda la información del momento
- por ejemplo `calc.momentInfo('enEjecucion')` devuelve `{"partOf":"activo","nombre":"En Ejecución","id":"enEjecucion"}`

#### momentName (id)
- devuelve el nombre de un momento especifico
- los momentos se configuran como un `code`.
- por ejemplo `calc.momentName('enEjecucion')` devuelve `'En Ejecución'`.

#### month (fecha)
- devuelve el número de mes de una fecha específica, considerando 1 = enero y 12 = diciembre.

#### monthName (fecha, verCorto)
- devuelve el nombre del mes de una fecha específica.
- se puede solicitar un nombre corto.

#### names (obj)
- obtiene la lista de nombres

#### netDiscount (argumentos)
- calcula un descuento neto en cascada usando cada parametro como un descuento adicional.
- por ejemplo `calc.netDiscount(10,20,30)` devuelve `49.6`.

#### newDoc (doc o docs, [tipo, deleteRef, untilRef])
- genera un nuevo ID, y pone la sección `_created`.

#### newId (tipo)
- genera un nuevo ID, se pueden usar los siguientes tipos (`uuid`, `shortid`, `shortid32`).

#### newUuid ()
- genera un uuid nuevo.
- es similar a usar `calc.newId('uuid')`

#### nextBimester (fecha, dia)
- regresa la fecha en el día específico del siguiente bimestre.

#### nextDate (fecha, dias)
- calcula la siguiente fecha aumentado los dias y lo devuelve en moment.

#### nextMonth (fecha, dia)
- agrega un mes y lo pone en un dia en particular.

#### nom50Ok (texto)
- valida un texto siguendo las reglas de la NOM y que no exceda 50 carácteres.

#### nomEspeciales2Ok (texto)
- valida un texto que sigula las reglas de la NOM considerando carácteres especiales y tienen mas consideranciones.

#### nomEspecialesOk (texto)
- valida un texto que sigula las reglas de la NOM considerando carácteres especiales.

#### nomNoEspeciales2Ok (texto)
- valida un texto que sigula las reglas de la NOM sin tomar en cuenta carácteres especiales y otras consideraciones.

#### nomNoEspeciales3Ok (texto)
- valida un texto que sigula las reglas de la NOM sin tomar en cuenta carácteres especiales y otras consideraciones.

#### nomNoEspecialesOk (texto)
- valida un texto que sigula las reglas de la NOM sin tomar en cuenta carácteres especiales.

#### normalize (valor)
- normalize el resultado como texto.

#### notDeductible (amount, type, percent, top)
- determina la parte no deducible de un importe, ya sea por porcentaje o tope

#### notFalse (valor)
- evalúa si el valor no es `false`, `'no'`, `'false'`, `'falso'`.

#### notIn (valor, arreglo)
- busca no existe un valor en un arreglo.

#### notInList (arreglo, llave, lista)
- analiza un campo llave de un arreglo y devuelve todos los elementos que no estan en la lista.

#### notMatch (arreglo, filtros) o (arreglo, lista de campos, valores...)
- es igual que `match`, pero devuelve lo que no coincide.

#### notWhere (arreglo, attributos)
- devuelve una lista, con los atributos que no coincidan.

#### now (formato)
- devuelve la fecha y hora actual
- se puede especificar un formato

#### nullIf (valor1, valor2)
- si el valor1 es igual al valor2 devuelve un `null`.

#### number (#)
- forza el valor como numérico.

#### number (valor)
- forza el resultado como numérico.

#### numberInText (valor)
- imprime un importe en texto.

#### object (lista, [valores])
- convierte arreglos en objetos.

#### objectId ()
- regresa un ObjectID de mongo nuevo.
- regresa un texto

#### pair (campo, valor, valor2, valor3)
- concatena un campo/valor si tiene valor
- puede concatenar hasta 3 valores
- por ejemplo: `calc.pair('nombre','juan','perez','lopez')`. genera 'nombre: juan perez lopez'.

#### pairIf (condicion, campo, valor, valor2, valor3)
- similar a la función calc.pair con la opción de agregar una condicion al principio.

#### paletMove (arreglo, posicionOrigen, posicionDestino)

#### parse (texto)
- convierte un texto JSON a objeto.

#### paymentApply (operacion, tabla, abono, recalcular)

#### paymentApply (prestamo, saldos, cobro)
- aplica un pago al préstamo
- regresa un objeto con 2 arreglos

#### paymentPlan (operacion, opciones)

#### paymentPlan (prestamo)
- regresa una arreglo con la tabla de amortización

#### paymentPlanSchool (doc, articulos)

#### periodFrom (tipo, periodo, ejercicio)

#### periodTo (tipo, periodo, ejercicio)

#### pesos (valor)
- imprime un importe en texto (pesos).

#### pluck (arreglo, llave)
- genera un nuevo arreglo con las puras llaves.

#### pluckEq (arreglo, llave, valor)
- extrae la lista cuando el campo llave corresponde con el valor.

#### pluckExpr (arreglo, llave)
- genera un nuevo arreglo con las puras llaves. 
- la llave puede ser una expresión.

#### pluckExprHasValue (arreglo, llave)
- busca sí en los resultados existe alguno `true`.

#### pluckRef (arreglo, llave)
- genera un nuevo arreglo con las puras llaves. 
- buscando en el objeto la referencia.

#### pluckRef2 (doc, llave1, llave2) 

#### pluckRefHasValue (arreglo[, llave])
- busca sí en los resultados existe alguno `true` o si tiene la llave opcional.

#### pluckRefKeys (arreglo, llaves, nombres, tiposDatos) 

#### pluckRefKeys (arreglo, llaves[, nombres, tipoDatos])
- genera un nuevo arreglo con múltiples referencias con la opción de cambiar de nombre la llave.

#### pluckRefMerge (arreglo, referencia)
- concatena todos los sub arreglos que vienen en la referencia indicada.

#### pluckRefs (arreglo, llaves)
- extrae todas las referencias de arreglo y lo une en un nuevo arreglo.

#### pluckUniq (arreglo, llave)
- extrae la lista de arreglo y devuelve los valores únicos.

#### pluckWhere (arreglo, llave, atributos) 
- obtiene la lista de la llave aplicando el filtro de los atributos.

#### pluckWhereIsEmpty (arreglo, llave, atributos) 
- valida que la lista obtenida este completamente vacia.

#### posStr (texto1, texto2)
- obtiene la poisición si existe el texto2 dentro del texto1
- por ejemplo `calc.posStr('hola como estas', 'como')` devuelve `5`.

#### prefixIf (texto, prefijo)
- si tiene un valor en `texto` retorna el `prefijo`+`texto`

#### prefixItems (prefijo, arreglo) 
- a un arreglo de valores le agrega el prefijo a todos los elementos.

#### preset (id)
- devuelve el preset completo.

#### preset (preset)
- devuelte un arreglo con el preset establecido.
- por ejemplo `calc.getPresetFromName('month')` regresa `{"1":"Enero","2":"Febrero","3":"Marzo","4":"Abril","5":"Mayo","6":"Junio","7":"Julio","8":"Agosto","9":"Septiembre","10":"Octubre","11":"Noviembre","12":"Diciembre"}`

#### presetDefinition (preset, id)
- devuelve toda la información del preset.

#### presetIdWhere (preset, filtro)
- devuelve la lista de id, del preset que corresponde al filtro.

#### presetInfo (preset, id)
- devuelve los datos de un `preset` especifico con un `id` especifico.

#### presetName (preset, id)
- devuelve el nombre de un `preset` especifico con un `id` especifico.

#### presetNames (preset, arreglo)
- devuelve la lista de nombres del preset pudiendo considerar el arreglo como filtro
- por ejemplo `calc.presetNames('cfg.diaSemana', ['1','2','3'])` devuelve `'Lunes, Martes, Miércoles.'`.

#### presetNamesList (preset, arreglo)
- similar a `presetNames` pero regresa un arreglo con la lista de nombres
- por ejemplo `calc.presetNamesList('cfg.diaSemana', ['1','2','3'])` devuelve `["Lunes","Martes","Miércoles"]`.

#### presetNotIn (preset, excluir, separadoComas)
- devuelve un arreglo con la lista o separado por Comas de la lista excluyendo la lista

#### presetToArray (preset, key)
- convierte un preset a un arreglo donde `key` es el nombre del `id`.

#### printIf (condicion, texto)
- si la condiciones es verdadera imprime el texto, 
- si no devuelve ''

#### profileMatch (obj1, obj2, propiedades)
- genera un % de macheo de los objetos en el arreglo de propiedades definido

#### promoDiscount
- calcula los descuentos usando las promociones aplicadas
  
#### promoId
- devuelve el id de la promoción aplicada

#### promoName
- devuelve el nombre de la promoción aplicada

#### prorrate (arreglo, campo, valor, tipo)
- `arreglo` arreglo a usar
- `campo` campo a modificar
- `valor` valor numérico a prorratear
- `tipo` por omisión `div` (hace una división del importe entre la cantidad de elementos del arreglo).

#### proyectDate (fecha, hora, unidadTiempo, fechaMaxima, hora, diasHabiles)
- proyecta una fecha a futuro con algunas restricciones como la fecha máxima o días habiles.

#### quotes (texto, comilla)
- pone el texto entre comillas dobles por omisión

#### r3 (cantidad1, total, cantidad2)
- calcula una regla de tres, asi `cantidad2*total/cantidad1`
- debe tener valor en los 3 valores.

#### random (factor, decimales)
- devulve un numero al azar
- por omisión regresa un numero entre 0 y 1
- se puede aplicar un factor y decimales.

#### rangeFromYearMonth (año, mes)
- devuelve `{from, to}` a una fecha en un mes en particular, dando el principio y fin de mes.
- por ejemplo `calc.rangeFromYearMonth(2026, 6)` regresa `{from: '2026-06-01', to: '2026-06-30'}`.

#### rangeTable (tabla, valor)
- devuelve todos los elementos de la configuración general `app.tablaRango` que cumplen con la tabla y valor indicado que corresponde al rango del valor.

#### recalcLimiteEdadDiagnostico (arreglo, fechaNacimiento, hoy, edadDesconocida)
- recalcula las edades en los diagnosticos
  
#### recalcLimitesDiagnostico (arreglo, fechaNacimiento, genero, hoy, edadDesconocida)
- recalcula los limites en los diagnosticos

#### reconcileMarketSales (renglones, ventas)
- una función interna para reconciliar la ventas del sistema vs las ventas de un Marketplace.

#### reconcilePreset (preset, lista, listaCampo, filtro, nombreCampo, camposCopiar)
- concilia un preset con una lista especifica.
- listaCampo es el nombre del campo que contiene el `id` en la lista.
- el filtro usa la sintaxis "campo=valor&campo2=valor2" (opcional).
- regresa la lista conciliada con el nombre del campo especifico, por omisión es `exists`.
- es posible poner una lista de campos separadas por comas de campos adicionales a copiar.
- por ejemplo: `reconcilePreset('app.tipoAdjunto', [{id: 'foto'}], 'id')`

#### removeEmptyRows (arreglo, campo)
- elimina los renglones que no tienen valor en el campo indicado.

#### removeEnters (texto)
- elimina todos los enter `\n` de un texto.
  
#### removeKeys (arreglo, llaves)
- elimina la lista de llaves del arreglo.

#### removePrefix (texto, prefijo)
- elimina el prefijo del texto indicado.

#### removeSuffix (texto, sufijo)
- elimina el sufijo del texto indicado.

#### repeat (valor, veces)
- genera un texto con el texto repetido la veces indicadas.

#### replaceAll (buscar, reemplazar, texto)
- devuelve el texto con todas las coincidencias reemplazadas.

#### rest (arreglo)
- regresa el resto del arreglo quitando el primer elemento.

#### retention (importe, retencion1, retencion2, decimales)
- calcula el % retención usando las 2 retenciones juntas
- se puede definir el rendondeo con las decimales opcionales.

#### rfcOk (rfc)
- valida que el `rfc` tenga el formato correcto.

#### rfcPhysicalPerson (nombre, apellidoPaterno, apellidoMaterno, fechaNacimiento)
- calcula el RFC de la persona Física.

#### rfcPhysicalPerson (nombre, apellidoPaterno, apellidoMaterno, fechaNacimiento)
- calcula el RFC de una persona física.

#### rightStr (texto, posicion)
- obtiene los caracteres a la izquierda de la posición en el texto.
- por ejemplo `calc.rightStr('hola mundo!', 6)` devuelve `' mundo!'`.

#### round(importe, decimales)
- redondea el importe a la decimales indicadas

#### round2 (numerico)
- rendondea un importe a 2 decimales.

#### rutOk (rut)
- valida que sea un RUT válido

#### safeDiv (valor, división)
- divide de manera segura

#### safeDivCeil (valor1, valor2)
- ejecuta una división segura (si el valor2 es cero no falla).
- redondea un número hacia arriba hasta el siguiente número entero mayor o más cercano.

#### safeDivRound (valor1, valor2, decimales)
- ejecuta una división segura (si el valor2 es cero no falla).
- redondea el resultado usando las decimales indicadas.

#### safeDivTrunc (valor1, valor2)
- ejecuta una división segura (si el valor2 es cero no falla).
- eliminar los decimales de un número, conservando únicamente la parte entera.

#### saveAsText (arreglo, nombreArchivo, encoding)
- guarda un arreglo como un archivo de texto separado por `\r\n`.
- el encodig por omisión es utf-8

#### saveAsTextFromText (texto, nombreArchivo, encoding)
- guarda un texto en un archivo de texto.
- el encodig por omisión es utf-8

#### saveFieldsAsCsv (arreglo, campos, textos, nombreArchivo, encoding)
- guarda un arreglo como un archivo csv.
- el encodig por omisión es utf-8

#### saveLayoutAsText (arreglo, tipo, nombreArchivo, encoding)
- guarda un arreglo usando un layout configurado en el metadata.
- el encodig por omisión es utf-8

#### scapeRegExp (texto)
- escapa todos los carácteres especiales para poder ejecutar una consulta en la base de datos.
#### scholarshipSchool (base, precioUnitario, cantidad, beca, subsidio, prestacion, precioAjustado)

#### searchItemsInItems (arreglo1, arreglo2, prefijo)
- busca si alguno de los elementos del arreglo2 existen en el arreglo1
- se puede usar un prefijo opcional.

#### semaforo (vencimiento, [horas, ahora])
- es la misma rutina que `semaphore` pero devuelve los colores en español.

#### semaphore (vencimiento, [horas, ahora, esVigenciaVerde])
- regresa un color green, yellow o red, si ya esta vencido
- también se pueden definir las horas de amarillo, por omisión 24.
- opcional mente se puede definir cuál es el día base por omisión es "ahora".
- si esVerde todo el periodo de vigencia es Verde, de la otra forma es azul hasta 1 día antes del vencimiento

#### semaphore2 (vencimiento, [horas, ahora, esVigenciaVerde])
- es la misma rutina que `semaphore` antes le agrega un dia al vencimiento.

#### serieToDate (serie)
- convierte una serie de mercado dinero a una fecha vencimiento.

#### setFactorInArray (arreglo, llaves, factor)
- en un arreglo a la lista de campos (llaves) les aplica un factor.

#### setIndication (type, lastIndication, startHour, requests)
- cambia los estatus, elimina los suspendidos o cancelados, genera nuevos id.

#### setInflation (arreglo, campo, inflacion)
- devulve en arreglo con la inflación aplicada al campo.

#### setPlan (tipo, ultimoPlan, seRepite, horaInicial, solicitudes)

#### setRef (objeto, llave, valor)
- devuelve el objeto modificando un valor en una llave (o referencia con puntos).

#### setTime (fecha, hora, minutos)
- pone una hora y minutos específicos a una fecha otorgada.

#### setTimeStr (fecha, tiempo)
- pone una hora (formato fecha) específico a una fecha otorgada.

#### setValueInArray (arreglo, campo, valor)
- a un arreglo le asigna un campo adicional con el valor específico.

#### sha1 (texto)
- genera un hash.

#### sha512 (texto)
- genera un hash tipo `sha512` del texto indicado.

#### smaller (valor1, valor2)
- devuelve el valor menor.

#### sortArray(arreglo, campos)
- ordena un arreglo de objetos
- lista de campos separados por comas.

#### sortSimple (arreglo [, direccion, limite])
- ordena un arreglo simple de valores, no de objetos.
- la dirección puede ser `asc` (por omisión) o `desc`.
- se puede limitar la cantidad de elementos del resultado.

#### split (texto, separador) 
- hace lo mismo que `splitAndTrim`.

#### split (texto, separador)
- convierte un text (separado por comas) a un arreglo
- por omisión el separador es `,`

#### splitAndTrim (texto, separador) 
- convierte un texto a un arreglo
- por omisión usa la coma como separador
- si lo valores tienen espacios el aplica un `trim`.

#### splitAndTrimFirst (texto, separador) 
- es igual que `splitAndTrim` pero devulve unicamente el primer valor del arreglo.

#### string (valor)
- forza el valor como texto.

#### stringify (objeto)
- convierte un objeto a una cadena de texto JSON.

#### strToDateFormat (valor, formato)
- convierte un texto a fecha usando momentjs para que tenga mucho mas tolerancia en el valor que llega.
- el formato puede ayudar a definir en que formato llega la fecha y en que formato se devuelve el resultado.

#### strToDateTimeFormat (fechaStr, horaStr, formato)
- convierte una fecha y hora por separando en una fecha y hora juntos
- puede tener un formato específico la fecha.
- por ejemplo `calc.strToDateTimeFormat('2026-12-31','19:20')` devuelve `'2026-12-31T19:20:00-06:00'`

#### strToItems (texto, separador)
- desglosa una lista de un texto, en el fondo usa la función `splitAndTrim`.
- por omisión usa la coma como separador.
- por ejemplo `calc.strToItems('a,b,c,d,e')` devuelve un arreglo de textos `['a','b','c','d','e']`.

#### strToItemsQuotes (texto, separador, comilla)
- hace algo similar a `strToItems` pero adicionalmente le agrega comillas al resultado.
- por ejemplo `calc.strToItemsQuotes('1,2,3,4',',','"')` regresa `['"1"', '"2"', '"3"', '"4"']`.

#### strToNumber (texto)
- convierte un texto a numerico, incluso forzando el valor si tiene comas.
- por ejemplo `calc.strToNumber('123,456.78')` devuelve `123456.78`

#### subItemsMap (arreglo, referenciaSubItem, exprId, exprNombre)
- genera un arreglo usando una sub referencia.

#### subsidySchool (base, precioUnitario, cantidad, subsidio)

#### substr (texto, inicio, tamaño)
- obtiene el `substr` del texto indicado.

#### subtractMargin (valor, pct)

#### success (mensaje)
- manda un mensaje de exito (verde) a la pantalla del usuario.

#### sum (arreglo, campo)
- suma un campo del arreglo o los campos de un objeto numéricos

#### sumArgs (argumentos)
- suma todos los argumentos
- por ejemplo: `calc.sumArgs(1,2,3,'4')` devuelve `10`

#### sumExpr (arreglo, expresión)
- suma las expresiones del arreglo

#### sumItems (arreglo)
- suma la lista de todos los elementos del arreglo
- por ejemplo: `calc.sumItems([1,2,3,'4'])` devuelve `10`

#### sumRef (arreglo, referencia)
- suma las referencias del arreglo

#### sumRefWhere (arreglo, referencia, filtro)
- suma las referencias del arreglo, aplicando un filtro previo

#### tagsToArray (preset, key)
- convierte un arreglo simple donde `key` es el nombre del `id`.

#### tagsWherePresetHas (tags, preset, attributos)
- devuelve los tags que cumplen con los attributos indicadas.

#### tax (amount, percent[, decimales])
- calcula el impuesto directo de un porcentaje en enteros
- opcionalmente se puede redondear el resultado

#### taxAmount (preset, taxTypes, amount, filter)
- Esta función regresa el importe de impuestos a nivel línea.

#### taxBreakdown (preset, items, grandTotal, action)
- Esta función regresa el desglose de los impuestos totales de un movimiento.

#### taxExcluded (amount, percent[, decimales])
- calcula el importe sin el impuesto incluido
- opcionalmente se puede redondear el resultado

#### taxIncluded (amount, percent[, decimales])
- calcula el impuesto incluido de un precio que incluye impuestos
- opcionalmente se puede redondear el resultado

#### taxTable (tabla, importe)
- devuelve todos los elementos de la configuración general `app.tablaImpuestos` que cumplen con la tabla y valor indicado que corresponde al rango del importe.

#### taxTablePyramidal (tabla, importe, importe2)
- hace un calculo piramidal (inverso) para buscar cual es el valor que corresponde.

#### text (valor)
- forza el resultado como texto.

#### time (formato)
- devuelve la hora actual
- se puede especificar un formato

#### tipoServicioSis (tipoServicioSis, tipoPersonalNom, genero, rangoEdad, tipoCode)

#### toArray (valor1, valor2, valorN)
- convierte los parámetros a un arreglo.

#### today (formato)
- devuelve la fecha sin hora actual
- se puede especificar un formato

#### topKeyValue (datos)
- devuelve el valor máximo de un objeto tipo campo valor.

#### toYear (año)
- pone el ultimo momento de un año especifico.

#### toYearMonth (año, mes)
- pone el ultimo momento de un mes especifico.

#### toYearMonth (año, mes)
- regresa la fecha fin de mes
- por ejemplo `calc.toYearMonth(2026, 6)` regresa `2026-06-30T23:59:59-06:00`

#### tpl (templateId, datos, [seccionId])
- ejecuta un templateId de la configuración `_app` de Handlebars.
- datos puede ser un arreglo de documentos, y se puede poner el nombre de la sección a extraer.

#### transformImage (url, opciones)
- url de la imágen a transformar.
- las opciones deben ser tipo `key=value` y puede ser múltiple agregando el separador `&`, ej: `key1=value1&key2=value2`, son las opciones de [transformImage](transformImage).

#### translate (valor)
- traduce algunos valores que estan definidos en el preset.

#### translate (value)
- traduce un texto usando el idioma del usuario

#### trim (valor)
- quita los espacios previos y posteriores del texto.

#### trimArray (lista)
- quita los espacios previos y posteriores de la lista 
- quita lineas vacías.

#### trimTextArea (valor)
- quita los espacios previos y posteriores del texto.
- quita lineas vacías.

#### trunc (valor)
- eliminar los decimales de un número, conservando únicamente la parte entera.

#### unDeleteFieldsFromArray (arreglo, campos)
- elimina todos los campos menos los campos especificados de un arreglo.

#### union (arreglo1, arreglo2, arregloN)
- une todos los arreglos

#### unique (arreglo)
- regresa un arreglo con valores únicos.

#### updateArray (arreglo, llave, valor, condicion)
- actualiza un arreglo y pone en un campo especifico un valor especifico
- es posible indicar una condición opcional.

#### updateArrayExpr (arreglo, llave, expr, condicion)
- actualiza un arreglo y pone en un campo especifico un valor especifico
- es posible indicar una condición opcional.

#### upperCase (valor)
- forza el resultado a mayúsculas.

#### urlFromBucket (req, nombreArchivo)
- devuelve la url completa que corresponde al archivo y usando el bucket que esta configurado en ese servidor.

#### urlKeyValueToItems (texto, llave, valor, opciones)
- hace lo inverso `itemsToUrlKeyValue` y genera un arreglo desde una url.

#### userName
- devuelve el nombre del usuario actual.
 
#### userTurn 
- devuelve el turno del usuario actual.

#### uuidOk (uuid)
- valida que sea un UUID válido

#### validarCurp (curp)
- devuelve `true` o `false` si el curp indicado cubre con las validaciones simples de tamaño y bloques de letras o números.

#### validarFechaEventoAtencion (fechaEvento, fechaAtencion, conHoras)

#### validateCfdiTotals (base, importes, descuentos, subTotal, descuento, impuestos, retenciones, total)
- valida si los totales del CFDI corresponden con todos los campos calculados.

#### valueMap (items, key, value)
- regresa un objeto con las llaves y valores mapeados

#### values (obj)
- obtiene la lista de valores

#### warning (mensaje)
- manda un mensaje de advertencia (amarillo) a la pantalla del usuario.
  
#### where (arreglo, attributos)
- devuelve una lista, con los atributos que coincidan.

#### whereExists (arreglo, llave, valor)
- devuelve una lista, con los valores que existan dentro del texto
- puede ser una arreglo de valores

#### whereExpr (arreglo, expr)
- devuelve una lista donde se cumplen las expresiones en cada uno de los elementos.

#### whereGreaterThan (arreglo, llave, valor)
- devuelve una lista de los elementos que tienen el valor superior.

#### whereHasValue (arreglo, llave)
- devuelve una lista, con los registros que tienen valor en ese campo

#### whereIsFalse (arreglo, llave)
- devuelve una lista, con los registros que tienen un valor falso en ese campo

#### whereLessThan (arreglo, llave, valor)
- devuelve una lista de los elementos que tienen el valor inferior.

#### whereNotHasValue (arreglo, llave)
- devuelve una lista, con los registros que no tienen valor en ese campo

#### whereNotValue (arreglo, llave, valor)
- devuelve la lista de todos los elementos que no corresponde el valor con la llave indicada.

#### whereRef (arreglo, referencia, valor)
- devuelve los elementos del arreglo que tienen una referencia con un valor específico.

#### whereRefIn (arreglo, ref, values)
- devuelve la lista con los valores múltiples que existan en la referencia.

#### whereRefIn (arreglo, referencia, valores)
-  similar a `whereRef` con la diferencia que puede aceptar múltiples valores.
-  los valores es un arreglo
  
#### year (fecha)
-  devuelve el año de la fecha específica.

#### years (desde, hasta)
- calcula los años entre las 2 fechas.

#### yearsToDate (fecha, ahora)
- calcula los años a hoy.
- se puede especificar el ahora para cambiar las fechas.

#### zeroFill (numero, dígitos)
- pone un numero relleno de ceros, por ejemplo `calc.zeroFill(123,6)` devuelve `000123`.

#### zeroFillCode (code, dígitos)
- pone un código relleno de ceros en las partes numéricas
- esta función es muy util para convertir cuentas contables a un texto que se pueda ordenar con seguridad
- por ejemplo: `calc.zeroFillCode('100-01-001',5)` devuelve: `'00100-00001-00001'`.
