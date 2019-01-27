# Objeto: **slots**
- lista de `slots` disponibles


## Parámetros
#### duration (#)
- duración de la cita

#### area
- area a solicitar

#### subArea
- sub area a solicitar (opcional)

#### resourceTypes
- tipos de recursos requieridos

#### from 
- fecha inicial de la búsqueda (opcional)

#### days (#)
- horizonte en días de la búsqueda (opcional)

#### cacheKey
- llave única del sub documento actual
- básicamente se usa para tener un llave única en redis

#### ttl (#)
- segundos de cache
- por omisión es `60`.

#### resourceSource
- tipo de documento que tiene los recursos
- este tipo de documento tiene que tener ciertos campos específicos como "planAgenda"