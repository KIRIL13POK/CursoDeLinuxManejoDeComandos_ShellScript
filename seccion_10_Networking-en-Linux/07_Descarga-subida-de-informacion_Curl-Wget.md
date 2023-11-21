#  Descarga y subida de información: Curl y Wget

### Curl

 No viene instalado por defecto en Ubuntu `sudo apt install curl`. 

 ![man curl](/img/1007-man-curl.png)
 
 Curl es una herramienta versátil para transferir datos, siendo útil para descargar páginas web, archivos servidos en la web, y para hacer peticiones de subida de información como HTTP post o uploads de FTP. Soporta varios protocolos de red populares y es especialmente útil para desarrolladores y técnicos que necesitan interactuar con APIs, permitiendo modificar cabeceras y argumentos de las peticiones. 

***
### Ejemplo de descarga de HTML :

1. 

![redirecion](/img/1007-winrar-html.png)

2. 
 
![firefox](/Img/1007.firefox-winrar-html.png)


Se muestra cómo utilizar Curl para descargar el código HTML de una página web (ejemplo de WinRAR), cómo redirigir esta salida a un archivo HTML.
****




Dentro de sus numerosas opciones, las banderas -O y -o se utilizan para descargar archivos y guardarlos localmente, pero con diferencias específicas en su comportamiento:

* ### `curl -O`

    La bandera -O (mayúscula) le dice a curl que descargue el archivo desde la URL especificada y que guarde el archivo en tu sistema local con el mismo nombre que tiene en el servidor.
  
     
* ### `curl -o`

    La bandera -o (minúscula), seguida de un nombre de archivo, le indica a curl que descargue el archivo y lo guarde con un nombre específico que tú determinas.
        
![curl -O -o](/img/1007-curl-O-o.png)       

Ambas opciones son muy útiles y te permiten tener un mayor control sobre cómo se guardan los archivos descargados en tu sistema. La elección entre una u otra dependerá de si deseas mantener el nombre original del archivo o asignarle un nombre específico al momento de la descarga.


### Wget

![man wget](/img/1007-man-wget.png)

Es más recomendado para la descarga de archivos de forma no interactiva. Wget puede manejar descargas grandes, permitiendo operar en segundo plano y guardar el progreso en un archivo log. A diferencia de Curl, Wget es más eficiente para la descarga de páginas web completas y archivos más grandes. Wget también permite descargar múltiples archivos desde un archivo de texto con URLs y cambiar el nombre de los archivos descargados.

### `wget -i archivo-URL.txt`

Este comando se utiliza para descargar archivos desde una lista de URLs que se encuentra en un archivo de texto llamado **archivo-URL.txt**. La opción **-i** se utiliza para especificar el archivo que contiene las URLs que wget debe descargar. El comando leerá las URLs del archivo y procederá a descargar los archivos correspondientes desde esas direcciones web.

***
**Curl es más útil para consultas a APIs, subir información y descargar datos de manera automatizada, mientras que Wget es superior para descargas más completas y eficientes de páginas web o archivos grandes.** 
***