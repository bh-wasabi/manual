# Objeto: **scheduler** (action)
- abre un visor del calendario

## Parámetros

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

#### color
- color de elemento
- es una expresión que se obtiene de cada recurso.

#### status
- lista de estatus separada por comas
- `busy, free, busy-unavailable, busy-tentative, entered-in-error`
