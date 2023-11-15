# Routing

El **routing** es un concepto clave en redes, especialmente en sistemas Linux. Este proceso se refiere a cómo los datos se dirigen desde un origen a un destino a través de una red. En el contexto de redes en Linux, el routing implica:

1. **Interfaz de Red**:  Son los puntos de conexión entre un dispositivo y la red. Estas interfaces tienen una dirección física o MAC, que identifica a cada dispositivo dentro de una red local.

2. **Direcciones IP**: Además de la dirección MAC, las interfaces de red también tienen una o más direcciones IP. Estas direcciones permiten la comunicación con dispositivos en otras redes, no solo en la red local.

3. **Unión de Redes**: Diferentes redes se conectan entre sí a través de dispositivos como routers. Los routers juegan un papel crucial en el routing, ya que ayudan a dirigir el tráfico de datos a través de múltiples redes.

4. **Proceso de Routing**: En términos simples, el routing en Linux se refiere a cómo el sistema determina la ruta que deben seguir los datos para llegar a su destino. Esto implica decidir a través de qué interfaces de red y routers deben pasar los paquetes de datos, basándose en su dirección IP de destino.

***
**El routing es fundamental para garantizar que los datos lleguen correctamente de un punto a otro en la red, especialmente cuando esos puntos están en diferentes redes.**
***

### `ip route`

![ip route](/img/1002-ip-route.png)

Es utilizado para mostrar y manipular la tabla de ruteo del sistema. Esta tabla es crucial para la operación de la red, ya que dicta cómo los paquetes de datos son dirigidos desde tu máquina a otras direcciones IP en redes externas. Aquí te explico algunas de sus funciones principales:

* **Mostrar la Tabla de Ruteo**: Al ejecutar ip route sin argumentos adicionales, el comando lista las rutas actuales definidas en la tabla de ruteo. Esta lista muestra a dónde se envían los paquetes de datos basándose en su destino.

* **Agregar Rutas** `ip route add`

 Esto es útil para definir caminos específicos que deben tomar los paquetes de datos para ciertos destinos.

* **Eliminar Rutas** `ip route del` 

 De manera similar, puedes eliminar rutas existentes con ip route del. Esto se hace para remover caminos obsoletos o incorrectos en la tabla de ruteo.

* **Modificar Rutas**
 También se pueden modificar rutas existentes para cambiar la forma en que se maneja el tráfico de la red.

***
**La gestión de la tabla de ruteo es esencial para el correcto funcionamiento de una red, permitiendo controlar cómo y por dónde se mueven los datos. Este comando es una herramienta poderosa en el arsenal de un administrador de sistemas para manejar la conectividad de red en un sistema Linux.**
***



### Tracerouter

Es una herramienta de diagnóstico de red que muestra:

* La ruta que siguen los paquetes de datos desde un origen hasta un destino (como un sitio web).

* Proporciona información sobre cada salto en la ruta, incluyendo las direcciones IP de los routers y el tiempo que toman los paquetes en cada punto. Esto ayuda a identificar dónde pueden estar ocurriendo problemas en la red. 

* Envía paquetes con valores TTL incrementales, que disminuyen en cada salto, permitiendo rastrear la ruta.

***
**Traceroute es una herramienta estándar en la mayoría de los sistemas operativos, incluyendo Linux, macOS y Windows (aunque en Windows se llama tracert), y es ampliamente utilizada para el troubleshooting de problemas de red.**
***