### Representación en Binario

 Los permisos se dividen en tres conjuntos de tres bits cada uno, correspondientes al propietario, al grupo y al resto de usuarios. Cada uno de estos tres bits se usa para representar un permiso específico:

* **4 representa el permiso de lectura.**
* **2 representa el permiso de escritura.**
* **1 representa el permiso de ejecución.**
* **0 representa la ausencia de permiso.**

Por ejemplo, si un archivo tiene permisos "rw-" (lectura y escritura para el propietario y "---" ningún permiso para el grupo y otros usuarios), se representaría en binario como "110". Esto se hace para cada conjunto de permisos, donde grupo seria "000" y otros usuarios tambien "000".

### Representación en Octal
 Agrupando los tres bits correspondientes y  cada conjunto de tres bits se interpreta como un número en binario, y ese número se convierte en su equivalente en octal. 

* `---`     **000** en binario se traduce a **0** en octal.
* `--x`     **001** en binario se traduce a **1** en octal.
* `-w-`     **010** en binario se traduce a **2** en octal.
* `-wx`     **011** en binario se traduce a **3** en octal.
* `r--`     **100** en binario se traduce a **4** en octal.
* `r-x`     **101** en binario se traduce a **5** en octal.
* `rw-`     **110** en binario se traduce a **6** en octal.
* `rmx`     **111** en binario se traduce a **7** en octal.

Así, los permisos del archivo se representan en octal utilizando los números obtenidos de la conversión de cada conjunto de permisos.

### `ls -la modificacion-permisos.txt `

![ls -la modificacion-permisos.txt ](/img/805-inicio.png)

Podemos ver los permisos :
 `-rw-rw-r-- 1 kiril kiril 0 oct 18 16:06 modificacion-permisos.txt`

Donde `rw-rw-r--` seria equvalente a 664 representando en octal.


# Modificación de permisos

### `chmod`

 Es utilizado para cambiar los permisos de archivos y directorios. Su nombre proviene de "change mode" (cambiar modo) y es una herramienta poderosa.

El comando chmod se usa con varios argumentos para especificar cómo cambiar los permisos:

**Modo Absoluto (en números octales)**

#### `chmod 600 modificacion-permisos.txt`

Establece que solo el propietario del archivo **modificacion-permisos.txt** tiene permisos de lectura y escritura, mientras que el grupo y otros usuarios no tienen ningún permiso en el archivo. Esto es un control estricto de acceso al archivo, permitiendo solo al propietario la capacidad de leer y modificar el contenido del archivo.     

![chmod 600 modificacion-permisos.txt](/img/805-chmod-mod.png)


