#### document
- tipo de documento

#### subType
- sub tipo documento

#### requestType
- tipo de solicitud

#### requestSubType
- sub tipo de solicitud

#### comments
- comentarios

#### service
- servicio

#### attribute1
- es posible agregar un atributo genérico a la póliza a nivel detalle

#### attribute2
- es posible agregar un segundo atributo genérico a la póliza a nivel detalle

#### attribute3
- es posible agregar un tercer atributo genérico a la póliza a nivel detalle

#### path
- ruta base del documento a fectar

#### subPath
- sub ruta base del documento a afectar

#### condition1
- es posible determinar condiciones previas a la ejecución dependiendo del scope actual

#### condition2
- es posible determinar condiciones previas a la ejecución dependiendo del scope actual

#### condition3
- es posible determinar condiciones previas a la ejecución dependiendo del scope actual

#### lastChange
- columna informativa para registrar el último cambio registrado manualmente

#### ignore (booleano)
- es posible comentar los renglones del metadata usando esta columna, tambien se recomienda poner el color de las letras en gris para que sea más visual lo comentado.

#### include
- lista de proyectos (separados por comas) que se desean incluir.

#### exclude
- lista de proyectos (separados por comas) que se desean excluir.

#### aux
- nombre del auxiliar a afectar normalmente se usa `contabilidad`

#### entity
- id de la empresa opcional

#### entityName
- nombre de la empresa opcional

#### serviceId
- id del servicio

#### serviceName
- nombre del servicio

#### market
- mercado, se usa como una dimensión opcional

#### valueType
- tipo valor, se usa como una dimensión opcional

#### branch
- id de la sucursal

#### branchName
- nombre de la sucursal

#### agent
- id del agente

#### agentName
- nombre del agente

#### costCenter
- id del centro de costos

#### costCenterName
- nombre del centro de costos

#### date
- fecha de la póliza a nivel detalle

#### type
- tipo de póliza, normalmente se usa `diario`, `ingresos` y `egresos`.
- el sistema genera un folio automático usando ese tipo de póliza queda guardado en `_created.bookName`

#### typeName
- nombre del tipo de póliza, normalmente se usa `Diario`, `Ingresos` y `Egresos`.

#### currency
- id de la moneda o divisa de la operación contable.

#### currencyRate
- tipo de cambio opcional.

#### coverage
- cobertura de la operación.

#### factorIva
- factor de IVA

#### factorIeps
- factor de IEPS

#### explotion
-

#### explotionQuantity
-

#### explotionUnit
-

#### explotionMethod
-

#### concept
- concepto de la póliza

#### reference
- referencia de la póliza

#### rfc
- RFC de la persona con la que se hizo la operación.

#### uuid
- UUID del CFDI que se emitió en esa operación.

#### paymentMethod
- id de la forma de pago

#### instrument
- instrumento utilizado, puede ser el código de un producto financiero.

#### item
-

#### itemName
-

#### operationType
-

#### operationTypeName
-

#### term
- terminos y condiciones

#### expiration
- fecha de vencimiento

#### ledger
-

#### ledgerName
-

#### account
- cuenta contable de la póliza
- se puede usar un mapeo de cuentas de la configuracion general para faciliar la implementación usando la función `calc.getAccount(tipo, subTipo)` para leer la cuenta final.

#### detailType
- tipo de detalle, normalmente se usa la `persona` pero puede ser cualquier otro tipo detalle que se quiera agregar a la póliza.

#### detail
- id del detalle

#### detailName
- nombre del detalle

#### subAccount
-

#### subAccountName
-

#### bankAccount
-

#### bankAccountName
-

#### bankAccountNumber
-

#### amount
-

#### amountMN
-

#### debit
- expresión que genera el debe de la póliza

#### credit
- expresión que genera el haber de la póliza

#### validateOverdraft
-
