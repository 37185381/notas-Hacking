## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.
## Datos de acceso al nivel
- **Host:** ssh bandit21@bandit.labs.overthewire.org -p 2220
- **Port:** 2220 -
- **Username:** bandit21 
- **Password:** VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Solución
```bash
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
```

## Notas Adicionales

## Referencias
