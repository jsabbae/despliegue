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

El DNS funciona de forma jerárquica y por niveles. Estos niveles se pueden ver como partes de una dirección de Interenet

1. *Dominio genérico.*

2. *Dominio de nivel superior patrocinado.*

3. *Dominio de nievel superior con código de país.*

4. *Dominio Raiz (Root Domain).*
El dominio raíz es la base de la jerarquia del DNS, que operan en la zona raíz. Estos servidores pueden responder 
directamente a las consultas de los registros almacenados en caché en la zona raíz, y también pueden remitir otras
solicitudes al servidor de dominio de nivel superior (TLD) apropiado.
Los servidores raíz son parte fundamental de la infraestructura de Internet; sin estos no funcionarian ni los 
navegadores web ni los navegadores web ni muchas otras herramientas de Internet. Hay 13 direcciones IP diferentes 
que siven a la zona raíz de DNS, y existen cientos de servidores raíz redundantes en todo el mundo para gestionar 
las solicitudes a la zona raíz.

### Zonas de búsqueda



###  Tipos de servidores



### Tipos de servidores



### Registros



### Funcionamiento



**_Consulta recursiva_**



**_Consulta iterativa_**