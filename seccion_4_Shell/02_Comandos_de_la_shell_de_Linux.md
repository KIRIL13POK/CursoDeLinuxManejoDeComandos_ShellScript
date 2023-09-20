Un comando es una instrucción que se introduce en una línea de comandos o en una interfaz de línea de comandos (CLI) para realizar una tarea específica en un sistema operativo o programa. Los comandos son una forma de interactuar con un sistema informático de manera textual o mediante palabras clave, en lugar de utilizar una interfaz gráfica de usuario (GUI) con ventanas y menús.

Los comandos suelen constar de una palabra clave o un conjunto de palabras clave que representan una acción o una operación, seguidos de argumentos o opciones que especifican cómo se debe realizar la tarea. Los comandos se utilizan en sistemas operativos como Linux, macOS y Windows, así como en aplicaciones y herramientas de línea de comandos específicas.


### Los comandos se dividen en cuatro tipos según su funcionalidad:

* **Comandos del Sistema**: Se utilizan para administrar el sistema operativo, como iniciar o apagar el sistema, gestionar usuarios, instalar software y configurar hardware.

* **Comandos de Navegació**: Están diseñados para la gestión de archivos y directorios, permitiendo moverse por el sistema de archivos, listar contenido, cambiar directorios y gestionar archivos.

* **Comandos de Manipulación de Datos**: Facilitan la creación, visualización, edición y procesamiento de datos. Pueden manipular texto, buscar patrones y mostrar contenido de archivos.

* **Comandos de Comunicación y Redes**: Se utilizan para interactuar con redes, realizar diagnósticos de red y comunicarse con otros sistemas a través de la red.

###  Integrados, Externos, Personalizados y Alias

* **Comandos Implementados en la Propia Shell**: Estos comandos están integrados en la shell misma y forman parte de su código fuente.

* **Comandos Externos**: Son programas independientes que residen en el sistema de archivos y pueden ser invocados desde la línea de comandos.

* **Funciones de Shell**: Son utilidades escritas en un lenguaje de programación de shell script y se asemejan a comandos personalizados.

* **Alias** : Son atajos que permiten invocar comandos con opciones específicas de manera más rápida y sencilla.

Estos conceptos son esenciales para comprender cómo funcionan los comandos en sistemas Unix/Linux y son útiles tanto para administradores de sistemas como para usuarios avanzados.


### `type`

Se utiliza para determinar el tipo de un comando, es decir, si el comando es un comando incorporado en la propia shell, un comando externo, una función de shell o un alias.

![type](/img/401_type.png)

### `cp`

Se utiliza para copiar archivos y directorios de un lugar a otro.

![type](/img/401_type-cp.png)

```shell
cp is /usr/bin/cp
```
Esto significa que "cp" es un programa externo que reside en el directorio "/usr/bin/".

### `ls`

Se utiliza para listar el contenido de un directorio. Su función principal es mostrar los archivos y subdirectorios presentes en el directorio especificado o en el directorio actual si no se proporciona ninguna ubicación.

![ls](/img/401_type-ls.png)

Es un alias definido en tu sistema, la respuesta muestra cómo está configurado el alias.

*"ls --color=auto", lo que significa que se ejecutará con la opción "--color=auto" para mostrar el contenido de directorios con colores.*

# Argumentos y Parametros de los comandos

* **Argumentos**: Son valores o cadenas de texto que se pasan después de un comando para personalizar su comportamiento o proporcionar datos de entrada. Se proporcionan en la línea de comandos al invocar un programa.

* **Parámetros**: Son variables dentro del código de un programa que reciben valores de entrada proporcionados como argumentos. Los parámetros se utilizan para procesar y personalizar el comportamiento del programa.

En resumen, los argumentos se pasan en la línea de comandos, mientras que los parámetros son las variables que los reciben dentro del programa.

![argumentos-parametros](/img/401_PARAMETRO-ARGUMENTO.png)


### `ls -lah Dekstop`

Se utiliza para listar el contenido del directorio llamado "Desktop" de manera detallada y con formato legible por humanos, incluyendo los archivos y directorios ocultos.

