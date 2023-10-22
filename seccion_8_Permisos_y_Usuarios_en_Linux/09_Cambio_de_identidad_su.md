# Creando un Nuevo Usuario en Linux

### `sudo adduser pokrovskiy`

Para crear un nuevo usuario en Linux, puedes usar el comando `sudo adduser`. 


![adduser](/img/809-adduser.png)

### `cat /etc/passwdn`

Viendo el contenido del archivo **/etc/passwd**, podemos observar que se ha creado un nuevo usuario .

![nuevo usuario](/img/809-etc-passwd.png)

```shell
pokrovskiy:x:1001:1001:pokrovskiy,,,:/home/pokrovskiy:/bin/bash
```
* **Nombre de usuario**: pokrovskiy
* **Contraseña:** x (indicando que la contraseña se almacena de forma segura en /etc/shadow)
* **Identificador de usuario UID**: 1001
* **Identificador de grupo GID**: 1001 (por lo general, coincide con el nombre de usuario)
* **Información de usuario**: pokrovskiy,,, (esto podría contener información adicional, como el nombre real)
* **Directorio de inicio**: /home/pokrovskiy
* **Shell**: /bin/bash



# Uso de su (Sustituir Usuario) en Linux: Cambio de Identidades

### `su`
Se utiliza para cambiar de usuario, y **su** es una abreviatura de **sustituir usuario**. Permite cambiar a otra cuenta de usuario, generalmente, pero no necesariamente, a la cuenta de superusuario (root) si tienes los permisos necesarios.

El uso básico del comando su es el siguiente:

```shell
su [nombre_de_usuario]
```
### `su pokrovskiy`

![su-pkrovskiy](/img/809-su-pokrovskiy.png)


Cuando ejecutas este comando, se te pedirá la contraseña del usuario al que deseas cambiar. Una vez que la contraseña se verifica correctamente, estarás "sustituyendo" al nuevo usuario y ejecutando comandos en el contexto de esa cuenta de usuario.

### `exit`

![exit](/img/809-exit.png)

Se utiliza  para salir de una sesión o cerrar una ventana de terminal. Cuando ejecutas `exit` generalmente, la sesión actual se cierra, y regresas al contexto anterior o al shell principal, si estabas en una sesión secundaria.


### `su - <otro-usuario>`

![su -](/img/809-su-guion.png)

El comando cambia al usuario especificado y carga su entorno de forma completa, lo que es útil para trabajar en su contexto como si fuera una nueva sesión de ese usuario.

La opción **-** (guión) al final del comando es importante, ya que indica que se debe iniciar una nueva sesión como el usuario de destino, lo que incluye cargar su entorno de shell como si fuera una sesión completamente nueva.


### Modificando Permisos de Otros Usuarios

![chmod](/img/809-cmod-de-kiril.png)

Como **pokrovskiy**, no puedes cambiar los permisos del directorio **kiril** porque ni siquiera puedes leer su contenido. Debes tener permisos de lectura en un directorio para poder modificar sus permisos con chmod.


### `su -c 'chmod o+r kiril' kiril`

![su -c ](/img/809-chmod-c.png)

* **su** es el comando para cambiar de usuario.
* **-c** es una opción que indica que se ejecutará un comando específico.
* **'chmod o+r kiril'** Esto es el comando a ejecutar en nombre del usuario "kiril" para agregar permisos de lectura a un archivo o directorio, y debe ir dentro de comillas para asegurar que sea tratado como un solo argumento.
* **kiril** es el nombre del usuario en cuyo nombre se ejecutará el comando.

Con `su -c`, puedes ejecutar un comando en nombre de otro usuario sin abrir una nueva sesión. Esto es útil para ejecutar comandos específicos con los permisos del usuario deseado sin cambiar completamente de usuario.