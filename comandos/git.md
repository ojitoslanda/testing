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
