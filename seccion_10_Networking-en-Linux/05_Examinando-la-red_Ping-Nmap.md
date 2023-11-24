
Examinando la red: Ping y Nmap .

**Ping** y **Nmap** son herramientas fundamentales para el análisis y la gestión de redes.

### Ping

![ping](/img/1005-pingpng.png)

* Qué es:
        
    Ping es una herramienta de diagnóstico en redes informáticas que verifica el estado de conectividad en redes IP (Internet Protocol). Su nombre proviene del sonido que hacen los sonares.

* Cómo funciona:

    El funcionamiento del comando "ping" puede entenderse con un ejemplo más detallado:

   Imagina que quieres verificar si tu computadora puede comunicarse con un sitio web, por ejemplo, www.google.com. Al usar el comando "ping", tu computadora envía un pequeño paquete de datos, conocido como un mensaje *ICMP ECHO_REQUEST*, al servidor donde se aloja www.google.com. Este mensaje es como un "llamado" digital que pregunta, "¿Estás ahí?"

   Cuando el servidor de Google recibe este mensaje, responde con un paquete similar, conocido como un mensaje *ECHO_REPLY*, que es básicamente una confirmación de que está activo y puede comunicarse.

   Este proceso se realiza varias veces para obtener una muestra representativa. Cada mensaje ICMP que regresa a tu computadora incluye información útil, como el tiempo que tardó en viajar (ida y vuelta) y si hubo alguna pérdida de paquetes. Por ejemplo, si envías cuatro solicitudes de eco y recibes cuatro respuestas, significa que la conexión es estable. Si no recibes respuestas, o hay una pérdida significativa de paquetes, indica problemas en la conexión o que el servidor destino no está accesible.

En resumen, "ping" es como hacer una llamada y esperar a escuchar un eco de vuelta. Si escuchas el eco, sabes que hay un camino claro y que el otro lado está respondiendo. Si no hay eco, indica un problema en la comunicación..

* Para qué sirve:

    1. Comprobar la disponibilidad de un host en una red IP.
    2. Medir el tiempo de ida y vuelta (RTT) de los paquetes enviados al host.
    3. Diagnosticar problemas de conectividad y calidad de la red.

### Nmap:

* Qué es: 

Nmap (Network Mapper) es una herramienta de seguridad y exploración de redes de código abierto.

* Cómo funciona:

  Supongamos que eres un administrador de red y necesitas auditar tu red corporativa para garantizar su seguridad y eficiencia. Utilizas Nmap para este propósito. Aquí está cómo lo haces:

    1. **Descubrimiento de Hosts**: Comienzas ejecutando un escaneo para identificar qué dispositivos están activos en tu red. Nmap envía diferentes tipos de paquetes, como ARP (para redes locales) o ICMP ECHO (ping), para ver qué dispositivos responden. Por ejemplo, encuentras que hay 50 dispositivos conectados a tu red.

    2. **Escaneo de Puertos**: Luego, Nmap examina estos dispositivos para ver qué puertos de red están abiertos. Un puerto abierto generalmente significa que hay un servicio de red escuchando, listo para recibir conexiones. Por ejemplo, descubres que varios dispositivos tienen el puerto 80 abierto, lo que sugiere que están ejecutando un servidor web.

    3. **Detección de Servicios**: Nmap puede ir más allá y determinar qué aplicaciones están ejecutándose en estos puertos abiertos. Por ejemplo, podría identificar que uno de los servidores web está ejecutando Apache 2.4.

    4. **Detección del Sistema Operativo**: Nmap puede utilizar varias técnicas, como el análisis de cómo los dispositivos responden a diferentes tipos de paquetes de red, para adivinar qué sistema operativo están ejecutando. Por ejemplo, podría determinar que la mayoría de tus servidores están ejecutando Windows Server 2016.

    5. **Detección de Firewall/Filtros de Paquetes**: Nmap puede inferir la presencia de un firewall o sistema de filtrado de paquetes observando cómo responden los dispositivos a ciertos tipos de paquetes o escaneos. Por ejemplo, si algunos paquetes no reciben respuesta o las respuestas son inusuales, podría indicar la presencia de un firewall.

Con toda esta información, como administrador de red, obtienes una visión detallada de tu red. Puedes identificar dispositivos no autorizados, verificar si los servicios que se ejecutan son los esperados, y asegurarte de que los sistemas operativos y aplicaciones estén actualizados y sean seguros. Además, la detección de firewalls te ayuda a entender cómo está protegida tu red.



* Para qué sirve:

1. Exploración de redes y auditoría de seguridad.
2. Identificación de dispositivos y servicios en una red.
3. Detección de posibles vulnerabilidades en los sistemas de la red.


***

**Ambas herramientas son esenciales para administradores de redes, ingenieros de seguridad, y profesionales de TI en general, permitiendo monitorear y diagnosticar la salud y seguridad de las redes.**

***