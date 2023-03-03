# HERENCIA 

- Seguir el principio "es-un"
    - Es un Jefe un Empleado? Si = Jefe hereda de empleado
    - Es un empleado un jefe? NO = Empleado no hereda de jefe
    - Es Director un empleado? SI = Director hereda de empleado
- Uno tiende a poner el Director en la cúspide de la pirámide, pero en este caso es Empleado
- A medida que bajas en la pirámide de herencia, tienden a ser clases más específicas que hacen más tareas que las que se encuentran en la cúspide
- También me podría preguntar: un Director es un Jefe? SI = Jefe hereda de Empleado, Director hereda de Jefe
- Debo preguntarme cuales son las caracteristicas comunes dentro de mi aplicación
    - Todos tienen nombre, edad, fecha de alta en la empresa, salario
    - Comportamientos: todos van a trabajar, todos generan informes
---

## HERENCIA II

- Sintaxis