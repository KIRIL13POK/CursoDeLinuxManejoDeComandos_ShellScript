# Permisos por defecto: umask

![umaskimg](https://phoenixnap.com/kb/wp-content/uploads/2021/04/linux-umask-command.png)

El término umask mas se refiere a los permisos por defecto que se aplican a archivos y directorios cuando se crean en un sistema operativo basado en Unix o Linux. 

![umask](/img/807-umask.png)


***
**La máscara de permisos umask se utiliza para especificar qué permisos se deben quitar de los permisos predeterminados cuando se crea un archivo o directorio. En otras palabras, el umask determina qué permisos no se otorgan automáticamente a los archivos y directorios al crearlos.**
***

### `umask`

Para mostrar la máscara de permisos actual, simplemente puedes ejecutar el comando "umask" en la terminal, y te mostrará un valor en octal, que representa la máscara actual.

![umask 002](/img/807-umasl-002.png)

Con una máscara de permisos **0002**, los archivos y directorios que crees tendrán permisos completos para el propietario y el grupo, pero los otros usuarios solo tendrán permisos de lectura. Esto significa que otros usuarios podrán leer el contenido de los archivos, pero no podrán modificarlos ni ejecutarlos.

### Intrpretacion de los digitos

* **Primer dígito**: Permisos especiales (SUID, SGID y sticky bit)
* **Segundo dígito**: Permisos del propietario del archivo
* **Tercer dígito**: Permisos del grupo del archivo
* **Cuarto dígito**: Permisos para otros usuarios (el mundo)

Estos dígitos, cuando se establecen en un valor umask, determinan cómo se quitarán ciertos permisos de los archivos y directorios creados en el sistema. Los valores numéricos en cada dígito representan los permisos en formato octal.

* **4** representa permisos de lectura, 
* **2** representa permisos de escritura 
* **1** representa permisos de ejecución.

### `umask 0000`

![umask 0000](/img/807-umask-000.png)

Si estableces la máscara de permisos (umask) en **0000**, significa que no se quitarán permisos por defecto al crear archivos y directorios. En otras palabras, todos los permisos por defecto se mantendrán intactos al utilizar esta máscara.

Los permisos por defecto típicos al crear archivos y directorios son los siguientes:

* **Propietario**: Lectura, escritura y ejecución.
* **Grupo**: Lectura y escritución.
* **Otros usuarios (el mundo)**: Lectura y ejecución.

***
**La elección de una máscara de permisos depende de los requisitos de seguridad y acceso en tu sistema. Un umask más restrictivo aumenta la seguridad limitando los permisos por defecto, pero también puede dificultar el trabajo colaborativo. Por lo tanto, la configuración adecuada de umask es una parte importante de la administración de permisos en un sistema Unix o Linux.**
***