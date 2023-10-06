 # Introducción a los conceptos relacionados con la redirección de entrada y salida en sistemas Linux.

* Los comandos en Linux producen dos tipos de información: la salida normal del programa y mensajes de estado y error.

1. La salida normal se envía al estándar output (stdout), que es un archivo especial conectado a la pantalla.

2. Los mensajes de estado y error se envían al estándar error (stderr), que es otro archivo especial conectado a la pantalla.

3. Los comandos pueden solicitar entrada del usuario a través del estándar input (stdin), que está asociado al teclado.

4. Todos estos archivos especiales (stdout, stderr, stdin) son en realidad enlaces simbólicos a ubicaciones específicas en el sistema de archivos.

5. La redirección de entrada y salida permite redirigir la salida normal o los mensajes de error a archivos en lugar de mostrarlos en la pantalla, o recibir la entrada desde archivos en lugar del teclado.

***

**En resumen, la redirección de entrada y salida es una característica esencial en Linux que permite controlar dónde van los datos generados por comandos y cómo se introducen datos en ellos. Esta capacidad es fundamental para la automatización de tareas y el procesamiento de datos en entornos de línea de comandos.**

***


### Estándar output (stdout)

![estandar output](/img/701-estandar-output.png)

En Linux, los comandos producen resultados que se envían al **estándar output** (stdout), un archivo especial en el sistema de archivos. Este **stdout** es un enlace simbólico a ubicaciones específicas, como **/dev/stdout**.

El **/dev/stdout** es, a su vez, un enlace simbólico a **/proc/self/fd/1**, que representa la pantalla de la terminal. Este archivo especial, de tipo **Device file** (C), actúa como interfaz para mostrar el texto en la pantalla.

Estos conceptos son esenciales para entender cómo los comandos en Linux redirigen su salida estándar a la pantalla de la terminal.

### Error estándar (stderr)

![error estandar](/img/607-eror-estandar.png)

Además de la salida estándar (stdout), en Linux también existe la salida de **error estándar (stderr)**, que se utiliza para enviar mensajes de error o estado. La salida de error estándar se maneja de manera similar a la salida estándar, pero se redirige a través de **/dev/stderr** o **/proc/self/fd/2**. Esto permite que los comandos muestren mensajes de error en la pantalla de la terminal de manera separada de la salida estándar.

***

**En Linux, se utiliza una estrategia de enlaces simbólicos que inicialmente pueden apuntar a ubicaciones diferentes, como "/dev/stdout" (salida estándar) y "/dev/stderr" (salida de error). Sin embargo, estos enlaces finalmente redirigen los datos al mismo archivo especial subyacente. Esto se hace por razones de organización y compatibilidad, permitiendo que los programas utilicen diferentes enlaces simbólicos para escribir datos en un único archivo especial.**

***

### La entrada estándar (stdin) 

![la entrada estandar](/img/701-la-entrada-estandar.png)

La entrada estándar (stdin) en Linux es la fuente desde la cual un programa o comando recibe datos. Por defecto, stdin está conectada al teclado, permitiendo ingresar datos manualmente. También se puede redirigir para obtener datos desde archivos u otras fuentes, lo que facilita la automatización y el procesamiento de datos en el sistema.

***

**La entrada estándar ("/dev/stdin") también sigue un enfoque similar. Los programas pueden utilizar enlaces simbólicos para redirigir la entrada desde diferentes fuentes hacia un único archivo especial subyacente. Esta práctica facilita la gestión de la entrada, salida estándar y los mensajes de error sin necesidad de cambiar las aplicaciones subyacentes.**

***
