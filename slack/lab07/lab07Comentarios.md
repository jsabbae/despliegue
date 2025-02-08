# lab07

## Slack04 - PHP

### Ejercicio 7.1 - Configuración de Apache

En este laboratorio vamos hacer configuraciones básicas de Apache explicando cómo 
leer y configurar el archivo apache2.conf, que es la configuración principal del 
servidor Apache.

El símbolo # indica que todo lo que siga en esa línea no se ejecutará, sino que 
solo es un comentario de explicación.

ServerName define el nombre del servidor que Apache utiliza para identificarse a sí 
mismo en el contexto de la red. El nombre de dominio o dirección IP que se usará 
para que los usuarios accedan al servidor.

DocumentRoot indica la ubicación del sistema de archivos donde se encuentra el 
contenido web del servidor. Es el directorio principal que Apache utiliza para 
servir los archivos a los clientes que hacen solicitudes.

/etc/httpd/mod_php.conf indica a Apache que debe cargar el archivo de configuración 
adicional. Este archivo contiene las configuraciones necesarias para habilitar y 
configurar el módulo PHP en Apache.

### Ejercicio 7.2 - Ejecutando Apache
Cuando realizamos cambios en la configuración del servidor Apache, necesitamos 
reiniciarlo para que los nuevos cambios tomen efecto. Esto se debe a cómo Apache 
maneja la configuración y la ejecución de los servicios. Así que Apache no podrá 
detectar automáticamente esos cambios mientras esté en funcionamiento.

- ps-aux: Es un comando utilizado para mostrar los procesos que están ejecutándose 
en el sistema.

- grep httpd: Es un comando utilizado para buscar un patrón en la salida de texto y 
httpd es el nombre que filtra la lista de procesos para mostrar solo aquellos que 
conitiene la palabra "httpd".

- pipe ( | ): Permite tomar la salida del comando y redirige como entrada a otro 
comando.

Todo esto lista todos los procesos en ejcución y filtra solo los que están 
relacionados con httpd, mostrando información sobre Apache si está en ejecución.


Al introducir el comando se ve la línea que incluye: El nombre del usuario que 
ejecuta Apache, el ID del proceso (PID) de cada instancia de Apache. El comando que 
se está ejecutando y la cantidad de recursos (CPU y memoria) que se está 
utilizando.

### Ejercicio 7.3 - Creación de archivos HTML

En un archivo HTML de servidor Apache, gestionaremos cómo vamos a visualizarloen un 
entorno de línea de comandos.

Los archivos index.htm y index.html son los archivos predeterminados que los 
servidores web buscan al cargar un directorio. Si un usuario accede 
http://127.0.0.1/, el servidor buscará automáticamente index.html o index.htm y lo 
mostrará sin necesidad de escribir el nombre del archivo en la URL.

Estos son los permisos y propiedad de mi archivo haciendo ls -l index.html.

La configuración de Apache en el archivo httpd.conf especifica el orden de 
prioridad de estos archivos mediante DirectoryIndex.

Teniendo instalado lynx visualizará la página desde la línea de comandos, dado que 
no se tiene una interfaz gráfica en Slackware.

### Ejercicio 7.4 - Visualización de archivos HTML en la interfaz de la terminal

- **CLI(Command-Line-Interface):** es una interfaz basada en texto donde los 
usuarios escriben comandos para interactuar con el sistema. Por ejemplo: la 
terminal de Linux, PowerShell.

- **GUI(Graphical User Interface):** es una interfaz gráfica que usa botones, 
iconos y ventanas para la interacción, por lo que permite a los usuarios 
comunicarse con el ordenador. EL funcionamiento de la Interfaz Gráfica hace parte 
de la arquitectura de software modelo-vista-controlador(MVC), el cual separa el 
procesamiento de los datos de la forma en la que estos son mostrados al usuario. 
Por ejemplo: Windows, macOS, escritorios de Linux como GNOME o KDE.

Los administradores que gestionan miles de sistemas o configuraciones de usuario 
encontrarán una GUI mucho menos eficiente que una CLI. Pero un simple comando CLI 
puede ajustar fácilmente las configuraciones para un gran grupo de sistemas a la 
vez.

**¿Qué tiene de especial la IP 127.0.0.1?** Es la dirección de loopback o 
localhost, lo que significa que apunta siempre a la propia máquina y permite probar 
servicios como Apache sin necesisdad de una red externa.

### Ejercicio 7.5 - Creación y visualización de archivos PHP en la terminal

En un archivo nse.php lo cargaremos en lynx. Visualizando las configuraciones de 
PHP en el servidor y acceder al archivo a través de un navegador en línea de 
comandos lynx.
Instalando paquetes verifico si todo ha ido bien.

### Ejercicio 7.6 - Exploración y modificación del archivo host

En el archivo /etc/hosts voy asignar nombre de dominio a direcciones IP locales, 
permitiendo que el sistema reconozca un nombre personalizado sin depender de un 
servidor DNS.

### Ejercicio 7.7 (Opcional)

Nos dedicaremos a crear y probar un archivo PHP en el servidor web implementando la 
autentificación de usuario y contraseña en Apache.

El archivo se cargará dependiendo de la configuración de DirectoryIndex en la 
configuración de Apache. Por defecto, Apache prioriza index.html sobre index.ph. 
Esto significa que si tanto index.html como index.php existen en el mismo 
directorio, index.html será el que se cargue primero.


