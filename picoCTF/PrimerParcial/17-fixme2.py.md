## Objetivo
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
## Solución

```
sebgg10-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/6/fixme2.py
--2024-03-02 18:02:43--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                     100%[================================================================================================>]   1.00K  --.-KB/s    in 0s      

2024-03-02 18:02:43 (711 MB/s) - 'fixme2.py' saved [1029/1029]

sebgg10-picoctf@webshell:~$ ls
fixme2.py
sebgg10-picoctf@webshell:~$ nano fixme2.py 
sebgg10-picoctf@webshell:~$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

```
## Notas adicionales
= es diferente de ==
## Referencias