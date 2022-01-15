1. Escriba una consulta que devuelva la cantidad de profesores que dictan más de un curso en el turno Noche.

__SELECT p.id AS 'Id del profesor',  
COUNT("a") AS 'Cantidad de cursos que da'  
FROM profesor p INNER JOIN curso c ON c.PROFESOR_id = p.id  
WHERE c.turno = 'Noche'  
GROUP BY p.nombre HAVING COUNT("a") > 1;__

2. Escriba una consulta para obtener la información de todos los estudiantes que no realizan el curso con código 105.

__SELECT *  
FROM estudiante e INNER JOIN inscripcion i on e.legajo = i.ESTUDIANTE_legajo  
WHERE i.CURSO_codigo != 105  
GROUP BY e.legajo;__
