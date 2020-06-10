 __<span style="color: green;">➤ COMANDOS  </span>__    
```sh
https://stackoverrun.com/es/q/10052713 -> Flush privileges
# conectamos a mysql
mysql -u root -p 
mysql -u admin -p

#Creamos un usuario
create user nameuser identified by 'passworduser'
grant all privileges on nametable.* to 'nameuser' with grant option
flush privileges

#DANDO PRIVILEGIOS Y CREANDO AL MISMO TIEMPO EL USUARIO
grant all privileges on *.* to gabriel@localhost identified by 'admin' with grant option
flush privileges

# Eliminamos a un usuario
drop user 'gabriel'@'localhost';

#Otro Metodo
SELECT user FROM mysql.user GROUP BY user;
DELETE FROM mysql.user WHERE user = 'usuario';




#Mostrar base de datos
show databases;

#Cómo listar todos los usuarios MySQL o MariaDB desde la consola
show tables;
describe user;                        #obtener las columnas de la tabla
select User from user;                #mostrar todos los usuarios MySQL con la consulta:
select User,Password,Host from user;  #mostrar todos los usuarios MySQL con la consulta:
select Host,Db,User from db;          # Consultar los usuarios y las bases de datos que tienen asignadas.
show grants for pepe;                #Listar privilegios por usuario

#nos permite mostrar los usuarios que tienen permisos sobre ciertas bases de datos:
SELECT host, user, password FROM mysql.user;
SELECT u.User,Db FROM mysql.user u,mysql.db d WHERE u.User = d.user;



SELECT USER(),CURRENT_USER();

``` 
<hr/>


MODELO E-R (ENTIDAD-RELACION)
------------------
![alt text](https://i.ytimg.com/vi/5dYAp88w6Uw/maxresdefault.jpg)
