# Operador Redirección > / >>

En Linux, puedes redirigir la salida estándar (stdout) de un comando a un archivo utilizando el operador de redirección >. 

Por ejemplo:

```shel
ls -lah > lista_cursoLinux.txt
```

Esto tomará la salida del comando y la redirigirá al archivo especificado.

![operador Redireccion](/img/702-operador-redireccion.png)

**(1)** Si el archivo no existe, se creará; 

Si ya existe, su contenido se sobrescribirá.

Si deseas concatenar la salida de varios comandos al final de un archivo sin sobrescribirlo, puedes utilizar el operador de redirección >>. 

Por ejemplo:

```shel
ls -lah >> lista_cursoLinux.txt
```

Esto agregará la salida al final del archivo existente, sin eliminar el contenido previo.

***
**Es importante destacar que estos operadores (> y >>) se utilizan para redirigir la salida estándar, y los errores generados por un comando se envían al estándar error (stderr). Para redirigir los errores, se utiliza un operador separado que se verá en secciones posteriores.**
***

