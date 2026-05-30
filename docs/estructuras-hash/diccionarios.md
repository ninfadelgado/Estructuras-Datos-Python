# Diccionarios

## ¿Qué son?

Los diccionarios son estructuras de datos que almacenan información en forma de **pares clave-valor**. A diferencia de las listas y las tuplas, donde los elementos se localizan mediante posiciones numéricas, en los diccionarios cada valor se accede mediante una clave identificadora.

---

## Representación conceptual

```mermaid
flowchart LR
    A["Clave:<br/>nombre"] --> B["Valor:<br/>Ana"]
    C["Clave:<br/>edad"] --> D["Valor:<br/>25"]
    E["Clave:<br/>ciudad"] --> F["Valor:<br/>Buenos Aires"]
```

---

## Mecanismo interno: tabla hash

```mermaid
flowchart TD
    A["Clave"] --> B["Función hash"]
    B --> C["Índice interno"]
    C --> D["Ubicación en tabla hash"]
    D --> E["Valor asociado"]
```

---

## Búsqueda por clave vs. búsqueda en lista

```mermaid
flowchart TD
    A["Buscar usuario"] --> B["Lista"]
    A --> C["Diccionario"]
    B --> D["Revisar elemento 1"]
    D --> E["Revisar elemento 2"]
    E --> F["Revisar elemento 3"]
    F --> G["... hasta encontrar"]
    C --> H["Usar clave"]
    H --> I["Hash"]
    I --> J["Acceso directo al valor"]
```

---

## Características principales

- Almacenan pares clave-valor.
- Las claves deben ser únicas.
- Mantienen el orden de inserción (Python 3.7+).
- Permiten acceso directo por clave.
- Son mutables.
- Son iterables.
- Utilizan tablas hash internamente.

---

## Complejidad de operaciones

| Operación | Complejidad |
|---|---|
| Acceso por clave | O(1) |
| Inserción | O(1) |
| Eliminación | O(1) |
| Búsqueda de clave | O(1) |

---

## ¿Cuándo utilizar esta estructura?

- Cuando se necesita acceso rápido mediante identificadores.
- Cuando los datos poseen nombres significativos.
- Para representar configuraciones.
- Para almacenar información tipo JSON.
- Para conteo de frecuencias.
- Para agrupaciones de datos.
- Para cache de resultados.

## ¿Cuándo evitar esta estructura?

- Cuando el acceso principal sea por posición numérica.
- Cuando se necesite una colección puramente secuencial.
- Cuando los datos sean extremadamente simples y una lista resulte suficiente.

---

## Ventajas y limitaciones

=== "Ventajas"
    - Acceso extremadamente rápido.
    - Claves descriptivas.
    - Gran flexibilidad.
    - Inserciones eficientes.
    - Excelente para modelar información estructurada.

=== "Limitaciones"
    - Mayor consumo de memoria.
    - No permiten claves duplicadas.
    - No poseen indexación numérica directa.
    - Requieren claves hashables.

---

## Comparación con Lista

| Característica | Diccionario | Lista |
|---|---|---|
| Acceso principal | Clave | Índice |
| Complejidad acceso | O(1) | O(1) |
| Claves descriptivas | ✅ | ❌ |
| Duplicados | ❌ en claves | ✅ |
| Orden secuencial | Secundario | Principal |
