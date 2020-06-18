https://www.youtube.com/watch?v=MhrPeOoEJBA

command -v nvm

 __<span style="color: green;">➤ NVM  (node version manager) </span>__    
```sh
Archivo
  --lts               # Programa de soporte a largo plazo (LTS).
  
   nvm use
 #Si no encuentra el archivo de node la version - Creamos ese archivo/Si no lo tiene pasamos a la siguiente   
   touch .nvmrc  
# En ese archivo escribimos la vesion actual 
   nvm ls-remote --lts      # Para ver que version actual hay en global
# Ejemplo 
     12.18.1       #Luego Guardamos 
# Luego usamos eso
  nvm use
# Te debe salir este mensaje 
  Now using node v12.18.1 (npm v6.14.5)
   
   
#Para mirar lista de versiones que esta utilizando
   nvm list

``` 
