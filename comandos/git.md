<strong>  ➤ Instalar git en Linux  </strong> 

Instalación en Linux
Si estás en una distribución basada en Debian como Ubuntu, puedes usar apt-get:

        $ apt-get install git
          sudo aptitude install git

Si alguna vez necesitas ayuda usando Git, existen tres formas de ver la página del manual (manpage) para cualquier comando de Git:

        $ git help <verb>
        $ git <verb> --help
        $ man git-<verb>

Configurando Git por primera vez
Tu Identidad
Lo primero que deberás hacer cuando instales Git es establecer tu nombre de usuario y dirección de correo electrónico. Esto es importante porque los "commits" de Git usan esta información, y es introducida de manera inmutable en los commits que envías:

        $ git config --global user.name "John Doe"
        $ git config --global user.email johndoe@example.com
        
Tu Editor
Ahora que tu identidad está configurada, puedes elegir el editor de texto por defecto que se utilizará cuando Git necesite que introduzcas un mensaje. Si no indicas nada, Git usará el editor por defecto de tu sistema, que generalmente es Vim. Si quieres usar otro editor de texto como Emacs, puedes hacer lo siguiente:

        $ git config --global core.editor emacs

Comprobando tu Configuración
Si quieres comprobar tu configuración, puedes usar el comando git config --list para mostrar todas las propiedades que Git ha configurado:

         $ git config --list
         
         
También puedes comprobar el valor que Git utilizará para una clave específica ejecutando git config <key>:
        
        $ git config user.name
        John Doe         
         
 Version de GIT
  
        git --version
  
<hr/>


 __<span style="color: green;">➤ ProTips  </span>__    
```sh
# COMANDOS 
sudo aptitude install git
git --version
git config --list
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git init
git status
git add .
git commit -m "mensaje"
git log
git checkout -- .     #Recuperar mis archivos  o carpetas borrachos, con el ultimo commit creado

# esto sirve para mandar y tambien crear tus archivos local a github directo          
git remote add origin https://github.com/ojitoslanda/proyecto.git
git push -u origin master     # Guardamos  
        
``` 




## Comandos Básicos de Git

| Comando | Descripción |
| - | - |
`git init`  | Empezar o para inicializar un proyecto nuevo con git
`git add <filename> `  | Para empezar agregar un archivo al staging area
`git log`  | Ver todos los commit que hemos creados
`git branch`  | Ver todas las Ramas o Version alternativa ("master" es la rama default)
`git merge tu_rama `  | Fusionamos los cambios de la rama test a rama master
`git checkout tu_rama`  | Cambiar de Rama o Version alternativa 
`git checkout -- filename.html `  | Invertir , Cambiar el orden o volver  los cambios de los archivos
`git diff`  | Ver las diferencias hechas en los archivos
`git checkout -- .`  | Volver todo a la normalidad ( Claro si guardaste con el Git )
`git reset HEAD CONTRIBUTING.md`  | Deshacer un Archivo Preparado (Git status)
  
 __<span style="color: green;">➤ Uso del SSH key (Deployment con git)  </span>__    
```sh
# Nos sirve para conectarnos fácilmente a un servidor o servidores, sin tener que poner una contraseñaa a cada momento
   ssh-keygen
   archivo.pub
   
# ➤ Llaves SSL 
eval "$(ssh-agent -s)"
ssh-add /home/gabriel/Documents/ssl/gabriel/gabriel
```   
 
 
 
 
 
 
 
 
 
 
  __<span style="color: green;">➤ WorkFlows   </span>__    
```sh
#Proyectos con equipos 
#Create an organization
        git branch -a  #Mostrar la ramas  ocultas

# (omar hace esto: ) Guardamos en el repositorio remoto (Github)
   git add .
   git commit -m "Mas especifico con tu mensajes"
   git push origin master 



/*
# (gabo debe ver esto:) Para ver primero si tenemos antigua la conexion de antes (MUY IMPORTANTE PARA NO TENER PROBLEMAS, SOLO EN CASO SI MOVI MI REPOSITORIO A OTRO ) 
      git remote -v
        Ejemplo
         origin  https://github.com/ojitoslanda/proyecto.git (fetch)
         origin  https://github.com/ojitoslanda/proyecto.git (push)
# Eliminamos eso
        git remote remove origin 
# Agregamos la nueva conexion - con el equipo de trabajo de la organizacion(su repositorio)           
        git remote add origin https://github.com/ODLSoft/Testing.git
# Ver si hicimos correctamente 
        git remote -v
*/
       
# (Gabo debe hacer esto si no tiene los cambios del otro compañero)  # Guardamos sus cambios de mis compañeros
   git fetch origin                    
   git merge origin/master   

```


 
 
 
 __<span style="color: green;">➤ Guardamos en Git  </span>__    
```sh
# COMANDOS 
# Si esta color verder  es por que ya esta en mi entorno de trabajo
# Si esta rojo es porque todavia no guardamos en el entorno de trabajo

# Ver el estado de los archivos
        git status                           
# Es para ver los las diferencias de los archivos
        git diff                                         
# Agregamos los nuevos cambios, dependendiendo el archivo 
# Puedes usar este `git add index.html` , que es para agregar uno por uno  
# Puedes usar este `git add .` , que es para agregar todo al entorno de trabajo
        git add index.html        
# Guardar los cambios
        git commit o git commit -m "Mensaje"    
            
```   
__<span style="color: green;">➤ Uso del Github con git </span>__    
```sh
 #Clonar un repositorio
          git clone https://github.com/example/example.git
          
          git remote -v                 #  Ver si esta correctamente vinculado mi proyecto con Git y Github
          git remote remove origin      #  Desvinculamos el Git y Github (REPOSITORIOS)
          
  # esto sirve para mandar y tambien crear tus archivos local a github directo          
        git remote add origin https://github.com/ojitoslanda/proyecto.git
        git push -u origin master     # Guardamos  
```   

 __<span style="color: green;">➤ Creamos un archivo .gitignore  </span>__    
```sh
# COMANDOS 
   
      # creamos un archivo `.gitignore`  dentro escribimos, las carpetas o archivos que queremos ignorar
      # Ejemplo 
      # Si la carpeta se llama `test`, pongamos dentro del archivo de gitignore ->     test
``` 
 __<span style="color: green;">➤ Creamos una rama  o version alternativa    </span>__    
```sh
#¿Qué es ramas?
      Es una linea de tiempo en nuestro proyecto, que nos sirven para arreglar errores, 
      experimentar, hacer grandes cambios, etc.
      
# dev es el nombre de rama o version alternativa    
      git branch dev      
# Ver si he creado correctamente    
      git branch  # Si me aparece dev es porque si se creo correctamente
# Ahora si yo quiero usar esa rama o version alternativa , ya que actualmente estoy con master ingreso este comando: 
      git checkout dev 
      git branch  # Si me aparece dev es porque si estoy en la rama que requiero
      
      
#Para crear una rama y usar esa rama automaticamente
     git checkout -b nombrerama
# Eso seria todo amiguitos xd      
``` 

 __<span style="color: green;">➤ Borramos una rama  o version alternativa    </span>__    
```sh
      # antes de eliminar tenemos que estar en la rama master (principal) ahi podemos eliminar la rama que deseo
       git branch -D nombrerama
       
        # Eso seria todo amiguitos xd      
``` 


 __<span style="color: green;">➤ Fusiones o Fusionar </span>__    
```sh
# Es la creación de un nuevo commit juntando una rama con otra (se usa en GIT).
        git checkout master #Tenemos que estar en la rama principal (master)
        git branch       # Aseguramos que estamos en la rama master
        git merge dev    # Fusionamos la rama "dev" para que pase todo el codigo a master


#MUY IMPORTANTE LEER ESTO
#Fast-Foward(Simple y automatico)
        Solo va a hacer la fusion, esto pasa normalmente cuando se trabaja con archivos diferentes o lineas de codigos distintas
#Manual Merge(Largo y Manual) - Trabajo en equipo
        Antes de hacer la fusion tiene que pasar por nosotros, normalmente ocurre cuando se trabaja en los mismo archivos o lineas de codigo
        
        
        
# Eso seria todo amiguitos xd      
``` 



 __<span style="color: green;">➤ Git Reset o Eliminar un commit  </span>__    
```sh
# Trabajar con cuidado -> mata a los commit 
        git log
        
        commit bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
                Author: ojitoslanda <ojitoslanda@gmail.com>
                Date:   Thu Jun 4 17:20:32 2020 -0500
                Mi primer commit 
                
   #Este Git reset más simple y que no toca nuestro "Working Area" (no se mete con nuestro codigo)
        git reset --soft bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
        
   #Este Git Reset borra el "Staging Area" , sin tocar el "Working Area"
        git reset --mixed bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
        
   #Este Git reset borra absolutamente todo lo que hay en el commit y los codigos
        git reset --hard bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
        git reset --hard HEAD~2 (FILA 2 DEL HEAD)
``` 

 __<span style="color: green;">➤ Revertir un commit  (Recomendable usar, en vez de Resetear)</span>__    
```sh
git log --oneline  o git log --oneline | cat  # Mostrar los commit con ordenado
git log --oneline --decorate       # Sirve para ver los nombres de los punteros que tenemos en el repositorio (HEAD -> Master)

#COMPARAR COMMIT 
          Anterior Actual      
git diff b43ec03 3ebe8bd           # Diferencia de los commit con el otro commit  
git diff HEAD~1 HEAD               # Comparar el ultimo commit con la anterior

#REVERTIR UN COMMIT 
  #- Descartar los cambios que se hicieron en un commit , pero te agrega otro commit nuevo 
  # ejemplo del commit que se crea solo --->  Revert "Mensaje"
git revert HEAD      <-- Descarta el ultimo commit pero te agrega un commit nuevo | no elimina el commit
git revert b8c6d57   <-- Descarta el commit con su propio llave individual pero te agrega un commit nuevo

# Descarta o vuelve lo anterior del commit pero No borra el commit que hiciste, pero lo pone en state area
 git revert --no-commit HEAD     
 git revert --continue 
``` 

 __<span style="color: green;">➤ Volver en el tiempo a tu repositorio o ver el codigo pasado      </span>__    
```sh
        ->  git log
          
          ->  commit bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
                Author: ojitoslanda <ojitoslanda@gmail.com>
                Date:   Thu Jun 4 17:20:32 2020 -0500
                Mi primer commit 

         ->   git checkout bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
          
             #Para volver al ultimo commit que hice o volver al actual
          ->   git checkout master
``` 

         
          
 __<span style="color: green;">➤ Concepto Head   </span>__    
```sh
# Head es el commit donde nos encontramos

        git log
        
        commit bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
                Author: ojitoslanda <ojitoslanda@gmail.com>
                Date:   Thu Jun 4 17:20:32 2020 -0500
                Mi primer commit 
                
       Head -> commit bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
```       

          
 __<span style="color: green;">➤ Creando un Tag ( Etiquetas ) - El uso de de versiones   </span>__    
```sh
#Las tag sirve para especificar a los commit que son las versiones de nuestro proyecto 
#Si tenemos o estamos en el commit 50, podemos decir que desde ahi es la version v1.0

# Tag anotadas (El mas usado -recomendada) : son almacenadas com objetos completos dentro de la base de Git y contienen mas información
        git tag -a v1.0 -m "Mensaje" 
# Tag ligeras : Son otra forma de crear tags, más simples y con poca informacion
        git tag v1.0

#Especificacion de Tag para los commit : Al agregar el codigo SHA Podemos especificar donde se va a aplciar una etiqueta
        git tag -a v0.1 -m "Version 0.1 de nuestro primer proyecto" bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
        
#Compartiendo o subir Nuestra tags  a Githu
        git push origin v0.8  

#Compartiendo  o Subir todos los tag que creamos en una sola a github
        git push origin  --tags

```
 __<span style="color: green;">➤ Modificar el ultimo Commit  </span>__    
```sh
#tenemos que ver si se guardo el commit en el github (No el modificado, me refiero el actual), osea el que queremos modificar
#si vemos que ese ultimo commit  que hicimos no queremos en el github y lo queremos modificar, hacemos lo siguiente

# Modificamos el ultimo commit que hicimos en el local
        git log
        git commit --amend -m "Modificando commit xd"    o      git commit --amend
#Guardamos tambien en el github, 
        git push origin master -f  # (-f) para forzar que suba estos cambios
    
```   


<strong> Git Hooks ➤  Creamos un archivo (git-dev.sh) , guardar automicamente, sin necesidad de escribir </strong> 

           #!/bin/bash
           fecha=`date +"%Y-%m-%d %T"`
           git checkout dev
           git add .
           git commit -m "Cambios al $fecha"
           git push origin dev
                      
           # Escribimos en el terminal 
            bash offline/git-dev.sh (la ruta depende de la carpeta donde fue creada el archivo)
            
 <strong>  ➤ Subir cambios o traer los cambios de mis compañeros de trabajo </strong> 

            git pull origin master -r    
            git pull
            git pull origin larama

