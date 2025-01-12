## Lab03:Linux shell

### Ejercicio 3.1:Creación de un script ejecutable en bash

El primer paso para este laboratorio crearemos un archivo test.sh, donde irá todo
el script. Especifica que el archivo es un script bash, limpia la terminal e
imprime el "Hello World".
Para la ejecución del archivo hay que darle permisos.

El chmod 777 test.sh se puede leer, modificar, o ejecutar el archivo, pero desde el
punto de vista, su seguridad es peligroso porque podría permitir que los usuarios
maliciosos modifiquen el contenido del archivo.

### Ejercicio 3.2:Creación de nuevos usuarios

Vamos a crear usuarios con bob y smith con su fichero correspondiente y
estableciendo su contraseña.

### Ejercicio 3.3:Creación de un script ejecutable compartido

Se creará un directorio con los permisos chmod 777 que en un archivo se va imprimir
Hello World y se ejecuta. Compruebo si tiene los permisos adecuados.

### Ejercicio 3.4:Acceso archivos desde diferentes cuentas de usuarios

En la creación de los nuevos usuarios iniciaremos sesión como bob y smith. Más
tarde se crea un archivo con su mensaje que va imprimir con sus permisos. Teniendo
los permisos dados al iniciar una sesión con otra cuenta podemos visualizar Hello
World en bob. Como observamos al iniciar de sesión en smith, sin problemas según lo
que se ha asignado con chmod se ejecuta un archivo público y otro archivo creado en
otra sesión.

### Ejercicio 3.5:Ejercicios opcionales

Nos dedicaremos a crear y gestionar grupos de Linux, cambiar de propiedad y los
permisos de archivos y verificar cómo los usuarios del mismo grupo tienen acceso a
los archivos. El grupo sysadmins se añadirá en bob y smith. Cambiamos el grupo
creado del directorio que se ha estado trabajando junto con los archivos. Lo
siguiente que se pide va ser deshabilitar la cuenta smith sin eliminarla, para
comprobar que esta deshabilitada al hacer un cat en un archivo si lleva un signi !
significa que la contraseña está desactivada y evita que el usuario inicie sesión.
