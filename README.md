O-Hare Air

Sistema automatizado de ventilación controlado por ESP32-C3, equipado con sensor de temperatura y humedad DHT11, pantalla OLED de estado y módulo de relé para control de potencia.

Especificaciones generales:

Dimensiones de la placa / diseño: Adaptado para montaje compacto.

Alimentación: Batería LiPo de 7.4V (2S).

Regulación: Voltaje estabilizado a 5V mediante regulador L7805 con condensadores de filtrado (100nF y 10µF).

Microcontrolador: ESP32-C3 Super Mini.

Componentes pasivos: Resistencias y condensadores en formato SMD 1206, diodo 1N4007 en encapsulado SMA.

Objetivo del proyecto:

El objetivo principal de este proyecto es diseñar e implementar un sistema de ventilación inteligente y automatizado que regule el flujo de aire en función de las condiciones ambientales medidas por sensores, aplicando conocimientos de diseño de circuitos impresos y programación de microcontroladores.

Componentes utilizados:

Microcontrolador: ESP32-C3 Super Mini.

Memoria: 400 KB SRAM, 4 MB Flash. Conectividad: Wi-Fi (2.4 GHz) y Bluetooth 5.0 LE.

Batería LiPo: 7.4V (2 celdas de 3.7V).

Regulador de voltaje: L7805.

Sensor de temperatura y humedad: DHT11.

Pantalla de visualización: Display OLED I2C.

Control de potencia: Módulo de relé.

Control general: Interruptor de palanca y conector de batería.

Protección: Diodo 1N4007 (encapsulado SMA).

Diseño del circuito:



Descripcion del funcionamiento:

El sistema monitorea constantemente la temperatura y la humedad del ambiente mediante el sensor DHT11. Los valores leídos se procesan en el ESP32-C3 y se visualizan en tiempo real a través de la pantalla OLED. Cuando la temperatura o la humedad superan los umbrales configurados, el microcontrolador activa el módulo de relé para encender el ventilador de forma automática. Todo el sistema es alimentado por una batería LiPo de 7.4V, la cual pasa por un interruptor general y se reduce a 5V limpios mediante el regulador lineal L7805 protegido por condensadores de desacoplamiento.

Esquematico:


Layout de PCB:



Pasos a seguir para armar el proyecto:

1. Preparación de la placa:

Descargar el archivo de diseño de PCB desde el repositorio.

Imprimir el diseño en una hoja fotográfica utilizando impresora láser con tóner.

Transferir el diseño a la placa de cobre mediante calor (planchado).

Revelar y grabar la placa utilizando percloruro férrico hasta eliminar el cobre sobrante.

Perforar los puntos necesarios y limpiar la placa adecuadamente.

2. Soldar los componentes:

Soldar los componentes en el siguiente orden recomendado para mayor comodidad:

Condensadores y resistencias SMD (formato 1206).

Diodo SMA y pines de conexión.

Regulador de voltaje L7805.

Conectores de batería, relé y pantalla.

3. Código y programación

El código establece las instrucciones que ejecutará el ESP32-C3 para leer el sensor DHT11, mostrar la información en la pantalla OLED y accionar el relé del ventilador según corresponda.

Compilación y carga:

Conectar la placa ESP32-C3 Super Mini a un ordenador mediante un cable USB-C.

Abrir el programa Arduino IDE.

Seleccionar la placa ESP32_C3_DEV_MODULE y el puerto USB correspondiente en las herramientas.

Instalar las librerías necesarias para el sensor DHT11 y la pantalla OLED desde el gestor de bibliotecas.

Verificar el código en busca de errores y proceder a subirlo al microcontrolador.
