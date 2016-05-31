# Objeto: **step** (workflow)
- define un paso del flujo de trabajo

## Parámetros
##### id
- identificador del paso
- si no se define el flujo de trabajo ejecuta todos los pasos en el orden en que están definidos.

##### name
- nombre visibile del paso

##### stage
- nombre visible de la fase

##### next
- identificador del siguiente paso.
- el siguiente paso puede ser un sub objeto, para casos donde se necesiten expresiones para determinar cual es el siguiente paso.
- si no hay un siguiente paso, termina el flujo de trabajo.
- es posible mandar varios pasos en paralelo (lista separada por comas).
- si se indica `next="(wait)"` no se concluye el flujo de trabajo y se pone en espera a que otros pasos avancen el flujo (esto es útil cuando se tiene pasos en paralelo).

##### updateSections
- en algunos casos se requiere actualizar el documento original parcialmente, con este parámetros podemos indicar la lista de secciones (separadas por comas) que queremos actualizar.

## Sub objetos

##### [next](step-next.md)

##### [each](step-each.md)

##### [user](step-user.md)

##### [update](step-update.md)

##### [insert](step-insert.md)

##### [request](step-request.md)

##### [get](step-get.md)

##### [find](step-find.md)

##### [sql](step-sql.md)

##### [excel](step-excel.md)

##### [create](step-create.md)

##### [queue](step-queue.md)

##### [transaction](step-transaction.md)

##### [post](step-post.md)

##### [balanceCut](step-balance-cut.md)

##### [cancelTransactions](step-cancel-transactions.md)

##### [log](step-log.md)

##### [email](step-email.md)

##### [when](step-when.md)

