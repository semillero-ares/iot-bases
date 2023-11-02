# Clase 7 

## TI 
### Protocolos
Los protocolos de comunicación son la forma como se conectan las cosas, la nube y el usuario. Estos protocolos son un conjunto de reglas que permiten la comunicación entre diferentes tipos de sistemas, este conjunto de reglas esran dados por una serie de instrucciones que indican a los elementos básicos.

Reglas:

- ¿Quién es el remitente del mensaje?
- ¿Quién es él o los destinatarios del mensaje?
- ¿Qué tipo de mensaje se va a enviar a través de la red?
- ¿Por qué medio se va a enviar este tipo de mensaje?

Los protocolos mas usados en IoT son:

- Protocolo Serial: se usa cuando se quiere realizar una depuración de las cosas, sensores y actuadores. Se hace para realizar una variación interna del dispositivo y verificar su correcto funcionamiento (Suele ser por cable, pero también tiene opción Bluetooth).

- Protocolo MQTT: Funciona de forma M2M (machine to machine), busca interconectar cosas, dispositivos, etc., mediante un broker que es un servidor al cual los dispositivos se suscriben o publican datos o recursos que normalmente son alojados en la nube.

- Protocolo HTTP: Funciona de forma cliente-servidor, el cliente realiza una petición a un servicio alojado en el servidor, este busca lo solicitado y responde al cliente. Ejemplo: direcciones web.

#### Serial
##### Serial Arduino

1. El Entorno de Desarrollo Integrado (IDE) permite comunicarse con nuestro equipo
a través del puerto serie. Lo anterior se conoce como comunicación serial.


2. Si bien es cierto que el uso de las nuevas formas de comunicación, como es el caso
de USB, ha desplazado la tradicional forma de comunicación (serial), la placa
Arduino aún cuenta con un convertidor serial a USB, que permite comunicarse con
nuestro ordenador como un dispositivo conectado a un puerto “COM” a pesar de
que la conexión este físicamente mediante USB.


3. De esta manera Arduino IDE permite enviar y visualizar datos que se gestionan a
través del puerto serie. Dicha herramienta se conoce bajo el nombre de monitor
serial, la cual, se encuentra en el menú de herramientas, en la opción “monitor
serial”; lo anterior constituye la forma más simple que existe para establecer
comunicación con la placa Arduino.


4. Es así como se presenta algunas partes importantes de la interfaz de IDE Arduino;
en el menú herramientas (1) se puede identificar el puerto al cual se conecta la
palca Arduino (2) y en la parte superior derecha se puede encontrar y abrir el
monitor serial para la visualización de la información adquirida.


5. Es importante aclarar que existe una la configuración previa para trabajar con la
comunicación serial mediante algunas instrucciones propias de la placa Arduino. Es
el caso de la velocidad de transmisión de datos (baudios), lectura y estrategias de
programación para generar acciones.

##### Serial Node-Red

1. El funcionamiento del serial de comunicación de Node Red se configura a partir de
la descarga del nodo “serial” el cual se puede realizar de la siguiente manera:
Ingresar al menú de Node Red (al lado del botón Deploy) y en la opción Manage
Palette se digita la búsqueda del nodo. En este caso será el nodo Serial.


2. Es importante aclarar que durante la instalación pueden generarse diferentes
mensajes sobre la descarga e instalación del paquete de nodos. Estos pueden
asemejarse a fallas, ya que informan que no se han podido compilar los errores, pero
a menudo son advertencias y el nodo continuará instalándose. Ocasionalmente,
algunas plataformas requerirán que instale el conjunto completo de herramientas
para compilar el paquete subyacente.

3. Inicialmente, existen tres nodos principales de nodos para la comunicación serial:
    - El nodo Serial In permite detectar automáticamente los puertos serie conectados
    al dispositivo; sin embargo, es necesario que lo especifique manualmente el puerto
    COM, la velocidad de transmisión etc.
    - El nodo Serial out proporciona una conexión a un puerto serie saliente. Como
    respuesta envía el msg.payload, el cual se agrega a cada mensaje enviado al puerto
    serie.
    - El nodo Serial request proporciona una conexión a un puerto serie de solicitud /
    respuesta. La idea es que el mensaje se reenviará al puerto serie siguiendo una
    cola estricta FIFO (primero en entrar, primero en salir), esperando una sola
    respuesta antes de transmitir la siguiente solicitud.

## TD

Para el trabajo dependiente se realizaran varias practicas con monitor Serial, tanto en arduino como en Node-Red

