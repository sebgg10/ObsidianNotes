## Objetivo
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)
## Solución

```
sebgg10-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2024-03-01 19:29:32--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                  100%[================================================================================================>]   1.16K  --.-KB/s    in 0s      

2024-03-01 19:29:32 (524 MB/s) - 'convertme.py' saved [1189/1189]

sebgg10-picoctf@webshell:~$ python3 convertme.py 
If 11 is in decimal base, what is it in binary base?
Answer: 00001011
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}

```
## Notas adicionales
Use cyber chef para convertir 11 a binario.
## Referencias