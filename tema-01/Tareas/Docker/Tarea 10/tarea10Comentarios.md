#DOCKERFILE

Se ira realizando dos partes en esta actividad:

- Primera Parte: Consiste en crear una imagen personalizada basada en ubuntu:20.04 
con algunas herramientas instaladas y un usuario creado, así que para empezar se 
inicia el contenedor interactivo. Dentro del contenedor crearemos un usuario 
llamado usuario con una contraseña que será usuario. Una vez craedo el usuario, nos 
salimos del contenedor y creamos la imagen personalizada, para ello necesitamos el 
id del contenedor. El último apartado de esta parte es la subida de imagen al 
*DockerHub*, antes tendremos que iniciar sesión en la consola subir la imagen.


- Segunda Parte: Tenemos que crear un archivo *DockerFile* que define cómo 
construir una nueva imagen basada en php:7.4-apache, esto se hace navegando al 
archivo con un comando cd. Creo la carpeta y teniendo el archivo Dockerfile se 
movera a esa carpeta, todo esto para que se visualice correctamente el resultado y 
a continuación subir la imagen. Importante tener el fichero Dockerfiles con las 
ordenes necesarias, en esas ordenes escribimos el siguiente contenido de usar la 
imagen base, instalar nano y git , por último crear archivos index.html y info.php.


Terminando las dos partes quedaría probar las imágenes y abrir en el navegador y 
buscar:

**http://localhost:8080**
**http://localhost:8080/info.php**

