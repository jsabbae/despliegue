## Instalación bind9
En esta actividad procederemos a usar unos de los servidores de DNS más utilizados 
en sistema operativo Linux. Su función se encargará de dar resolución de nombres de 
dominio, para ello necesitamos su instalación que en mi caso ya está realizada.

## Configuración bind9
Necesitamos configurar el archivo de configuración de bind9 para manejar sus 
consultas DNS y reenviar las que nos se puede resolver. Para editar el ficherode 
configuración voy a iniciar una nueva sesión como si fuera un inicio de sesión 
completo.

El dominio será ejemplo.com y se especifica los archivos donde se encuentran las 
configuraciones de las zonas para que bind9 sepa cómo realizar las resoluciones 
DNS. También se añade la zona directa(resuelve ejemplo.com en direcciones IP) e 
inversa(resuelve direcciones IP en ejemplo.com).

Al crear un nuevo fichero y copiar todo lo creado de db.local 
/etc/bind/zones/ejemplo.com.zone, veremos el resultado y todos los localhost serán 
sustituidos por el dominio.

En el archivo de configuración tendrá de nombre de dominio ejemplo.com y al 
realizar los siguientes tres comandos. Comprobamos que el servidor DNS está 
funcionando correctamente y resolviendo el dominio a la dirección IP.

##  Comprobaciones de comandos nslookup, dig, dig -x

Introduciendo el dig ejemplo.com podemos visualizar un registro que es A, el cual 
asocia el dominio de la dirección IPv4. Si nos referimos al tipo de registro AAA la 
dirección será IPv6.

Su valor puede variar dependiendo del dominio consultado y su configuración DNS y 
indica las direcciones IP.

No tiene registro NS, pero si lo tuviera sería un recurso de DNS que identifica un 
servidor de nombre responsable de la resolución de consultas para un nombre host
concreto y permiten configurar subdominios individuales.
