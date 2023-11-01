En Linux, los archivos y directorios tienen propietarios y grupos propietarios que determinan quién puede acceder a ellos.

1. Puedes usar el comando `chown` para cambiar el propietario de un archivo o directorio. 

  ### `sudo chown pokrovskiy fichero-prueba.txt `

  ![sudo chown ](/img/813-sudo-chown1.png)

  Cuando ejecutas el comando, estás cambiando el propietario del archivo **fichero-prueba.txt** al usuario **pokrovskiy**. Este usuario tendrá control total sobre el archivo y podrá realizar operaciones como modificarlo, cambiar sus permisos, o eliminarlo.
  
  ### `sudo chown :pokrovskiy fichero-prueba.txt`

  ![sudo chown ](/img/813-sudo-chown2.png)

  Al ejecutar el comando, estás asignando el grupo **pokrovskiy** como el grupo propietario del archivo **fichero-prueba.txt**. El propietario del usuario del archivo no se modifica; solo el grupo propietario se cambia a **pokrovskiy**.

  El archivo tenga restricciones de permisos que impiden que el usuario actual acceda a su contenido

  ![cat](/img/813-cambiodetodo.png)

  Si deseas cambiar tanto el propietario como el grupo propietario al mismo tiempo: 

  ### `sudo chown kiril:kiril fichero-prueba.txt`

  ![sudo chown ](/img/813-sudo-chown3.png)

   Cambia tanto el propietario del usuario como el grupo propietario del archivo fichero-prueba.txt al usuario y grupo llamados kiril


  

2. El comando `chgrp` también puede cambiar el grupo propietario de un archivo o directorio.

El comando chown también puede cambiar el grupo propietario si lo especificas como nuevo_propietario:nuevo_grupo.

Los permisos de lectura y escritura están relacionados con el propietario y el grupo propietario, por lo que cambiarlos puede afectar quién puede acceder a un archivo o directorio.

