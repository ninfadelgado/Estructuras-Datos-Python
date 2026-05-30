# Conjuntos

## ¿Qué son?

Los conjuntos son estructuras de datos diseñadas para almacenar **elementos únicos**. Su principal objetivo es permitir búsquedas rápidas y evitar duplicados automáticamente. Internamente utilizan mecanismos de hashing para optimizar el acceso.

---

## Mecanismo de hashing

```mermaid
flowchart LR
    A["Elemento<br/>'hola'"] --> B["hash('hola')"]
    B --> C["Número hash"]
    C --> D["Ubicación interna"]
    D --> E["Elemento almacenado"]
```

---

## Eliminación automática de duplicados

```mermaid
flowchart LR
    A["Entrada:<br/>1, 2, 2, 3, 1, 4"] --> B["Conjunto"]
    B --> C["Salida conceptual:<br/>1, 2, 3, 4"]
```

---

## Operaciones matemáticas

```mermaid
flowchart TD
    A["Conjunto A"] --> D["Unión<br/>A ∪ B"]
    B["Conjunto B"] --> D
    A --> E["Intersección<br/>A ∩ B"]
    B --> E
    A --> F["Diferencia<br/>A - B"]
    B --> F
```

---

## Características principales

- No admiten duplicados.
- Son mutables.
- Son iterables.
- Utilizan hashing.
- Permiten operaciones matemáticas de conjuntos.
- No poseen acceso por índice.

---

## Complejidad de operaciones

| Operación | Complejidad |
|---|---|
| Verificar pertenencia | O(1) promedio |
| Agregar | O(1) promedio |
| Eliminar | O(1) promedio |

---

## ¿Cuándo utilizar esta estructura?

- Cuando se necesita unicidad.
- Cuando las búsquedas son muy frecuentes.
- Para eliminar duplicados.
- Para operaciones matemáticas entre colecciones.

## ¿Cuándo evitar esta estructura?

- Cuando el orden es importante.
- Cuando se necesita acceso por índice.
- Cuando se requieren elementos repetidos.

---

## Ventajas y limitaciones

=== "Ventajas"
    - Búsquedas muy rápidas.
    - Eliminación automática de duplicados.
    - Operaciones matemáticas eficientes.
    - Excelente rendimiento para verificación de pertenencia.

=== "Limitaciones"
    - No poseen indexación.
    - Solo almacenan elementos hashables.
    - No están diseñados para acceso secuencial.

---

## Comparación con Lista

| Característica | Conjunto | Lista |
|---|---|---|
| Duplicados | ❌ | ✅ |
| Índices | ❌ | ✅ |
| Búsqueda | O(1) | O(n) |
| Orden secuencial | ❌ | ✅ |
