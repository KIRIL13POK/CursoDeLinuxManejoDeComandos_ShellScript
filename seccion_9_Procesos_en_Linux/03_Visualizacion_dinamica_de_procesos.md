 # Visualizar de manera dinámica el rendimiento de los procesos en tiempo real
 
Visualizar de manera dinámica el rendimiento de los procesos en tiempo real significa observar y analizar continuamente cómo se comportan los procesos en un sistema operativo en un flujo en constante cambio. Esto implica obtener información actualizada sobre el uso de recursos como CPU, memoria, tiempo de ejecución y otros parámetros de los procesos mientras están en funcionamiento.

En un contexto de sistemas informáticos, la visualización dinámica permite monitorear y comprender cómo los procesos consumen recursos y se comportan a medida que ocurren en el sistema en tiempo real. Esta información en tiempo real es valiosa para administradores de sistemas y usuarios, ya que les permite identificar problemas, ajustar la asignación de recursos y tomar decisiones informadas sobre la gestión de los procesos y la optimización del sistema.
 
 
### `top `

![man top](/img/903-man-top.png) 

Es una herramienta poderosa que proporciona información sobre el consumo de CPU, la memoria, el tiempo de ejecución y más. La pantalla de top se divide en dos partes: la cabecera que muestra información general del sistema y la lista de procesos.

![top](/img/903-top.png)

En la cabecera, se encuentran datos como:
* la hora actual 
* el tiempo de encendido del sistema 
* los usuarios conectados y la carga promedio del sistema en diferentes intervalos de tiempo. 

También se muestra información sobre el consumo de CPU y memoria, incluyendo la memoria RAM y la memoria de intercambio (swap).

En la lista de procesos, se muestran detalles de cada proceso, como su identificador (PID), usuario, prioridad, consumo de CPU, consumo de memoria, estado y tiempo de ejecución. Los procesos se ordenan por consumo de CPU de mayor a menor por defecto.

El comando top permite interactuar de manera interactiva, y se pueden utilizar teclas como:

**S** para cambiar el tiempo de refresco 
**U** para filtrar los procesos por usuario 
**E** para cambiar las unidades de los valores absolutos y **O** para filtrar los procesos por columnas específicas, como PID o porcentaje de CPU.

Al presionar la tecla **h** en el comando `top`, se despliegan más opciones disponibles para su configuración y uso.

![top h](/img/903-top-h.png)

***

**`top` es una herramienta útil para supervisar el rendimiento del sistema y comprender cómo se están utilizando los recursos del sistema en tiempo real.**

***