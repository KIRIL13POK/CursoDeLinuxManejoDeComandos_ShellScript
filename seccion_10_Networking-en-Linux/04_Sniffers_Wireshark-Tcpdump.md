# Los sniffers

Los sniffers de red, también conocidos como analizadores de paquetes, son herramientas utilizadas en el campo de las redes informáticas para capturar y analizar el tráfico de red. Su función principal es copiar el tráfico que entra y sale de una máquina, permitiendo visualizarlo para su análisis. Esto es esencial para diferentes propósitos, como la identificación de problemas de red, la monitorización de la actividad de la red para detectar posibles amenazas de seguridad, o para entender mejor cómo funcionan ciertas aplicaciones y protocolos.

En el contexto de Linux, hay dos sniffers de red principales:

### TCPDump

 Es un sniffer de terminal muy conocido y usado en el ámbito de Linux. Viene preinstalado en muchas distribuciones de Linux. TCPDump permite capturar tráfico de red a través de la línea de comandos y redirigir ese tráfico a ficheros o procesarlo como se desee. Requiere privilegios de administrador (sudo) para capturar tráfico. Ofrece varias opciones para configurar la captura y el nivel de detalle en la visualización de los paquetes.


 ### `$ sudo tcpdump -i ens33`

![tcpdump](/img/1004-tcpdump.png)

Cuando ejecutas este comando, tcpdump comienza a capturar todos los paquetes que entran y salen a través de la interfaz ens33. Los detalles de cada paquete, como las direcciones IP de origen y destino, los puertos, el protocolo utilizado (por ejemplo, TCP, UDP), y otros detalles relevantes se muestran en la terminal.

Este tipo de captura es especialmente útil para el diagnóstico de problemas de red, la monitorización de la actividad de la red para propósitos de seguridad, o simplemente para entender mejor cómo fluye el tráfico en una red específica. Sin embargo, debido a la gran cantidad de información que puede generar, a menudo se utilizan opciones adicionales con tcpdump para filtrar los paquetes y reducir la salida a solo aquellos paquetes que son de interés para el usuario.

### Wireshark

A diferencia de TCPDump, Wireshark ofrece una interfaz gráfica de usuario y es muy conocido por su capacidad para proporcionar una visualización detallada y clara del tráfico de red. No suele venir instalado por defecto y necesita ser instalado manualmente `sudo apt install wireshark`. Wireshark permite seleccionar la interfaz de red para la captura y presenta el tráfico de red de manera detallada, mostrando las distintas capas del modelo OSI, como Ethernet, IP, TCP, y HTTP. Es una herramienta muy útil para el análisis profundo de los paquetes y para entender las interacciones a nivel de protocolo.


### `sudo wireshark`

![wireshark](/img/1004-sudo-wireshark.png)

***
**Ambas herramientas son esenciales para administradores de sistemas y profesionales de la seguridad informática, ya que permiten monitorear y analizar el tráfico de red para identificar problemas, auditar la seguridad y entender mejor el comportamiento de las redes.**
***



