MATCH (p:Persona)-[:TRABAJA_EN]->(e:Empresa)
RETURN e.nombre, COUNT(p) AS num_empleados