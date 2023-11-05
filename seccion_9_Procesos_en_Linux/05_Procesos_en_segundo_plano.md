# Primer Plano y Segundo Plano

 En Linux cuando ejecutas un comando en una terminal, por defecto, se ejecuta en el primer plano. Esto significa que la terminal está bloqueada y espera tu interacción con el comando. Puedes interactuar directamente con el programa en ejecución.

**Ejecución en Segundo Plano**

Puedes ejecutar programas en segundo plano para liberar la terminal y permitirte seguir trabajando en ella. Para hacerlo, simplemente agrega un signo **&** al final del comando. Esto permite que el proceso se ejecute en segundo plano mientras la terminal permanece disponible para otros comandos.

![segindo plano &](/img/904-emacs-segundo-plano.png)

### `[1] 22994`
Es una salida común en una terminal de Linux después de dejar un proceso en segundo plano.

* **[1]**: Este número entre corchetes es el identificador del trabajo o job. Cada trabajo en segundo plano recibe un número de identificación único para que puedas referirte a él fácilmente en comandos posteriores.

* **22994**: Este es el número de identificación del proceso en sí. Cada proceso en el sistema tiene un identificador único llamado PID (Process ID), y este número es el PID del proceso que se ha ejecutado en segundo plano.

Por lo tanto, `[1] 22994` significa que el proceso con el PID 22994 se ha colocado en segundo plano y se le ha asignado el identificador de trabajo [1]. Puedes utilizar este identificador para gestionar el proceso en segundo plano si es necesario..

### Gestión de Procesos en Segundo Plano:

### `jobs`

Puedes utilizar el comando jobs para ver una lista de todos los procesos en segundo plano.

![jobs](/img/905-jobs.png)

### `fg` 

Utiliza `fg` seguido del identificador del trabajo para traer un proceso en segundo plano al primer plano.

![emacs bg](/img/905-emacs-fg.png)

### `bg`

Con `bg`, puedes enviar un proceso en primer plano al segundo plano.

![emacs bg](/img/905-emac-bg.png)

Interrumpir Procesos en Primer Plano: En el primer plano, puedes interrumpir un proceso presionando Ctrl + C. Sin embargo, esto no afecta a los procesos en segundo plano.

Detener un Proceso en Segundo Plano: Para detener un proceso en segundo plano sin traerlo al primer plano, puedes utilizar señales.