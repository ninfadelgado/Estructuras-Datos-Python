# Guía de Selección de Estructuras

## ¿Cómo elegir la estructura adecuada?

La mejor estructura depende de las operaciones que se ejecutarán con mayor frecuencia. Una estructura excelente para un problema puede ser una mala elección para otro.

---

## Árbol de decisión

```mermaid
flowchart TD
    A["Operación dominante"] --> B["Búsqueda rápida"]
    A --> C["Orden secuencial"]
    A --> D["Unicidad"]
    A --> E["Procesamiento LIFO"]
    A --> F["Procesamiento FIFO"]
    A --> G["Cálculo numérico"]
    B --> H["Diccionario / Conjunto"]
    C --> I["Lista / Tupla"]
    D --> J["Conjunto"]
    E --> K["Pila"]
    F --> L["Cola"]
    G --> M["Array NumPy"]
```

---

## Árbol de decisión extendido

```mermaid
flowchart TD
    A["¿Necesitas acceso por posición numérica?"] -->|Sí| B["¿Datos numéricos y alto rendimiento?"]
    B -->|Sí| C["Array NumPy"]
    B -->|No| D["Lista"]
    A -->|No| E["¿Necesitas clave → valor?"]
    E -->|Sí| F["Diccionario"]
    E -->|No| G["¿Necesitas elementos únicos?"]
    G -->|Sí| H["Conjunto"]
    G -->|No| I["¿Los datos deben ser inmutables?"]
    I -->|Sí| J["Tupla"]
    I -->|No| K["¿Procesamiento LIFO o FIFO?"]
    K -->|LIFO| L["Pila"]
    K -->|FIFO| M["Cola"]
```

---

## Comparación por escenarios

| Necesidad | Estructura recomendada |
|---|---|
| Acceso por índice | Lista |
| Datos inmutables | Tupla |
| Eliminar duplicados | Conjunto |
| Búsqueda por clave | Diccionario |
| Deshacer / Rehacer | Pila |
| Procesamiento por orden de llegada | Cola |
| Inserciones frecuentes al inicio | Lista enlazada |
| Cálculo numérico intensivo | Array NumPy |
| Datos ordenados dinámicamente | BST |
