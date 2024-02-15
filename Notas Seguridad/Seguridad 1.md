# Subir repositorio
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

Conectarse a bandit0
ssh bandit0@bandit.labs.overthewire.org -p 2220