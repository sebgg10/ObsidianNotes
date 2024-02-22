## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de acceso al nivel
**Usuario:** bandit12
**Contraseña:** JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
**Servidor:** bandit.labs.overthewire.org
```
ssh bandit@bandit.labs.overthewire.org -p 2220
```
## Solución
Descomprimiendo iterativamente.
```
bandit12@bandit:~$ xxd -r data.txt
�h44�z��A����@=�h4hh�␦␦␦��hd����������������9���1����������;,�
�����2�3d*58�~  �S�ZP^��luY��Br$�FP!%�s��h�?�)[=�h��O(B��2A���)�tZc��:�pã)�A�ˈ�0���΅A�yjeϢx,�(����z�E�+"�2�/�-��e"���^����t�j���$�d�@�dJơ'7\���$��m1c��#>�aԽ�EV��F��OCӐc@M�C���]��Y2^h8���D=��~        O�I��NDpF�+�|b#Jv�#�J��d�LފW$�Û�͖y�`
                    �\& ��[�@*w�M�0θ��nr��C��`e$b�
                                                  ~�{���
                                                        ��`�<����a��?e:T���e�T4±b����)�@ِ���x=bandit12@bandit:~$
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ mkdir /tmp/37183950
bandit12@bandit:~$ cd /tmp/37183950
bandit12@bandit:/tmp/37183950$ xxd -r ~/data.txt > data
bandit12@bandit:/tmp/37183950$ ls
data
bandit12@bandit:/tmp/37183950$ file data
data: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 573
bandit12@bandit:/tmp/37183950$ mv data data.gz
bandit12@bandit:/tmp/37183950$ gzip -d data.gz
bandit12@bandit:/tmp/37183950$ ls
data
bandit12@bandit:/tmp/37183950$ file data
data: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/37183950$ mv data data.gbz2
bandit12@bandit:/tmp/37183950$ ls
data.gbz2
bandit12@bandit:/tmp/37183950$ mv data data.bz2
mv: cannot stat 'data': No such file or directory
bandit12@bandit:/tmp/37183950$ mv data.gbz2 data.bz2
bandit12@bandit:/tmp/37183950$ ls
data.bz2
bandit12@bandit:/tmp/37183950$ file data.bz2
data.bz2: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/37183950$ file data
data: cannot open `data' (No such file or directory)
bandit12@bandit:/tmp/37183950$ bzip2 -d data.bz2
bandit12@bandit:/tmp/37183950$ ls
data
bandit12@bandit:/tmp/37183950$ file data
data: gzip compressed data, was "data4.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/37183950$ mv data data.gz
bandit12@bandit:/tmp/37183950$ ls
data.gz
bandit12@bandit:/tmp/37183950$ gzip -d data.gz
bandit12@bandit:/tmp/37183950$ ls
data
bandit12@bandit:/tmp/37183950$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/37183950$ mv data data.tar
bandit12@bandit:/tmp/37183950$ ls
data.tar
bandit12@bandit:/tmp/37183950$ tar xf data.tar
bandit12@bandit:/tmp/37183950$ ls
data5.bin  data.tar
bandit12@bandit:/tmp/37183950$ rm data.tar
bandit12@bandit:/tmp/37183950$ ls
data5.bin
bandit12@bandit:/tmp/37183950$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/37183950$ mv data5.bin data5.tar
bandit12@bandit:/tmp/37183950$ tar xf data5.tar
bandit12@bandit:/tmp/37183950$ ls
data5.tar  data6.bin
bandit12@bandit:/tmp/37183950$ rm data5.tar
bandit12@bandit:/tmp/37183950$ ls
data6.bin
bandit12@bandit:/tmp/37183950$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/37183950$ mv data6.bin data6.bz2
bandit12@bandit:/tmp/37183950$ bzip2 -d data6.bz2
bandit12@bandit:/tmp/37183950$ ls
data6
bandit12@bandit:/tmp/37183950$ file data6
data6: POSIX tar archive (GNU)
bandit12@bandit:/tmp/37183950$ mv data6 data6.tar
bandit12@bandit:/tmp/37183950$ ls
data6.tar
bandit12@bandit:/tmp/37183950$ tar xf data6.tar
bandit12@bandit:/tmp/37183950$ ls
data6.tar  data8.bin
bandit12@bandit:/tmp/37183950$ rm data8.bin
bandit12@bandit:/tmp/37183950$ tar xf data6.tar
bandit12@bandit:/tmp/37183950$ rm data
data6.tar  data8.bin
bandit12@bandit:/tmp/37183950$ rm data6.tar
bandit12@bandit:/tmp/37183950$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/37183950$ mv data8.bin  data8.gz
bandit12@bandit:/tmp/37183950$ ls
data8.gz
bandit12@bandit:/tmp/37183950$ gzip -d data8.gz
bandit12@bandit:/tmp/37183950$ ls
data8
bandit12@bandit:/tmp/37183950$ file data8
data8: ASCII text
bandit12@bandit:/tmp/37183950$ cat data8
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```

Solución rápida

```
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar x0 | file -
tar: Options '-[0-7][lmh]' not supported by *this* tar
Try 'tar --help' or 'tar --usage' for more information.
/dev/stdin: empty
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

```
## Notas adicionales
**xxd**: Hace un vaciado hexadecimal.
**xxd -r**: Deshace el vaciado hexadecimal.
.gz gzip -d zcat
.bz2 bzip2 -d bzcat
.tar tar xf tar xO
## Referencias