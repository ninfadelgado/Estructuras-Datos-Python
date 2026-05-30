# Conclusiones

## Principio fundamental

!!! success "Regla de oro"
    No existe una estructura de datos universalmente superior. Cada estructura fue diseñada para optimizar determinadas operaciones.

    Al elegir una estructura de datos, la pregunta más importante es:

    **¿Qué operación realizaré con mayor frecuencia?**

---

## Recomendaciones generales

### Utilice listas cuando
- Necesite flexibilidad.
- Requiera acceso por posición.
- Esté desarrollando soluciones generales.

### Utilice tuplas cuando
- Los datos no deban modificarse.
- Necesite claves compuestas para un diccionario.

### Utilice conjuntos cuando
- La unicidad sea importante.
- Las verificaciones de pertenencia sean muy frecuentes.

### Utilice diccionarios cuando
- La velocidad de búsqueda sea crítica.
- Los datos tengan nombres significativos.

### Utilice pilas cuando
- El último elemento agregado deba procesarse primero.
- Implemente lógica de deshacer/rehacer o recursión.

### Utilice colas cuando
- El procesamiento deba respetar el orden de llegada.

### Utilice listas enlazadas cuando
- Existan muchas inserciones y eliminaciones frecuentes.
- El tamaño varíe significativamente.

### Utilice Arrays NumPy cuando
- El rendimiento numérico sea prioritario.
- Trabaje con ciencia de datos o álgebra lineal.

### Utilice BST cuando
- Necesite mantener datos ordenados dinámicamente.
- Las búsquedas ordenadas sean frecuentes.

---

## Reflexión final

Una buena elección de estructura de datos puede simplificar enormemente un problema y mejorar significativamente el rendimiento de una solución.

El conocimiento de estas estructuras, sus fortalezas y sus limitaciones, es uno de los fundamentos del pensamiento computacional.
