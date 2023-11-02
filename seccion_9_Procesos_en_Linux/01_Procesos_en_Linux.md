# El concepto de procesos 

El concepto de procesos es fundamental en cualquier sistema operativo, incluyendo Linux. 
***
**Un proceso es una instancia activa en ejecución de un programa.**

***

**Un programa es simplemente un archivo ejecutable almacenado en el disco duro de un equipo, mientras que un proceso es lo que ocurre cuando ejecutas ese programa**.

  ![/usr/bin/](/img/901-CD-USR-BIN.png)

***  

En un sistema operativo multitarea como Linux, se tiene la ilusión de que varios programas se ejecutan al mismo tiempo, pero en realidad, el kernel administra los recursos y los asigna secuencialmente a los procesos. Esto sucede tan rápido que parece que todos los programas se ejecutan simultáneamente.

Cada proceso tiene un identificador único llamado **PID (Process ID)**, y el kernel mantiene información sobre la memoria asignada, los archivos abiertos y otros datos relacionados con el proceso.

### `pidof`

Se utiliza para encontrar el PID (Process ID) de un programa en ejecución.

![pidof emacs](/img/901-pidof-emacs.png)

Cuando accedes al directorio **/proc/PID/**, donde **PID** es el número de identificación de proceso, y ejecutas el comando `ls`, verás una lista de archivos y subdirectorios que proporcionan información específica sobre ese proceso, como su estado, propiedades y recursos utilizados. Esta información es útil para el diagnóstico y monitoreo del proceso, pero ten en cuenta que modificar o eliminar archivos en estos directorios puede causar problemas en el sistema.

![/proc/PID](/img/901-ls-proc-PID.png)
*Los archivos en el directorio /proc/ son archivos virtuales que proporcionan información en tiempo real sobre el estado y la configuración del sistema y los procesos. Son interfaces para acceder a datos del kernel del sistema operativo, y se utilizan para el monitoreo y diagnóstico del sistema y los procesos.*

***

**En resumen, un programa es un archivo ejecutable, y un proceso es una instancia activa en ejecución de ese programa en un sistema operativo como Linux. Los procesos son administrados por el kernel y tienen un identificador único PID) que permite interactuar con ellos.**

***