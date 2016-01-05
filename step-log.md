# Objeto: **log** (step)
- despliega en la consola del servidor mensajes, para poder "debuggear" los pasos de afectación.

## Parámetros
##### id
- es posible establecer un indicador especifico, para que quede mas claro porque motivo aparece ese mensaje en la consola.

##### otros parámetros
- se pueden pasar otros parámetros abiertamente.

# Ejemplo:
````
{{#each as="sp"}}
  {{log id="vigentes" desde="sp.desde" hasta="sp.hasta"}}
{{/each}}
````