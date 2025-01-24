# Lab04

## Slack02 - Demons

### Ejercicio 4.1 Explorando los procesos actuales
Se encontrará y describirá los procesos más intensos para la CPU:

1. /usr/lib/firefox-esr/firefox-esr -> Navegador Firefox-ESR, con pestañas 
abiertas. 

2. /usr/bin/gnome-shell -> Proporciona la interfaz gráfica de GNOME, 
gestionando ventanas en el escritorio.

3. /usr/lib/firefox-esr/firefox-esr-contentproc -> Proceso de contenido de Firefox-ESR, 
asociado a una pestaña o extensión del navegador.

4. /usr/libexec/packagekitd -> Servicio para gestionar instalaciones y 
actualizaciones de software en el segundo plano.

5. /usr/bin/Xwayland :0 -> Proceso que permite compatibilidad entre aplicaciones 
X11 y Wayland en el entorno gráfico.

6. /usr/lib/firefox-esr/firefox-esr-contentproc -> Otro porceso de contenido de 
Firefox-ESR, manejando actividades en el navegador.

7. /usr/lib/firefox-esr/firefox-esr-contentproc -> Otro porceso de contenido de 
Firefox-ESR , probablemente otra pestaña activa.

8. /usr/bin/gnome-software --grappication-service -> Herramienta GNOME para 
gestionar aplicaciones y actualizaciones, funcionando como un servicio en segundo 
plano.

9. /usr/lib/firefox-esr/firefox-esr-contentproc -> Otro proceso de contenido de 
Firefox-ESR, una pestaña activa.

10. /usr/lib/firefox-esr/firefox-esr-contentproc -> Proceso de contenido de 
Firefox-ESR, también relacionado con una nueva pestaña del navegador.

### Ejercicio 4.2: Explorando los Procesos de Red

**Servicio SSH:** Servicio de Secure Shell, utilizado para realizar conexiones 
 remostas seguras al sistema. Permite el acceso remoto al servidor de forma 
 cifrada.

**Servicio IPP:** Protocolo de Impresión de Internet. Este puerto está asociado con 
la gestión de impresoras en red y servicios de cola de impresión.

**Servicio IRP:** Permite la comunicación en tiempo real mediante salas de chat o 
mensajería. Este puerto podría estar abierto si hay un servidor IRC en ejecución.

**Servicio Domain:** Servicio de DNS utilizado para resolver nombres de dominio en 
direcciones IP. Si este puerto está abierto, es probable que el sistema esté 
ejecutando un servidor DNS local o un servicio relacionado.

**FTP:** Servicio de transferencia de archivos remota.
**Telnet:** Servicio de acceso remoto no seguro.

### Ejercicio 4.3: Explorando las Señales de UNIX
- SIGHUP = Se usa para reiniciar un proceso. 
- SIGNIT = Disparado por Ctrl + C (Interrupción) 
- SIGQUIT = genera un volvado de memoria (Salir). 
- SIGILL = Señal de interrupción ilegal ocurre cuando un programa 
intenta ejecutar una instrucción iválida.
- SIGTRAP = Usada por depuradores para establecer puntos de interrupción en programas.
- SIGABRT = Generada por la función abort() para terminar un programa.
- SIGBUS = Error de acceso a memoria no alineada o inexistente.
- SIGFPE = Error de punto flotante, como división por cero.
- SIGKILL = Termina el proceso de inmediato.
- SIGTERM = Pide a un proceso que termine de manera cortada.
- SIGUSR1 = Señal definida por el usuario 1.
- SIGUSR2 = Señal definida por el usuario 2.
- SIGALRM = Expiración de un temporizador.
- SIGCHLD = El proceso hijo ha terminado o se ha detenido.
- SIGSTOP = Detener el proceso.


### Ejercicio 4.4: Procesos y Redes
 
A continuación nos proponemos a configurar y probar el servicio de red FTP y Telnet 
utilizando el daemon inetd. Habrá un archivo de configuración que nos ayudará para 
hacer su uso. Creando archivos en mi sesión con localhost ftp marcando la sesión de 
bob podemos manipular el archivo desde ahi, ya sea subirlo al servidor (put), 
descargarlo(get), eliminarlo (delete), renombrarlo (rename) y lo mismo es con 
telnet, aunque sea otros comandos. Primero de todo es necesario habilitarlo.
En caso de deshabilitarlo hay que comentar el fichero de configuración.

SFTP: Es una versión segura de FTP que funciona sobre SSH.
SSH: Es un protocolo para inicio de sesión remoto seguro y ejecución de comandos.

Telnet transmite datos en texto plano, lo que representa un riesgo de seguridad ya 
que pueden se interceptado por atacantes. SSH es preferible porque cifra la 
conexión.

### Ejercicio 4.5: Opcional

Para combinar es: kill -HUP $(pidof inetd)

Se puede hacer FTP com root, pero no es una buena idea debido a los riesgos de 
seguridad. SI se permite el FTP para el usuario root, los atacantes que accedan al 
servicio FTP podrían ejecutar comandos como root. Es más seguro deshabilitar el FTP 
para el usuario root.



Desde una máquina Windows, usa un cliente FTP como FileZilla para conectarte a tu 
máquina virtual Slackware. También se podría usar un cliente Telnet para conectarte 
a la máquina virtual.

