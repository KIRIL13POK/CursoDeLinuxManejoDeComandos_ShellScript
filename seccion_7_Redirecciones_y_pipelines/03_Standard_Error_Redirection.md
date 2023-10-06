# Los file descriptors (descriptores de fichero)

Son números utilizados para identificar y acceder a ficheros y recursos en sistemas Unix y sistemas basados en Unix, como Linux. Constituyen una parte fundamental del manejo de ficheros y recursos en estos sistemas operativos.

Puntos clave sobre los file descriptors:

1. **Numeración**: Los file descriptors son números enteros no negativos. Por convención, se asignan ciertos valores estándar:

![012](/img/703-012.png)

* Descriptor de fichero 0 (stdin): Se utiliza para la entrada estándar.
* Descriptor de fichero 1 (stdout): Se utiliza para la salida estándar.
* Descriptor de fichero 2 (stderr): Se utiliza para el estándar error.

2. **Tabla global**: El kernel mantiene una tabla global de file descriptors que contiene información sobre los recursos abiertos por un proceso, como la posición de lectura/escritura actual y restricciones de acceso.

3. **Operaciones de lectura y escritura**: Los programas utilizan file descriptors para llevar a cabo operaciones de lectura y escritura en recursos, como ficheros. Por ejemplo, para leer de un archivo, un programa utiliza el file descriptor correspondiente.

4. **Redirección**: Los file descriptors se emplean para redirigir la entrada y salida de programas en la línea de comandos. Esto permite, por ejemplo, redirigir la salida estándar de un programa hacia un archivo utilizando un file descriptor.

En relación a la redirección del estándar error (stderr), el estándar error se asocia al file descriptor número 2. Cuando se realiza la redirección del estándar error en la línea de comandos, se está utilizando la capacidad de redirección de file descriptors, empleando el operador **2> o 2>>** para indicar que se desea redirigir el descriptor de fichero número 2 (stderr). Esto permite que los mensajes de error generados por un comando se dirijan a un archivo o a otro destino específico.

### Estándar error (stderr)

Puedes redirigir el estándar error (stderr) de un comando a un archivo utilizando el operador de redirección **2>** de la siguiente manera:

Por ejemplo:

```shell
comando_incorrecto 2> errores.txt
```
![redireccion err](/img/703-redireccion-err.png)


Esto tomará la salida de error generada por el comando y la redirigirá al archivo especificado (en este caso, "errores.txt").

Si deseas agregar la salida de error al final de un archivo sin sobrescribirlo, puedes utilizar el operador de redirección 2>>:

```shell
otro_comando_incorrecto 2>> errores.txt
```
![redireccion err](/img/703-redirecion-err-cat.png)

Esto agregará la salida de error al final del archivo existente, sin eliminar el contenido previo en "errores.txt".