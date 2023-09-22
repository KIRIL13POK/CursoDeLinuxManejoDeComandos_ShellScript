![linus](https://softwarelab.org/wp-content/uploads/Linux.jpg)

* **Origen del Sistema de Archivos**: El sistema de archivos se originó para ayudar a las personas a almacenar y estructurar información en los primeros ordenadores. Se basa en conceptos similares a la organización física de documentos en carpetas y archivos en el mundo real.

* **Estructura Jerárquica**: El sistema de archivos en Linux está organizado de manera jerárquica. Comienza con una carpeta principal llamada el "directorio raíz" representada por una barra ("/"). A partir de aquí, se crean subdirectorios y archivos que forman una estructura de árbol.

***
### `sudo apt install tree`

*Este comando instalará la utilidad "tree" que se utiliza para mostrar de manera estructurada y jerárquica la estructura de directorios y archivos en tu sistema de archivos. Asegúrate de utilizar el comando correcto para que la instalación se realice correctamente.*

***
### `tree /`

Se utiliza para mostrar la estructura de directorios y archivos de tu sistema de archivos a partir del directorio raíz ("/"). Esto te dará una vista jerárquica de todos los directorios y archivos que se encuentran en tu sistema. En un sistema Ubuntu recién instalado, verás una gran cantidad de archivos y subdirectorios. Esto se debe a que una distribución de Ubuntu típica viene con una variedad de software y configuraciones preinstaladas, lo que resulta en una estructura de directorios bastante compleja.

* **Exploración del Sistema de Archivos**: Puedes explorar el sistema de archivos desde la terminal de Linux utilizando comandos. El comando "ls" es comúnmente utilizado para listar los contenidos de un directorio, y "cd" se utiliza para cambiar entre directorios.


* **Niveles del Árbol de Directorios**: Puedes explorar diferentes niveles del árbol de directorios utilizando la utilidad "tree". Por ejemplo, puedes ver solo los subdirectorios inmediatos del directorio raíz o profundizar más en la estructura.

### `tree -L 1 /`

![primer nivel arbol](/img/501_tree-L1.png)


Se utiliza para mostrar la estructura de directorios y archivos en el directorio raíz ("/") de tu sistema de archivos, limitando la profundidad a 1 nivel. Esto significa que mostrará solo los archivos y subdirectorios directamente dentro del directorio raíz.

*Puedes limitar la profundidad de visualización utilizando la opción -L seguida de un número para especificar cuántos niveles de profundidad deseas mostrar.*



En resumen, el sistema de archivos en Linux se organiza jerárquicamente con un directorio raíz y subdirectorios, y se utiliza para almacenar y estructurar datos y programas en el sistema operativo. La terminal de Linux ofrece herramientas para explorar y navegar por esta estructura de manera eficiente.