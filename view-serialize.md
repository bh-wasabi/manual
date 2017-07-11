# Objeto: **serialize** (view)
- serializa o pivotea los resultados de una vista
- es muy útil para las gráficas.

## Parámetros
##### key
- campo clave

##### value
- valor clave

##### arguments
- lista (separadas por comas) de campos adicionales a usar como argumentos.

## Ejemplo:
````
{{serialize key="estatus" value="cantidad" arguments="tienda"}}
````
Antes: 
````
[
  {
    "_count": 1,
    "estatus": "pendiente",
    "tienda": "soriana",
    "cantidad": 9
  },
  {
    "_count": 1,
    "estatus": "efectuado",
    "tienda": "superama",
    "cantidad": 2
  },
  {
    "_count": 1,
    "estatus": "pagado",
    "tienda": "superama",
    "cantidad": 4
  },
  {
    "_count": 1,
    "estatus": "pendiente",
    "tienda": "superama",
    "cantidad": 12
  }
]
````
Después:
````
[
  {
    "_count": 1,
    "tienda": "soriana",
    "pendiente": 9
  },
  {
    "_count": 3,
    "tienda": "superama",
    "efectuado": 2,
    "pagado": 4,
    "pendiente": 12
  }
]
````
