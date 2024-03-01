## Objetivo
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag).
## Solución

```
sebgg10-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
--2024-02-27 18:21:08--  https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                  100%[======================>]      34  --.-KB/s    in 0s      

2024-02-27 18:21:08 (11.5 MB/s) - 'flag' saved [34/34]

sebgg10-picoctf@webshell:~$ ls
README.txt  flag
sebgg10-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_1a94e0f9}

```
## Notas adicionales
**wget + url**: Permite descargar archivos de internet.
## Referencias