##Volúmenes
LOs contenedores por defecto son **volátiles**, lo que significa que todos los 
datos almacenados dentro de ellos se perderán cuando el contenedor se detenga o se 
elimine. Para evitar esto existe volúmenes que son áreas de almacenamiento 
gestionadas que pueden ser compartidas entre contenedores.

La realización de esta actividad será crear dos volúmenes y dos contenedores y 
aplicarles el volumen asignado.

Si el volumen tiene contenedores activos o se encuentra en uso, docker no permitirá 
borrarlo hasta que los contenedores sean eliminados.
