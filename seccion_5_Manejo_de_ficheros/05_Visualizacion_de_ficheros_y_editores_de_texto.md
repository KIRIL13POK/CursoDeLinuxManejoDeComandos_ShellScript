### `file`

Se utiliza para determinar el tipo de un fichero en Linux, incluso si no tiene una extensión reconocible. Proporciona información sobre el tipo y contenido del fichero.

![file](/img/505_file.png)


Con una ruta relativa entramos `cd /var/log` y co `ls ` vamos a observar su contenido:

![/var/log/](/img/505_var-log.png)

Nos interesa concer el **auth.log** 

 * `file auth.log`:
     ![file ](/img/505_file-auth-log.png)

 * `pico auth.log`:
    ![pico](/img/505_pico-log.png)  

### `cat`    

Se utiliza para concatenar y mostrar el contenido de uno o varios ficheros en la terminal. Su nombre proviene de "concatenate" (concatenar), pero su función principal es mostrar el contenido de archivos.

![cat](/img/505_cat-log.png)


### `more auth.log`

Es una herramienta útil para visualizar y navegar por archivos de texto largos en la terminal de manera interactiva. Te permite examinar el contenido página por página y buscar texto dentro del archivo sin cargar todo el contenido de una vez.

![more](/img/505_more.png)


### `less auth.log`

Es una herramienta similar a more, pero ofrece una mayor funcionalidad y flexibilidad para visualizar y navegar por archivos de texto largos en la terminal de manera interactiva. Al igual que more, less permite ver el contenido página por página, pero también permite desplazarse hacia arriba y abajo dentro del archivo.

Navegar con less: Una vez que el archivo se muestra en la vista paginada, puedes usar las siguientes teclas para navegar:

* Tecla Espacio o Avance de página: Avanza a la siguiente página.
* Tecla B o Retroceso de página: Retrocede a la página anterior.
* Teclas de flecha hacia arriba y flecha hacia abajo: Desplazarse línea por línea dentro del archivo.
* Tecla G (mayúscula o minúscula): Ir al final del archivo.
* Tecla 1G o gg: Ir al principio del archivo.
* Tecla / seguida del texto a buscar: Permite buscar texto dentro del archivo. Puedes usar n para avanzar a la siguiente coincidencia o N para retroceder a la anterior.
* Tecla q (minúscula): Salir de less y regresar al símbolo del sistema.

* Ver el número de línea: Para mostrar el número de línea actual en la vista, puedes presionar la tecla =.

Otras funciones avanzadas: less ofrece muchas otras funciones avanzadas, como la capacidad de filtrar el contenido, marcar y seguir referencias de archivos, y más. Puedes acceder a estas funciones presionando la tecla h dentro de less para obtener ayuda.

![les](/img/505_less.png)

Al presionar la tecla h dentro de less, obtendrás acceso a la ayuda integrada que te guiará en el uso de las diversas funciones y comandos disponibles en less, lo que puede ser útil para aprovechar al máximo esta herramienta de visualización de archivos de texto.

![les](/img/505_less-h.png)


