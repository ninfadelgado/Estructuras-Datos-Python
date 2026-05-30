# Arrays NumPy

## ¿Qué son?

Los Arrays de NumPy son estructuras de datos especializadas para el procesamiento eficiente de datos numéricos. A diferencia de las listas tradicionales de Python, están diseñados para almacenar grandes cantidades de datos **homogéneos** y realizar operaciones matemáticas de forma extremadamente eficiente.

NumPy es una de las bibliotecas fundamentales del ecosistema científico de Python y constituye la base de herramientas como Pandas, Scikit-Learn, TensorFlow y SciPy.

---

## Almacenamiento contiguo en memoria

```mermaid
flowchart LR
    A["Dirección 0x00<br/>10"] --> B["Dirección 0x04<br/>20"]
    B --> C["Dirección 0x08<br/>30"]
    C --> D["Dirección 0x0C<br/>40"]
    D --> E["Dirección 0x10<br/>50"]
```

---

## Operaciones vectorizadas

```mermaid
flowchart LR
    A["Array original<br/>[1, 2, 3, 4]"] --> B["Operación vectorizada<br/>× 2"]
    B --> C["Resultado<br/>[2, 4, 6, 8]"]
```

---

## Array NumPy vs. Lista Python

```mermaid
flowchart TD
    A["Colección de datos"] --> B["Lista Python"]
    A --> C["Array NumPy"]
    B --> D["Flexible"]
    B --> E["Datos heterogéneos"]
    B --> F["Tamaño dinámico"]
    C --> G["Eficiente"]
    C --> H["Datos homogéneos"]
    C --> I["Operaciones vectorizadas"]
```

---

## Características principales

- Estructura secuencial.
- Orden preservado.
- Acceso por índice.
- Datos **homogéneos** (mismo tipo).
- Operaciones vectorizadas.
- Tamaño relativamente fijo.
- Muy eficiente en memoria.

---

## Complejidad de operaciones

| Operación | Complejidad |
|---|---|
| Acceso por índice | O(1) |
| Recorrido | O(n) |
| Inserción | O(n) |
| Eliminación | O(n) |

---

## ¿Cuándo utilizar esta estructura?

- Procesamiento numérico intensivo.
- Ciencia de datos.
- Inteligencia artificial.
- Álgebra lineal.
- Simulaciones matemáticas.
- Procesamiento de señales.
- Procesamiento de imágenes.

## ¿Cuándo evitar esta estructura?

- Cuando los datos son heterogéneos.
- Cuando el tamaño cambia constantemente.
- Cuando se requieren muchas inserciones o eliminaciones.
- Cuando las necesidades son simples y una lista resulta suficiente.

---

## Ventajas y limitaciones

=== "Ventajas"
    - Altísima velocidad de procesamiento.
    - Bajo consumo de memoria.
    - Operaciones matemáticas optimizadas.
    - Excelente integración con bibliotecas científicas.

=== "Limitaciones"
    - Menor flexibilidad.
    - Solo admite datos homogéneos.
    - Inserciones costosas.
    - Requiere biblioteca externa.

---

## Comparación con Lista Python

| Característica | Array NumPy | Lista |
|---|---|---|
| Datos homogéneos | ✅ | No necesariamente |
| Memoria | Muy eficiente | Menos eficiente |
| Operaciones matemáticas | Muy rápidas | Más lentas |
| Tamaño dinámico | No ideal | ✅ |
| Uso científico | Excelente | Limitado |
