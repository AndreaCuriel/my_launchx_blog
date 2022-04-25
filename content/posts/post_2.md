---
title: "Acordeón de Git"
date: 2022-04-25
description: 'Resumen de los comandos básicos de Git'
---

En mi misión en launchX – Backend con mi Mission Commander Carlo Gilmar, tuve el placer de tomar un taller de Git, donde mi MC nos brindó como referencia y además es el autor. 

Este taller me permitió realizar un acordeón de los comandos de Git, con el fin de tener una herramienta sencilla que pueda usar en mi día a día.

A continuación, les dejo el acordeón, esperando que les sea de utilidad.

## Áreas de Git
- Working Directory
- Stage Area
- Local Repository


## Comandos básicos de Git

|Comando|Descripción|
|:--------------|:----------------|
|mkdir my_proyect|Crear directorio|
|git init|Inicializador de repositorio básico, crea la carpeta. git|
|git status|Muestra el estado del working directory|
|git add archivo archivo|Agregar el archivo en Stage Area|
|git add .|Agrega todos los archivos faltantes que están en working Area a Stage Area|
|git rm --cached archivo|Elimina el archivo en el stage Area|
|git checkout --archivo_en_stage|Regresa un archivo del stage al working directory|
|git commit -m "Descripcion"|Agrega los archivos de stage area al local Repository|
|git log|Muestra el estado del Local Repository|

## Comandos Prácticos

|Comando|Descripción|
|:--------------|:----------------|
|git diff archivo|Muestra las diferencias entre el estado de un archivo que ha sido modificado|
|git checkuot -- archivo_modificado|Elimina los cambios del archivo modificado en el working directory|
|git stash|Guarda en una pila los cambios encontrados en working directory, al correr déspues git status, te dirá que no hay modificación|
|git stash pop|Regresa los archivos guardados temporalmente en la pila hacia working directory|
|git reset|Te permite deshacer commits previamente hechos|
|git reset HEAD~1|Se refiere a eliminar el ultimo commint realizado HEAD~n n=número de commits|
|git reset --hard HEAD~1|Se descartan todos los cambios|
|git commit --amend -m "reescribir"|Reescribe el nombre del último commit realizado|
|git restore --staged files|Regresa los cambios del comando git add|

## Manipulación de un repositorio

|Comando|Descripción|
|:--------------|:----------------|
|git log --pretty=oneline|Ver los commits|
|git checkout no.commit|Regresar a un commit especifico (ir al pasado)|
|git checkout master|Regresar al último commit realizado (presente)|
|git log --grep="palabras-a-buscar-en-log"|Búsqueda especifica por palabra en el log|
|git log -p|Ver commits y contenidos de cada uno|
|git show hash-del-commit|Ver el contenido de un commit en específico, agregando el hash|
|git blame archvio|Muestra los commits que se realizaron en un archivo en especifico|

## Repositorio remoto a repositorio local y  viceversa

|Comando|Descripción|
|:--------------|:----------------|
|git remote add origin url-del-repositotio-remoto|Copiar la url o https del repositorio remoto en el proyecto local, dándolo de alta|
|git remote - v|Comprueba la url donde se encuentra el repositorio remoto|
|git push origin main|Enviar los cambios del repositorio local al remoto por medio de la branch|
|git pull origin master|Enviar los cambios del repositorio remoto al local por medio de la branch|
|git fetch|Actualiza el repositorio local con la información del repositorio remoto (tags y branchs)|
|git clone <url del repositorio remoto>|Sincronizar el repositorio remoto al repositorio local, para empezar, operarlo desde local|
  
 ## Submodulos 
  
|Comando|Descripción|
|:--------------|:----------------|
|git submodule add url-del-repositorio-remoto nombre-de-la-carpeta-en-que-se-descargará|Un repositorio de git puede tener referencias a otros repositorios, esto es común cuando se necesita enlazar a varios proyectos en uno solo|
 

## Branches

|Comando|Descripción|
|:--------------|:----------------|
|git rev-parse --abbrev-ref HEAD|Saber en cual branch estas|
|git branch|Listar las branches que se tienen en local|
|git branch -a|Listar todos los branchas incluyendo los remotos|
|git branch nombre-de-branch|Crear un branch nuevo|
|git branch -D nombre-de-branch|Borrar un branch|
|git checkout nombre-de-branch|Posicionarse en un branch existente|
|git checkuot -b nombre-del-branch-nuevo>|Crear y posicionarse en un nuevo branch|
|git merge branch-a-mezclar|Unir los cambios del branch donde te encuentras hacia la especificada en el comando|
  
Referencia
|Autor|URL|
|:-----|:------|
|Carlo Gilmar|[Taller de Git](https://carlogilmar.gitbooks.io/git-course/content/)|
  
Saludos y agredecimientos a Carlo Gilmar por su aportación y ser un excelente mentor.
