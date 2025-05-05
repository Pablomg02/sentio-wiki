Protocolo de comunicación serie asíncrona, ampliamente utilizado en drones y sistemas embebidos para la transmisión punto a punto de datos digitales. Funciona mediante dos líneas principales: **TX (transmisión)** y **RX (recepción)**, sin necesidad de un reloj compartido entre los dispositivos.

Se basa en una transmisión secuencial de bits a una **velocidad de baudios acordada** (por ejemplo, 57600 o 115200 bps) y es especialmente popular por su simplicidad y bajo coste.

En el contexto de drones, **UART es una de las principales interfaces físicas para enviar y recibir datos MAVLink**, conectando el autopiloto con módulos externos como:
- Receptores GPS
- Módulos de telemetría por radio (ej. SiK)
- Sensores adicionales (barómetros, magnetómetros)
- Computadores de a bordo (companion computers)+
