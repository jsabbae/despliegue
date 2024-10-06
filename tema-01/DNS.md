# Despliegue

## DNS

### Resolución

La mayoría de los hosts de una red (interna o externa) tiene una dirección IP única y un nombre de host.
Los nombres host comprenden el dominio local o subdominio del host, su nombre de dominio del host, su nombre de dominio
principal y su extensión de dominio (por ejemplo, .com, .org, .net). Juntos estos segmentos proporcionan a los 
hosts una identidad accesible con la que los clientes pueden interactuar.

### Nombre de Dominio

Es una cadena de texto que se asigna a una dirección IP numérica, que se utiliza para acceder a un sitio web desde 
el software cliente. Suelen estar divididos en dos o tres partes, cada uno de ellas separada por un punto. Cuando
se leen de derecha a izquierda, los identificadores de los nombres de dominio van de lo general a lo más específico. 
La sección a la  derecha del último punto de un nombre de dominio es el dominio de nivel superior (TLD), entre ellos, 
se encuentran los TLD "genéricos" como ".com", ".net" y ".org".

### Niveles de dominio

El DNS funciona de forma jerárquica y por niveles. Estos niveles se pueden ver como partes de una dirección de Interenet.

1. **Dominio de nivel superior (TLD-Top-Level Domain).**
Es la más alta categoria de los FQDN que es traducida a direcciones IP por los DNS oficiales de Internet. Los nombres 
de servidores por los DNS oficiales de Internet. Los nombres servidos por los DNS oficiales son administrativos por 
Internet Corporation for Assigned Names and Numbers (ICANN). Alternativamente a los DNS oficiales, hay una serie de 
servidores de DNS alternativos, como es OpenNIC. Existen 3 tipos:

- *Genéricos*: por ejemplo, .com, .org, .net, .info, etc.
- *Geográficos o de código de país (ccTLDs)*: por ejemplo, .es (España), .mx (México), .ar (Argentina).
- *TLDs patrocinados*: creados para comunidades o industrias específicas, como .edu (educación), .gov(gobierno), .mil(militar).

2. **Dominio de segundo nivel (SLD-Second-Level Domain).**
Es el nombre de la marca, organización u empresa dueña del sitio web en cuestión.
Por ejemplo, en nuestro dominio: espacio.net.mx. La palabra, "espacios", sería SLD.

3. **Dominio de tercer nivel o subdominio.**
Estos tipos de dominio genérico (gTLD), con un dominio específico del país (ccTLD).
Por lo que la terminación ".com.mx", hace referencia a este tipo de dominio, ya que es genérico, pero a su vez específico 
para usuarios de México. 

4. **Dominio Raiz (Root Domain).**
El dominio raíz es la base de la jerarquia del DNS, que operan en la zona raíz. Estos servidores pueden responder 
directamente a las consultas de los registros almacenados en caché en la zona raíz, y también pueden remitir otras
solicitudes al servidor de dominio de nivel superior (TLD) apropiado.
Los servidores raíz son parte fundamental de la infraestructura de Internet; sin estos no funcionarian ni los 
navegadores web ni los navegadores web ni muchas otras herramientas de Internet. Hay 13 direcciones IP diferentes 
que siven a la zona raíz de DNS, y existen cientos de servidores raíz redundantes en todo el mundo para gestionar 
las solicitudes a la zona raíz.

### Zonas de búsqueda
Una zona DNS es una parte del espacio de nombres DNS que está gestionada por una organización específica o un
administrador. Permite más control granular de los componentes DNS como los servidores de nombre autoritario.
Las zonas de búsqueda directa facilitan  la traducción de nombres de dominio a direcciones IP, lo que permite 
a los usuarios acceder a recursos en Internet, mientras que las zonas de búsqueda inversa asignan direcciones 
IP a nombres de dominio para tareas como diagnóstico de red y verificación de seguridad. 


###  Tipos de servidores

1. **Servidor recursivo.**
Encuentra respuestas DNS mediante la consulta de otros servidores.
2. **Servidor raíz.**
Primer nivel en la jerarquía DNS; dirige las consultas a servidores TLD.
3. **Servidor TLD.**
Administra dominios de nivel superior (TLD) como .com, .org, etc.
4. **Servidor autoritario.**
Tiene la información final sobre los registros de un dominio específico.
5. **Servidor de caché.**
Almacena temporalmente la respuesta DNS para mejorar el rendimiento.
6. **Servidor de reenvío.**
Envía las consultas DNS a otros servidores recursivos.
7. **Servidor DNS inverso.**
Traduce direcciones IP a nombres de dominio.

### Registros

Los registros DNS son instrucciones radicadas en servidores DNS autoritativosque proporcionan información 
sobre un dominio, como la dirección IP asociada con este y cómo gestionar solicitudes dirigidas a dicho dominio.
Estos registros contienen en una serie de archivos de textos en lo que se conoce como sintaxis DNS. La sintaxis
DNS es simplemente una cadena de caracteres utilizados como comandos que dicen al servidor DNS qué hacer.
Estos son los tipos de registros que existen:
1. **Registro A.** 
 Registro que contiene la dirección IP de un dominio.
2. **Registro AAAA.**
El registro que contiene la dirección IPv6 de un dominio (a diferencia de los registros A, que enumeran 
la dirección IPv4).
3. **Registro CNAME.**
Reenvia un dominio o subdominio a otro dominio, NO proporciona una dirección IP.  
4. **Registro MX.**
Dirige el correo a un servidor de correo electrónico. 
5. **Registro TXT.**
Permite que un administrador pueda almacenar notas de texto en el registro. Estos registros se suelen 
utilizar para la seguridad del correo electrónico.
6. **Registro NS.**
Almacena el servidor de nombre para una entrada DNS.
7. **Registro SOA.**
Almacena la información del administrador sobre un dominino
8. **Registro SRV.**
Especifica un puerto para servicios específicos 
9. **Registro PTR.**
Proporciona un nombre de dominio en búsqueda inversas.


### Funcionamiento

El uso de uno u otro depende del tipo de consulta, y de los roles de los diferentes servidores DNS
en el proceso de resolució

**_Consulta recursiva_**

Una consulta recursiva es cuando un servidor DNS se comunica con otros servidores DNS para buscar una
dirección IP y devolverla al cliente. 
Un programa se llama a sí mismo repetidamente hasta que se cumple una condición, mientras que en la 
iteración se repite un conjunto de intrucciones hasta que se cumple una condición. Esta diferencia es
difícil de ilustrar sin ver código, pero la clave es que la recursión es una solución que se llama a 
sí mismo de forma repetida.  


**_Consulta iterativa_**

El cliente se comunica directamente con cada servidor DNS implicado en la búsqueda.
Cada consulta DNS responde directamente al cliente con una dirección para que otro 
servidor DNS pregunte, y el cliente sigue consultando a los servidores DNS hasta que
uno de ellos responda con la dirección IP correcta para el dominio dado.