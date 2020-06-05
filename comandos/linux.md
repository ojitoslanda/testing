
```sh
# Listar paquetes instalados
# Para listar el total de paquetes instalados ejecutamos el siguiente comando.
   sudo dpkg --get-selections

# Desinstalar programa desde la Terminal
   sudo apt-get remove [nombre del programa] 
   
# Desinstalar nginx 
   sudo apt-get remove nginx
   sudo apt-get autoremove nginx
   sudo apt-get purge nginx
   sudo apt-get autoremove --purge nginx
   
# Desinstalar mysql-workbench 
#  Para desinstalar unicamente mysql-workbench en Debian  ejecutar los siguientes comandos:
   sudo apt-get remove mysql-workbench
   sudo apt-get autoremove mysql-workbench
   sudo apt-get purge mysql-workbench
   sudo apt-get autoremove --purge mysql-workbench
   
# Desinstalar mariadb-server-10.0  /  Mysql
   sudo apt-get remove mariadb-server
   sudo apt-get autoremove mariadb-server
   sudo apt-get purge mariadb-server
   sudo apt-get autoremove --purge mariadb-server
   
#Desistalar NGNIX
   sudo apt-get remove nginx nginx-common  # Elimina todos, pero los archivos de configuración.
   sudo apt-get purge nginx nginx-common  # Quita todo.
   sudo apt-get autoremove   # Después de usar cualquiera de los comandos anteriores, el uso de este en orden para eliminar 
   las dependencias utilizadas por nginx que no son necesarios.
   sudo apt-get autoremove
   sudo apt-get autoclean

# Desinstalar php , To remove php 7, you can try:
  sudo apt-get remove php-fpm
  sudo apt-get autoremove php-fpm
  sudo apt-get purge php-fpm
  sudo apt-get autoremove --purge php-fpm
  sudo apt-get autoremove
   sudo apt-get autoclean
```


```sh
#Instalando LEMP (Linux - Nginx - MariaDB / Mysql - PHP )
sudo apt update
sudo apt install nginx
sudo apt install mariadb-client mariadb-server
sudo apt install php php-mysql
```


```sh
# Instalando
   sudo apt-get update        //actualice el repositorio de paquetes disponibles para instalar.
   sudo apt-get upgrade
   
   Sin su Root
   sudo apt-get install git
    
    
   su root
   apt-get install apache2
   apt-get install mariadb-client mariadb-server
   apt-get install php php-mysql
   
   sudo aptitude install
   
   
   //instalar archivos .deb
   sudo chmod 777 filename.bin  // 1prt dando permisos de sudo (superusuario para instalar 
   sudo ./namefile.bin         // 2prt  listo para instalar    
   
   sudo dpkg -i nombredelarchivo.deb  //otra manera para instalar
   
```

```sh
# Instalando las dependencias
    
   sudo apt-get build-dep nombredelprograma
```


 putty
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








eliminar - los Paquetes instalados se quita (NO incluye los archivos de configuración)

purga - Purga es idéntica a eliminar, excepto en que los paquetes que se quitan y se purga. Purgar lo que significa que los archivos de configuración también se eliminarán.

Por supuesto, esto no se aplica a los paquetes que mantenga la configuración de los archivos dentro de la carpeta principal del usuario (por ejemplo: /home/SexyNoJutsuUser), estos archivos no serán tocados ( ¿por Qué "Purga" no quita todo lo relacionado con una aplicación? )

Así, por ejemplo, si se va a eliminar de Chrome, Firefox, XBMC o cualquier otro que contiene algunos archivos de configuración dentro de su /home carpeta, esta los archivos de la estancia allí.

Por otro lado, si usted fuera a instalar apache, squid, mysql o cualquier otro servicio similar que guardar sus archivos en /etc, esta configuración se eliminarán los archivos si utilizas purge.

Fuente: https://www.enmimaquinafunciona.com/pregunta/24038/cual-es-la-diferencia-entre-apt-get-purge-y-apt-get-remove
