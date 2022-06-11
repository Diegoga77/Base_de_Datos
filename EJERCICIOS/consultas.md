En la BD utilizada en clase realiza las siguientes consultas:

* La tabla empleado
* SELECT * FROM empleados;
* Los titulos de las revistas
* SELECT titulo FROM revista;
* Los nombres, apellidos y especialidad de los periodostas
* SELECT nombre_periodista,apellidos_periodista,especialidad FROM periodistas;
* Muestra los empleados que estan en x sucursal
* SELECT nombre_empleado,codigo_de_sucursal
FROM empleados INNER JOIN sucursal ON empleados.codigo_de_sucursal1=sucursal.codigo_de_sucursal;
* Muestra que periodistas colaboraron en x revista y en que sucursal se publico la revista
* SELECT nombre_periodista,numero_de_registro FROM periodistas INNER JOIN revista ON periodistas.nombre_periodista=revista.numero_de_registro;
* 
* Mustra que seccion esta en x revista, en que sucursal se imprimio y que empleados estan en esa sucursal.
* En la tabla peridistas muestra solo los que escriban sobre cine
* De la tabla revistas muestra las que sean de publicacion quincenal
* Muestra el nombre de ka revista que se hayan impreso despues del 30 de septiembre del 2021
* Muestra el nombre de la revista que se haya publicado en la sucursal 1 cuyos ejemplares tengan más de 80 páginas.

https://www.db-fiddle.com/f/iAUjGLoFoHtam2pK68Xh1B/1

