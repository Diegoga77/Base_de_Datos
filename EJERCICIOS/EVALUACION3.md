
## Práctica 4
### Data warehouse

Objetivo: Demostrar la identificación de los elementos que componen data warehouse y
su esquema

Ejercicio:

1. ¿Qué es un DataWarehouse?(valor 2)

Es un sistema que agrega y combina información de diferentes fuentes en un almacén de datos único y centralizado; consistente para respaldar el análisis empresarial, la minería de datos, inteligencia artificial y Machine Learning. Data warehouse permite a una organización o empresa ejecutar análisis potentes en grandes volúmenes petabytes y petabytes de datos históricos de formas que una base de datos estándar simplemente no puede.

2. Realiza un diseño del modelo en estrella (valor 2)

![image](https://user-images.githubusercontent.com/104279937/173208916-ce1c80d3-d72f-4c17-9f4c-24e64a0455d0.png)

3. Realiza un diseño del modelo copo de nieve (valor 2)

<img width="592" alt="image" src="https://user-images.githubusercontent.com/104279937/173972139-eae2d6a8-2c2f-4b1d-8cb8-a05f2e5dbb16.png">


## Práctica 7
### Funciones en SQL
Objetivo: Demostrar el uso y aplicación en una base de datos para mejorar la gestión

Ejercicio:

1. Calcula el número total de productos que hay en la tabla productos. (valor 4.5)

SELECT COUNT(id producto) FROM producto;

2. Muestra el número total de productos que tiene cada uno de los fabricantes. El listado
también debe incluir los fabricantes que no tienen ningún producto. El resultado
mostrará dos columnas, una con el nombre del fabricante y otra con el número de
productos que tiene. Ordene el resultado descendentemente por el número de
productos. (valor 4.5)

3. Muestra el precio máximo, precio mínimo y precio medio de los productos de cada
uno de los fabricantes. El resultado mostrará el nombre del fabricante junto con los
datos que se solicitan. (valor 4.5)

4. Muestra el nombre de cada fabricante, junto con el precio máximo, precio mínimo,
precio medio y el número total de productos de los fabricantes que tienen un precio
medio superior a 200€. Es necesario mostrar el nombre del fabricante. (valor 4.5)


