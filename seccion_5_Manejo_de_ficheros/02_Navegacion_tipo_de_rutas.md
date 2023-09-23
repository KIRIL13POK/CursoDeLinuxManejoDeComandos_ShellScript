### `pwd`  (print working directory) 

Muestra la ruta completa del directorio en el que te encuentras actualmente en el sistema de archivos.

![pwd](/img/502_pwd.png)

### Ruta absoluta

```shell
/home/kiril
```
Es una ruta absoluta . Una ruta absoluta es una especificación completa de la ubicación de un directorio o archivo desde el directorio raíz del sistema de archivos. 
***
**La ventaja de las rutas absolutas es que son independientes de la ubicación actual del directorio desde el que se inicia un comando. Puedes acceder a la misma ubicación, "/home/kiril", desde cualquier lugar del sistema de archivos utilizando esta ruta absoluta.**
***
### Ruta relativas

Una ruta relativa es como proporcionar indicaciones desde tu ubicación actual. En lugar de dar la ruta completa desde el punto de partida, solo mencionas los pasos necesarios para llegar a lugares cercanos. Es similar a dar direcciones en la vida cotidiana: en lugar de explicar todo el camino desde el inicio, te centras en cómo llegar a tu destino desde donde te encuentras actualmente en la estructura de carpetas de un sistema de archivos.


### `ls`

Se utiliza para listar el contenido del directorio actual.
Puedes usar opciones como:
 
 `ls -a` para mostrar archivos y directorios ocultos.

  ![ls -a](/img/502_ls-a.png)

 `la -l` para obtener detalles adicionales sobre los archivos y directorios.
  
  ![ls -l](/img/502_ls-l.png)

 `ls -lh` obtienes una lista de archivos y directorios en formato largo con tamaños de archivo legibles por humanos.

  ![ls -lh](/img/502_ls-lh.png)

 `ls -t`  para listar archivos y directorios en un directorio específico ordenados por fecha y hora de modificación, en orden descendente.

 ### `cd`  (Change Directory):

Se utiliza para cambiar de directorio en el sistema de archivos.
Puedes usar rutas absolutas o relativas como argumento para moverte a un directorio específico.

  * Ruta absoluta:

  ![cd ruta absoluta](/img/502_cd.png)

  * Ruta relativa:

Para moverte utilizando rutas relativas en la línea de comandos de un sistema Unix/Linux, puedes usar los siguientes pasos:

  * **Identifica tu ubicación actual**: Antes de comenzar a navegar con rutas relativas, debes saber en qué directorio te encuentras actualmente.

  * **Para moverte** al directorio "workspace" que está dentro de tu directorio actual, simplemente usa el nombre del directorio:

  ![workspace](/img/502_CD_WORSPACE.png)


  * **Si deseas retroceder** al directorio padre (el directorio un nivel arriba del actual), usa ..:

  ![nivele ruta relativa](/img/502_MOVIENDO-rutas-relativas.png)

  *  ### `cd morkspace/cursoLinux` 

   Una ruta relativa te llevará desde el directorio raíz a "workspace/cursoLinux".




### `cd` 

Sin argumentos te llevará automáticamente al directorio de inicio del usuario y 

### `cd -` 

Me duevolve al directorio anterior donde trabajabamos**