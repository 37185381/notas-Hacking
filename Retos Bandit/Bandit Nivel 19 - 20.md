## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Datos de acceso al nivel
- **Host:** ssh bandit19@bandit.labs.overthewire.org -p 2220
- **Port:** 2220 -
- **Username:** bandit19
- **Password:** hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
## Solución
kali@kali:~$ ssh bandit19@bandit.labs.overthewire.org -p 2220
bandit19@bandit.labs.overthewire.org's password: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rwsr-x---  1 bandit20 bandit19 14876 Feb 21 22:03 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile

bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id

bandit19@bandit:~$ ./bandit20-do whoami
bandit20

bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT

bandit19@bandit:~$

## Notas Adicionales
| comando | descripción                |
| ------- | -------------------------- |
| setui   | agrega permisos a terceros |
## Referencias
