## Objetivo
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solución
Identar bien el archivo .py

```
sebgg10-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2024-03-01 19:35:46--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                     100%[================================================================================================>]     837  --.-KB/s    in 0s      

2024-03-01 19:35:46 (487 MB/s) - 'fixme1.py' saved [837/837]

sebgg10-picoctf@webshell:~$ nano fixme1.py 
sebgg10-picoctf@webshell:~$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
sebgg10-picoctf@webshell:~$ 

```
## Notas adicionales
## Referencias