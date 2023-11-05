# Las señales

Las señales son una parte fundamental de la gestión de procesos en sistemas operativos tipo Unix, ya que permiten una comunicación eficiente entre el sistema operativo y los programas en ejecución. Los programadores pueden utilizar señales para controlar el comportamiento de sus aplicaciones y gestionar eventos importantes, como la recarga de configuraciones o la finalización ordenada de un proceso.   

### `kill`

![man kill](/img/906-man-kill.png)

Es un comando que se utiliza para enviar señales a procesos en ejecución. Aunque el nombre del comando es **kill**, su función no es necesariamente matar o finalizar un proceso; más bien, se utiliza para enviar diferentes señales a los procesos, lo que puede tener diversos efectos en su funcionamiento. Estas señales pueden usarse para controlar o interactuar con los procesos de manera específica.

    
### STOP

### SIGTSTP `kill -TSTP <PID>` / `kill -20 <PID>` 

![kill -20](/img/905-kill-CONT.png)

Se utilizan para enviar una señal de parada (stop) a un proceso en ejecución. Esta señal hace que el proceso se detenga temporalmente, permitiendo que se pause su ejecución. Es similar a lo que ocurre cuando presionas `Ctrl+Z`  en la terminal, lo que suspende el proceso en primer plano. El proceso no se cierra ni se finaliza, pero queda en estado de pausa.

### SIGSTOP `kill -STOP <PID>` / `kill -19 <PID>`

Cuando se envía esta señal a un proceso, el proceso se detiene y se suspende en su estado actual. Esto significa que el proceso no puede realizar ninguna operación adicional hasta que se le envíe una señal de reanudación.

***
La diferencia clave entre SIGSTOP y SIGTSTP radica en cómo se manejan y qué control tiene el proceso sobre ellas:

* **SIGSTOP** es una señal de detención extremadamente fuerte y enérgica. Cuando se envía esta señal a un proceso, el kernel obliga al proceso a detenerse de inmediato sin permitir que el proceso realice ninguna acción previa. En otras palabras, el proceso se congela instantáneamente y no puede realizar ninguna tarea adicional antes de la pausa. Es una pausa forzada.

* **SIGTSTP**, por otro lado, es una señal de parada que el proceso puede gestionar de manera más flexible. Cuando se envía esta señal, el proceso puede optar por detenerse o ignorarla según su propia lógica. Si el proceso decide detenerse, puede realizar tareas de limpieza o guardar su estado antes de la pausa. Esto le da al proceso cierto control sobre cómo manejar la señal.

**En resumen, SIGSTOP es una pausa inmediata y forzada, mientras que SIGTSTP permite al proceso decidir si se detiene o continúa, con la opción de realizar acciones antes de la pausa.**

***

###  Interrupción:

### SIGINT `kill -2 <PID>` / `kill -INT <PID>`

![KILL -2](/img/906-KILL-2.png)

Esta señal se utiliza para interrumpir o detener un proceso de manera controlada. Puedes enviar **SIGINT** a un proceso presionando la combinación de teclas `Ctrl+C` en la terminal.

Cuando un proceso recibe la señal **SIGINT**, generalmente responde interrumpiendo su ejecución actual y terminando de manera ordenada. Esto permite al proceso realizar acciones de limpieza, liberar recursos y cerrar correctamente antes de finalizar. La mayoría de las aplicaciones de línea de comandos en Linux responderán a SIGINT finalizando la ejecución, pero el comportamiento exacto puede variar según el programa.

En resumen, **SIGINT** es una señal de interrupción que se utiliza para detener un proceso de manera controlada, permitiéndole realizar tareas de cierre ordenado antes de finalizar su ejecución.


### SIGKILL `kill -9 <PID>` / `kill -KILL`

se utiliza para enviar una señal extremadamente fuerte de terminación a un proceso en Linux. La señal **KILL** (también conocida como SIGKILL) no permite que el proceso la ignore y fuerza la terminación inmediata del proceso, sin darle la oportunidad de realizar ninguna acción de cierre o limpieza.

***
**La diferencia fundamental entre kill y SIGINT (señal de interrupción) es que kill ofrece al proceso la oportunidad de realizar acciones antes de que se interrumpa su funcionamiento, pero no permite que el proceso la ignore. En cambio, con SIGINT, el proceso puede optar por ignorar la señal y continuar su funcionamiento, lo que le da la oportunidad de decidir si realiza tareas de cierre antes de finalizar. En resumen, kill no permite que el proceso ignore la señal y fuerza una interrupción, mientras que SIGINT permite al proceso decidir si la ignora o realiza tareas de cierre antes de finalizar.**
***


###  SIGCONT (Continuar)

### `kill -18 <PID>` / `kill -CONT <PID>`

![kill CONT](/img/906-kill-18.png)
    
Esta señal se utiliza para reanudar un proceso que ha sido detenido previamente con las señales INT o STOP. Puede ser enviada con el comando kill -CONT.

#### Terminar 

### `kill -15 <PID> ` `kill -TERM <PID>`

La señal TERM se utiliza para finalizar un proceso de manera ordenada.

**Para listar todas las señales disponibles en un sistema Linux es el comando `kill -l`**

![kill-l](/img/906-kill-l.png)

### `killall`

![killall](/img/906-killall.png)

### `killall <nombre-de-proceso>`

Se utiliza para finalizar (matar o detener) todos los procesos que coinciden con un nombre de proceso específico en un sistema Linux. Cuando ejecutas `killall` con el nombre de un proceso como argumento, buscará y terminará todos los procesos cuyo nombre coincida con el que proporcionaste.


***
**En Linux, el envío de señales a procesos se rige por permisos:**

* **El superusuario (root) puede enviar señales a cualquier proceso.**
* **Los usuarios pueden enviar señales a sus propios procesos.**
* **Los usuarios no pueden enviar señales a procesos de otros usuarios, a menos que tengan permisos especiales o sean el superusuario.**

**Estas reglas se aplican para garantizar la seguridad y la integridad del sistema.**

***