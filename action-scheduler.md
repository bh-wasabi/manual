# Objeto: **scheduler** (action)
- abre un visor del calendario

## Parámetros

#### actorId
- es posible definir el campo se encuentra el `id` del actor de la agenda.
- por omisión toma el `_id` del documento.

#### type
- `plan` muestra el calendario planeado
- `busy´ muestra el calendario reservado

#### plan
- lista de planeación anual.

#### startDayHour
- hora inicial del calendario
- por omisión 8am

#### endDayHour
- hora final del calendario
- por omisión 8pm

#### cellDuration
- duración del espacio
- por omisión 30 minutos

#### resources
- lista de recursos (agendas)
- es una expresión que se obtiene de cada plan.

#### resourceField
- campo que contiene el recurso

#### views
- posibles vistas del calendario
- `month`, `week`, `day`.

#### currentView
- vista por omisión

#### color
- color del recurso (agenda)
- es una expresión que se obtiene de cada recurso.


