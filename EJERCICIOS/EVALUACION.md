## Práctica 1.

1. Introducción a base de datos

Objetivo: Identificar el nivel de comprensión de los conceptos de base de datos,
mediante preguntas abiertas.
 
Preguntas:

1. ¿Cuáles son las cinco funciones principales del administrador de bases de datos?
(valor 1.5)
Asegurar el buen funcionamiento de las BD
Retención de información de las BD
Evitar pérdida de datos
Solucionar incidencias y pérdidas de datos
Asegurar la seguridad de los dato

2. Indíque cinco responsabilidades del sistema gestor de bases de datos (valor 1.5)

Instalar, configurar y gestionar bases de datos.
Dar soporte al equipo de desarrollo, seguridad informática y redes.
Definir el esquema del diccionario de datos.
Especificar restricciones de integridad para asegurar los datos.
Garantizar la alta disponibilidad de la base de datos.

3. En una BD al usuario del sistema se le brindarán recursos para realizar diversas
operaciones sobre estos archivos, tales como: (valor 1.5)
• Efectuar cargos o abonos en las cuentas.

• Añadir cuentas nuevas.

• Calcular el saldo de las cuentas.

• Generar los extractos mensuales.

4. ¿Qué es un Sistema de Información? (valor 1.5)

Conjunto de elementos orientados al tratamiento y administración de datos e información, organizados y listos para su posterior uso, generados para cubrir necesidad. "Sistema de información" es el término general utilizado para la estructura global que incluye todos los mecanismos para compartir datos que se han instalado.

## Práctica 2.

2. Diseño de un modelo relacional

Objetivo: Representar desde un modelo entidad relación un problema


CREATE DATABASE editorial;
USE editorial;

CREATE TABLE empleado(
  tif_e VARCHAR (100) PRIMARY KEY,
  telf_e VARCHAR (100) NOT NULL,
  apell_e VARCHAR (100) NOT NULL,
  nomb_e VARCHAR (100) NOT NULL
  );

--INSERTAMOS DATOS


CREATE TABLE secciones(
ext_s VARCHAR (50)  PRIMARY KEY,
 tit_s VARCHAR (100) NOT NULL 
);

--INSERTAMOS DATOS 

INSERT INTO secciones VALUES ('esp','Espectalucos');
INSERT INTO secciones VALUES ('dep','Deportes');
INSERT INTO secciones VALUES ('pol','Politica');
INSERT INTO secciones VALUES ('cin','Cine');
INSERT INTO secciones VALUES ('hog','Hogar');
INSERT INTO secciones VALUES ('cul','Cultura');
INSERT INTO secciones VALUES ('vid','Videojuegos');


CREATE TABLE ejemplar(
numejem_vend VARCHAR (100) PRIMARY KEY,
 numpag_e VARCHAR (100) NOT NULL,
 fecha_e  VARCHAR (100) NOT NULL 
);

--INSERTAMOS DATOS

INSERT INTO ejemplar VALUES ('4855','56','23/09/2021');
INSERT INTO ejemplar VALUES ('1234','89','30/09/2021');
INSERT INTO ejemplar VALUES ('5343','78','09/10/2021');
INSERT INTO ejemplar VALUES ('5654','90','06/04/2022');
INSERT INTO ejemplar VALUES ('3434','100','15/03/2022');
INSERT INTO ejemplar VALUES ('6546','100','01/06/2021');
INSERT INTO ejemplar VALUES ('4534','56','15/05/2022');

CREATE TABLE sucursal(
cod_su VARCHAR (100) PRIMARY KEY,
  telf_su BIGINT UNSIGNED UNIQUE,
  dom_su VARCHAR (100) NOT NULL
  ); 
  
-- INSERTAMOS LOS DATOS

INSERT INTO sucursal VALUES ('suc01',5573485948,'Tenayuca 15, Colonia Porvenir');
INSERT INTO sucursal VALUES ('suc 02',3395847649,'Ahuehuetes 24, Colonia Reynosa');
INSERT INTO sucursal VALUES ('suc03',7293840947,'San Juan 12, Colonia Electricistas');
INSERT INTO sucursal VALUES ('suc04',8293459375,'Manuel Buendia 948, Colonia Refineria');
INSERT INTO sucursal VALUES ( 'suc05',7394850993,'Petroleos 12, Colonia Alabama');
INSERT INTO sucursal VALUES ('suc06',5587394785,'Petén 1209, Colonia Roma Norte');
INSERT INTO sucursal VALUES ('suc07',4593849058,'Tlahuac 10, Colonia Reyes');
INSERT INTO sucursal VALUES ('suc08',3384909859,'Anaxagoras 15, Colonia Polanco');
INSERT INTO sucursal VALUES ('suc09',3338930403,'Miguel Hidalgo 98,Colonia Angus');
INSERT INTO sucursal VALUES ('suc10',2288473845,'Cervantes 56, Colonia Juarez');

                             
  
  CREATE TABLE revista (
    num_r INT UNSIGNED PRIMARY KEY,
    titu_r VARCHAR(100),
    peri_r VARCHAR (50) NOT NULL,
    tip_r VARCHAR (100) NOT NULL
    );
    
-- INSERTAMOS DATOS 

INSERT INTO revista VALUES (098,'Politica Hoy','Semanal','Politica');
INSERT INTO revista VALUES (099,'Emoción Deportiva','Quincenal','Deportiva');
INSERT INTO revista VALUES (100,'Mundo Rosa','Semanal','Espectaculos');
INSERT INTO revista VALUES (1001,'Videogamer','Mensual','Videojuegos');
INSERT INTO revista VALUES (102,'Cine hoy','Semanal','Cine');
INSERT INTO revista VALUES (103,'Todo en Cultura','Mensual','Cultural');

    
 CREATE TABLE periodista (
 espe_p VARCHAR (100) PRIMARY KEY,
 nom_p VARCHAR (100) NOT NULL,
 apell_p VARCHAR (100) NOT NULL,
 telf_p BIGINT UNIQUE NOT NULL,
 tif_p VARCHAR (100)
 );
   
-- INSERTAMOS DATOS
INSERT INTO periodista VALUES ('Deportes','Karla','Perez',5534563748,'per_01');
INSERT INTO periodista VALUES ('Politica','Beatriz','Angeles',7289467349,'per_02');
INSERT INTO periodista VALUES ('Espectaculos','Tito','Galindo',8203978465,'per_03');
INSERT INTO periodista VALUES ('Videojuegos','Isabel','Jimenez',8263748987,'per_04');
INSERT INTO periodista VALUES ('Cine','Pablo','Duarte',5523784938,'per_05');
INSERT INTO periodista VALUES ('Cine1','Sergio','Morales',7238946574,'per_06');
INSERT INTO periodista VALUES ('Cultura','Carlos','Cisneros',3398475840,'per_07');
INSERT INTO periodista VALUES ('Deportes1','Juan','Macias',5682394848,'per_08');
INSERT INTO periodista VALUES ('Politica1','Pedro','Garay',5548738495,'per_09');
INSERT INTO periodista VALUES ('Videojuegos1','Angel','Fuentes',8236475894,'per_10');
INSERT INTO periodista VALUES ('Cine2','Cesar','Rodriguez',4585968495,'per_11');
INSERT INTO periodista VALUES ('Politica2','Magda','Sanchez',7683749594,'per_12');



Ejercicio:

Tenemos que diseñar una base de datos sobre proveedores y disponemos de la siguiente
información:

Realiza el modelo entidad relación. (valor 6)

Tenemos esta información sobre una cadena editorial:

● La editorial tiene varias sucursales, con su domicilio, teléfono y un código de
sucursal.

● Cada sucursal tiene varios empleados, de los cuales tendremos su nombre,
apellidos, NIF y teléfono. Un empleado trabaja en una única sucursal.

● En cada sucursal se publican varias revistas, de las que almacenaremos su título,
número de registro, periodicidad y tipo.

● Una revista puede ser publicada por varias sucursales.

● La editorial tiene periodistas (que no trabajan en las sucursales) que pueden
escribir artículos para varias revistas. Almacenaremos los mismos datos que para
los empleados, añadiendo su especialidad.

● También es necesario guardar las secciones fijas que tiene cada revista, que
constan de un título y una extensión.

● Para cada revista, almacenaremos información de cada ejemplar, que incluirá la
fecha, número de páginas y el número de ejemplares vendidos.


![image](https://user-images.githubusercontent.com/104279937/170845732-4e6c1dcc-951b-498f-8674-c121eceffbf7.png)
