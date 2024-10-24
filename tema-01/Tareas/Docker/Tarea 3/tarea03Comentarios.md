En la sigiente tarea arrancaremos el contenedor y se realizará tres acciones. Se 
utilizará un contenedor con el mismo nombre basado en la imagen de Ubuntu 18.04. Lo 
primero será arrancarlo y salir con un exit, como ya he creado un contenedor antes 
voy a proceder a eliminarlo y volver arrancarlo.

Una vez que estamos en el contenedo, nos salimos y comprobamos si se ha parado con 
docker ps -a.

La segunda acción es rearrancar el contenedor con docker start ubunto reinicia 
el contenedor y luego se comprueba su estado.

Por último docker exec ubuntu car 'ruta del fichero', mustra el fichero sin 
entrar en el contenedor.
