# ¿Qué significa "is hashed"?

En el contexto de la shell de Linux, cuando se dice que un comando "is hashed," significa que la shell ha realizado un proceso de resolución de la ruta del comando y ha guardado esa ruta en una estructura de datos llamada tabla hash (hash table). La tabla hash es una forma eficiente de almacenar datos para que puedan ser recuperados rápidamente.

Cuando un comando se "hash" en la shell, significa que se ha encontrado su ubicación en el sistema de archivos y se ha guardado en la tabla hash para futuras referencias. Esto es beneficioso porque acelera el tiempo de ejecución del comando, ya que la shell no necesita buscar la ubicación del comando cada vez que se solicita. En lugar de eso, simplemente consulta la tabla hash para obtener la ubicación del comando y lo ejecuta desde allí.

El comando hash en la shell de Linux te permite ver la lista de comandos que se han "hashed" y se han guardado en la tabla hash. También puedes utilizar hash -r para borrar todas las entradas de la tabla hash, lo que significa que la shell tendrá que buscar nuevamente la ubicación de los comandos la próxima vez que se ejecuten.

En resumen, cuando se dice que un comando "is hashed" en la shell de Linux, significa que su ubicación se ha resuelto y almacenado en una tabla hash para una ejecución más rápida en el futuro.

![hash](/img/407_hash.png)

* **/usr/bin/ls**: El comando "ls" se ha ejecutado 2 veces en tu sistema. Este comando se utiliza para listar los archivos y directorios en un directorio.

* **/usr/bin/clear**: El comando "clear" también se ha ejecutado 2 veces en tu sistema. Este comando se utiliza para limpiar la pantalla de la terminal, eliminando el contenido anterior y dejando solo la línea de comandos visible.

Estos números indican la frecuencia con la que se han ejecutado estos comandos específicos en tu sesión actual de la shell o en tu sistema en general. Puedes utilizar esta información para tener una idea de cuáles son los comandos que más utilizas o para realizar un seguimiento de tus actividades en la terminal.