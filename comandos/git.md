<strong>  ➤ Instalar git en Linux  </strong> 

Instalación en Linux
Si quieres instalar Git en Linux a través de un instalador binario, en general puedes hacerlo mediante la herramienta básica de administración de paquetes que trae tu distribución. Si estás en Fedora por ejemplo, puedes usar yum

        $ yum install git
Si estás en una distribución basada en Debian como Ubuntu, puedes usar apt-get:

        $ apt-get install git

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


## Comandos Básicos de Git

| Comando | Descripción |
| - | - |
`git init`  | Empezar o para inicializar un proyecto nuevo con git
`git add <filename> `  | Para empezar agregar un archivo al staging area
`git log`  | Ver todos los commit que hemos creados
`git branch`  | Ver todas las Ramas o Version alternativa ("master" es la rama default)
`git merge tu_rama `  | 
`git checkout tu_rama`  | Cambiar de Rama o Version alternativa 
`git checkout -- filename.html `  | Invertir , Ccambiar el orden o volver  los cambios de los archivos
`git diff`  | Ver las diferencias hechas en los archivos

     
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
        
        
        
 
 #######################
 # Esto es opcional o un ejemplo, porque cuando creas un repositorio de github ahi te mostrara ese codigo
 # …or create a new repository on the command line 
 # esto sirve para mandar y tambien crear tus archivos local a github directo 
          git add README.md
          git remote add origin https://github.com/ojitoslanda/proyecto.git
          git push -u origin master
 #Clonar un repositorio
          git clone https://github.com/example/example.git
               
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
# COMANDOS 

# dev es el nombre de rama o version alternativa    
      git branch dev      
# Ver si he creado correctamente    
      git branch  # Si me aparece dev es porque si se creo correctamente
# Ahora si yo quiero usar esa rama o version alternativa , ya que actualmente estoy con master ingreso este comando: 
      git checkout dev 
      git branch  # Si me aparece dev es porque si estoy en la rama que requiero
      
# Eso seria todo amiguitos xd      
``` 


 __<span style="color: green;">➤ Git Reset   </span>__    
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
        git reser --mixed bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
        
   #Este Git reset borra absolutamente todo lo que hay en el commit y los codigos
        git reset --hard bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
``` 



<strong>  ➤ Volver en el tiempo a tu repositorio o ver el codigo pasado </strong> 

          ->  git log
          
          ->  commit bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
                Author: ojitoslanda <ojitoslanda@gmail.com>
                Date:   Thu Jun 4 17:20:32 2020 -0500
                Mi primer commit 

         ->   git checkout bdc1c52658ab7c277c5d5ce611a7f926e9b27f56
          
             #Para volver al ultimo commit que hice o volver al actual
          ->   git checkout master
          
           
<strong>  ➤ Llaves SSL </strong> 

           eval "$(ssh-agent -s)"
           ssh-add /home/gabriel/Documents/ssl/gabriel/gabriel
           
<strong>  ➤ Guardamos Github </strong> 

          git status
          git add .
          git commit -m "comentario"
          git push origin nombre_rama


<strong>  ➤ Creamos un archivo (git-dev.sh) , guardar automicamente, sin necesidad de escribir </strong> 

           #!/bin/bash
           fecha=`date +"%Y-%m-%d %T"`
           git checkout dev
           git add .
           git commit -m "Cambios al $fecha"
           git push origin dev
                      
       Escribimos en el terminal 
            bash offline/git-dev.sh (la ruta depende de la carpeta donde fue creada el archivo)
            
 <strong>  ➤ Subir cambios o traer los cambios de mis compañeros de trabajo </strong> 

            git pull origin master -r    
            git pull
            git pull origin larama

