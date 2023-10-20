# Setuid, Setgid, Sticky bit

Los bits **Setuid (Set User ID), Setgid (Set Group ID) y Sticky Bit** son atributos especiales que se pueden establecer en archivos y directorios en sistemas Unix y Unix-like, como Linux.Estos bits son una parte importante de la gestión de la seguridad y los permisos en sistemas Unix y ayudan a garantizar que los usuarios tengan el nivel adecuado de acceso y control sobre los archivos y directorios.

Cada uno de ellos tiene un propósito específico:

1. **Setuid (SUID)**

Cuando se establece el bit SUID en un archivo ejecutable, este archivo se ejecuta con los privilegios del propietario del archivo en lugar de los del usuario que lo está ejecutando. Esto es útil en situaciones en las que un programa necesita acceso a ciertos recursos o archivos que normalmente solo están disponibles para el propietario del archivo. Por ejemplo, el comando "passwd" que permite a los usuarios cambiar sus contraseñas necesita acceder al archivo "/etc/shadow", que generalmente solo puede ser leído por el superusuario (root). Al establecer el bit SUID en el archivo "passwd", los usuarios normales pueden ejecutarlo y cambiar sus contraseñas sin requerir acceso de superusuario.

### `chomd 4770 Setuid_Setgid_Sticky-bit.txt`

![SUID](/img/808-setuid.png)

**4 (SUID)**: El dígito **4** establece el bit **SUID** en el archivo "Setuid_Setgid_Sticky-bit.txt". Esto significa que cuando este archivo se ejecute, lo hará con los privilegios del propietario del archivo en lugar de los del usuario que lo está ejecutando. El bit SUID es representado por **4** en la notación octal de permisos.

2. **Setgid (SGID)**

Cuando se establece el bit SGID en un archivo ejecutable, este archivo se ejecuta con los privilegios del grupo propietario del archivo en lugar de los del grupo del usuario que lo está ejecutando. Esto es útil en situaciones en las que varios usuarios necesitan acceso a ciertos archivos o directorios y se quiere asegurar que todos los archivos creados en ese contexto pertenezcan al mismo grupo. Por ejemplo, en un directorio compartido por un equipo de desarrollo, al establecer el bit SGID en el directorio, todos los archivos creados dentro de él pertenecerán al mismo grupo que el directorio.

### `chmod 2770 Setuid_Setgid_Sticky-bit.txt`

![SGID](/img/807-setgid.png)

**2 (SGID)**: El dígito **2** establece el bit SGID en el archivo **Setuid_Setgid_Sticky-bit.txt**. Esto significa que cuando un usuario crea un archivo en el mismo directorio, ese archivo heredará el grupo del directorio en lugar del grupo del usuario que lo creó. El bit SGID es representado por **2** en la notación octal de permisos.

3.  **Sticky Bit**

El sticky bit se utiliza comúnmente en directorios, y su propósito principal es evitar que los usuarios eliminen archivos de otros usuarios en un directorio en el que tienen permiso de escritura. Cuando se establece el sticky bit en un directorio, solo el propietario del archivo o el superusuario pueden eliminar o renombrar archivos dentro de ese directorio, incluso si otros usuarios tienen permiso de escritura en el directorio.


### `chmod 1770 Sticky-bit_DIR` 

![sticky-byt](/img/808-styki-byt.png)

**1 (Sticky Bit)**: El dígito **1** establece el Sticky Bit en el directorio **Sticky-bit_DIR**. Esto significa que cuando se aplica el Sticky Bit a un directorio, solo el propietario del archivo o el superusuario pueden eliminar o renombrar  el archivo **Sticky-bit_fichero.txt**
dentro de ese directorio, incluso si otros usuarios tienen permiso de escritura en el directorio.

***

### Es importante aclarar :

**SUID (Set User ID)**: Cuando el bit **SUID** está configurado en un archivo ejecutable, verás la **s** en lugar de la **x** en el lugar de los permisos del propietario.

**SGID (Set Group ID)**: Cuando el bit **SGID** está configurado en un archivo ejecutable, verás la "s" en lugar de la "x" en el lugar de los permisos del grupo.

**Sticky Bit**: Generalmente se aplica a directorios, y cuando está configurado, verás **T** en lugar de la **x** en los permisos de otros usuarios.

***

# Establecer y quitar los bits SUID, SGID y Sticky Bit utilizando notación simbólica


1. **SUID (Setuid)**:
    * Para establecer el bit **SUID** para el propietario: `chmod u+s archivo.txt`
    * Para quitar el bit **SUID** para el propietario: `chmod u-s archivo.txt`

2. **SGID (Setgid)**:
    * Para establecer el bit **SGID** para el grupo:`chmod g+s archivo_o_directorio` 
    * Para quitar el bit **SGID** para el grupo: `chmod g-s archivo_o_directorio`

3. **Sticky Bit**:
    * Para establecer el **Sticky Bit** en un directorio:`chmod +t directorio` 
    * Para quitar el **Sticky Bit** en un directorio: `chmod -t directorio`


### Estos bits son una parte importante de la gestión de la seguridad y los permisos en sistemas Unix y ayudan a garantizar que los usuarios tengan el nivel adecuado de acceso y control sobre los archivos y directorios.
