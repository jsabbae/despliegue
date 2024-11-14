# Gestión de imágenes
A continuación se realizará una gestión de imágenes y contenedores, para ello 
necesitaremos un comando que nos de detalles técnicos de la imagen, la 
configuración de red, el punto de entrada, las variables de entorno 
predeterminadas, etc y volcar el fichero info.txt. Pero primero comprobaremos si se 
ha instalado la imagen.

- docker inspect ubuntu:20.04

Comprobamos si el contenedor modulo3 ha sido creado.

Si vamos eliminar un contenedor ** no podemos ** borrar la imagen directamente, si 
el contenedor sigue existiendo. En mi caso que esta ya detenido podemos eliminar el 
contenedo, pero al tener contenedores dependientes no se puede borrar.

