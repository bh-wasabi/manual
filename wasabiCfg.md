# Documentación de `wasabiCfd/cfg.json`

Este archivo concentra la configuración principal de la plataforma Wasabi. Está escrito en JSON. Su contenido organiza credenciales, conexiones, flags funcionales, integraciones externas y tareas programadas.

## Alcance general

- Define conexiones a MongoDB, Redis, PostgreSQL, SQL Server, Elasticsearch y servicios de almacenamiento.
- Centraliza banderas de negocio para activar o desactivar módulos del sistema.
- Incluye parámetros de autenticación, cifrado, correo, mensajería, facturación electrónica e integraciones externas.
- Contiene varias variantes por cliente, entorno o producto, como `app`, `facturama`, `verificamex`, etc.

## Estructura por secciones

### `mongodb`
Configuración principal de MongoDB.

- `user`: usuario administrativo.
- `host` y `host1`: nodos local y remoto o réplica.
- `database`: base activa para la sesión actual.
- `url`: cadenas de conexión local y remota.

### `auth0`
Parámetros para autenticación con Auth0.

- `authRequired`: indica si el acceso exige login.
- `auth0Logout`: habilita cierre de sesión sincronizado.
- `domain`, `baseURL`, `clientID`, `secret`: datos del tenant y la aplicación registrada.

### `authExternal`
Integración con un servicio externo de validación.

- `url` y `urlPayment`: endpoints para login y pagos.
- `secret`: llave compartida.
- `authType`: esquema de autenticación esperado.

### `app`
Configuración central del comportamiento global del sistema.

- `multiCompany`: permite operar con varias empresas en la misma instancia.
- `companies`: identifica las empresas activas.
- `disableNewIndexes`: evita la creación automática de índices en MongoDB.
- `disableMovSituation`: oculta la visualización del estado de situación de movimientos.
- `validateMovSituation`: valida flujos de estados en los procesos.
- `defaultMovSituation`: estado inicial de los registros.
- `viewLogs`: permite consultar bitácoras.
- `sqlDisabled`: indica que no se usarán bases SQL relacionales por defecto.
- `encryptEnabled`: activa el cifrado de datos en reposo.
- `protocol`: protocolo de comunicación.
- `id`: identificador único del proyecto.
- `dot`: dominio de nivel superior.
- `tenant`: identificador del cliente.
- `hideTenant`: oculta elementos visuales específicos para un grupo.
- `online`: estado de mantenimiento del sistema.
- `mode`: perfil de comportamiento del entorno.
- `privateKey`, `certificate`, `intermediate1`, `intermediate2`, `intermediate3`: archivos de certificados SSL.
- `favicon`: icono de la aplicación.
- `urlSupport`: enlace a soporte técnico.
- `tokenExpiresIn`: duración de la sesión JWT.
- `sessionSecret`: sal para hashes de sesión.
- `makeDisabled`: habilita o deshabilita la integración con Make/Integromat.
- `makeToken`: llave usada en la compilación del sistema.
- `makeTokenTutorial`: llave usada en la compilación del sistema de tutoriales.
- `suggestToken`: token para servicios de sugerencias AI.
- `useSystemCode`: usa IDs internos en lugar de nombres en la UI.
- `useTranscribeService`: habilita dictado por voz.
- `startSessionWithoutProyect`: permite iniciar sesión sin elegir proyecto previo.
- `mongoTenant`: habilita separación de datos por base de datos o colección según tenant.
- `autoStampDisabled`: desactiva el timbrado automático de facturas al guardar.
- `mongoBatchSize`: tamaño de bloques para inserciones masivas.
- `mongoTimeoutMS`: límite de tiempo de espera para consultas.
- `mongoAllowDiskUse`: controla si Mongo puede usar disco para ordenamientos pesados.
- `idleTimeout`: segundos para cierre automático por inactividad.
- `allowChangePassword`: permite cambiar la contraseña.
- `dontRepeatPasswordTimes`: política de no repetir claves anteriores.
- `maxAccessAttempts`: límite de intentos de login fallidos.
- `mongoDisableNewUrlParser`: desactiva el nuevo parser de URL de MongoDB.
- `mongoDisableUnifiedTopology`: desactiva el modo unified topology de MongoDB.
- `anonymous`: permite acceso sin credenciales a ciertas áreas.
- `reProcess`: flag para forzar re-cálculo de históricos.
- `allowLogon`: permite el acceso global a la plataforma.
- `allowInsertLot`: permite registro masivo de inventario o lotes.
- `allowChangeCompany`: permite cambiar de empresa.
- `allowChangeProyect`: permite cambiar de proyecto.
- `allowChangeReference`: permite cambiar de referencia.
- `sicDeleteData`: permite borrado en el módulo SIC.
- `sicDeleteToken`: token de seguridad para borrado.
- `locale`: idioma principal.
- `saveLogs`: guarda logs de operación.
- `multi`: permite múltiples sesiones del mismo usuario.
- `isNom`: activa el modo Nómina.
- `isErp`: activa el modo ERP.
- `isTGlobal`: activa el modo TGlobal.
- `avgCostType`: método de valuación de costos.
- `disableBrowsers`: deshabilita navegadores en el entorno.
- `disableCostValidation`: ignora si hay costo cero al procesar.
- `disableDuplicateNoteValidation`: desactiva la validación de notas duplicadas.
- `enableChartJs`: habilita integración con Chart.js.
- `enableAccounting`: activa la generación automática de pólizas.
- `enableServiceAlerts`: habilita alertas de servicio.
- `enableCurpValidation`: habilita validación de CURP.
- `enableSpecialtyCardValidation`: habilita validación de cédulas profesionales médicas.
- `emailEngine`: proveedor de correo.
- `insecureRequest`: permite llamadas a APIs sin certificado válido.
- `disableShootdownGraceful`: activa apagado rápido del servidor.
- `forceS3Path`: fuerza el uso de ruta S3.
- `disableMedicalCeil`: desactiva topes máximos en prescripciones.
- `disableDuplicateCondition`: desactiva validación de condiciones duplicadas.
- `disableClickFirstItem`: desactiva el auto click del primer elemento.
- `bulkPostgres`: desactiva el envío masivo a Postgres.
- `unsubscribeUrl`: URL de cancelación de suscripción.
- `iframe1`: enlace a un reporte incrustado.
- `sinbaPath`: ruta para integración con salud.
- `affectPostgre`: define si se escribe en Postgres al guardar en Mongo.
- `helpExpr`: habilita expresiones de ayuda dinámica.
- `aiReports`: habilita reportes generados por IA.
- `usePostgre2`: entidades que se replican en Postgres.
- `home`: dashboard de inicio.
- `homeSub`: rutas secundarias de inicio.
- `attachLimits.status`: estado del control de adjuntos.
- `attachLimits.mimeTypes`: tipos de archivo permitidos.
- `attachLimits.maxFileSize`: tamaño máximo en KB.

### `facturama`
Parámetros para facturación electrónica.

- `isDisabled`: activa o desactiva el servicio.
- `multiCompany`: soporte multiempresa.
- `ExpeditionPlace`, `Currency`, `version`, `token`, `url`: configuración principal de API.
- En `facturama3`, `compactItems` y `chunkSize` controlan el procesamiento de partidas.

### `iframe`
Enlaces a dashboards publicados en Google Sheets.

- `dashboardBalance`: balance general.
- `dashboardResultados`: estado de resultados.
- `dashboardIndicadores`: indicadores financieros.

### `verificamex_sandbox` y `verificamex`
Integración con Digitafirma para validación de identidad y firmas.

- `isDisabled`: habilita o deshabilita el entorno.
- `url`: endpoint base del servicio.
- `customerId`, `secret`, `companyId`, `webhook`: credenciales e ինտégración de eventos.
- La variante `sandbox` se usa para pruebas y la variante principal para operación real.

### `movControl`
Reglas control Interno y de validación de movimientos.

- `allowOverdraft`: cuentas que pueden quedar en negativo.
- `relativeDates`: permite expresiones relativas de fecha.
- `tolerance`: margen de redondeo o ajuste.

### `api`
Parámetros de seguridad para servicios internos y microservicios.

- `jwt.secret` y `jwt.expiresIn`: firma y expiración de tokens.
- `interop.userId`: usuario para interoperabilidad.
- `webhook.status` y `webhook.url`: receptor de eventos.
- `request.auth.secret`: secreto para solicitudes autenticadas.
- `eds`, `sic`, `rh`, `masari`, `messageIn`: esquemas de autenticación por módulo o integración.

### `mongoDatabaseRedis` y `redis`
Mapeo entre bases Mongo y bases Redis.

- `mongoDatabaseRedis`: relaciona bases como `his`, `xps` y `eds` con índices de Redis.
- `redis.host` y `redis.db`: servidor e índice base de Redis.

### `minio`, `s3`
Configuraciones de almacenamiento compatible con S3.

- `endPoint`, `port`, `useSSL`, `bucket`, `region`: conexión y destino.
- `accessKey`, `secretKey` o variantes `key` y `secret`: credenciales.
- `bucketTemplates`, `bucketInterfaces`, `bucketBackup`: destinos especializados.

### `vidal` Servicios farmacológicos Vidal.

- `isDisabled`: control de activación.
- `host`: endpoint del servicio.
- `tk`: token de acceso.

### `twilio`
Canales para SMS y llamadas automatizadas.

- `localUrl`: simulador o servicio local.
- `accountSid`, `authToken`: credenciales de Twilio.
- `from`: número emisor.
- `waitUrl`: flujo TwiML de espera.

### `clever` y `nemesysco`
Herramientas de análisis de voz y emociones.

- `analysisUrl`, `audioLanguage`, `analysisLanguage`, `token`: parámetros del servicio Clever.
- `url`, `url2`, `token`, `token2`, `apiKey`, `apiKeyPassword`: credenciales y endpoints de Nemesysco.
- `alianzasEspecificas`: lista de organizaciones con tratamiento particular.

### `jobs`
Lista de tareas programadas del sistema.

Cada elemento suele incluir:

- `status`: activo o inactivo.
- `second`, `hour`, `minute`: programación.
- `type`: tipo de proceso programado.
- `charge`, `notify`, `close`, `edi`, `remove`, `autoExpire`, `paps`, etc.: configuración específica por tarea.

Tareas incluidas en el archivo:

- `autoExpires`: cancelación automática de notas vencidas.
- `sumQueue`, `serviceLevel`, `nonCompliance`, `pullQueue`: colas y procesos de sincronización.
- `paps`: generación de solicitudes para servicios hospitalarios.
- `notify`: avisos a personas con plantilla personalizada.
- `remove`: limpieza de información con patrón `core.*`.
- `removeFreeSlots`: limpieza de citas no tomadas.
- `close`: cierre diario de servicios.
- `charge`: generación de cargos por hospitalización o urgencias.
- `edi`: procesamientos de intercambio de resultados.

### `edi` y `fhir`
Rutas de interoperabilidad.

- `edi.monitor.get` y `edi.monitor.processed`: colas o carpetas para monitor.
- `fhir.paris.put`, `get`, `processed`: intercambio FHIR para París.

### `quickSight`
Integración con AWS QuickSight.

- `region`, `key`, `secret`: conexión a AWS.
- `AwsAccountId`, `IdentityType`: identificación de la cuenta.
- `ResetDisabled`, `SessionLifetimeInMinutes`, `UndoRedoDisabled`: políticas de uso.

### `facturama_ykt`, `facturamaCliente`, `facturama_33`
Variantes adicionales de Facturama para clientes específicos.

- Comparten estructura general de CFDI.
- Cambian `ExpeditionPlace`, `token`, `version` o banderas de activación según el cliente.

### `mssql`, `pg3`, `pg4`, `sql`, `sql2`
Conexiones a bases relacionales.

- `mssql.connectionString`: cadena de conexión SQL Server.
- `pg3` y `pg4`: parámetros PostgreSQL.
- `sql` y `sql2`: conexiones MySQL o equivalentes para ETL, reporteo o integraciones.

### `elasticLog`, `elasticOperation`, `elasticSearch`
Configuración de Elasticsearch.

- `elasticLog.host`: host para logs.
- `elasticOperation.types` y `host`: tipos y servidor de operaciones.
- `elasticSearch.host`: servicio de búsqueda.

### `sqs`
Colas de AWS SQS usadas para sincronización entre sistemas.

- ejemplos: `sness-to-basa`, `basa-to-sness`, `meli-sync`: URLs de cola.

### `ses`
Servicio de correo AWS SES.

- `accessKeyId`, `secretAccessKey`, `region`: acceso a AWS.
- `Source`, `ReplyToAddresses`: remitente y respuesta.

### `sum`
Tokens y usuarios para el sistema SUM.

- `secretQuerys`, `secretSync`: llaves para pruebas.
- `secretQuerysProd`, `secretSyncProd`: llaves para producción.
- `secretSyncFiduciarioPruebas`, `secretSyncFiduciarioProd`: llaves de fiduciario.
- `userId`: usuario asociado.

### `email`, `emailMasari`, `mailgun`
Configuración de correo electrónico.

- `email`: arreglo de perfiles SMTP.
  - `profile`: nombre del perfil.
  - `from`: remitente.
  - `transport.host`, `transport.port`, `transport.auth.user`, `transport.auth.pass`: conexión SMTP.
- `emailMasari`: servicio alterno para envío de correos.
- `mailgun.apiKey` y `mailgun.publicKey`: credenciales de Mailgun.

### `postman`
Definiciones de endpoints externos usados por integraciones.

- Incluye módulos como `basaLaborales`, `basaDiversos`, `basaEmpleado`, `basaPromocion`, `basaBaja`, `basaRiesgos` y otros.
- También incluye servicios especializados como `chartjs`, `bulkPostgres`, `pagoProveedorSum`, `pldUnitario`, `pldMultiple`, `pacienteInsabi` y `atencionInsabi`.
- Los atributos comunes son `url`, `json`, `token`, `method`, `auth`, `retryIn`, `agentOptions`, `data` y `stringify`.

### `dropbox`, `onesignal`, `cloudconvert`, `cloudinary`, `jotForm`
Servicios externos adicionales.

- `dropbox`: integración con Dropbox.
- `onesignal`: notificaciones push.
- `cloudconvert`: conversión de archivos.
- `cloudinary`: hosting y procesamiento de imágenes.
- `jotForm`: formularios externos.

### `keys`
Rutas a llaves criptográficas.

- `hash`, `public`, `private`: archivos usados para firma o cifrado.

### `sns`
Tópicos de AWS SNS.

- `satDownload`, `revalidarCfdi`, `generarArchivos`, `reclasificar`: eventos para automatizaciones.

### `accessTurns`
Catálogo de turnos de acceso.

- `turns`: mapeo entre código y etiqueta de turno.

### `accessMethods`
Catálogo de métodos de autenticación y políticas de contraseña.

Cada objeto puede definir:

- `id`, `name`: identificador y nombre visible.
- `newUsers`, `newUsersData`: comportamiento para altas nuevas.
- `mfa`, `multiCompany2`, `userLowerCase`, `passwordReset`: reglas de acceso.
- `minLength2`, `requiresNumbers`, `requiresUpperCase`, `requiresLowerCase`, `requiresSpecialCharacters2`, `limitConsecutiveCharacters2`: políticas de contraseña.
- `passwordPattern3`, `passwordPatternError`, `passwordExpiresDays2`, `passwordReservedWords2`: validación y expiración.

### `paylink`, `paylink2`, `paylink3`, `openpay`, `paypal`
Pasarelas de pago.

- `paylink`: llaves y modo de operación.
- `openpay`: configuración de la pasarela con bandera de producción, moneda y webhook.
- `paypal`: configuración del cliente, país, locale, moneda e intent.

### `numeral`
Configuración de formato numérico.

- `locale.mx.delimiters`: separadores de miles y decimales.
- `locale.mx.abbreviations`: abreviaturas numéricas.
- `locale.mx.currency.symbol`: símbolo monetario.

## Notas de uso

- El archivo mezcla configuración de aplicación, credenciales y parámetros operativos; conviene tratarlo como información sensible.
- Las secciones `app` y las variantes por cliente suelen controlar el comportamiento visible del sistema.
- Las secciones de integraciones externas deben mantenerse sincronizadas con sus servicios correspondientes.
- Las tareas en `jobs` dependen del estado `active` o `inactive`, además de horarios o segundos programados.

## Recomendación

Si este archivo cambia con frecuencia, conviene documentar también qué llaves son obligatorias, cuáles son por entorno y cuáles no deben compartirse fuera del equipo.
