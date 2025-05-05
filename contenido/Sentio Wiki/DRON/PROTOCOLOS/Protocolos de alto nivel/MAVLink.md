[[Protocolo]] de comunicación más utilizado en drones. Está basado en mensajes binarios muy ligeros, ideal para enlaces débiles.
Se utiliza para
	- Enviar comandos
	- Recibir telemetría
	- Programar misiones autónomas
	- Detectar fallos o errores
El protocolo permite control de muy bajo nivel, con comunicación personalizada. Sin embargo, si se desea algo simple, se puede utilizar [[MAVSDK]],
## Sistemas Autopiloto compatibles
Es compatible con muchos autopilotos, entre ellos los principales:
- [[PX4]]
- [[ArduPilot]]
## Estaciones de Tierra compatibles
Las siguientes estaciones utilizan MAVLink para comunicarse con los drones. Entre ellas:
- QGroundControl (oficial de PX4)
- Mission Planner (oficial de ArduPilot)
- MAVProxy (interfaz de línea de comandos)
- APM Planner 2
- DroneKit GCS (para desarrolladores)
## Lenguajes
El núcleo está desarrollado en C/C++, pero tiene soporte para Python, Java, JavaScript / Node.js, Rust, Go y ROS / ROS 2.
## Protocolos de transporte de red
MAVLink puede transmitirse a través de múltiples interfaces físicas y protocolos de red, según el tipo de conexión y el entorno operativo:
- [[Serial]]:
    - [[UART]]: interfaz punto a punto, muy común en drones pequeños y medios.
    - [[MAVCAN]]: adaptación de MAVLink al bus [[CAN]], ideal para conexiones internas robustas.    
- [[UDP]] y [[TCP]]: protocolos de red sobre IP, usados en comunicaciones inalámbricas (WiFi, 4G) o con simuladores.
- [[LoRa]]: protocolo inalámbrico de largo alcance y baja velocidad, útil para telemetría o comandos simples en drones operando en zonas remotas.
## Simuladores compatibles
Se puede utilizar MAVLink en diferentes simuladores mediante diferentes técnicas. Entre ellos:
- [[Gazebo]]
- [[AirSim]]
- [[JSBSim]]
## Otros dispositivos y ecosistemas
En drones DJI no se utiliza MAVLink de forma nativa ([[DJI Mobile SDK]]), pero existen bridges o wrappers para convertir datos.
También