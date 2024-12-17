Medición Energética de un Sistema IoT con ESP32 y MQTT
Descripción del Proyecto
Este proyecto consiste en la medición y monitoreo energético en tiempo real de un sistema IoT utilizando una ESP32 como microcontrolador principal y el protocolo MQTT como medio de comunicación. La ESP32 se encarga de recolectar datos sobre el consumo energético del sistema y transmitirlos a un servidor MQTT para su visualización y análisis.

El objetivo principal es facilitar la medición eficiente del consumo energético, optimizando el desempeño y obteniendo información valiosa para aplicaciones IoT en entornos industriales o domésticos.

Características Principales
Plataforma IoT: Implementación con ESP32.
Protocolo de Comunicación: Utilización de MQTT para la transmisión de datos.
Medición Energética: Monitoreo de parámetros eléctricos como voltaje, corriente y potencia.
Transmisión en Tiempo Real: Envío periódico de los datos medidos a un broker MQTT.
Configuración Flexible: Permite la personalización del intervalo de muestreo y otros parámetros clave.
Requisitos del Sistema
Hardware
Microcontrolador ESP32.
Sensor para medición de energía:  INA219.
Fuente de alimentación para la ESP32: Batería 14400 mAh
Conexión Wi-Fi estable.
Software
Broker MQTT (por ejemplo: Mosquitto, HiveMQ, o cualquier otra plataforma compatible con MQTT).
Entorno de desarrollo para la ESP32: Arduino IDE o PlatformIO.
Librerías necesarias para el manejo del protocolo MQTT y sensores:
PubSubClient (para MQTT).
Librería específica del sensor de medición energética.
Instalación y Configuración

1. Preparación del Entorno
  Instala el Arduino IDE o PlatformIO.
  Configura la placa ESP32 en tu entorno de desarrollo.
  Descarga e instala las librerías necesarias:
    PubSubClient
    Adafruit MPU6050 Library
    Adafruit Unified Sensor
    ArduinoJson
2. Configuración del Broker MQTT
  Instala y configura un broker MQTT (local o en la nube).
  Asegúrate de tener acceso a la IP del broker y el puerto de comunicación (por defecto: 1883)
3. Carga del Código en la ESP32
  Abre el archivo principal del proyecto en tu entorno.
  Configura los parámetros clave:
  SSID y contraseña de tu red Wi-Fi.
  Dirección IP y puerto del broker MQTT.
  Intervalo de envío de datos (en milisegundos).
  Compila y carga el código en la ESP32.
Uso del Proyecto
Encender la ESP32: Una vez alimentada, la ESP32 se conectará a la red Wi-Fi y comenzará a enviar datos al broker MQTT.
Visualización de Datos:
Utiliza un cliente MQTT (por ejemplo, MQTT Explorer, Node-RED, o una aplicación personalizada) para suscribirte al tópico donde la ESP32 publica los datos.
Los datos enviados incluyen información de voltaje, corriente y potencia en tiempo real.
Estructura del Proyecto
bash

📂 Medicion_Energetica_IoT
│
├── 📄 README.md           # Descripción del proyecto
├── 📁 src                 # Código fuente principal
│   └── main.ino           # Código Arduino para la ESP32
│
├── 📁 docs                # Documentación adicional
└── 📁 libs                # Librerías utilizadas
Tópicos MQTT
A través del tópico "esp32/tesis" se envían los datos de salud y posición del usuario

json
{

}
Próximos Pasos y Mejoras

Implementar almacenamiento local de datos en caso de pérdida de conexión.
Visualización avanzada de datos mediante dashboards (ej. Grafana, Node-RED).
Adición de alertas cuando se superen ciertos umbrales de medición de pulso cardíaco y/o caídas del usuario.
Licencia
Este proyecto está bajo la licencia MIT. Siéntete libre de usar, modificar y distribuir el código.

Créditos
Desarrollado por Benjamin Yaupe
Contacto: byaupesanchez@gmail.com

