***

**Los inodos son una parte fundamental del sistema de archivos de Linux y son esenciales para su funcionamiento. Contienen detalles importantes que permiten al sistema operativo gestionar los archivos y directorios de manera eficiente.**

***

* **Introducción a los Inodos**: Los inodos son estructuras cruciales dentro del sistema de archivos de Linux que almacenan metadatos y detalles de implementación de archivos y directorios. Contienen información como *permisos, propietario, tamaño y ubicación en disco de los datos del archivo.*

* **Metadatos**: Los metadatos son *información adicional sobre los archivos y directorios, como permisos, propietario, fecha de creación, etc*. Estos datos se almacenan en el inode correspondiente.

* **Identificador Único**: Cada archivo y directorio en el sistema de archivos de Linux está asociado con un inode único que contiene información sobre él. El sistema operativo usa este identificador para gestionar y referenciar los archivos.

* **Número de Inodos**: El número de inodos disponibles en el sistema de archivos es aproximadamente igual al número total de archivos y directorios que puede contener el sistema. Esto es independiente del espacio de almacenamiento en disco.

* **Fragmentación**: Cuando los archivos son muy grandes o no pueden almacenarse en bloques consecutivos en disco, se fragmentan en múltiples fragmentos. Los inodos almacenan información sobre estos fragmentos para su recuperación.

* **Uso de Bloques**: Los inodos almacenan información sobre los bloques utilizados por un archivo. Esto es importante para localizar y recuperar los datos del archivo en el disco.

* **Comandos para Ver Inodos**: Se pueden utilizar comandos como `ls -i ` para mostrar el número de inode asociado a un archivo o directorio y `stat <nombre-de-fichero>`  para obtener información detallada sobre un inode específico.

    ![ls-i](/img/601_ls-i.png)



* **Checksum**: Los inodos también contienen un checksum, que se utiliza para verificar la integridad del inode y sus datos.

* **Extensiones**: En el caso de archivos fragmentados, los inodos pueden utilizar extensiones para almacenar información sobre los fragmentos en lugar de mantener una lista de bloques individuales.


### `df -i`

![df -i](/img/601_df-i.png)


Cuando ejecutas df -i, obtendrás una lista de sistemas de archivos montados y la siguiente información:

* **Sistema de archivos (Filesystem)**: El nombre o la ruta del sistema de archivos montado.
* **Inodos (Inodes)**: El número total de inodos disponibles en ese sistema de archivos.
* **Inodos utilizados (IUsed)**: El número de inodos utilizados actualmente en ese sistema de archivos.
* **Inodos libres (IFree)**: El número de inodos disponibles (sin utilizar) en ese sistema de archivos.
* **Porcentaje de uso de inodos (IUse%)**: El porcentaje de inodos utilizados en relación con el número total de inodos disponibles.

Este comando es útil para verificar el uso de inodos en un sistema de archivos y puede ser especialmente importante cuando se trabaja con sistemas de archivos que pueden contener una gran cantidad de archivos pequeños, como servidores web o sistemas de correo electrónico, donde la gestión de inodos es esencial para garantizar un funcionamiento adecuado del sistema.

***
Es posible que te encuentres en una situación en la que todavía tengas espacio de almacenamiento disponible en tu disco duro, pero te has quedado sin inodos libres. Esto significa que, aunque haya espacio físico en tu disco para almacenar datos, no podrás crear nuevos archivos o directorios en el sistema de archivos porque no quedan inodos disponibles para describir y gestionar esos nuevos elementos.

Los inodos son estructuras que almacenan información sobre los archivos, como permisos, propietario, ubicación en disco y otros metadatos. Cada archivo o directorio en el sistema tiene un inode asociado. Cuando te quedas sin inodos libres, incluso si tienes espacio en disco, no podrás crear más archivos o directorios hasta que se liberen inodos existentes o se amplíe la cantidad de inodos disponibles en el sistema de archivos. Esta es una limitación importante a considerar al gestionar tu sistema de archivos.

***