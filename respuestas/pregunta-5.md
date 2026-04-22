MATCH (e:Empresa)
WITH collect(e) AS empresas
MATCH (p:Persona)
WHERE ALL(emp IN empresas WHERE
    EXISTS {
        MATCH (p)-[:AMIGO_DE]->(:Persona)-[:TRABAJA_EN]->(emp)
    }
)
RETURN p.nombre