## Operaciones basicas


1. **Agregar un nuevo usuario**

Para agregar un nuevo usuario en Linux, se utilizan comandos como `useradd` o `adduser`. Los privilegios de superusuario (sudo) son necesarios para realizar esta operación. Se pueden especificar atributos como el directorio base del usuario, nombre completo y más.

![man useradd](/img/812-man-useradd.png)

2. **Crear un nuevo grupo**

Para crear un nuevo grupo, se emplean comandos como `groupadd` o `addgroup`. También se requieren privilegios de superusuario. Puedes asignar opciones al grupo, como su ID de grupo (GID).

![man groupadd](/img/812-man-groupadd.png)

3. **Agregar un usuario a un grupo**

Para agregar un usuario a un grupo existente, se utiliza el comando `usermod`. Nuevamente, se necesita "sudo". El usuario se agrega al grupo especificado con la opció `sudo -a -G` 

![man groupadd](/img/812-man-usermod.pnp.png)

4. **El grupo primario**

El grupo primario de un usuario es importante, ya que determina el grupo propietario de los archivos que el usuario crea. Se puede cambiar el grupo primario con `usermod`.

5. **Modificar nombre**

Los atributos de un usuario, como el nombre de usuario y  el directorio de inicio, se pueden modificar con `usermod`.

6. **Cambiar la contraseña**

Para cambiar la contraseña de un usuario, se utiliza el comando "passwd". Se introduce la nueva contraseña y se verifica.

7. **Eliminar**

Para eliminar usuarios y grupos, se emplean comandos como `userdel` o `deluser` para usuarios y `groupdel` o `delgroup ` para grupos. Se deben tomar precauciones al eliminar grupos que son el grupo primario de usuarios.