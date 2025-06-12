SISTEMA DE RESPALDO AUTOMATICO A GOOGLE DRIVE CON BASH
----------------------------------------------------
La seguridad de la informacion es fundamental, tanto para los usuarios como para las empresas.
La perdida de los archivos importantes debido a fallos en el sistema, errores humanos
o ataques informaticos puede tener consecuencias graves. Por esto, contar con un sistema 
de respaldo automatizado es escencial.
----------------------------------------------------
Por lo cual se elaboro un laboratorio en el cual se enseñara paso a paso sobre como aplicar este metodo.

Paso 1: Instalacion de las dependencias.

Se comienza con la instalación de rclone, una herramienta de línea de comandos utilizada para gestionar archivos en servicios de almacenamiento en la nube, como Google Drive.

![instalacion de dependencias](https://github.com/user-attachments/assets/5161c9c8-e712-4393-b031-bc472122fb4f)

----------------------------------------------------
Paso 2: Configuracion de rclone.

La configuracion de rclone nos permite establecer una conexion entre un sistema y un servicio en la nube. 

![2 configuracion de rclone](https://github.com/user-attachments/assets/555a0f3c-8b61-4827-8058-a632613e6a36)

----------------------------------------------------
Paso 3:Seleccion de el servicio en la nube.

Siguiendo con la configuracion de rclone aqui podemos seleccionar el servicio preferido por el usuario. En este caso se seleccionara la opcion 13 (Google Drive) y se nos proporciona un ID de cliente y clave secreta.

![3 seleccion de google drive y acceso full](https://github.com/user-attachments/assets/c10ab11b-d2ae-4c09-a5f6-40b7569e6484)

----------------------------------------------------
Paso 4: seleccion de configuracion avanzada 

Para finalizar la configuracion se utilizo la opcion de auto-configuracion para autorizar el acceso a traves de OAuth2. En donde rclone logro generar un enlace para que el usuario inicie sesion en su cuenta. Una vez que se autorizo el inicio de sesion, rclone completo la configuracion. 

![4 seleccion de configuracion avanzada - auto configuracion y redireccionamiento de acceso a google](https://github.com/user-attachments/assets/0b35b6e2-ec13-4f29-8a53-c870f0cf52fc)

----------------------------------------------------
