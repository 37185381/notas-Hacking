## Objetivo
El objetivo de este nivel es obtener la contraseña para el siguiente nivel enviando la contraseña del nivel actual al puerto 30001 en localhost utilizando cifrado SSL. ## Datos de acceso al nivel
## Datos de acceso al nivel
- **Host:** bandit.labs.overthewire.org -
- **Port:** 2220 
- **Username:** bandit15
- **Password:** jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución
![[15 -16 pt1.jpg]]
![[15-16 pt2.jpg]]

## Notas Adicionales
 comando `openssl s_client` para establecer una conexión SSL con el puerto 30001 en localhost.
 
Al enviar la contraseña del nivel actual al servidor, aseguramos la comunicación mediante SSL, lo que garantiza la confidencialidad y la integridad de los datos transmitidos.

La nota útil proporcionada en el desafío sobre "HEARTBEATING" y "Read R BLOCK" indica que puedes usar la opción `-ign_eof` con `openssl s_client` para evitar problemas relacionados con la terminación de la conexión.
## Referencias
- [Secure Socket Layer/Transport Layer Security en Wikipedia](https://en.wikipedia.org/wiki/Transport_Layer_Security) 
- [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)
