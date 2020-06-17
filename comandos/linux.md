### Debian 10
```sh

# instalar paquetes  de programas //antiguamente era apt-get Y ahora es aptitude
apt-get install aptitude
aptitude update
aptitude upgrade

sudo aptitude install rar
```


### Instalando rar & unrar
```sh
# Instalando rar & unrar
   sudo apt-get install rar
   sudo apt-get install unrar
   
#Si esta orden nos reportará algún tipo de problema, 
#cosa que me sucedió a mi mismo, añadiremos al final –fix-missing quedando de esta manera:
   sudo apt-get install unrar –fix-missing
#Con la primera orden añadiremos los archivos uno a uno, y con la segunda incluiremos todos los archivos que estén dentro del directorio en que nos encontremos.

#Para comprimir archivos usaremos el comando:
   rar a nombre_archivo.rar archivos a incluir
   rar a nombre_archivo.rar  *
   
#Para descomprimir será tan sencillo como usar el comando unrar:
unrar x nobre_del_rar.rar
unrar x nombre_del_rar.rar ruta donde lo queramos descomprimir
#Con la primera orden lo descomprimiremos en el directorio que nos encontramos y con la segundo le diremos el directorio en el que queremos que lo descomprima.
```

### Listar paquetes instalados
```sh
# Listar paquetes instalados
# Para listar el total de paquetes instalados ejecutamos el siguiente comando.
   sudo dpkg --get-selections
```
### Listar paquetes instalados
```sh
# Desinstalar programa desde la Terminal
   sudo apt-get remove [nombre del programa] 
```
###  Instalando a lo antigua
```sh
# Instalando
   sudo apt-get update        //actualice el repositorio de paquetes disponibles para instalar.
   sudo apt-get upgrade
   
#  Sin su Root
   sudo apt-get install git
    
   //instalar archivos .deb
   sudo dpkg -i nombredelarchivo.deb  //otra manera para instalar
   sudo apt install -f              //Eso significa que instale las dependencias faltantes  - Las dependencias que faltan
   
   
   sudo chmod 777 -R nombre_de_la_carpeta  // Dando permiso a las carpetas y a las demas carpetas
   sudo chmod 777 filename.bin  // 1prt dando permisos de sudo (superusuario para instalar 
   sudo ./namefile.bin         // 2prt  listo para instalar    
   
 
   
```

```sh
# Instalando las dependencias
    
   sudo apt-get build-dep nombredelprograma
```

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
