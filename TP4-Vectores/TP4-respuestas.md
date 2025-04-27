## Ejercicio 1: Crear y Consultar 

### Crea un documento nuevo con el texto:  `"La gravedad es una fuerza fundamental en el universo."`

### Realiza una consulta para encontrar documentos similares a la frase: `"Fuerzas naturales que gobiernan el cosmos".` 

### ¿Qué tipo de operación CRUD usaste primero? 
La primera operación utilizada fue create_example() para crear el documento requisitado.

### ¿Cuál es el ID del documento creado? (Usa collection.peek()). 
No fue possible buscar el ID del documento correcto ya que collection.peek() devuelve solo una muestra de documentos.
Para ese fin, fue utilizado collection.query() y hizo la busqueda por el texto para encontrar el ID con el codigo abajo:

`ID: ca601395-c2b2-4d4e-a409-c2ecdfa915d0`

Sigue parte del codigo que hace la busqueda en la opcion 2:

```python
query_emb = get_embeddings(query)
results = collection.query(
    query_embeddings=[query_emb],
    n_results=1
)   
```


### Explica por qué el documento aparece como coincidencia en la consulta. 

El motor de búsqueda de vectores trabaja basándose en similaridad semántica, no necesariamente trae los resultados altamente relacionados con la busqueda, si no hay control de score mínimo, puede traer resultados debiles.

## Ejercicio 2: Actualizar y Eliminar 

### Crea un documento con el texto: `"Redes neuronales imitan procesos cerebrales". `

### Encuentra su ID, luego actualízalo por: `"Deep Learning es un subcampo de IA con redes neuronales profundas".`
### Elimina el documento original usando el mismo ID. 

### ¿Qué ocurre si intentas actualizar un documento eliminado? 
Al intentar actualizar el documento eliminado, solo avisa que el documento ya no existe y se crea un nuevo documento con el contenido nuevo.

### ¿Cómo se garantiza la integridad de los datos en las operaciones? 
Para garantizar la integridad, hay que implementar la condición de validar si el dato existe y está grabado exitosamente como un prerequisito para la actualización, en ese caso, la actualización del documento se hace mismo si el documento original no existe, sin condiciones adicionales.

## Ejercicio 3: Errores y Validación 

### Intenta eliminar un documento con el ID "no_existe". 
### Crea un nuevo documento sin usar get_embeddings() (ejemplo: enviar un array vacío). 
### ¿Qué errores ocurren en cada caso? 

En el caso del documento con ID "no_existe", se informó que el documento inexistente con el ID fue borrado.

En el caso del intento de la creación del documento con el array vacío, fue intentado crear pasando `embedding = []` como parametro en la creación del documento y falló la creación con el error:

chromadb.errors.InvalidDimensionException: Dimensionality of (0) does not match indexdimensionality (384)

### ¿Cómo prevenir estos problemas? 
En el caso del borrado de documento con ID "no_existe", se puede implementar un chequeo de la existencia del documento antes de la ejecución del proceso de borrado.

En el caso del intento de la creación del documento con el array vacío, se puede implementar la condición de prerequisito que el valor de los embeddings sea existentes y diferentes de un array vacio. 

## Ejercicio 4: Consultas por Tema 

### Crea tres documentos: 
`"Python es ideal para ciencia de datos"`

`"JavaScript maneja interacciones web dinámicas"`

`"Java se usa en aplicaciones empresariales"`

### Realiza una consulta por la frase: "Lenguajes backend y frontend". 
### ¿Cuáles documentos aparecen como coincidencias? 

Los documentos que coinciden son:

`lenguaje natural (PNL) es un campo de la inteligencia artificial que se centra en la comprensión y generación del lenguaje humano. Los embeddings son una herramienta fundamental en muchas tareas de PNL.`

`Los sistemas de recomendación utilizan bases de datos vectoriales para encontrar elementos similares a los que un usuario ha mostrado interés previamente. Esto permite ofrecer sugerencias personalizadas de productos, películas o música.`

### Analiza cómo las palabras clave influyen en los resultados. 

La busqueda por la frase "Lenguajes backend y frontend" resultó en documentos con similitud cercana a las palabras "lenguaje" o con poca similitud.

En ese caso, para realizar la busqueda por los tres documentos agregados, hay que realizar la busqueda de una palabra mas cercana al contenido del texto como por ejemplo "java" o "python", donde la similitud semántica será mayor y, consecuentemente, el resultado será más preciso.

## Ejercicio 5: Eliminaciones Selectivas 

### Crea dos documentos con tópicos opuestos (ejemplo: uno sobre "Ecología" y otro sobre "Minería de datos").
`"La ecología estudia las interacciones entre los organismos y su entorno natural."`

`"La minería de datos extrae patrones útiles de grandes volúmenes de información."`

### Elimina el documento sobre ecología usando su ID. 
### Verifica que solo quede un documento. 

### ¿Cómo usar collection.count() para confirmar? 
Se puede implementar el contaje de registros antes de la creación para validar que no se duplicó registros y realizar el chequeo despues del borrado para validar si el registro fue borrado exitosamente volviendo a la cantidad original.

Ejemplo de codigo implementado en la creación del documento:

```python
def create_example(new_doc):
    """Añadir un documento nuevo"""
    embedding = get_embeddings(new_doc)
    #embedding = [] # Array vacio para pruebas
    doc_id = str(uuid.uuid4())
    metadata = {"source": "nuevo_documento.txt"}
    
    print(f"Total original de documentos en la colección: {collection.count()}")
    collection.add(
        documents=[new_doc],
        embeddings=[embedding],
        metadatas=[metadata],
        ids=[doc_id]
    )
    print(f"✅ Documento añadido con ID: {doc_id}")
    print(f"Total de documentos en la colección actualizado: {collection.count()}")
```

Ejemplo de codigo implementado en el borrado del documento:

```python
def delete_example(doc_id):
    """Eliminar por ID"""
    print(f"Total de documentos en la colección antes del borrado: {collection.count()}")
    collection.delete(ids=[doc_id])
    print(f"🗑️ Documento con ID '{doc_id}' eliminado.")
    print(f"Total de documentos en la colección despues de borrar: {collection.count()}")
```

## Ejercicio 6: Actualización en Cadena 

### Crea un documento con el texto "IA y ética son temas actuales". 

### Actualízalo dos veces: 
### Primera actualización: `"Ética en IA aborda dilemas morales"`
### Segunda actualización: `"El uso de IA debe estar regulado por principios éticos".` 

### ¿Cómo sigue evolucionando el contenido del documento con cada update? 

1. Primer paso (Creación del documento):

    ```
    Texto: "IA y ética son temas actuales"
    Embedding: Calculado para este texto.
    ID: Nuevo ID generado.
    
    Resultado: La colección tendrá un solo documento con este contenido y un ID nuevo específico.
    ```

2. Primera actualización:
    ```
    El documento con el texto "IA y ética son temas actuales" es eliminado.
    El nuevo texto "Ética en IA aborda dilemas morales" se agrega con un nuevo ID.

    Resultado: La colección ahora tendrá un documento con el nuevo contenido y un nuevo ID, reemplazando el anterior.
    ```

3. Segunda actualización (utilizando el mismo ID del primer paso):

    ```
    El documento con el texto "IA y ética son temas actuales" ya no existe y mismo así avisa que un documento no existente fue eliminado.

    El nuevo texto "El uso de IA debe estar regulado por principios éticos" se agrega con un nuevo ID.

    Resultado: La colección tendrá los dos documentos de la primera actualización y la segunda actualización cada uno con su texto y un ID distinto.
    ```


## Ejercicio 7: Consultas Ambiguas 

### Crea dos documentos similares pero no idénticos: 
`"Blockchain garantiza transacciones seguras"`

`"Criptomonedas usan tecnología blockchain".` 

### Realiza una consulta por `"Seguridad en finanzas digitales"`. 
### ¿Ambos documentos aparecen? Explica la similitud semántica. 

No, el unico documento que se encuentra con similitud es "Blockchain garantiza transacciones seguras", pues hay una similitud semantica con las palabras "seguras" y "seguridad", ya el otro documento no poseé ninguna similitud.

## Ejercicio 8: Reiniciar Base de Datos 

### Elimina todos los documentos usando delete() con el parámetro correcto.

Se implementó una mejora en el codigo para busqueda de todos los documentos y borrado utilizando el metodo delete() cuando se pasa como parametro la palabra "all_documents" como el ID:

```python
def delete_example(doc_id):
    if doc_id == 'all_documents':
        neutral_embedding = [0.0] * 384
        results = collection.query(
            query_embeddings=[neutral_embedding],  # embedding neutro para traer resultados.
            n_results=1000 
        )
        doc_ids = results["ids"][0] 
        if doc_ids:
            """Eliminar todos los documentos"""
            print(f"Total de documentos en la colección antes del borrado: {collection.count()}")
            collection.delete(ids=doc_ids)
            print(f"🗑️ Todos los documentos fueran eliminados. Total actualizado: {collection.count()}")
        else:
            print("🗑️ No hay documentos a eliminar.")
    else:
        """Eliminar por ID"""
        print(f"Total de documentos en la colección antes del borrado: {collection.count()}")
        collection.delete(ids=[doc_id])
        print(f"🗑️ Documento con ID '{doc_id}' eliminado.")
        print(f"Total de documentos en la colección despues de borrar: {collection.count()}")
```

### Vuelve a cargar la base desde cero con crear_base_datos(). 
### ¿Cuántos documentos hay ahora? (Usa collection.count()). 

Utilizando el codigo abajo, se observó la cantidad total de 34 documentos:

```python
print(f"Total de documentos en la colección actualizado: {collection.count()}")
```

## Ejercicio 9: Errores de Inserción 

### Intenta crear un documento sin texto (ejemplo: cadena vacía). 
### Corrige el error usando la función get_embeddings(). 

Se corrige el error implementando un chequeo para no permitir una entrada vacia de datos como por ejemplo:

```python
# Verificar si el documento está vacío
    if not new_doc.strip():  # Si el texto está vacío o solo tiene espacios en blanco
        print("❌ El documento está vacío. No se puede agregar.")
        return
```
### ¿Qué lección aprendemos sobre los requisitos de ChromaDB? 

ChromaDB requiere que los documentos tengan un contenido válido. Si un documento tiene un texto vacío, se debe validar antes de proceder con la inserción, ya que no tiene sentido generar un embedding a partir de un texto vacío.
El embedding generado para cada documento debe tener una dimensionalidad que coincida con la dimensionalidad de la collection y también es importante siempre validar los datos antes de intentar insertarlos en la base de datos.
