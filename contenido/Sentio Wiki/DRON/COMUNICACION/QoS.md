Políticas configurables que garantizan características de entrega de mensajes en sistemas [[Publish-Suscribe|pub/sub]]. Entre estos aspectos se encuentran los siguientes:
- **Fiabilidad**: define cómo de crítico es la recepción del mensaje, haciendo un balance entre velocidad y seguridad.
	- **Reliable**: el broker reintenta hasta confirmar recepción
	- **Best_effort**: envía una vez sin confirmación
- **History**: define cuántos mensajes recientes mantiene el broker si el suscriptor se desconecta.
- **Liveliness**: Permite detectar nodos muertos si dejan de publicar en un intervalo establecido.
- **Durability**: decide si los mensajes se transmiten si los suscriptores llegan tarde.
De esta forma, se puede realizar un trade-off entre rendimiento y robustez.