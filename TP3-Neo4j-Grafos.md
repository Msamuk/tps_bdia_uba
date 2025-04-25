1. Obtener los nodos de todas las personas de la red. 

`MATCH (p:Persona) RETURN p`

Result: 
```json
[
  {
    "p": {
      "identity": 0,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Corrado",
        "fechanac": "01/08/1966",
        "nombre": "Gustavo",
        "email": "gustavo.corrado@gmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:0"
    }
  },
  {
    "p": {
      "identity": 1,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Díaz",
        "fechanac": "10/12/1978",
        "nombre": "Analía",
        "email": "adiaz@hotmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:1"
    }
  },
  {
    "p": {
      "identity": 2,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Dominguez",
        "fechanac": "31/10/1990",
        "nombre": "Mariana",
        "email": "mariana@yahoo.com",
        "pais": "Chile"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:2"
    }
  },
  {
    "p": {
      "identity": 3,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Pereyra",
        "fechanac": "18/05/1993",
        "nombre": "Claudio",
        "email": "cpereyra30@yahoo.com.ar",
        "pais": "Estados Unidos"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:3"
    }
  },
  {
    "p": {
      "identity": 4,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "López",
        "fechanac": "11/02/1970",
        "nombre": "Mario",
        "email": "mario.lopez@gmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:4"
    }
  },
  {
    "p": {
      "identity": 5,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Ferreira",
        "fechanac": "07/04/1972",
        "nombre": "Natalia",
        "email": "nf@hotmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:5"
    }
  },
  {
    "p": {
      "identity": 6,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "García",
        "fechanac": "23/01/1985",
        "nombre": "Eduardo",
        "email": "garcia@live.com.ar",
        "pais": "Chile"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:6"
    }
  },
  {
    "p": {
      "identity": 7,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "González",
        "fechanac": "09/11/1974",
        "nombre": "Bibiana",
        "email": "bibiana@live.com.ar",
        "pais": "España"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:7"
    }
  },
  {
    "p": {
      "identity": 8,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Lupis",
        "fechanac": "27/09/1980",
        "nombre": "Jorge",
        "email": "jlup@gmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:8"
    }
  },
  {
    "p": {
      "identity": 9,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Mendez",
        "fechanac": "28/02/1968",
        "nombre": "Verónica",
        "email": "veromendi@yahoo.com.ar",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:9"
    }
  }
]
```

2. Obtener el nombre y fecha de nacimiento de la persona de apellido Domínguez. 

`MATCH (p:Persona {apellido: "Dominguez"}) RETURN p.nombre AS nombre, p.fechanac AS fecha_de_nacimiento`

Result:
```json
[
  {
    "nombre": "Mariana",
    "fecha_de_nacimiento": "31/10/1990"
  }
]
```

3. Obtener la lista de empresas en las que trabajó Domínguez. 

```sql
MATCH (p:Persona {apellido: "Dominguez"})-[t:TRABAJO]->(e:Empresa)
RETURN e.nombre AS empresa, 
       t.fechad AS desde, 
       t.fechah AS hasta, 
       t.puesto AS puesto 
```

Result:
```json
[
  {
    "empresa": "Lan",
    "desde": "01/12/2005",
    "hasta": null,
    "puesto": "Supervisor área Legales"
  },
  {
    "empresa": "Banco Nación",
    "desde": "01/04/2001",
    "hasta": "01/07/2001",
    "puesto": "Abogado Jr."
  },
  {
    "empresa": "Claro",
    "desde": "01/08/2001",
    "hasta": "01/11/2005",
    "puesto": "Abogado Sr."
  }
]
```

4. Obtener la lista de personas que estudiaron carreras que no son de nivel 
“Universitario” y los nombres de las carreras. 

```sql
MATCH (p:Persona)-[:ESTUDIO]->(c:Carrera)
WHERE c.nivel <> "Universitario"
RETURN p.nombre + ' ' + p.apellido AS persona, c.nombre AS carrera, c.nivel AS nivel
```

Result:

```json
[
  {
    "persona": "Mario López",
    "carrera": "Comercialización",
    "nivel": "Terciario"
  },
  {
    "persona": "Mario López",
    "carrera": "MBA",
    "nivel": "Postgrado"
  },
  {
    "persona": "Jorge Lupis",
    "carrera": "MBA",
    "nivel": "Postgrado"
  },
  {
    "persona": "Eduardo García",
    "carrera": "Tec. En Programación",
    "nivel": "Terciario"
  }
]
```

5. Obtener los nodos etiquetados como Conocimiento. 

```sql
MATCH (c:Conocimiento) RETURN c
```

Result truncated:
```json
[
  {
    "c": {
      "identity": 21,
      "labels": [
        "Conocimiento"
      ],
      "properties": {
        "nombre": "PHP"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:21"
    }
  },
  {
    "c": {
      "identity": 22,
      "labels": [
        "Conocimiento"
      ],
      "properties": {
        "nombre": "Java"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:22"
    }
  },
  {
    "c": {
      "identity": 23,
      "labels": [
        "Conocimiento"
      ],
      "properties": {
        "nombre": "Análisis Funcional"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:23"
    }
  },
  {
    "c": {
      "identity": 24,
      "labels": [
        "Conocimiento"
      ],
      "properties": {
        "nombre": "Gestión de proyectos"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:24"
    }
  },
  {
    "c": {
      "identity": 25,
      "labels": [
        "Conocimiento"
      ],
      "properties": {
        "nombre": "Revisión y elaboración de contratos"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:25"
    }
  }
  ...
]


6. Obtener los nodos de todas las personas con nombre terminado en a. 

```sql
MATCH (p:Persona) WHERE p.nombre =~ ".*a" RETURN p
```

Result: 

```json
[
  {
    "p": {
      "identity": 1,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Díaz",
        "fechanac": "10/12/1978",
        "nombre": "Analía",
        "email": "adiaz@hotmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:1"
    }
  },
  {
    "p": {
      "identity": 2,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Dominguez",
        "fechanac": "31/10/1990",
        "nombre": "Mariana",
        "email": "mariana@yahoo.com",
        "pais": "Chile"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:2"
    }
  },
  {
    "p": {
      "identity": 5,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Ferreira",
        "fechanac": "07/04/1972",
        "nombre": "Natalia",
        "email": "nf@hotmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:5"
    }
  },
  {
    "p": {
      "identity": 7,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "González",
        "fechanac": "09/11/1974",
        "nombre": "Bibiana",
        "email": "bibiana@live.com.ar",
        "pais": "España"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:7"
    }
  },
  {
    "p": {
      "identity": 9,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Mendez",
        "fechanac": "28/02/1968",
        "nombre": "Verónica",
        "email": "veromendi@yahoo.com.ar",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:9"
    }
  }
]
```

7. Crear un nodo para la persona Analía Martinelli si no existe. 

```sql
MERGE (p:Persona { nombre: "Analía", apellido: "Martinelli" })
ON CREATE SET p.email = "amartinelli@empresaeejemplo123.com",
              p.fechanac = "15/09/1982",
              p.pais = "Argentina"
```

8. Asociar un conocimiento "Cálculo" a Analía Martinelli si no lo posee. 

// Crea el conocimiento
MERGE (c:Conocimiento { nombre: "Cálculo" })

// Aseguramos que exista la persona
MERGE (p:Persona { nombre: "Analía", apellido: "Martinelli" })

// Creamos la relación
MERGE (p)-[:POSEE]->(c)

9. Verificar si se creó duplicado del conocimiento "Cálculo". 

```sql
MATCH (c:Conocimiento {nombre: 'Cálculo'})
RETURN c.nombre, COUNT(c) as count
```
```json
[
  {
    "c.nombre": "Cálculo",
    "count": 1
  }
]
```

10. Crear una relación ESTUDIO para Analía Martinelli con la carrera "Lic en Sist de Inf", 
estado "En curso". 

```sql
MERGE (a:Persona {nombre: "Analía", apellido: "Martinelli"})
MERGE (c:Carrera {nombre: 'Lic en Sist de Inf'})
MERGE (a)-[r:ESTUDIA]->(c) SET r.estado = 'En curso'
```

11. Crear un nodo para Verónica Mendez. 

MERGE (p:Persona { nombre: "Verónica", apellido: "Mendez" })

12. Crear una relación CONOCE_A entre Analía y Verónica, asegurando que solo se 
cree una vez. 
```sql
MATCH (a:Persona {nombre: "Analía", apellido: "Martinelli"}), (v:Persona {nombre: "Verónica", apellido: "Mendez"}) 
MERGE (a)-[:CONOCE_A]->(v)
```

13. Actualizar o crear el nodo de Analía Martinelli con fecha de nacimiento 30/06/1968. 

```sql
MERGE (a:Persona {nombre: "Analía", apellido: "Martinelli"})
SET a.fechanac = '1968-06-30'
```

14. Agregarle la etiqueta "Empleado" y el país Argentina a Analía. 

```sql
MERGE (a:Persona {nombre: "Analía", apellido: "Martinelli"})
SET a.pais = 'Argentina'
SET a:Empleado
```

15. Eliminar la fecha de nacimiento y la etiqueta Persona de Analía. 

```sql
MATCH (a:Persona {nombre: "Analía", apellido: "Martinelli"})
REMOVE a:Persona, a.fechanac
```

16. Eliminar el nodo de Analía y todas sus relaciones. 

```sql
MATCH (a:Persona {nombre: "Analía", apellido: "Martinelli"})
DETACH DELETE a
```

17. Contar los nodos en total. 

```sql
MATCH (n)  
RETURN count(n) AS total_nodos
```

Result:

```json
[
  {
    "total_nodos": 61
  }
]
```

18. Contar los tipos de relaciones. 
```sql
MATCH ()-[r]->()  
RETURN type(r) AS tipo_relacion, count(*) AS cantidad
```

```json
[
  {
    "tipo_relacion": "TRABAJO",
    "cantidad": 22
  },
  {
    "tipo_relacion": "POSEE",
    "cantidad": 34
  },
  {
    "tipo_relacion": "ESTUDIO",
    "cantidad": 11
  },
  {
    "tipo_relacion": "CONOCE_A",
    "cantidad": 6
  },
  {
    "tipo_relacion": "DICTADA_EN",
    "cantidad": 9
  },
  {
    "tipo_relacion": "ESTUDIA",
    "cantidad": 1
  }
]
```

19. Listar todos los nodos y sus relaciones. 

```sql
MATCH (a)-[r]->(b)
RETURN a, type(r) AS relacion, b
```
Result truncated:

```json
[
  {
    "a": {
      "identity": 0,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Corrado",
        "fechanac": "01/08/1966",
        "nombre": "Gustavo",
        "email": "gustavo.corrado@gmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:0"
    },
    "relacion": "TRABAJO",
    "b": {
      "identity": 10,
      "labels": [
        "Empresa"
      ],
      "properties": {
        "rubro": "Telefonía",
        "ubicacion": "Argentina",
        "id": "1",
        "nombre": "Telefónica de Argentina",
        "tamano": "Grande"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:10"
    }
  },
  {
    "a": {
      "identity": 0,
      "labels": [
        "Persona"
      ],
      "properties": {
        "apellido": "Corrado",
        "fechanac": "01/08/1966",
        "nombre": "Gustavo",
        "email": "gustavo.corrado@gmail.com",
        "pais": "Argentina"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:0"
    },
    "relacion": "TRABAJO",
    "b": {
      "identity": 11,
      "labels": [
        "Empresa"
      ],
      "properties": {
        "rubro": "Consultoría",
        "ubicacion": "Argentina",
        "id": "2",
        "nombre": "Accenture",
        "tamano": "Grande"
      },
      "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:11"
    }
  }
]
```

20. Obtener los nombres y rubros de las empresas registradas, reemplazando el rubro 
"Telefonía" por IT. 

```sql
MATCH (e:Empresa)
RETURN 
  e.nombre AS nombre, 
  CASE 
    WHEN e.rubro = "Telefonía" THEN "IT" 
    ELSE e.rubro 
  END AS rubro
```

Result:

```json
[
  {
    "nombre": "Telefónica de Argentina",
    "rubro": "IT"
  },
  {
    "nombre": "Accenture",
    "rubro": "Consultoría"
  },
  {
    "nombre": "CSF",
    "rubro": "Gestión de Información Farmacéutica"
  },
  {
    "nombre": "Chevron",
    "rubro": "Petrolera"
  },
  {
    "nombre": "Lan",
    "rubro": "Aviación"
  },
  {
    "nombre": "Gomez & Asoc",
    "rubro": "Reventa"
  },
  {
    "nombre": "Alteon",
    "rubro": "Capacitación"
  },
  {
    "nombre": "IBM",
    "rubro": "IT"
  },
  {
    "nombre": "Banco Nación",
    "rubro": "Banco"
  },
  {
    "nombre": "Carrefour",
    "rubro": "Supermercado"
  },
  {
    "nombre": "Claro",
    "rubro": "IT"
  }
]
```

21. Determinar qué etiquetas tienen los nodos que son destino de la relación ESTUDIO. 

```sql
MATCH (:Persona)-[:ESTUDIO]->(destino)
RETURN DISTINCT labels(destino) AS etiquetas
```

Result:
```json
[
  {
    "etiquetas": [
      "Carrera"
    ]
  }
]
```

22. Verificar las etiquetas de la carrera en la relación ESTUDIO. 

```sql
MATCH (:Persona)-[:ESTUDIO]->(carrera)
RETURN DISTINCT labels(carrera) AS etiquetas_carrera
```
Result:
```json
[
  {
    "etiquetas_carrera": [
      "Carrera"
    ]
  }
]
```

23. Usar UNWIND para transformar una colección en filas individuales. 

```sql
MATCH (p:Persona) WHERE p.pais = "Argentina"
UNWIND p.pais AS pais
RETURN p.nombre,p.apellido, pais
```

Result:

```json
[
  {
    "p.nombre": "Gustavo",
    "p.apellido": "Corrado",
    "pais": "Argentina"
  },
  {
    "p.nombre": "Analía",
    "p.apellido": "Díaz",
    "pais": "Argentina"
  },
  {
    "p.nombre": "Mario",
    "p.apellido": "López",
    "pais": "Argentina"
  },
  {
    "p.nombre": "Natalia",
    "p.apellido": "Ferreira",
    "pais": "Argentina"
  },
  {
    "p.nombre": "Jorge",
    "p.apellido": "Lupis",
    "pais": "Argentina"
  },
  {
    "p.nombre": "Verónica",
    "p.apellido": "Mendez",
    "pais": "Argentina"
  },
  {
    "p.nombre": "Analía Martinelli",
    "p.apellido": null,
    "pais": "Argentina"
  }
]
```

24. Contar la cantidad de personas que estudiaron una carrera en cualquier estado. 

```sql
MATCH (p:Persona)-[:ESTUDIO]->(:Carrera)
RETURN count(DISTINCT p) AS cantidad_personas
```
Result:

```json
[
  {
    "cantidad_personas": 8
  }
]
```
25. Identificar si puede llegarse directa o indirectamente desde Mario López hasta Jorge 
Lupis mediante la relación CONOCE_A. 

```sql
MATCH (m:Persona {nombre: "Mario", apellido: "López"}), (j:Persona {nombre: "Jorge", apellido: "Lupis"})
MATCH path = (m)-[:CONOCE_A*]->(j)
RETURN path
LIMIT 1
```

Result:

Vacio.


26. Obtener el camino más corto entre Gustavo y Mario en la relación CONOCE_A. 

```sql
MATCH (g:Persona {nombre: "Gustavo"}), (m:Persona {nombre: "Mario"})
MATCH path = shortestPath((g)-[:CONOCE_A*]-(m))
RETURN path
```
Result: 
```json
[
  {
    "path": {
      "start": {
        "identity": 0,
        "labels": [
          "Persona"
        ],
        "properties": {
          "apellido": "Corrado",
          "fechanac": "01/08/1966",
          "nombre": "Gustavo",
          "email": "gustavo.corrado@gmail.com",
          "pais": "Argentina"
        },
        "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:0"
      },
      "end": {
        "identity": 4,
        "labels": [
          "Persona"
        ],
        "properties": {
          "apellido": "López",
          "fechanac": "11/02/1970",
          "nombre": "Mario",
          "email": "mario.lopez@gmail.com",
          "pais": "Argentina"
        },
        "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:4"
      },
      "segments": [
        {
          "start": {
            "identity": 0,
            "labels": [
              "Persona"
            ],
            "properties": {
              "apellido": "Corrado",
              "fechanac": "01/08/1966",
              "nombre": "Gustavo",
              "email": "gustavo.corrado@gmail.com",
              "pais": "Argentina"
            },
            "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:0"
          },
          "relationship": {
            "identity": 1155177702467043328,
            "start": 0,
            "end": 8,
            "type": "CONOCE_A",
            "properties": {
              "motivo": "Estudio",
              "fechad": "1994"
            },
            "elementId": "5:76fabbc7-4da8-4469-ba6f-eda164723fc0:1155177702467043328",
            "startNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:0",
            "endNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:8"
          },
          "end": {
            "identity": 8,
            "labels": [
              "Persona"
            ],
            "properties": {
              "apellido": "Lupis",
              "fechanac": "27/09/1980",
              "nombre": "Jorge",
              "email": "jlup@gmail.com",
              "pais": "Argentina"
            },
            "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:8"
          }
        },
        {
          "start": {
            "identity": 8,
            "labels": [
              "Persona"
            ],
            "properties": {
              "apellido": "Lupis",
              "fechanac": "27/09/1980",
              "nombre": "Jorge",
              "email": "jlup@gmail.com",
              "pais": "Argentina"
            },
            "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:8"
          },
          "relationship": {
            "identity": 1152925902653358088,
            "start": 8,
            "end": 4,
            "type": "CONOCE_A",
            "properties": {
              "motivo": "Estudio",
              "fechad": "1994"
            },
            "elementId": "5:76fabbc7-4da8-4469-ba6f-eda164723fc0:1152925902653358088",
            "startNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:8",
            "endNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:4"
          },
          "end": {
            "identity": 4,
            "labels": [
              "Persona"
            ],
            "properties": {
              "apellido": "López",
              "fechanac": "11/02/1970",
              "nombre": "Mario",
              "email": "mario.lopez@gmail.com",
              "pais": "Argentina"
            },
            "elementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:4"
          }
        }
      ],
      "length": 2.0
    }
  }
]
```

27. Listar los caminos de relaciones de un camino determinado. 

```sql
MATCH path = (a:Persona {nombre: "Gustavo"})-[:CONOCE_A*]->(b:Persona {nombre: "Mario"})
RETURN relationships(path) AS relaciones
```

Result:

```json
[
  {
    "relaciones": [
      {
        "identity": 1155177702467043328,
        "start": 0,
        "end": 8,
        "type": "CONOCE_A",
        "properties": {
          "motivo": "Estudio",
          "fechad": "1994"
        },
        "elementId": "5:76fabbc7-4da8-4469-ba6f-eda164723fc0:1155177702467043328",
        "startNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:0",
        "endNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:8"
      },
      {
        "identity": 1152925902653358088,
        "start": 8,
        "end": 4,
        "type": "CONOCE_A",
        "properties": {
          "motivo": "Estudio",
          "fechad": "1994"
        },
        "elementId": "5:76fabbc7-4da8-4469-ba6f-eda164723fc0:1152925902653358088",
        "startNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:8",
        "endNodeElementId": "4:76fabbc7-4da8-4469-ba6f-eda164723fc0:4"
      }
    ]
  }
]
```

28. Verificar si una persona trabajó o trabajó en empresas que otro determinado 
profesional trabajo, para sugerir contactos. 

```sql
MATCH (a:Persona {nombre: "Verónica", apellido: "Mendez"})-[:TRABAJO]->(empresa:Empresa)<-[:TRABAJO]-(b:Persona {nombre: "Gustavo"})
RETURN empresa.nombre AS empresaCompartida
```

Result: 

```json
[
  {
    "empresaCompartida": "Telefónica de Argentina"
  },
  {
    "empresaCompartida": "Accenture"
  }
]
```

29. Obtener los conocimientos más compartidos en cada carrera. 

```sql
MATCH (p:Persona)-[:ESTUDIO]->(c:Carrera)<-[:ESTUDIO]-(otra_person:Persona),
      (p)-[:POSEE]->(k:Conocimiento),
      (otra_person)-[:POSEE]->(k)
WITH c.nombre AS carrera, k.nombre AS conocimiento, count(DISTINCT otra_person) AS cantidad
ORDER BY carrera, cantidad DESC
WITH carrera, collect({conocimiento: conocimiento, cantidad: cantidad}) AS conocimientos
RETURN carrera, conocimientos[0] AS conocimiento_mas_compartido
```

Result:

```json
[
  {
    "carrera": "Ing en Sistemas de Información",
    "conocimiento_mas_compartido": {
      "cantidad": 3,
      "conocimiento": "Java"
    }
  }
]
```
30. Ranking de los primeros 2 conocimientos de la carrera "Ing en Sistemas de 
Información". 

```sql
MATCH (p:Persona)-[:ESTUDIO]->(c:Carrera {nombre: "Ing en Sistemas de Información"}),
      (p)-[:POSEE]->(k:Conocimiento)
WITH k.nombre AS conocimiento, count(DISTINCT p) AS cantidad
ORDER BY cantidad DESC
LIMIT 2
RETURN conocimiento, cantidad
```
Result:
```json
[
  {
    "conocimiento": "Java",
    "cantidad": 3
  },
  {
    "conocimiento": "Análisis Funcional",
    "cantidad": 3
  }
]
```