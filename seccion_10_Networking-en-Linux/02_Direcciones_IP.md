# La dirección IP

La dirección IP (Protocolo de Internet) es un identificador único que se asigna a cada dispositivo conectado a una red que utiliza el protocolo IP, como Internet. Esta dirección permite que los dispositivos se identifiquen y comuniquen entre sí en una red. Existen dos versiones principales de direcciones IP: IPv4 y IPv6.

IPv4, la versión más común, consta de direcciones de 32 bits representadas habitualmente en formato decimal (por ejemplo, 192.168.1.1). Sin embargo, debido a la escasez de direcciones IPv4, se desarrolló IPv6, que utiliza direcciones de 128 bits, permitiendo una cantidad mucho mayor de direcciones únicas.

Las direcciones IP se diferencian de las direcciones MAC, que son identificadores físicos únicos incorporados en las interfaces de red por el fabricante. Mientras que las direcciones MAC son permanentes y únicas a nivel mundial, las direcciones IP pueden cambiar y son asignadas por el administrador de la red o automáticamente a través de protocolos como DHCP.

En el contexto de redes, las direcciones IP se utilizan para varias funciones, como la identificación de dispositivos, la realización de rutas de tráfico y la definición de ubicaciones geográficas y de red. Además, las direcciones IP pueden ser estáticas (asignadas manualmente y fijas) o dinámicas (asignadas automáticamente y cambiantes).

***
**En resumen, las direcciones IP son fundamentales para el funcionamiento de las redes basadas en IP, permitiendo la comunicación y el intercambio de datos entre dispositivos en una red o a través de Internet.**
***

### `ip address` / `ip a`

![IPV4/IPV6](/img/1001-IPV4-IPV6.png)

 Este comando se utiliza para mostrar y manipular las direcciones IP en las interfaces de red del sistema. Cuando se ejecuta ip a, el sistema realiza las siguientes acciones:

* **Listado de Interfaces de Red y sus Direcciones IP**: Muestra todas las interfaces de red disponibles en el sistema, como Ethernet, Wi-Fi, loopback, etc., junto con sus direcciones IP asociadas. Esto incluye tanto direcciones IPv4 como IPv6, si están configuradas.

* **Estado de la Interfaz**: Indica el estado actual de cada interfaz (por ejemplo, si está activa o inactiva).

* **Información Adicional**: Además de las direcciones IP, este comando también muestra otra información relevante como la dirección MAC (dirección de control de acceso a medios), MTU (unidad máxima de transmisión), y otros detalles técnicos de la interfaz.

El uso básico del comando es simplemente ip a, que proporciona un resumen de todas las interfaces de red y sus configuraciones de IP actuales. Es una herramienta útil para los administradores de sistemas y usuarios que necesitan obtener información rápida sobre la configuración de red del sistema.

Además, el comando ip tiene varias otras opciones y argumentos que permiten realizar operaciones más específicas, como agregar o eliminar direcciones IP, configurar rutas, y más. Por ejemplo, `ip address add` o `ip address del` se utilizan para agregar o eliminar direcciones IP en una interfaz específica.

![IPv4 IPv6](/img/1001-ipv4-ipv6-2png.png)

La salida de la terminal muestra la configuración de direcciones IPv4 e IPv6 para una interfaz de red:

**Dirección IPv4: inet 192.168.233.130/24**

* Es la dirección IP asignada a la interfaz.
* /24 indica una máscara de subred que permite hasta 256 direcciones en la subred.

**Dirección de Broadcast IPv4: brd 192.168.233.255**

* Usada para enviar mensajes a todos los dispositivos en la subred.

**Configuración IPv4 Adicional**:

* scope global: La dirección es válida en toda la red.
* dynamic: Asignada dinámicamente, probablemente por DHCP.
* noprefixroute: No se crean rutas automáticas basadas en esta dirección.

**Tiempo de Vida de la Dirección IPv4**:

*valid_lft 1420sec preferred_lft 1420sec: Tiempo durante el cual la dirección es válida.

**Dirección IPv6: inet6 fe80::3979:17f7:effd:d13c/64**

* Dirección IPv6 link-local asignada a la interfaz.
* /64 indica la longitud del prefijo de la red IPv6.

**Configuración IPv6 Adicional**:

* scope link: La dirección es válida solo en la red local.
* noprefixroute: Similar a IPv4, no se crean rutas automáticas.

Estas direcciones IP permiten que la interfaz se comunique dentro de la red local y, potencialmente, con el Internet más amplio.
