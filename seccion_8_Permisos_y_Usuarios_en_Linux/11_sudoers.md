**1. Ubicación del archivo sudoers**

 El archivo sudoers se encuentra en /etc/sudoers. Este archivo contiene reglas de permisos que determinan quién puede ejecutar comandos con privilegios elevados utilizando el comando sudo.

 ![sudo cat sudoers](/img/811-sudo-cat-sudoers.png)


**2. Permisos del archivo sudoers**

 El archivo sudoers está altamente protegido. El usuario propietario es root, y el grupo propietario también es root. El archivo sudoers tiene permisos de solo lectura tanto para el usuario como para el grupo propietario.

 ### `ls -la /etc/sudoers`

![ls -la /etc/sudoers](/img/811-ls-la-sudoers.png)

Este es el comportamiento típico para el archivo sudoers, ya que es esencial para la seguridad del sistema y debe protegerse de modificaciones no autorizadas.

**3.Edición del archivo sudoers**

 El archivo sudoers no debe editarse directamente con editores de texto como nano, pico, etc. 

### `sudo pico /etc/sudoers`

![sudo pico /etc/sudoers](/img/811-sudo-pico-sudoers.png)


### `sudo visudo`

En su lugar, se debe utilizar el comando `sudo visudo` para abrir y editar el archivo. Esto garantiza la integridad del archivo y evita problemas de sintaxis.



**4. Estructura del archivo sudoers**

El archivo sudoers contiene comentarios y reglas. Las reglas no comentadas especifican quién puede ejecutar comandos con sudo. Cada regla consta de los siguientes elementos:

*  Usuario al que se aplican los permisos.
*  Host o hosts en los que se aplican los permisos (generalmente se usa "ALL" para cualquier host).
*  Lista de usuarios que el usuario especificado puede suplantar.
*  Lista de grupos que el usuario especificado puede suplantar.
*  Lista de comandos que el usuario puede ejecutar con sudo.

Ajustes predeterminados en el archivo sudoers que configuran el comportamiento de sudo.

![811-000](/img/811-oooo.png)

1. **Defaults env_reset**: 
Restablece las variables de entorno al ejecutar comandos con sudo para mejorar la seguridad.

2. **Defaults mail_badpass**:
 Envía un correo electrónico si alguien ingresa una contraseña incorrecta al usar sudo.

3. **Defaults secure_path**:
Establece una ruta segura para buscar comandos, evitando comandos no deseados.

4. **Defaults use_pty**:
 Utiliza una ventana de terminal pseudo-TTY para ejecutar comandos con sudo, útil para aplicaciones interactivas.

![ppp](/img/811-ppp.png)

1. `root ALL=(ALL:ALL) ALL` Esta regla permite al usuario root ejecutar cualquier comando (ALL) en cualquier host, como cualquier usuario (ALL) y en nombre de cualquier usuario (ALL) y grupo (ALL). Básicamente, root tiene todos los privilegios.

2. `%admin ALL=(ALL) ALL`: Los miembros del grupo admin pueden obtener privilegios de superusuario y ejecutar cualquier comando en cualquier host, en nombre de cualquier usuario y grupo. Esto permite que los miembros del grupo admin sean administradores.

3. `%sudo ALL=(ALL:ALL) ALL`: Los miembros del grupo sudo también pueden obtener privilegios de superusuario y ejecutar cualquier comando en cualquier host, en nombre de cualquier usuario y grupo. Esto es típico en muchas distribuciones de Linux donde los usuarios en el grupo sudo pueden usar sudo para obtener privilegios elevados.

4. `@includedir /etc/sudoers.d`: Esta línea indica que el archivo /etc/sudoers puede incluir configuraciones adicionales desde archivos en el directorio /etc/sudoers.d. Esto permite una gestión más modular de las configuraciones de sudo. Cada archivo en ese directorio contendrá configuraciones adicionales.

En resumen, este fragmento de sudoers define las reglas de acceso y privilegios para el usuario root, los miembros del grupo admin y los miembros del grupo sudo, otorgando a estos usuarios y grupos acceso a ejecutar comandos con privilegios elevados.

**5. Creación de reglas**

 En lugar de agregar usuarios individualmente al archivo sudoers, es más común agregar usuarios a grupos y luego permitir que un grupo tenga permisos en el archivo sudoers. Esto simplifica la administración de permisos.

**6. Uso de visudo** 

La herramienta `visudo` ayuda a evitar errores de sintaxis al editar el archivo sudoers. Después de modificar el archivo, verifica su validez antes de guardar los cambios.


***
**En resumen, el archivo sudoers es una parte crucial de la administración de permisos en sistemas Unix y Linux. Permite especificar quién puede ejecutar comandos con privilegios elevados utilizando sudo, y se debe editar con precaución para evitar errores de configuración.**

***
