<strong>  ➤ Instalar git en Linux  </strong> 

Configurando Git por primera vez
Tu Identidad
Lo primero que deberás hacer cuando instales Git es establecer tu nombre de usuario y dirección de correo electrónico. Esto es importante porque los "commits" de Git usan esta información, y es introducida de manera inmutable en los commits que envías:

        $ git config --global user.name "John Doe"
        $ git config --global user.email johndoe@example.com
        
Tu Editor
Ahora que tu identidad está configurada, puedes elegir el editor de texto por defecto que se utilizará cuando Git necesite que introduzcas un mensaje. Si no indicas nada, Git usará el editor por defecto de tu sistema, que generalmente es Vim. Si quieres usar otro editor de texto como Emacs, puedes hacer lo siguiente:

        $ git config --global core.editor emacs


<hr/>

<strong>  ➤ Empezar un proyecto nuevo con git  </strong> 

           git init
           
<strong>  ➤ Ver todos los commit  </strong> 
           
           git log  
           
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
            
<strong>  ➤ Ver todas las ramas </strong> 
   
            git branch 
            
<strong>  ➤ merge es para pasar los cambios de una rama a otra </strong> 
   
            git merge "turama"
            
<strong>  ➤ Cambiar de Rama </strong> 
   
            git checkout master

