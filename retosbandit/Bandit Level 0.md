## Objetivo
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is **bandit.labs.overthewire.org**, on port 2220. The username is **bandit0** and the password is **bandit0**. Once logged in, go to the [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) page to find out how to beat Level 1.
## Datos de acceso al nivel
**Usuario:** bandit0
**Contraseña:** bandit0
**Servidor:** bandit.labs.overthewire.org
## Solución
```
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[bandit.labs.overthewire.org]:2220' (ED25519) to the list of known hosts.
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password:

...
...
For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

```  
## Notas adicionales
* ssh es un protocolo seguro para conexiones.
## Referencias
- [Secure Shell (SSH) on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
- [How to use SSH on wikiHow](https://www.wikihow.com/Use-SSH)

winget install --id Git.Git -e --source winget
git init en la carpeta de obsidiannotes
git config user.name "sebgg10"
git config user.email "sebasorlon.n@gmail.com"
git config --list
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:sebgg10/ObsidianNotes.git
git push -u origin main

git add .
git commit -m "hola"
git push