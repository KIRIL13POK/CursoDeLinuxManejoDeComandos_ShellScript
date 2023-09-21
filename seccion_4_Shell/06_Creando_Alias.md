### Alias
***
**Un alias en la Shell de Linux es una abreviatura que asignas a un comando o secuencia de comandos para simplificar su ejecución. Sirven para reducir la cantidad de texto que debes escribir en la línea de comandos y mejorar la eficiencia en tareas repetitivas. Los alias se utilizan para personalizar el entorno de trabajo y se pueden definir temporalmente en una sesión o configurar de forma permanente en archivos de inicio de la Shell para que estén disponibles en todas las sesiones de terminal.**
***

### Creando nuestro propio comando alias

1. Seleccionar un nombre para el alias: Es importante elegir un nombre que no esté en conflicto con comandos existentes en Linux.

2.  Para crear un alias, se utiliza el comando "alias" seguido del nombre del alias que se desea crear y la expresión entre comillas simples que se ejecutará cuando se invoque el alias. Por ejemplo:

```shell
alias clist='clear ; ls'
```
*La definición de un alias debe realizarse sin espacios entre el nombre del alias, el signo igual (=) y la expresión, y todo debe estar entre comillas simples.*
***
**Esto crea un alias llamado "clist" que ejecutará los comandos "clear" y "ls" en secuencia cuando se invoque.**
***

3. ### `alias`

Verificar los alias existentes: Para ver todos los alias definidos en la sesión actual, se puede utilizar el comando "alias" sin argumentos.

![clist](/img/406_clist.png)

4. ### `unalias clist`

Se utiliza para eliminar un alias previamente definido en la sesión de la Shell de Linux. 

5. Es importante destacar que los alias definidos en una sesión de terminal no persisten entre sesiones, por lo que se perderán cuando se cierre la terminal. Sin embargo, se pueden configurar alias permanentes en el entorno de la Shell de Linux para que estén disponibles en todas las sesiones.

 A continuación ` Ctrl + D   ` Cierra la Shell :

 ![alias despues de cerrar ](/img/406_alias-despues.png)
