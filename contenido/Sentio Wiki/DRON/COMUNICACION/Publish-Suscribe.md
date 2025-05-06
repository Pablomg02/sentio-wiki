---
aliases:
  - pub/sub
---
Patrón de comunicación donde un *publisher* (o nodo) envía mensajes a *topics*, donde otros nodos pueden suscribirse (*subscribers*) para recibir los mensajes.

Caracterizado por lo siguiente:
- Asíncrono y uno-a-muchos: varios suscriptores pueden procesar el mismo mensaje.
- Broker: se encarga de gestionar la distribución (por ejemplo: [[MQTT]] o [[DDS]]).
- Desacoplado: los emisores publican pensajes a un tópico sin conocer quién lo recibirá.

En caso de requerir una confirmación explícita de recepción, o bien querer comunicarse directamente con otros nodos, la opción correcta es [[Request-Response]].