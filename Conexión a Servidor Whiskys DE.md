# Conexión a Servidor Whiskys DE
Toda conexión debe iniciarse via llave SSH.  El procedimiento para lograr esto lo describo a continuación.

##  Configuración Inicial

Los siguientes pasos solamente deben realizarse la primera vez que se conectan al servidor.  Luego de generar la llave, pueden utilizar `Pageant` para conectar al servidor las veces que sean necesarias.

1.  Instalar Chocolatey
El procedimiento para instalar Chocolatey lo pueden encontrar aquí: [Chocolatey Install](https://chocolatey.org/install)

2.  Abrir una ventana con privilegios de administrador en Powershell
3.  Instalar los siguientes paquetes con Chocolatey
###  WinSCP
`choco install winscp`

###  putty(y paquetes afines)
`choco install putty`

4.  Abrir Puttygen para generar llave SSH de acceso (ventana Powershell).
`puttygen`

5.  Presionar botón "Generate" (Putty Key Generator)
![Puttygen Image](https://github.com/suprematis/whiskys20/blob/master/screenshot_putty.jpg)
*  Seguir las instrucciones de la herramienta para completar la generación de la llave.

6.  Una vez generada la llave, por favor compartir el contenido de "Public key" via correo electrónico.  El formato es el siguiente:
`ssh-rsa AAAAB3NzaC1yc2EAAAABJQAAAQEAn/LhfxnwPKI7SIStLQKVtVtTlRJ/dM4xxx4eNg9m7WQCsmoZXSEyCmpyVhiQLjsXgxrF8SUsj1IoeuqlRIUwCvgen7g6YCmghTNzkUaW6ol0XuV96e5L8enqljLChQtfhH6BQFcurI0smTRitLZljYLUORH1owfBXVu6bgoqXUKHHwKhj/UF4AmXPsVonllND0MHP4msG7j3FASFY54CW3jQ3J93ekVcoakE0O5rS2yrERhW8vx`


##  Conexión a Servidor

###  Pageant

Para transferir archivos al servidor se requiere WinSCP, que debería estar instalado como indica el paso (3).
7.  Abrir una ventana de Powershell y tipear `pageant`
8.  Pageant aparece en la barra de tareas con este ícono:
![Pageant Image](https://github.com/suprematis/whiskys20/blob/master/screenshot_pageant_taskbar.jpg)
9.  Cargar en Pageant la llave privada generada en el paso (5) presionando el botón "Add Key"
![Pageant Image Taskbar](https://github.com/suprematis/whiskys20/blob/master/screenshot_pageant_addkey.jpg)


###  WinSCP

Para transferir archivos al servidor se requiere WinSCP, que debería estar instalado como indica el paso (3).
10.  Abrir una ventana de Powershell y tipear `winscp`
11.  Iniciar una nueva sesión presionando "New Session"
12.  En la ventana de nueva de sesión seleccionar SCP como método "File Protocol"
13.  En el campo "hostname" ingresar el IP del servidor.
14.  Ingresar el usuario proporcionado en el campo "User Name"
15.  Si la llave fue ingresada correctamente, podrán conectarse si utilizar su contraseña.
