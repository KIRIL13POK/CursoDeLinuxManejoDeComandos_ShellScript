* **Enlaces Simbólicos**: Los enlaces simbólicos, también conocidos como "symlinks," son referencias a otros archivos o directorios en el sistema de archivos de Linux. Funcionan de manera similar a los accesos directos en Windows.

* **Retrocompatibilidad**: Los enlaces simbólicos pueden utilizarse para mantener la retrocompatibilidad con software más antiguo que esperaría encontrar archivos en ubicaciones específicas del sistema de archivos.

* **Actualización de Versiones**: Se pueden crear enlaces simbólicos para asegurarse de que siempre se ejecute la última versión de un programa o script sin que el usuario necesite conocer la versión específica.

Características Técnicas:

 * Cada enlace simbólico tiene su propio inode (número de identificación).
 * Los enlaces simbólicos no almacenan la información del archivo o directorio al que apuntan; en su lugar, almacenan la ruta hacia el objetivo.
 * El tamaño de un enlace simbólico está relacionado con la longitud de la ruta al objetivo.

Creación de Enlaces Simbólicos: Se pueden crear enlaces simbólicos utilizando el comando ln con la `opción -s` para indicar que se trata de un enlace simbólico. Por ejemplo:

```bash

 ln -s /ruta/al/objetivo nombre_del_enlace

```
Rutas Absolutas vs. Rutas Relativas: Puede utilizar rutas absolutas o rutas relativas al crear enlaces simbólicos. La elección depende de si desea que el enlace sea portátil (rutas absolutas) o relativo a su ubicación actual (rutas relativas).

Enlaces Simbólicos a Directorios: Los enlaces simbólicos también pueden apuntar a directorios y funcionan de manera similar.

![enlaces simbolicos](/img/602_ln-s.png)

Cuando borras el archivo al que apunta un enlace simbólico, el enlace simbólico se convierte en un enlace roto. Esto significa que el enlace ya no tiene un objetivo válido en el sistema de archivos porque el archivo original ha sido eliminado. Como resultado:

![enlace roto](/img/602_rm-enlace.png)


1.  El enlace simbólico sigue existiendo en el sistema de archivos, pero su objetivo ya no está disponible.

2. Cualquier intento de acceder o utilizar el enlace simbólico resultará en un error, ya que no puede encontrar el archivo al que apuntaba.

3. El enlace simbólico en sí mismo no ocupa espacio significativo en el disco, ya que solo almacena la ruta al archivo o directorio objetivo. Por lo tanto, no libera mucho espacio cuando se elimina el archivo original.

Cuando borras el archivo al que apunta un enlace simbólico, el enlace sigue existiendo pero se convierte en inútil, ya que su objetivo ha desaparecido.




En resumen, los enlaces simbólicos son útiles para crear referencias flexibles a archivos o directorios en un sistema de archivos de Linux, lo que permite una gestión más eficiente y la optimización de la retrocompatibilidad y la actualización de software.