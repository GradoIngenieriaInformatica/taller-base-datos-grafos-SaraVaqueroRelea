MATCH (p:Persona)-[*1..]-(pr:Proyecto)
RETURN DISTINCT p.nombre