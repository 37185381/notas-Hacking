## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso al nivel
- **Host:** ssh bandit20@bandit.labs.overthewire.org -p 2220
- **Port:** 2220 -
- **Username:** bandit20
- **Password:** VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solución
kali@kali:~$ ssh bandit20@bandit.labs.overthewire.org -p 2220
bandit20@bandit.labs.overthewire.org's password: NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

bandit20@bandit:~$ nc -nlvp 1843 <<< NvEJF7oVjkddltPSrdKEFOllh9V1IBcq &
[1] 3131313
bandit20@bandit:~$ Listening on 0.0.0.0 1843

bandit20@bandit:~$ ./suconnect 1843
Connection received on 127.0.0.1 53030
Read: NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
Password matches, sending next password
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
[1]+  Done                    nc -nlvp 1843 <<< NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
bandit20@bandit:~$ ahora este

## Notas Adicionales
| comando | descripción                      |
| ------- | -------------------------------- |
| jobs    | muestra las tareas en backgrpund |
| &       | manda el proceso al background   |
## Referencias
