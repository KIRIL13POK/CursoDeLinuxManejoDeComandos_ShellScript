![sudo img](https://media.threatpost.com/wp-content/uploads/sites/103/2019/10/15115000/sudo-e1571154617286.jpg)

El comando **sudo** en Linux es una herramienta que permite a los usuarios ejecutar comandos con privilegios de otro usuario, generalmente el usuario **root**. Aquí tienes un resumen de las principales características y diferencias con respecto a **su**:

1. **sudo** permite a un usuario ejecutar comandos como si fuera otro usuario, generalmente **root**.

2. La contraseña que se solicita al usar **sudo** es la del usuario actual, no la del usuario **root**. Esto mejora la seguridad al evitar que los usuarios con pocos privilegios conozcan la contraseña de **root**.

3. No proporciona una shell interactiva, a diferencia de **su**. En lugar de cambiar completamente de usuario y proporcionar una nueva interfaz de línea de comandos, **sudo** ejecuta comandos de manera puntual.

4. La configuración de **sudo** se encuentra en el archivo **/etc/sudoers**, donde se especifican los privilegios elevados, los comandos permitidos y los usuarios que pueden utilizar **sudo**. Es importante configurar **sudo** de manera adecuada para garantizar la seguridad del sistema.

5. **sudo** se utiliza comúnmente para asumir los privilegios de **root**, pero también se puede configurar para permitir que los usuarios asuman los privilegios de otros usuarios.

6. Si se ejecuta **sudo** seguido de un comando, este comando se ejecutará en nombre del usuario especificado en la configuración de **sudo**.

7. Se puede obtener una sesión interactiva con `sudo -i `, lo que permite ejecutar múltiples comandos con privilegios elevados en una secuencia interactiva. Sin embargo, esto no es recomendable para usuarios que no sean administradores del sistema.

![sudo -i](/img/810-root-i.png)

***
**En resumen, **sudo** es una herramienta esencial en entornos Linux para permitir a los usuarios realizar tareas administrativas sin necesidad de conocer la contraseña de **root** y sin proporcionarles una shell interactiva de **root**. Esto mejora la seguridad y el control del sistema.**
***