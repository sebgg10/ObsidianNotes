## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución

```
sebgg10-picoctf@webshell:~$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py
sebgg10-picoctf@webshell:~$ nano level3.p
sebgg10-picoctf@webshell:~$ nano level3.py 
sebgg10-picoctf@webshell:~$ python3 level3.py level3.flag.txt.enc 
Please enter correct password for flag: 8799
That password is incorrect
sebgg10-picoctf@webshell:~$ python3 level3.py level3.flag.txt.enc 
Please enter correct password for flag: d3ab
That password is incorrect
sebgg10-picoctf@webshell:~$ python3 level3.py level3.flag.txt.enc 
Please enter correct password for flag: 1ea2
That password is incorrect
sebgg10-picoctf@webshell:~$ python3 level3.py level3.flag.txt.enc 
Please enter correct password for flag: acaf
That password is incorrect
sebgg10-picoctf@webshell:~$ python3 level3.py level3.flag.txt.enc 
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}

```
## Notas adicionales
## Referencias