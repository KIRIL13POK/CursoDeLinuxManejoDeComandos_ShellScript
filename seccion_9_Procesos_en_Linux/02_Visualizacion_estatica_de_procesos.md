### `ps`

Es un comando que muestra un snapshot de los procesos en ejecución en un sistema Linux en un momento específico.

![man ps](/img/902-ps-man-ps.png)

Por defecto, **ps** muestra solo los procesos asociados con la terminal actual. Esto significa que solo muestra los procesos que se ejecutan en la misma terminal desde la que se ejecuta el comando.

![ps](/img/902-ps.png)

Las columnas principales en la salida de `ps` incluyen:

* **PID** (identificador de proceso)
* **TTY** (terminal)
* **TIME** (consumo de tiempo de CPU)
* **CMD** (comando que generó el proceso)
* **Estado** (estado del proceso)

El estado del proceso se representa con letras, y se pueden consultar los significados de estas letras en el manual de `ps`.

### `ps -x`

Al ejecutar **ps -x** (o **ps aux**), se pueden ver todos los procesos en el sistema, no solo los de la terminal actual. Esto proporciona una vista más completa de los procesos en ejecución.

![ps -x](/img/902-ps-x.png)


![ps -x](/img/902-ps-x2.png)

* **3387**: Es el identificador de proceso (PID, Process ID). Cada proceso en el sistema tiene un número único de PID.

* **pts/0**: Esto indica el terminal en el que se ejecuta el proceso. "pts" se refiere a un terminal pseudo (generalmente una sesión de terminal de usuario), y "/0" es el número del terminal. Esto muestra desde qué terminal se inició el proceso.

* **Sl+**: Estos son indicadores de estado del proceso. En este caso:

    * **S** significa que el proceso se encuentra en estado de dormido (sleep).
    * **l** indica que el proceso está en segundo plano.
    * **+** indica que el proceso tiene alta prioridad de planificación.

    #### `man ps ` PROCESS STATE CODES

    ![PROCESS STATE CODES](/img/902-process-state-code.png)

* **0:00**: Esto muestra el tiempo de CPU que ha consumido el proceso. En este caso, "0:00" significa que el proceso ha consumido muy poco tiempo de CPU, es decir, se ha ejecutado durante 0 minutos y 0 segundos.

### `ps aux `

![ps aux ](/img/902-ps-aux-less.png)

Al agregar el comando `ps aux | less`, se obtiene una salida más detallada que incluye información sobre el usuario, el consumo de CPU, la memoria, el tiempo de inicio y el comando para cada proceso.


