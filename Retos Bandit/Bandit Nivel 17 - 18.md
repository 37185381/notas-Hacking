## Objetivo
The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.
## Datos de acceso al nivel
- **Host:** ssh bandit17@bandit.labs.overthewire.org -p 2220
- **Port:** 2220 -
- **Username:** bandit17
- **Password:** VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
## Solución
```bash
bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ wc passwords.new
 100  100 3300 passwords.new
bandit17@bandit:~$ wc passwords.old
 100  100 3300 passwords.old
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$

```


## Notas Adicionales

| comando | descripción                          |     |
| ------- | ------------------------------------ | --- |
| diff    | compara dos archivos linea por linea |     |
|         |                                      |     |
|         |                                      |     |
|         |                                      |     |
## Referencias
