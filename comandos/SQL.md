 __<span style="color: green;">➤ PRIVILEGIOS DE USUARIOS  </span>__    
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
 __<span style="color: green;">➤ Lenguaje SQL  </span>__    
```sh
# Mostrar las bases de datos
 show databases;

# Crear una base de datos;
  create database prueba;
  
# Usar la base de datos; 
  use empresa;

# Crear una tabla para la DB
  create table productos( 
    id_producto INT NOT NULL AUTO_INCREMENT,
    nombre_producto VARCHAR(45) NOT NULL,
    tipo_producto VARCHAR(45) NOT NULL,
    precio_producto varchar(10) NOT NULL,
    primary key(id_producto)
  )

 CREATE TABLE empleados(
  id_empleado INT NOT NULL auto_increment,
  nombre_empleado varchar(50) not null,
  apellido_empleado varchar(50) not null,
  area_trabajo varchar(50) not null,
  titulo varchar(45) not null,
  primary key(id_empleado)
 );
 
# Insertar datos en la tabla de la DB
insert into empleados(nombre_empleado,apellido_empleado,area_trabajo,titulo)values('Alex Gabriel',' Gomez','Mercadotecnia','Licenciatura en Mercadotecnia');

# Seleccionar o mostrar datos de la tabla
select * from administrador;

# Actualizar o modificar datos de la tabla
update administrador set arealaboral_admin = 'Finanzas' where id_administrador = 2;
update administrador set correo = 'alex.gomez@gmail.com' where id_administrador = 2;

# Eliminar datos de la tabla
delete from administrador where id_administrador = 1;

# Eliminar DB
    DROP DATABASE prueba;
``` 

__<span style="color: green;">➤ Consultas con Patron LIKE  </span>__    
```sh
# Espera una comparación de datos contra un cadena con parámetros definidos. 
# Por ejemplo, la cadena de parámetros ´ P% ´ indica que el primer carácter deberá ser una P y 
# posteriormente seguirá cualquier cadena de valores.

SELECT * FROM alumnos where nombre LIKE 'A%';      # Desplegará el listado de los alumnos cuyos nombres comienzan con a 
``` 

__<span style="color: green;">➤ Operadores de comparacion </span>__    
```sh
# BETWEEN: espera un conjunto de valores numéricos bajo el cual poder hacer la comparación de los datos.
# muy importante: Estos deben ser datos numéricos, del mismo conjunto o deberán pertenecer a un conjunto continuo de valores

SELECT * FROM pedidos WHERE fecha BETWEEN '2015' AND '2020';


# IN: para la operación se deberá especificar el conjunto de datos para comparación exacta contra los parámetros de nuestra elección. 
# De esta forma, aplicamos IN a aquellos digitos que se desean cumplan con una función, 
# que puede ser explicada o validada lógicamente mediante un conjunto de datos.

SELECT * FROM pedidos WHERE provincia IN('Madrid','Barcelona','Sevilla');


# 


``` 

__<span style="color: green;">➤ Ordenar datos ASCENDENTE o DESCENDENTE</span>__    
```sh
# ORDER BY: Permite ordenar los datos previo a la presentación al usuario. 
# Los datos se pueden ordenar de manera ASCENDENTE O DESCENDETE. Si no se especifica, el valor por defecto es ASCENDENTE

SELECT nombre,apellido FROM alumnos ORDER BY apelllidos DESC, nombre ASC;
``` 


__<span style="color: green;">➤ Funciones de agregados</span>__    
```sh
#  COUNT : Cuenta el número de filas que cumplen con las especificaciones dadas.
#  SUM   : Suma los datos en una columna determinada
#  AVG   : Promedia los datos en una columna determianda.
#  MAX   : Devuelve el máximo valor en una columna determinada.
#  MIN   : Devuleve el minimo valor de una columna nada.

SELECT COUNT(*) FROM carros;
SELECT SUM(precio) FROM articulos;
SELECT AVG(promedio) FROM carros;

Asesoría en SQL Server
‘’PARA OBTENER EL ULTIMO CODIGO SIN SER AUTOINCREMENTAL
Select  Top(1)  id_boleta FROM boleta ORDER BY  id_boleta DESC ;

‘PARA OBTENER EL ULTIMO CODIGO CON AUTO INCREMENTAL 
Select IDEN_T CURRECT(‘boleta’);


``` 


__<span style="color: green;">➤ SELECCIONAR 2 o 3 TABLAS  PARA HACER CONSULTA </span>__    
```sh
Sede y farmacéutico son (ENTIDADES)

# PARA INGRESAR Y CONSULTAR 2 TABLAS 
SELECT sede.direccion , farmacéutico.apellidos, farmacéutico.nombres	
FROM   sede , farmacéutico 
WHERE  sede.ciudad='pucallpa' and farmacéutico.direccion='pucallpa';


SELECT producto.descripcion,presentaciondos.nombre, presentaciondos.descripcion 
FROM producto,presentaciondos 
WHERE presentaciondos.id_producto='2' and producto.id_producto='2';

# PARA INGRESAR Y CONSULTAR 3 TABLAS 
SELECT peliculas.titulo,actor.nombre,actor.apellido FROM peliculas
INNER JOIN pelicula_actua ON peliculas.id_pelicula =  pelicula_actua.peliculaID
INNER JOIN actor ON pelicula_actua.actorID = actor.id_actor

``` 

<hr/>




MODELO E-R (ENTIDAD-RELACION)
------------------
![alt text](https://i.ytimg.com/vi/5dYAp88w6Uw/maxresdefault.jpg)
