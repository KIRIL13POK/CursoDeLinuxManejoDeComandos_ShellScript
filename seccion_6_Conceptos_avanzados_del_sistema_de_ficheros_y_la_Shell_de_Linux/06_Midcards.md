En esta clase, se trata el tema de los "Wildcards" o comodines en la Shell de Linux, que son caracteres especiales que permiten hacer búsquedas y operaciones en grupos de archivos de manera eficiente.
En esta tarea hemos organizado en la ruta `/home/kiril/workspace/cursoLinux` una serie de carpetas y archivos para trabajar con wildcards. En total, hemos creado tantas carpetas como archivos.

![entrada](/img/606-entrada.png)

### Wildcards

Los Wildcards, también conocidos como comodines o caracteres comodín, son caracteres especiales que se utilizan para representar uno o varios caracteres en nombres de archivos o directorios. Estos comodines son una característica esencial de la Shell de Linux y son útiles para realizar diversas operaciones, como búsqueda, manipulación y selección de archivos y directorios de manera más eficiente y flexible. Aquí hay una descripción más detallada de los Wildcards más comunes:

1. **Asterisco** (*): El asterisco representa cero o más caracteres en un nombre de archivo o directorio. Por ejemplo:

    * *.txt coincidirá con todos los archivos que tienen la extensión ".txt".
        ![fichero](/img/606-fichero.png)

    * file* coincidirá con cualquier archivo o directorio cuyo nombre comience con "file".
        ![carpeta](/img/606-carpeta.png)


2. **Signo de interrogación** (?): 

El signo de interrogación representa un solo carácter en un nombre de archivo o directorio.
 
  Por ejemplo:
    carpeta?.txt coincidirá con archivos como "carpeta1.txt" o "carpetaA.txt", donde el "?" puede ser cualquier carácter individual.
        ![carpeta?](/img/606-carpeta2.png)

3. **Corchetes** []:

 Los corchetes se utilizan para definir un conjunto de caracteres que pueden coincidir con un solo carácter en esa posición.

  Por ejemplo:

  * [123] coincidirá con cualquier dígito del 1 al 3.
  * [a-zA-Z] coincidirá con cualquier letra minúscula o mayúscula.
  * [aeiou] coincidirá con cualquier vocal en minúscula.
    
    ![carpeta3](/img/606-carpeta3.png)

 Negación en corchetes [!]: Al colocar un signo de exclamación (!) dentro de los corchetes, se negará el conjunto de caracteres. 


 ![carpeta4](/img/606-carpeta4.png)

4. **Clases predefinidas**: Linux proporciona clases predefinidas para caracteres comunes, como:

```shell
[[:digit:]] coincide con cualquier dígito.
[[:alpha:]] coincide con cualquier letra.
[[:alnum:]] coincide con cualquier letra o dígito.
[[:lower:]] coincide con letras minúsculas.
[[:upper:]] coincide con letras mayúsculas.
```
       
***
**Los Wildcards son especialmente útiles en combinación con comandos como "ls" para listar archivos, "cp" para copiar archivos, "mv" para mover archivos y "rm" para eliminar archivos en función de patrones de nombres. Por ejemplo, puedes usar Wildcards para seleccionar y operar en múltiples archivos a la vez sin tener que especificar cada nombre de archivo individualmente.**

**Sin embargo, es importante tener precaución al usar Wildcards, especialmente con comandos como "rm", ya que un patrón incorrecto podría llevar a la eliminación accidental de archivos no deseados. Siempre se recomienda verificar los resultados con un comando "ls" antes de ejecutar comandos que afecten a archivos en masa.**

***