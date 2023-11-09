# El Rol Fundamental de Init en el Arranque y Mantenimiento del Sistema

Iniciamos nuestra inmersión en el corazón de las distribuciones Linux con el proceso **init**. Este componente crítico, cuyo nombre es una abreviatura de **inicialización**, se convierte en el pionero del sistema operativo al arrancar. El kernel se encarga de iniciar init durante el proceso de arranque, siendo el proceso raíz que da vida a todos los demás.

***
Si por alguna razón init no puede llevar a cabo su tarea, se desencadena un error conocido como **kernel panic**, impidiendo que el sistema se inicie y deteniendo todas las operaciones.
***

### `ps ax` / `ps aux`

![ps ax](/img/907-ps-ax.png)

Init persiste en segundo plano desde el encendido hasta el apagado del sistema, actuando como el ancestro directo o indirecto de todos los procesos subsiguientes. Al ejecutar un comando como `ps ax` en la terminal, podemos observar que init, con el identificador de proceso 1, es el punto de origen de la jerarquía de procesos del sistema.

***
### `1 ?   Ss     0:14 /sbin/init auto noprompt splash`

* **1**: Es el identificador de proceso (PID) asignado a este proceso. En este caso, el PID es 1, lo que confirma que se trata del proceso init, el primer proceso que se inicia en el sistema.

* **?** (Estilo de Ejecución): Indica que el estilo de ejecución del proceso es desconocido o no se puede determinar.

* **Ss** (Estado del Proceso): La "S" indica que el proceso está en estado de sueño (sleep), lo que significa que está a la espera de eventos. La "s" indica que es el líder de sesión.

* **0:14** (Tiempo de CPU): Indica el tiempo total de CPU utilizado por el proceso desde su inicio. En este caso, ha consumido 14 segundos de tiempo de CPU.

* **/sbin/init auto noprompt splash**: Muestra la ruta del ejecutable del proceso y los parámetros con los que se inició. En este caso, init se inició desde el directorio "/sbin" con los parámetros "auto noprompt splash".

**En resumen, esta salida indica que el proceso con PID 1 es el proceso init, está en estado de sueño como líder de sesión, ha consumido 14 segundos de tiempo de CPU y se inició con ciertos parámetros desde el directorio "/sbin". La presencia de "splash" sugiere que se está utilizando un modo gráfico durante el arranque.**

***

### Demonios y Servicios

Los procesos iniciados por init, generalmente en segundo plano o modo no interactivo, desempeñan funciones cruciales para el sistema operativo, como respaldar la funcionalidad de la terminal y mantener la interactividad. Estos procesos, que se ejecutan opacamente para los usuarios, reciben el nombre específico de **demonios**.

Es fundamental comprender la distinción entre **demonios** y **servicios**. 
 * **Los demonios** - son procesos que se ejecutan en segundo plano sin interacción directa con los usuarios. 
 * **Los servicios** -aunque también suelen ser demonios, responden a las solicitudes de otros programas o procesos mediante mecanismos de comunicación, como la red.

 La exploración de directorios como **/etc/init.d/** revela archivos de configuración que definen los servicios y demonios que se inician al principio.

![scripts](/img/907-script.png)

Para gestionar estos procesos, init se basa en scripts almacenados en ubicaciones específicas del sistema de archivos. Los scripts **K (kill)** se ejecutan antes, mientras que los scripts **S (startup)** se inician posteriormente.

***
**En resumen, init desempeña un papel crucial en el arranque y mantenimiento del sistema Linux, estableciendo y orquestando la ejecución de procesos esenciales. Este conocimiento profundo de init proporciona una comprensión clave del funcionamiento interno de las distribuciones Linux.**
*** 