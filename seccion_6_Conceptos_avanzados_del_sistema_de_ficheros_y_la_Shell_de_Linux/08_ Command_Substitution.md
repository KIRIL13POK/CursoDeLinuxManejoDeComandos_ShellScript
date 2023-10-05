# Command substitution 

Es una característica que te permite tomar la salida de un comando y usarla como entrada para otro comando. Esto es útil cuando deseas usar el resultado de un comando como argumento o entrada para otro comando sin tener que guardar la salida en un archivo temporal. En Linux, puedes realizar la "command substitution" de dos maneras: usando comillas inversas (``) o el subshell $().
*** 

### `which`
     
![which](/img/608-which.png)

 Se utiliza para obtener información sobre la ubicación de un archivo, enlace o ejecutable en el sistema de archivos. 

 Por ejemplo:

 ![which cat](/img/608-which-cat.png)

Muestra la ubicación de la utilidad "cat" en el sistema.

* **Problema de interpretación**: 

Si intentas utilizar la salida de un comando como argumento para otro comando sin command substitution, la shell interpretará la salida como un argumento y generará un error si no encuentra un archivo con ese nombre.
  
  ![nombre](/img/608-nombre.png)

* **Command Substitution**: La command substitution es una técnica que te permite tomar la salida de un comando y usarla como entrada o argumento para otro comando. 

![which cat](/img/608-which-cat2.png)

Se puede lograr de dos maneras:

![las dos formas de lograr](/img/608-lograr.png)

*** 
**En resumen, la command substitution es una técnica útil en la línea de comandos de Linux que te permite aprovechar la salida de un comando y utilizarla en otros comandos de manera eficiente, lo que facilita el procesamiento de datos y la automatización de tareas.**
***