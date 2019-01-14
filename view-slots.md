# Objeto: **slots**
- lista de `slots` disponibles


## Parámetros
#### duration (#)
- duración de la cita

#### resources
- lista de recursos requeridos

#### from 
- fecha inicial de la búsqueda (opcional)

#### key
- llave única del sub documento actual
- básicamente se usa para tener un llave única en redis

#### ttl (#)
- segundos de cache
- por omisión es `60`.