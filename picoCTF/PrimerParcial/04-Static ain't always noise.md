## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!
## Solución

```
sebgg10-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
--2024-03-01 18:43:15--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                        100%[================================================================================================>]   8.18K  --.-KB/s    in 0s      

2024-03-01 18:43:15 (304 MB/s) - 'static' saved [8376/8376]

sebgg10-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
--2024-03-01 18:43:29--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                      100%[================================================================================================>]     785  --.-KB/s    in 0s      

2024-03-01 18:43:29 (277 MB/s) - 'ltdis.sh' saved [785/785]

sebgg10-picoctf@webshell:~$ ls
ltdis.sh  static
sebgg10-picoctf@webshell:~$ file ltdis.sh 
ltdis.sh: Bourne-Again shell script, ASCII text executable
sebgg10-picoctf@webshell:~$ file static 
static: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=277d07901cf99a335a8107fbdd6642d9c6140bb5, not stripped
sebgg10-picoctf@webshell:~$ ./ltdis.sh static
-bash: ./ltdis.sh: Permission denied
sebgg10-picoctf@webshell:~$ chmod +x ltdis.sh 
sebgg10-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
sebgg10-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_f5aeda17}

```
## Notas adicionales
## Referencias