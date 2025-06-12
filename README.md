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

La configuración de Rclone permite establecer una conexión entre el sistema local y un servicio de almacenamiento en la nube, facilitando así la sincronización, copia y gestión de archivos de forma segura y eficiente.

![2 configuracion de rclone](https://github.com/user-attachments/assets/555a0f3c-8b61-4827-8058-a632613e6a36)

----------------------------------------------------
Paso 3:Seleccion de el servicio en la nube.

Durante la configuración de Rclone, se presenta una lista de servicios en la nube para que el usuario seleccione su opción preferida. En este caso, se elige la opción 13, correspondiente a Google Drive. A continuación, se solicita ingresar un ID de cliente y una clave secreta, los cuales son necesarios para autenticar y autorizar el acceso a la cuenta de Google Drive.

![3 seleccion de google drive y acceso full](https://github.com/user-attachments/assets/c10ab11b-d2ae-4c09-a5f6-40b7569e6484)

----------------------------------------------------
Paso 4: seleccion de configuracion avanzada.

Para finalizar la configuración, se utilizó la opción de auto-configuración para autorizar el acceso mediante el protocolo OAuth2. En este proceso, Rclone generó un enlace que permitió al usuario iniciar sesión en su cuenta de Google Drive. Una vez autorizado el acceso, Rclone completó automáticamente la configuración, estableciendo la conexión entre el sistema local y el servicio en la nube.

![4 seleccion de configuracion avanzada - auto configuracion y redireccionamiento de acceso a google](https://github.com/user-attachments/assets/0b35b6e2-ec13-4f29-8a53-c870f0cf52fc)

![5  Es un bloque de configuración que le dice a rclone cómo conectarse a tu cuenta de Google Drive](https://github.com/user-attachments/assets/14f055d9-7b09-4b18-91a8-8f5721b36cbf)

----------------------------------------------------
Paso 5: Comprobacion de la exitosa configuracion.

Aqui podemos ver que ya se verifico la configuracion de rclone, en donde se confirma la conexion con Google Drive fue creada correctamente.

![6](https://github.com/user-attachments/assets/c26a80ee-488f-4368-9272-b36f79394a51)

----------------------------------------------------
Paso 6: Crear el script de respaldo.

Una vez rclone este configurado correctamente se deberan dirigir a el archivo que se creo para el backup.

![7 crear el script de respaldo ](https://github.com/user-attachments/assets/ccc88165-1535-492a-a2a3-464b6f6725e7)

Una vez dentro del archivo se pondra el siguiente script el cual sera el encargara de generar el backup en Google Drive.

[gdrive]
Nombre que le diste al “remote” o conexión. Puedes usarlo para referirte a esta configuración en comandos.

type = drive
Indica que el tipo de almacenamiento es Google Drive.

client_id = TU_CLIENT_ID
Es el identificador único de tu aplicación en Google Cloud Console. Rclone lo usa para autenticar tu app.

client_secret = TU_CLIENT_SECRET
La contraseña secreta de tu app. Junto con el client_id, sirve para acceder a Google Drive.

scope = drive
Indica los permisos que le das a rclone. “drive” significa acceso completo a Google Drive.

token = {...}
Es un objeto JSON que contiene el “access_token” y “refresh_token”. Estos tokens permiten que rclone acceda a tu cuenta sin pedir usuario y contraseña cada vez.

![7 5](https://github.com/user-attachments/assets/e1306481-8a6c-49f7-b99d-e92bcbbbac92)

----------------------------------------------------
Paso 7: Otorgar los permisos para ejecutar el script.

Se le asignaran permisos de ejecucion mediante chmod +x, permitiendo que el script pueda ser ejecutado directamente desde la terminal. 

![8 dar permisos para ejecutar script](https://github.com/user-attachments/assets/38585b9e-7950-4237-95b3-00bdf5bfa089)

----------------------------------------------------
Paso 8: Comprobar funcionamiento.

Una vez otorgado los permisos se ejecutara el script manualmente para lograr verificar su funcionamiento, en el cual se mostrara un mensaje de confirmacion "Backup realizado y subido a Google Drive", lo cual nos confirmaria que el proceso se completo con exito.

![9 prueba manual de el script](https://github.com/user-attachments/assets/979659f5-508b-4007-aaa8-2a0cf22965dc)

----------------------------------------------------
Paso 9: Configuracion de cron para la ejecucion automatica del script.

Se configurara el proceso de ejecucion automatica del script para que este haciendo el backup automaticamente a las 2:00 AM todos los dias.

![10 programar que el script se ejecute a las 2 am](https://github.com/user-attachments/assets/7e81880a-8ac5-4520-b916-7758e3f9a1ed)

![10 5    ](https://github.com/user-attachments/assets/e3214375-8688-4fd8-b160-29a2b7d1ef26)

----------------------------------------------------
Paso 10: Comprobacion desde Google Drive.

Finalizando se comprobara directamente metiendonos a Google Drive en donde se reflejaran los backup ya realizaados y con exito.

![11](https://github.com/user-attachments/assets/c4a5d56d-806c-4814-b098-3b8a971736a4)

![12](https://github.com/user-attachments/assets/786c8cdd-caf1-4f9a-b270-340b23c1ee79)

----------------------------------------------------

## Equipo del Proyecto

- **Diego Calderon** 
- **Ricardo Duarte**
- **Raul Vergara** 
