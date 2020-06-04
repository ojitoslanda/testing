```sh
# Desinstalar programa desde la Terminal
   sudo apt-get remove [nombre del programa] 
```
```sh
# Instalando
    
   sudo apt-get update        //actualice el repositorio de paquetes disponibles para instalar.
   sudo apt-get install git
    
    
   su root
   apt-get install apache2
   apt-get install mariadb-client mariadb-server
   apt-get install php php-mysql
   
   
   //instalar archivos .deb
   
   sudo dpkg -i nombredelarchivo.deb
   
```

```sh
# Instalando las dependencias
    
   sudo apt-get build-dep nombredelprograma
```

aptitude install mariadb-server

cd Dowloads/
sudo dpkg -i "nombre"

sudo aptitude install putty


mkdir ssl -> nose xd




## Comandos Básicos de Linux


| Comando | Descripción |
| - | - |
`ls -l o dir `  | Listar directorio actual
`cp`            | Copiar Archivos
`mkdir`         | Crear directorios
`rmdir`         | borrar directorios vacios
`rm -r`         | borrar directorios 
`more filename`  | ver o mostrar el archivo
`mv `           | Mover archivos y carpetas
`exit `         | Salir de una sesion en terminal
`cat namefile`  | Leer o mostrar arcivos
`su  o su root` | Iniciar sesion como root
`sudo`          | ejecutar comandos directamente como root
`sudo rm -r`    | Eliminar un archivo
`clear`         | Limpiar pantalla
`who`           | Mostrar los usuarios que han iniciado session
`whoami`        | Mostrar el usuario actual
`pwd`           | Ver que directorio estamos


```sh
# Ejemplo del comando mv
  mv archivo.txt carpeta/     - Ejemplo 1
  mv archivo.txt ..           - Ejemplo 2
```


```sh
# Ejemplo del comando cp
  cp archivo.txt carpeta/archivo2.text     - Ejemplo 1  copiando y cambiando de nombre  en esa carpeta
  cp archivo.txt carpeta/     - Ejemplo 2  copiando en esa carpeta
```


```sh
# `Sistema de Permisos para directorios y archivos
    
    r (read) 4
    w (write) 2
    x (execute) 1
    
    rwx = propietario = u
    rwx = grupo  = g
    rwx = otros = o
    
    
    //touch archivo.txt   El comando touch de Linux se usa principalmente para crear archivos vacíos 
    
    ls -l
    
    chmod u+rwx archivo.txt
    o 
    chmod u=rwx archivo.txt
    
    
    
    //Cambiar el propietario del archivo (El que puede cambiar solo puede hacer el root)
    
    chown juan archivo.text
    ls -l
    chmod gou+rwx archivo.text
    
    
```
