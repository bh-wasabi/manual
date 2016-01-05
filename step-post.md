# Objeto: **post** (step)
- define como va a ser la afectación del indicador.

## Parámetros
##### indicator
- identificador del indicador a afectar, es recomendable que el nombre sea en minúsculas separando las palabras con guión medio `este-es-un-ejemplo`.

##### side
- todos los indicadores pueden tener lados de afectación, esto es muy util para conceptos como el presupuesto.

##### notAccumulate
- aquí se define en que campos no queremos llevar al saldo (lista de campos separados por comas).

##### section
- sección del documento donde nos vamos a posicionar para realizar esta afectación.

##### newPending (true, false)
- con esta opción podemos generar un nuevo pendiente.

## Sub objetos

##### [set](set.md)
- se asignan los valores del indicador a afectar.
- únicamente los [campos de afectación](balance.md).

##### [breakdown](step-post-breakdown.md)
- con esta función podemos hacer un prorrateo sobre un arreglo del documento.
