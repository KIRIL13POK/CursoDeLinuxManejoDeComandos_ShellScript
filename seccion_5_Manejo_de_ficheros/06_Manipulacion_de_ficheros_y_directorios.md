Para esta clase con comandosque ya conocemos en la terminal vamos a crear 3 ficheros txt y una carpeta "ficheroPadre" nuevos:

![tres ficheros](/img/506_tres-ficheros-padre.png)

`cp`

Se utiliza para copiar ficheros y directorios. Puedes copiar un fichero a otro destino especificando el nombre del fichero de origen y el nombre del fichero de destino.

`cp fichero-1.txt fichero1-1.txt`

Este comando realiza una copia del archivo fichero-1.txt y la almacena en un nuevo archivo llamado fichero1-1.txt si este último no existe. Si el archivo fichero1-1.txt ya existiera, el contenido de fichero-1.txt se sobrescribiría en fichero1-1.txt.

![cp f1](/img/505_cp-f1.png)

Ten en cuenta que si el fichero de destino ya existe, se sobrescribirá sin preguntar.

![cp f2](/img/506_cp-f2.png)

### `cp -i `

Se utiliza para copiar archivos con la opción interactiva. Cuando se copian archivos con esta opción, el comando cp preguntará al usuario si desea sobrescribir un archivo de destino si ya existe un archivo con el mismo nombre.


Para copiar los archivos fichero-1.txt, fichero-2.txt, y fichero-3.txt al directorio ficheroPadre, puedes utilizar el comando `cp` de la siguiente manera:

`cp fichero-1.txt fichero-2.txt fichero-3.txt ficheroPadre`

Este comando copiará los tres archivos (fichero-1.txt, fichero-2.txt, y fichero-3.txt) al directorio ficheroPadre. Asegúrate de que el directorio ficheroPadre exista en la ubicación actual o proporciona la ruta completa al directorio si está en una ubicación diferente.

![padre](/img/506_cp-ficheroPadre.png)

###  Copiar directorios y su contenido:

El comando `cp ficheroPadre ficheroCopiaDePadre` no funcionará para copiar un directorio completo si ficheroCopiaDePadre no existe. Para copiar un directorio completo y su contenido a un directorio de destino que aún no existe, debes usar la opción ` -r` (o -R) junto con el comando cp.

`cp -r ficheroPadre ficheroCopiaDePadre`

![copiaPadre](/img/506-copi-ficeroPadre.png)