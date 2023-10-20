# La representación simbólica de permisos

La representación simbólica de permisos es una forma de expresar los permisos de archivos y directorios utilizando símbolos y letras para indicar quién tiene qué tipo de acceso. Esta notación es una alternativa a la representación en notación octal y suele considerarse más intuitiva y legible para los usuarios. 

Los símbolos utilizados para representar sobre quién se aplicarán los permisos son:
* **U**: Usuario propietario.
* **G**: Grupo propietario.
* **O**: Otros usuarios (el mundo).
* **A**: Todos (que incluye al usuario propietario, al grupo propietario y otros).

Los símbolos para representar los permisos son los mismos que en la notación octal:
* **R**: Lectura.
* **W**: Escritura.
* **X**: Ejecución.


### `chmod a=r representacion_simbolica.txt  `

En este comando, se está otorgando permiso de lectura (r) a todos los usuarios (propietario, grupo y otros) del archivo representacion_simbolica.txt.

![ejemplo 1](/img/806-ejemplo1.png)

Después de ejecutar este comando, el archivo representacion_simbolica.txt tendrá permisos de lectura para todos los usuarios en el sistema. Esto significa que cualquier usuario, independientemente de si es el propietario, pertenece al grupo propietario o es un usuario no relacionado, podrá leer el contenido del archivo, pero no podrá modificarlo o ejecutarlo.

### `chmod u+w,g+w representacion_simbolica.txt `

Este comando se utiliza para agregar permisos de escritura al usuario propietario (propietario del archivo) y al grupo propietario en el archivo representacion_simbolica.txt. 

![ejemplo 2](/img/806-ejemplo2.png)

Después de ejecutar este comando, el usuario propietario del archivo y los miembros del grupo propietario podrán escribir o modificar el contenido del archivo representacion_simbolica.txt. Otros usuarios, que no sean el propietario ni estén en el grupo propietario, no tendrán permisos de escritura en el archivo.

### `chmod o+wx representacion_simbolica.txt `

Este comando se utiliza para agregar permisos de escritura (w) y ejecución (x) a otros usuarios (mundo) en el archivo.

![ejemplo 3](/img/806.ejemplo3.png)

Es importante recordar que al agregar estos permisos a otros usuarios, estás dando acceso a cualquiera que tenga permisos de lectura a ese directorio para realizar estas acciones en el archivo en cuestión. Por lo tanto, debes ser cuidadoso al otorgar permisos de escritura y ejecución a "otros usuarios".

***

**La representación simbólica es más intuitiva que la notación octal, pero puede ser un poco más larga y compleja de escribir. Sin embargo, es útil conocer ambas formas, ya que la notación octal es más común y ampliamente utilizada en entornos Unix.**

***