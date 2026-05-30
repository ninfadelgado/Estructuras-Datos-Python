# Tabla Comparativa General

## Comparación de todas las estructuras

| Estructura | Orden | Duplicados | Mutable | Acceso Principal | Búsqueda |
|---|---|---|---|---|---|
| Lista | ✅ Secuencial | ✅ | ✅ | Índice | O(n) |
| Tupla | ✅ Secuencial | ✅ | ❌ | Índice | O(n) |
| Conjunto | ❌ No secuencial | ❌ | ✅ | Pertenencia | O(1) |
| Diccionario | Inserción | ❌ Claves únicas | ✅ | Clave | O(1) |
| Pila | LIFO | ✅ | ✅ | Tope | O(n) |
| Cola | FIFO | ✅ | ✅ | Extremos | O(n) |
| Lista Enlazada | ✅ Secuencial | ✅ | ✅ | Secuencial | O(n) |
| Array NumPy | ✅ Secuencial | ✅ | Parcial | Índice | O(n) |
| BST | ✅ Ordenado | ✅ | ✅ | Jerárquico | O(log n)* |

> *O(log n) promedio en árboles balanceados. Puede degradarse a O(n) en árboles degenerados.

---

## Complejidades por operación

| Estructura | Acceso | Inserción inicio | Inserción final | Búsqueda |
|---|---|---|---|---|
| Lista | O(1) | O(n) | O(1) amort. | O(n) |
| Tupla | O(1) | — | — | O(n) |
| Conjunto | — | O(1) | O(1) | O(1) |
| Diccionario | O(1) clave | O(1) | O(1) | O(1) |
| Pila | O(1) tope | — | O(1) | O(n) |
| Cola | O(1) frente | O(1) | O(1) | O(n) |
| Lista Enlazada | O(n) | O(1) | O(n) | O(n) |
| Array NumPy | O(1) | O(n) | O(n) | O(n) |
| BST | — | O(log n)* | O(log n)* | O(log n)* |
