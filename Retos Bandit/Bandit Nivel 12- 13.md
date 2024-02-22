## Objetivo
El objetivo de este nivel es encontrar la contraseña para el siguiente nivel, la cual está almacenada en el archivo "data.txt", que es un volcado hexadecimal de un archivo que ha sido comprimido repetidamente.
## Datos de acceso al nivel
- **Host:** bandit.labs.overthewire.org -
- **Port:** 2220 
- **Username:** bandit12
- **Password:** JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Solución
![[11-12 1.jpg]]
## Notas Adicionales
El comando `xxd` es útil para convertir volcados hexadecimales a archivos binarios y viceversa.

Utiliza el comando `file` para determinar el tipo de archivo y qué tipo de compresión puede haber sido aplicada al archivo original.
## Referencias
https://www.geeksforgeeks.org/hexdump-command-in-linux-with-examples/

https://www.fpgenred.es/GNU-Linux/hexdump_hd.html

https://ioflood.com/blog/hexdump-linux-command/