En esta tarea se dedicará en ejecutar ** varios servicios ** y ** bases de datos ** 
en contenedores, por ello este proceso configura un entorno básico con un servidor 
web(Apache) y una base de datos(MariaDB). Necesitaremos la instancia de la imagen 
php:7.3apache instalada en la tarea anterior, una vez que ya esta corriendo se 
realizará una creación de archivo llamado index.html y servirá como la página de 
inicio de un servidor web introduciendo mi nombre y mis apellidos en modo 
encabezado.

Al crear el fichero tenemos que apuntar la ruta local para hacer la copia a la 
máquina local que se había creado al directorio raiz del servidor web. Todo esto 
también con index.php y ejecutamos el contenedor con los sgientes requisitos.

Para verificar el resultado podemos verlo por:

-- http://localhost:8181

-- http://localhost:8181/index.php
-- http://localhost:8181/index.html
