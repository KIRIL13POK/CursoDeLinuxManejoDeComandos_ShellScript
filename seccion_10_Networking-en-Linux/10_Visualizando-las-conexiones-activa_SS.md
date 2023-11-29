Esta clase se centra en el uso de la herramienta SS en sistemas Linux para visualizar conexiones activas. La utilidad SS es clave para investigar sockets, que son conceptos abstractos en redes informáticas utilizados para el intercambio de información entre procesos, ya sea en la misma máquina o entre diferentes máquinas.

![man ss](/img/1010-man%20ss.png)

La herramienta SS muestra todos los sockets y conexiones activas, tanto en la máquina local como entre la máquina local y otras remotas. Es útil para entender y diagnosticar el comportamiento del sistema, especialmente en situaciones donde se sospecha de conexiones remotas no autorizadas o para verificar conexiones activas en segundo plano.

Las conexiones se pueden clasificar en diferentes tipos, como TCP, UDP y Unix Domain Sockets. Los Unix Domain Sockets facilitan la comunicación interprocesos dentro de la misma máquina. Para visualizar conexiones específicas, se pueden usar diferentes opciones con SS, como -a para todas las conexiones, -t para conexiones TCP, -u para UDP, -x para Unix Domain Sockets, y -l para conexiones en estado de escucha.

### `ss -a`

![ss -a](/img/1010-ss-a.png)

### `ss -t` / `ss -u`

![ss -t ss -u](/img/1010-ss-t-ss-u.png)

Cada conexión mostrada incluye detalles como el estado (por ejemplo, establecido o escuchando), la dirección IP y el puerto involucrado. Esta información es crucial para comprender qué servicios están corriendo y cómo se están comunicando los procesos en el sistema. Además, SS ofrece opciones para filtrar y detallar aún más la información mostrada, adaptándose a las necesidades específicas del usuario.