# SSH o Secure Shell

![ssh](https://www.hostinger.es/tutoriales/wp-content/uploads/sites/7/2017/09/ssh-tutorial-how-does-ssh-work.webp)

Es un protocolo de red utilizado para operaciones de red seguras, que permite a los usuarios controlar y modificar sus servidores remotos a través de Internet. La función principal de SSH es proporcionar una comunicación segura y cifrada entre dos dispositivos, utilizando técnicas de criptografía para garantizar que todas las comunicaciones entre el cliente y el servidor estén protegidas contra ataques o interceptaciones.

### Características clave de SSH:

1. **Autenticación segura**: SSH utiliza una variedad de métodos de autenticación, como contraseñas, claves públicas o certificados digitales, para asegurar que sólo los usuarios autorizados puedan acceder al servidor.

2. **Cifrado**: Todos los datos transmitidos durante una sesión SSH están cifrados, lo que significa que la información es incomprensible para cualquier persona que intente interceptarla.

3. **Integridad de los datos**: SSH garantiza la integridad de los datos transmitidos, asegurando que la información enviada y recibida durante la sesión no ha sido alterada o dañada.

4. **Túneles y port forwarding**: SSH permite el reenvío de puertos y la creación de túneles seguros, lo que puede ser utilizado para proteger otros protocolos de red que no son intrínsecamente seguros.

### Usos comunes de SSH:

1. **Acceso remoto seguro**: SSH es ampliamente utilizado para acceder de forma segura a servidores y otros dispositivos de red a través de Internet o redes locales.

2. **Transferencia de archivos**: Aunque SSH en sí mismo no es un protocolo de transferencia de archivos, proporciona un canal seguro a través del cual se pueden transferir archivos utilizando protocolos como SCP (Secure Copy Protocol) o SFTP (SSH File Transfer Protocol).

3. **Administración de sistemas y redes**: Los administradores de sistemas utilizan SSH para administrar servidores y redes de forma remota, realizar actualizaciones, configurar sistemas y realizar tareas de mantenimiento.

4. **Ejecución de comandos remotos**: SSH permite a los usuarios ejecutar comandos en una máquina remota, lo que es útil para automatizar tareas a través de scripts y otras herramientas de software.
***
**En resumen, SSH es una herramienta esencial en el ámbito de la informática y la administración de redes, proporcionando un método seguro y eficiente para gestionar dispositivos y servidores de forma remota, transferir datos de forma segura y realizar una amplia gama de tareas relacionadas con la seguridad y la administración de sistemas.**
***


Para establecer una conexión SSH, necesitas instalar SSH Server en la máquina a la que deseas conectarte (la máquina remota) y SSH Client en la máquina desde la que te estás conectando (la máquina local). Aquí te explico un poco más sobre cada uno:

### SSH Server:

* **¿Qué es?**: Es el software que escucha las conexiones entrantes vía SSH. Es responsable de aceptar las conexiones de los clientes, autenticar a los usuarios y ejecutar los comandos enviados desde el cliente SSH.

* **¿Dónde se instala?**: Debe instalarse en la máquina remota, es decir, en el servidor o computadora a la que deseas acceder de forma remota.

### SSH Client:

* **¿Qué es?**: Es el programa que utilizas para iniciar una sesión SSH con un servidor remoto. Es responsable de iniciar la conexión, autenticar al usuario en el servidor remoto y enviar comandos para ser ejecutados en ese servidor.

* **¿Dónde se instala?**: Se instala en la máquina local, es decir, en la computadora desde la que estás intentando acceder a la máquina remota.

***
**En resumen, necesitas instalar SSH Server en la máquina a la que quieres acceder (máquina remota) y SSH Client en la máquina desde la que te conectarás (máquina local). En muchos sistemas operativos basados en Linux, como Ubuntu, el cliente SSH suele venir instalado por defecto, por lo que principalmente tendrás que asegurarte de que el servidor SSH esté instalado y configurado en la máquina remota.**
***


Un ejemplo simplificado de tres tareas comunes que un administrador de sistemas podría realizar utilizando SSH, junto con las herramientas y características específicas de SSH que facilitan estas tareas: 

1. ### Acceso Remoto y Monitoreo de Servidores

    **Tarea**: Conectar a servidores remotos para monitorear su rendimiento y estado.

    **Herramientas SSH**:

    * **Autenticación Segura**: Utilizar claves SSH para un acceso seguro y sin contraseñas.

    * **Comandos de Monitoreo**: Ejecutar comandos como htop, vmstat, o tail -f /var/log/syslog para revisar el rendimiento y los registros del sistema.

2. #### Despliegue y Actualización de Software

    **Tarea**: Instalar o actualizar software en servidores remotos.

    **Herramientas SSH**:

    * **Ejecución de Comandos Remotos**: Usar SSH para ejecutar comandos de instalación o actualización como sudo apt update && sudo apt upgrade.

    * **Automatización**: Crear scripts que se ejecuten a través de SSH para automatizar despliegues y actualizaciones.

3. ### Transferencia Segura de Archivos

    **Tarea**: Mover archivos de configuración o datos entre el servidor local y los servidores remotos.

   **Herramientas SSH**:

    * **SCP o SFTP**: Utilizar estos protocolos basados en SSH para transferir archivos de manera segura.

    * **Montaje de Sistemas de Archivos Remotos**: Usar herramientas como sshfs para montar directorios remotos como si estuvieran localmente disponibles.

Estas tareas, realizadas con las herramientas que SSH proporciona, son esenciales en la administración cotidiana de sistemas y redes, facilitando el mantenimiento seguro y eficiente de infraestructuras de TI(Tecnologías de la Información).
