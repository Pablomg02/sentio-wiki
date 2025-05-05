# Protocolos

Los protocolos definen las reglas y formatos para el intercambio de información entre componentes de un sistema (firmware, GCS, sensores, companion computers).

## Gestión básica

- Selección según latencia, fiabilidad, ancho de banda y alcance  
- Configuración de parámetros físicos (baudios, velocidad CAN, canales RF, puertos UDP/TCP) y lógicos (versión de [[MAVLink]], plugins)  
- Monitorización de errores (CRC, HEARTBEAT, logs) y actualización de versiones  

## Clasificación

### Protocolos de alto nivel  
- **[[MAVLink]]**: mensajes binarios ligeros para drones  
- **[[MAVSDK]]**: SDK sobre [[MAVLink]] con funciones (`arm()`, `takeoff()`, `mission()`)  
- **[[DJI Mobile SDK]]**: control propietario de drones DJI  

### Protocolos de transporte / medios físicos  
- **Bus cableado**  
  - **[[UART]]** (punto a punto, baudios)  
  - **[[CAN]]** (bus síncrono, robusto)  
  - **[[MAVCAN]]** ([[MAVLink]] sobre [[CAN]])  
- **Red IP**  
  - **[[UDP]]** (sin conexión, baja latencia)  
  - **[[TCP]]** (conexión fiable, orden de paquetes)  
- **Enlace inalámbrico**  
  - **[[LoRa]]** (largo alcance, bajo ancho de banda)  

Cada protocolo de alto nivel puede transmitirse sobre uno o varios medios físicos según necesidad.  
```