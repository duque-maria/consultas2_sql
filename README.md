# Consultas SQL - Taller

## Modelo físico de la BD
**Implementado en phpMyAdmin**

![Modelo fisico](img/BDFisica.png "Modelo fisico")

## Tabla Departamento
**Poblada con los datos indicados, en phpMyAdmin**

![Tabla departamento](img/tabla_departameto.png "Tabla departamento")


## Estructura Empleado
![Empleados](img/estructuraEMPLEADO.png "Empleados")

# Consultas SQL

1. Obtener la lista de los apellidos de todos los empleados.

` SELECT apellidos_empleado AS Apellidos FROM Empleado;
 `

![Consulta 1](img/consulta1.png "Consulta 1")

2. Obtener los apellidos de todos los empleados sin repeticiones.

` SELECT DISTINCT apellidos_empleado FROM Empleado;
 `

![Consulta 2](img/consulta2.png "Consulta 2")

3. Obtener todos los datos de los empleados que se apellidan 'Gomez'.

` SELECT apellidos_empleado AS Apellidos FROM Empleado WHERE apellidos_empleado = 'Gomez'; `

![Consulta 3](img/consulta3.png "Consulta 3")

4. Obtener todos los datos de los empleados que se apellidan "Diaz" y los que se apellidan "Rodriguez".  Usar OR o IN

` SELECT apellidos_empleado AS Apellidos FROM Empleado WHERE apellidos_empleado LIKE 'Diaz%' OR apellidos_empleado LIKE 'Rodriguez%'; `

![Consulta 4](img/consulta4.png "Consulta 4")

5. Obtener los nombres de los empleados que trabajan en el departamento 11

` SELECT nombre_empleado AS Empleado FROM Empleado WHERE id_departamento = 11; ` 

![Consulta 5](img/consulta5.png "Consulta 5")

6. Obtener todos los datos de los empleados cuyo apellido empiece por 'P'

` SELECT apellidos_empleado AS Apellido FROM Empleado WHERE apellidos_empleado LIKE 'P%'; `

![Consulta 6](img/consulta6.png "Consulta 6")

7. Obtener el presupuesto total de todos los departamentos.

` SELECT SUM(presupuesto_departamento) AS Presupuesto_Total FROM Departamento; `

![Consulta 7](img/consulta7.png "Consulta 7")

8. Obtener el número de empleados de cada departamento.

` SELECT id_departamento, COUNT(*) AS Numero_Empleados FROM Empleado GROUP BY id_departamento; `

![Consulta 8](img/consulta8.png "Consulta 8")

9. Obtener un listado completo de empleados, incluyendo por cada empleado los datos del empleado y de su departamento.

` SELECT e.*, d.* FROM Empleado e INNER JOIN Departamento d ON e.id_departamento = d.id_departamento; `

![Consulta 9](img/consulta9.png "Consulta 9")

10. Obtener un listado completo de empleados, incluyendo el nombre y apellidos del empleado junto al nombre y presupuesto de su departamento.

` SELECT e.nombre_empleado, e.apellidos_empleado, d.nombre_departamento, d.presupuesto_departamento FROM Empleado e INNER JOIN Departamento d ON e.id_departamento = d.id_departamento; `

![Consulta 10](img/consulta10.png "Consulta 10")

11. Obtener los nombres y apellidos de los empleados que trabajen en departamentos cuyo presupuesto sea mayor a 100000000

` SELECT e.nombre_empleado, e.apellidos_empleado FROM Empleado e INNER JOIN Departamento d ON e.id_departamento = d.id_departamento WHERE d.presupuesto_departamento > 100000000; `

![Consulta 11](img/consulta11.png "Consulta 11")