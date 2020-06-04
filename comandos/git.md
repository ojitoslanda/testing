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
`git merge tu_rama `  | Ver el estado de nuestro archivos
`git log`  | Ver todos los commit que hemos creados
`git branch`  | Ver todas las ramas
`git merge tu_rama `  | Cambiar de Rama 
`git checkout tu_rama`  | Ver todas las ramas
`git checkout -- filename.html `  | Invertir los cambios de los archivos
`git diff`  | Ver las diferencias hechas en los archivos

     
 __<span style="color: green;">➤ Guardamos en Git  </span>__    
```sh
# COMANDOS 
# Si esta color verder  es por que ya esta en mi entorno de trabajo
# Si esta rojo es porque todavia no guardamos en el entorno de trabajo

git status                                             # Ver el estado de los archivos
git diff                                               # Es para ver los las diferencias de los archivos
git add index.html                                     # Agregamos los nuevos cambios, dependendiendo el archivo 
git commit o git commit -m "Mensaje"                   # Guardar los cambios

```    
 __<span style="color: green;">➤ Creamos un archivo .gitignore  </span>__    
```sh
# COMANDOS 
   
      # creamos un archivo .gitignore dentro escribimos, las carpetas o archivos que queremos ignorar
      # Ejemplo 
      # Si la carpeta se llama "test" , pongamos dentro del archivo de gitignore ->     test
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
      git branch  # Si me aparece dev es porque si se creo correctamente
      
# Eso seria todo amiguitos xd      
``` 

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

