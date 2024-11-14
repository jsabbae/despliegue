##Bind Mounts

bind mount es una técnica que permite a un directorio o archivo este disponible
dentro de un contenedor. A diferencia de los volúmenes, los bind mounts se refieren
a directorios específicos en el sistema,así que por primera parte bind mounts va
hacer persistencia al archivo index.html en la imagen que se utilizado en la
anterior actividad.

Una vez arrancados los dos contenedores se podran acceder en el buscador del
navegador web:

- http://localhost:8181
- http://localhost:8282

Se deberá de ver el mismo saludo, ya que los dos contenedores están usando el mismo
archivo index.html desde el mismo bind mount.
