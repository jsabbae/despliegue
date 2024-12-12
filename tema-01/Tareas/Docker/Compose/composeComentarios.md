Esta actividad consiste en instalar y configurar MediaWiki en un entorno Debian 
utilizando Docker Compose, una herramienta para definir y gestionar aplicaciones 
multi-contenedor.
El objetivo será lo siguiente, pero antes de nada, comprobaré si lo tengo todo instalado:

1. Desplegar MediaWiki usando DockerCompose.

2. Configurar MediaWiki. Para ello nos basaremos en un editor de texto nano para 
crear el archivo de configuración de Docker Compose. Levantamos los contenedores 
con docker-compose up -d, sin ningún error en el fichero creado ya que hemos 
añadido el host de la base de datos "db", el usuario "wikiuser", la contraseña 
"wikisecret".

3. Crear una Página de Prueba. En http://localhost:8080 se configurará la conexión 
de la base de datoscon los campos que se ha rellenado en el archivo creado.
Por último se reiniciará los contenedores. 

4. Verificar Persistencia de Datos. 
