## Objetivo
El objetivo de este nivel es encontrar la contraseña para el siguiente nivel, la cual está almacenada en el archivo "data.txt", el cual contiene datos codificados en base64.
## Datos de acceso al nivel
- **Host:** bandit.labs.overthewire.org -
- **Port:** 2220 
- **Username:** bandit10 
- **Password:** [G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s]
## Solución
![[Bandit 10 - 11.jpg]]
## Notas Adicionales
Al trabajar con archivos codificados en base64, puedes utilizar el comando `base64 -d` seguido del nombre del archivo para decodificar su contenido y obtener la información original.

Al utilizar la opción `-n` con el comando `echo`, evitas que se agregue un carácter de nueva línea al final del texto, lo cual puede ser útil al codificar texto con `base64`.
## Referencias
https://ubunlog.com/base64-codificacion-decodificacion-terminal/