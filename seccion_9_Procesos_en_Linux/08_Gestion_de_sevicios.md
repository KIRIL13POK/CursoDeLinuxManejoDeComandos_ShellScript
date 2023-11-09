
 # La gestión de servicios

La gestión de servicios  se refiere al control y supervisión de programas o procesos que se ejecutan en segundo plano. Esto incluye acciones como iniciar servicios al arrancar el sistema, detenerlos cuando ya no son necesarios, y verificar su estado para asegurarse de que estén funcionando como se espera. **En resumen, se trata de administrar el ciclo de vida de estos programas para garantizar un funcionamiento eficiente y fiable del sistema operativo.**

* **Invocar Scripts (init.d)**:
    Se pueden ejecutar scripts ubicados en `/etc/init.d/` para interactuar con servicios.
    Argumentos como **start, stop, restart, y reload** permiten acciones específicas.

* **System CTL**:
        System CTL es un gestor de servicios avanzado que ofrece una interfaz de usuario más alta.
        Comandos como systemctl **start/stop/restart/status** permiten controlar servicios individualmente.

* **Service Tool**:
        La herramienta Service envuelve el comportamiento de System CTL y, en última instancia, init.d.
        Ejemplos incluyen service <nombre_servicio> **start/stop/restart/status**.

* **Privilegios de Superusuario**:
        Se requieren privilegios de superusuario (sudo) para iniciar, detener o reiniciar servicios.

* **Listar Servicios en Ejecución**:
        Se puede listar todos los servicios en ejecución con systemctl list-units.

.