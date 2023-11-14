# Interfaz de red

Una interfaz de red es un componente de software y hardware que permite a un ordenador comunicarse con otras máquinas en una red. Actúa como un puente entre el sistema operativo del ordenador y dispositivos físicos como la tarjeta de red. Es esencial para enviar y recibir datos a través de la red. Cada interfaz de red tiene una dirección única, como una dirección MAC, que la identifica en la red. Las interfaces de red son configurables y gestionables mediante comandos específicos en sistemas operativos como Linux, permitiendo controlar cómo se conecta el ordenador a la red y cómo procesa el tráfico de red.

### `ip`

![man ip](/img/101-man-ip-png.png)

El comando `ip` opera con objetos que representan diferentes componentes de red.

![ip](/img/101-ip.png)

Por ejemplo, el objeto **link** se refiere a dispositivos de red e interfaces, mientras que otros objetos como **address** y **road** se relacionan con direcciones IP y rutas de red, respectivamente. Se muestra cómo obtener información detallada de las interfaces, incluyendo su estado operativo y dirección física (MAC).


***
### `Usage: ip [ OPTIONS ] OBJECT { COMMAND | help }

Es una sinopsis del comando `ip` en Linux, que proporciona una estructura general de cómo se utiliza este comando en la terminal. Aquí se desglosan los componentes de la línea:

1.  **ip**: Este es el comando principal. ip es una herramienta versátil para configurar y gestionar interfaces de red, rutas de red, y otros aspectos relacionados con la red en sistemas operativos basados en Linux.

2. **[ OPTIONS ]**: Indica que el comando ip puede incluir opciones opcionales. Las opciones son parámetros adicionales que modifican el comportamiento del comando. Están encerradas entre corchetes, lo que significa que son opcionales y no siempre son necesarias para ejecutar el comando.

3. **OBJECT**: Los objetos son componentes esenciales del comando ip. Representan diferentes entidades de red que se pueden gestionar con este comando. Algunos ejemplos de objetos incluyen:

    * **link**: Se refiere a las interfaces de red (como Ethernet, Wi-Fi). Permite al usuario ver y modificar propiedades de las interfaces de red físicas y virtuales.

    * **address**: Relacionado con las direcciones IP asignadas a las interfaces de red. Permite gestionar estas direcciones (añadir, eliminar, mostrar).

    * **route**: Este objeto se utiliza para manipular y mostrar la tabla de enrutamiento.

    * **neigh**: Utilizado para manipular y mostrar la tabla ARP (Protocolo de resolución de direcciones), que asocia direcciones IP con direcciones MAC.

4. **{ COMMAND | help }**: Este segmento indica que, después de especificar el objeto, el usuario debe ingresar un comando específico relacionado con ese objeto o utilizar la palabra help para obtener más información. Los comandos varían según el objeto y pueden incluir acciones como add, delete, show, etc.
***

### `ip link`

![ip link](/img/101-ip-link.png)

La salida del comando `ip link` varía dependiendo de la configuración de red y el hardware de cada sistema. Generalmente, muestra información sobre todas las interfaces de red disponibles en el sistema, incluyendo:

**Nombre de la Interfaz**: Cada interfaz de red tiene un nombre, como eth0 para la primera interfaz Ethernet o lo para la interfaz de loopback.

**Estado de la Interfaz**: Indica si la interfaz está activa (up) o inactiva (down).

**Dirección MAC**: Muestra la dirección de control de acceso a medios (MAC) de la interfaz, que es su identificador único a nivel de hardware.

**Información Adicional**: Puede incluir detalles como el tipo de enlace (Link/ether para Ethernet), MTU (Maximum Transmission Unit), y otras banderas y configuraciones específicas.



### `ip -s link`

![ip -s link](/img/101-ip-s-link.png)

Se utiliza para mostrar estadísticas detalladas de todas las interfaces de red del sistema.

El sistema devuelve una lista de todas las interfaces de red disponibles junto con estadísticas detalladas para cada una. 

Estas estadísticas incluyen:

* **Número de paquetes transmitidos y recibidos**: Indica cuántos paquetes de datos ha enviado y recibido la interfaz.

* **Número de bytes transmitidos y recibidos**: Muestra la cantidad total de datos enviados y recibidos por la interfaz, en bytes.

* **Información sobre errores y descartes**: Proporciona datos sobre cualquier error que haya ocurrido en la interfaz, así como el número de paquetes que han sido descartados.

Este comando es útil para diagnosticar problemas de red y para monitorear el rendimiento y el uso de las interfaces de red .


### `ip l ls up`

![interfaces activas](/img/101-ip-l-ls-up.png)

Es una forma abreviada de mostrar información sobre todas las interfaces de red que están actualmente "activas" o "levantadas" (up) en el sistema. 

El comando devolverá una lista de todas las interfaces de red que están en estado "up". Esta información es útil para verificar rápidamente qué interfaces están operativas y listas para la comunicación en la red. La salida incluirá detalles como el nombre de la interfaz, el tipo de enlace, la dirección MAC, la MTU (Unidad Máxima de Transmisión), y otras configuraciones y banderas específicas.
