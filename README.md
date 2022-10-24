# Comandos-Git-Github

Repositorio creado para documentar el proceso de aprendizaje de git y los comandos útiles que necesitaré en este proceso 
https://www.youtube.com/watch?v=VdGzPZ31ts8&t=518s (Aprende GIT ahora! curso completo GRATIS desde cero)

## Table of Contents
1. [Install Git ](#1-install-git)
2. [Setting up Git](#2-setting-up-git)  
2.1 [List of commands](#21-list-of-commands)    
2.1.1 [Carriage Return](#211-carriage-return)  
2.1.2 [Terminal basic commands](#212-terminal-basic-commands)  
2.1.3 [Initializing Repository](#213-working-with-a-repository)  

## 1. Install Git
Descarga Git desde esta url: https://git-scm.com/downloads  
Si ya tienes instalado Git, puedes obtener la última versión de desarrollo a través del propio Git:
```
git clone https://github.com/git/git
```
## 2. Configuración de Git
### 2.1 Lista de comandos
Pongamos algunos comandos en el terminal (si está usando Windows no use CMD mejor use git-bash)
```
git --version 
```
> Este comando nos devolverá la versión de git que tenemos instalada.
```
git config --global user.name "user name"
```
> Esto es para establecer su nombre de usuario en la configuración global.
```
git config --global user.email "youremail@yourdomain.com"
```
> Esto es para establecer su correo electrónico en la configuración global.

Una vez que hemos establecido estos comandos hemos configurado nuestro git para utilizar esta información, el siguiente paso será configurar nuestro editor de código, yo he preferido VScode.  
Descargar VScode de esta url: https://code.visualstudio.com/download  
```
git config --global core.editor "code --wait"
```
> Esto es para establecer VScode como nuestro editor de código por defecto, el "--wait" se utiliza para que la terminal espere hasta que cerremos el archivo que estamos editando.
```
git config --global -e
```
> Este comando es para abrir nuestro archivo de configuración global en VScode, si funciona el archivo de configuración se abrirá mostrándonos la configuración que pusimos antes.  

#### 2.1.1 Retorno del carro:  
Cada vez que se pulsa "intro" en el teclado, se inserta un carácter invisible llamado fin de línea o retorno de carro. Esto se maneja de manera diferente en los distintos sistemas operativos.   
Cuando colaboras en proyectos con Git y Github, Git puede producir resultados inesperados si, por ejemplo, estás trabajando en Windows y tu colaborador hizo cambios en macOS. 
Puedes configurar git para que gestione el final de línea automáticamente, de modo que puedas colaborar eficazmente con personas que utilicen otros sistemas operativos.  

```
git config --global core.autocrlf input
```
> In case you are using macOS or linux you must use "input" to set up autocrlf.
```
git config --global core.autocrlf true
```
> In case you are using Windows you must use "true" to set up autocrlf.

If you want to know what other configuration possibilities git has you can use
```
git config -h
```

#### 2.1.2 Terminal basic commands
```
ls
```
> El comando "ls" le devolverá la lista de archivos del directorio en el que se encuentra.
```
ls -a
```
> El comando "ls -a" le devolverá la lista de archivos del directorio en el que se encuentra, incluidos los archivos ocultos.
```
pwd
```
> El comando "pwd" le devolverá el directorio en el que se encuentra.
```
cd <directory>
```
> El comando "cd" nos permitirá movernos a otro directorio, por ejemplo, imaginemos que estamos en /Escritorio, y dentro tenemos un directorio llamado Proyecto, por lo que para acceder a Proyecto tenemos que teclear "cd Proyecto" ahora pulsamos enter y nos daremos cuenta si usamos el comando "pwd" que estamos en /Escritorio/Proyecto.
```
mkdir <directory>
```
> El comando "mkdir" nos permitirá crear un nuevo directorio, por ejemplo, si necesitamos crear un directorio llamado "workspace", debemos escribir "mkdir workspace" que creará el directorio workspace.

#### 2.1.3 Trabajar con un repositorio
```
git init
```
> Una vez que estamos dentro del directorio de nuestro proyecto debemos teclear el comando "git init" para inicializar el repositorio git.
```
git add
```
> Añadir un archivo a la fase de la etapa.
```
git add .
```
> El comando "git add ." es para añadir todos los archivos del repositorio a la fase de stage. Intenta no usar esto demasiado porque será un lío si accidentalmente añades un archivo que no quieres poner en fase. Por ejemplo, hay archivos como binarios grandes o imágenes o cosas como el archivo venv, si usas este comando empujará todos los archivos al repositorio.
```
git commit -m "Description of the commit"
```
> Confirmar los cambios de la fase de la etapa
```
git status
```
> El comando "git status" nos dará el estado del repositorio

## Commandos sueltos

```
git log
```
> git log es para ver el historial de commits que se han hecho en el repositorio

```
git remote add origin <direccion del repositorio>
```
> git remote add origin es para agregar el repositorio remoto, en este caso el repositorio de github

```
git pull origin <nombre de la rama>
```
> git pull origin es para traer los cambios que se han hecho en el repositorio remoto, en este caso github

```
git push origin <nombre de la rama>
```
> git push origin es para subir los cambios que se han hecho en el repositorio local, en este caso el repositorio de la computadora

```
git branch
```
> git branch es para ver las ramas que existen en el repositorio

```
```

```
git branch <nombre de la rama>
```
> git branch es para crear una nueva rama


```
git checkout -b <nombre de la rama>
```
> git checkout -b es para crear una nueva rama y moverse a ella

```
git switch -c <nombre de la rama>
```
> git switch -c es para crear una nueva rama y moverse a ella

```
git fetch
```
> git fetch es para traer los cambios que se han hecho en el repositorio remoto, en este caso github

```
git stash
```
> git stash es para guardar los cambios que se han hecho en el repositorio local, en este caso el repositorio de la computadora. Se queda en un estado alternativo llamado `stash`, para devolver los cambios del stash ver `git stash pop`

```

```
git stash pop
```
> git stash pop es para traer los cambios temporales que se han guardado con git stash

```
