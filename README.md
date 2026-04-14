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

` SELECT apellidos_empleado AS Apellidos FROM Empleado WHERE apellidos_empleado = 'Gomez';
 `

![Consulta 3](img/consulta3.png "Consulta 3")