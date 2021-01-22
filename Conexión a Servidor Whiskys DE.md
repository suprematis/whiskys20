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
*  Seguir las instrucciones de la herramienta para completar la generación de la llave.
