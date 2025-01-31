# lab06

## Slack03-Email

### Ejercicio 6.1
Para comenzar enviaremos correos electrónicos locales usando el comando email con 
el paquete que tengo ya instalado mailutils. Realizando copias manualmente enviando 
el mismo mensaje a múltiples destinatarios y asin recibirán el correo.

## Ejercicio 6.2 
El funcionamiento del sistema de correo de este ejercicio se procesan, envían, 
reciben y almacenan los correos electrónicos en un sistema operativo basado en Linux. 
Con mail lista los correos, dentro de mail hay realizaciones básicas como: 
- h muestra la lista de correso en bandeja.
- d borra el correo actual.
- q sale del cliente del correo guardando los cambios .
- ? Una ayuda para saber los comandos disponibles del mail.

Sendmail revisará la cola de correos si aún no han sido entregados.

### Ejercicio 6.3
Con el comando mail sabiendo lo que tenemos en el almacenamiento de correos, el uso 
de telnet va interactuar con servidores SMTP y POP3, y los puertos asociados a 
estos protocolos. Principalmente se hará un una consola (cmd) Windows con la 
siguiente captura enviada en el repositorio o en la actividad, antes de todo hay 
que editar el /etc/inetd.conf y saber que ip utilizaremos.
Con SMTP su puerto es 25 y POP3 110

## Ejercicio 6.4
**IMAP** (Internet Mail Access Protocol) es un protocolo de correo electrónico que 
permite acceder a los mensajes desde cualquier dispositivo sin necesidad de 
descargarlo localmente. Funciona como una conexión directa con el servidor de 
correo manteniendo todos los mensajes en el servidor mientras permite su acceso y 
gestión desde múltiples dispositivos.

Este protocolo no envía correos, lo que hace realmente es dar acceso a los mensajes 
que hay almacenados en ese servidor. También IMAP mantiene los correos en el 
servidor, permite acceso sincronizado entre dispositivos, requiere conexión 
constante para acceso completo y permite búsqueda en el servidor. A diferencia con 
POP3 se caracteriza por descargar correos al dispositivo y poder eliminarlo del 
servidor, esta limitado a un dispositivo salvo que se configuren copias en el 
servicio, gestión limitadas en carpetas, el estado se mantiene solo en el 
dispositivo local, permite acceso offline después de la descarga, limitados a 
correos descargados.

**PGP**(Pretty Good Privacy) es un sistema de cifrado que utiliza criptografía 
asimétrica para proteger mensajes electrónicos. Funciona mediante un sistema de 
pares de clave:

Una clave pública puede compartir con cualquier persona que quiera enviarle 
mensajes o archivos cifrados, pero la clave privada sólo debe conocer, para poder 
descifrar los mensajes recibidos.
 
