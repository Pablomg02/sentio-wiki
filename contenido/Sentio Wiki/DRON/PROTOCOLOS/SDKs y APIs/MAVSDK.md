SDK de alto nivel construido sobre [[MAVLink]]. Está diseñado para poder controlar drones fácilmente sin preocupaciones por el bajo nivel.
Es mantenido principalmente por [[PX4]], aunque se está avanzando en la compatibilidad con [[ArduPilot]].
## Estructura interna
MAVSDK tiene una arquitectura cliente-servidor, especialmente cuando se usa en lenguajes distintos de C++. El componente central es **`mavsdk-server`**, una aplicación escrita en C++ que implementa toda la lógica de bajo nivel y se comunica con el dron usando [[MAVLink]].

Cuando se usa desde lenguajes como Python, Java o Swift, la aplicación cliente se comunica con `mavsdk-server` a través de **[[Google Remote Procedure Call (gRPC)]]** . Este permite invocar funciones remotas (como `arm()`, `takeoff()` o `get_gps_position()`) como si fueran locales, enviando los datos a través de una red o proceso intermedio de forma eficiente y tipada.