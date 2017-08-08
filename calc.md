# calc
- funciones predefinidas

#### fn (id, parámetros...)
- ejecuta una función configurable.
- debe existir el identificador en la configuración (`_cfg`).
- Nota: esta función también se puede ejecutar directamente sin el prefijo `calc.`

#### log (parámetros...)
- despliega en la consola los parámetros indicados.

#### in (valor, arreglo)
- busca si existe un valor en un arreglo.

#### text (valor)
- forza el resultado como texto.

#### concat (valor1, valor2, valorN)
- concatena varios valores, por omisión agrega un espacio entre los valores.
- es posible agregar comas para separar estos valores, por ejemplo: `calc.concat(@apellidoPaterno,',', @nombre)`. genera "Perez, Juan".

#### number (valor)
- forza el resultado como numérico.

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

#### parse (texto)
- convierte un texto JSON a objeto.

#### presetName (preset, id)
- devuelve el nombre de un `preset` especifico con un `id` especifico.

#### stringify (objeto)
- convierte un objeto a una cadena de texto JSON.

#### sha1 (texto)
- genera un hash. 

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

#### findDuplicates (arreglo, agrupadores)
- `arreglo`
- `agrupadores` lista de campos separados por comas

#### preset (id)
- devuelve el preset completo.

#### fromNow (fecha)
- calcula el tiempo desde cierta fecha en español.

#### fromNowShort (fecha)
- calcula el tiempo desde cierta fecha en español.
- en la forma mas corta.

#### fromNowShort2 (fecha)
- calcula el tiempo desde cierta fecha en español.
- en la forma mas corta diferente.

#### findWhere (arreglo, attributos)
- devuelve el primer elemento de la lista, con los atributos que coincidan.

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

#### updateArray (arreglo, llave, valor)
- actualiza un arreglo y pone en un campo especifico un valor especifico

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