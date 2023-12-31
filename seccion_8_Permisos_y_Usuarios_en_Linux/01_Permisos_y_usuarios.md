# Comprender la Base de la Seguridad en Linux: Usuarios y Permisos.

### Multitarea en Linux:
Linux es un sistema operativo multitarea, lo que significa que puede ejecutar varios procesos (programas o tareas) de manera simultánea en un solo sistema. Esto permite que los usuarios realicen varias tareas al mismo tiempo sin interferir entre sí. Cada proceso tiene su propio espacio de memoria y recursos asignados, lo que evita conflictos y mejora la eficiencia del sistema. Los procesos se ejecutan en segundo plano o en primer plano, y el sistema operativo gestiona su planificación para garantizar un uso eficiente de la CPU.

### Multiusuario en Linux:
Linux es también un sistema operativo multiusuario, lo que implica que varios usuarios pueden acceder y utilizar el sistema al mismo tiempo. Cada usuario tiene su propia cuenta con un nombre de usuario único y sus propias configuraciones y archivos personales. Esto es fundamental en entornos compartidos, como servidores o sistemas empresariales, donde varios usuarios deben acceder a los recursos del sistema de forma segura y simultánea. Linux administra el acceso y los privilegios de cada usuario para garantizar la seguridad y el aislamiento de datos.

En resumen, la multitarea permite la ejecución simultánea de múltiples tareas o procesos en un sistema Linux, mientras que la multiusuario permite que varios usuarios accedan y utilicen el sistema de manera independiente. Estos conceptos son esenciales para comprender cómo Linux gestiona la concurrencia y proporciona un entorno de trabajo eficiente y seguro para usuarios múltiples.

# Permisos y usuarios: passwd, shadow, group

Los archivos "passwd", "shadow" y "group" son elementos esenciales en sistemas operativos tipo Unix y Linux para gestionar permisos y usuarios.  

### Resumen de su función y propósito:

1. **passwd**: Este archivo almacena información básica de usuario, como:

* nombres de usuario
* identificaciones de usuario (UID)
* identificaciones de grupo principal (GID) 
* nombres de usuario completos 
* directorios de inicio  
* shells predeterminados. 

#### `cat /etc/passwd`

![passwd](/img/801-passwd.png)

También guarda una referencia a la ubicación del archivo "shadow" que almacena contraseñas cifradas.

2. **shadow**: El archivo "shadow" almacena contraseñas cifradas de los usuarios. Este archivo se utiliza para mejorar la seguridad, ya que las contraseñas no se almacenan en el archivo "passwd" a simple vista. Solo el superusuario (root) tiene acceso de lectura al archivo "shadow", lo que evita que otros usuarios vean las contraseñas.

#### `sudo cat /etc/shadow`

![shadow](/img/801-shadow.png)

3.  **group**: El archivo "group" contiene información sobre grupos de usuarios. Al igual que el archivo "passwd", almacena identificaciones de grupo (GID) y una lista de usuarios que pertenecen a cada grupo. Esto es útil para gestionar permisos y acceso de grupos en el sistema.

#### `cat /etc/group`

![group](/img/801-group.png)

***

**En resumen, estos archivos son parte fundamental de la administración de usuarios y permisos en sistemas Unix y Linux.** 
* **El archivo "passwd" contiene información básica del usuario.** 
* **El archivo "shadow" almacena las contraseñas cifradas de los usuarios.**
* **El archivo "group" contiene información sobre grupos de usuarios.** 

**Juntos, facilitan la gestión de usuarios y grupos en el sistema, así como la configuración de permisos y accesos.**

***

### `id`


El comando id en sistemas Unix y Linux se utiliza para mostrar la identidad del usuario actual o de un usuario específico en el sistema. Proporciona información sobre el usuario y los grupos a los que pertenece. La salida del comando id suele incluir la siguiente información:

* **El identificador de usuario (UID)**: Es un número único que identifica de manera exclusiva a cada usuario en el sistema.
* **El nombre del usuario**: Muestra el nombre de usuario correspondiente al UID.
* **El identificador de grupo principal (GID)**: Indica el grupo principal al que pertenece el usuario.
* **Los identificadores de grupos adicionales (si los hay)**: Enumera otros grupos a los que el usuario pertenece.

Por ejemplo, si ejecutas el comando id sin argumentos, mostrará la información de identidad del usuario que está actualmente conectado al sistema.

![id](/img/801-id.png)

También puedes proporcionar un nombre de usuario como argumento para ver la identidad de otro usuario.

```shell
uid=1000(kiril) gid=1000(kiril) groups=1000(kiril),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),122(lpadmin),135(lxd),136(sambashare)
```

En esta salida:

* "uid"- representa el identificador de usuario
* "gid"- es el identificador de grupo principal
* "groups"- lista los grupos a los que pertenece el usuario, incluyendo el grupo principal y otros grupos adicionales.


En sistemas tipo Unix y Linux, es común encontrar un grupo con el mismo nombre que un usuario. En lugar de utilizar un grupo común llamado 'usuarios,' la práctica moderna de Linux es crear un grupo único con un solo miembro, que tiene el mismo nombre que el usuario correspondiente. Esto simplifica la gestión de permisos, ya que los permisos se pueden asignar a grupos en lugar de a usuarios individuales. Esta estrategia facilita la administración de permisos y mejora la eficiencia en la gestión de usuarios y recursos en el sistema.