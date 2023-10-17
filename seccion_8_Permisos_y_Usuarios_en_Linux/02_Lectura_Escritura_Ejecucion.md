# Lectura (r), Escritura (w) y Ejecución (x)

En Linux, los usuarios tienen asociados permisos de **lectura, escritura y ejecución** en los archivos y directorios del sistema de archivos. 
Estos permisos se aplican a tres colectivos: 

* El dueño del archivo 
* El grupo propietario 
* El resto de usuarios del sistema (world). 

Los permisos se representan mediante nueve letras en grupos de tres, donde cada grupo corresponde a un colectivo. 
Las tres letras representan los permisos de : 
* lectura (R) 
* escritura (W) 
* ejecución (X)
* un guión ("-") indica que no se tiene ese permiso. La distribución de permisos se ve así:

![permisos](/img/802-permisos.png)

* Los tres primeros caracteres indican los permisos del dueño del archivo.
* Los siguientes tres caracteres indican los permisos del grupo propietario.
* Los últimos tres caracteres indican los permisos del resto de usuarios (world).

Ejemplo:

Si un archivo tiene permisos `rwxr-x--x`, significa que el dueño tiene permisos de lectura, escritura y ejecución, el grupo propietario tiene permisos de lectura y ejecución, y el resto de usuarios solo tiene permiso de ejecución.

Es importante comprender que estos permisos se aplican tanto a archivos como a directorios. Los permisos son fundamentales para controlar quién puede acceder, modificar o ejecutar archivos y directorios en el sistema Linux.

##  La salida de un comando `ls -l`

```shell
drwxr-xr-x  2 kiril kiril 4096 oct 14 17:34 Desktop
```

Esta línea muestra información sobre un directorio llamado "Desktop". Aquí está una desglosada de lo que significa cada campo:

1. `drwxr-xr-x`: Esto representa los permisos del directorio "Desktop". La "d" inicial indica que se trata de un directorio. Luego, los siguientes nueve caracteres indican los permisos. En este caso, "rwxr-xr-x" se desglosa de la siguiente manera:

    * El primer conjunto de tres caracteres "rwx" se refiere a los permisos del dueño del directorio (usuario "kiril"). Tiene permisos de lectura, escritura y ejecución.
    *  El segundo conjunto de tres caracteres "r-x" se refiere a los permisos del grupo propietario (grupo "kiril"). Tiene permisos de lectura y ejecución, pero no de escritura.
    *  El tercer conjunto de tres caracteres "r-x" se refiere a los permisos para el resto de usuarios (world). También tienen permisos de lectura y ejecución, pero no de escritura.

2. `2`: Indica la cantidad de enlaces duros que apuntan a este directorio. En este caso, hay dos enlaces duros que hacen referencia a este directorio.

3. `kiril`: Es el nombre del usuario propietario del directorio "Desktop".

4. `kiril`: Es el nombre del grupo propietario del directorio "Desktop".

5. `4096`: Muestra el tamaño en bytes del directorio. En este caso, el directorio "Desktop" ocupa 4096 bytes en el sistema de archivos.

6. `oct 14 17:34`: Indica la fecha y hora en que se creó o modificó por última vez el directorio "Desktop". En este caso, fue modificado por última vez el 14 de octubre a las 17:34.

***
En resumen la línea proporcionada se desglosa de la siguiente manera:

* Tipo de archivo y permisos
* Cantidad de enlaces duros
* Usuario propietario
* Grupo propietario
* Tamaño en bytes
* Fecha y hora de modificación
* Nombre del directorio
***
