# ¿Qué significa que una estructura use Hash?

Los conjuntos (`set`) y diccionarios (`dict`) pertenecen a una familia de estructuras llamadas **estructuras basadas en hash**.

La idea principal detrás del hash es muy sencilla:

En lugar de recorrer todos los elementos hasta encontrar uno, el sistema intenta calcular directamente dónde debería estar almacenado.

---

## Una analogía sencilla: biblioteca con casilleros

Imagina una biblioteca con muchos casilleros numerados.

Cada vez que llega un libro, existe una regla que decide directamente en qué casillero colocarlo.

```text
Libro
↓
Función Hash
↓
Casillero
```

Ejemplo conceptual:

```text
Libro 824
↓
Función Hash
↓
Casillero 24
```

Cuando luego alguien quiere buscar el libro:

```text
824
↓
Función Hash
↓
Casillero 24
↓
Encontrado
```

No fue necesario revisar todos los casilleros.

---

## ¿Qué es una función hash?

Una **función hash** es una función que recibe un dato y genera un número.

Ese número se utiliza como una posición aproximada donde almacenar o buscar el dato.

Conceptualmente:

```text
Dato
↓
Función Hash
↓
Número Hash
↓
Ubicación interna
```

Ejemplos conceptuales:

```text
hash("Juan") → 34827

hash("Pedro") → 12094

hash("Maria") → 87531
```

> Los números son ilustrativos. Lo importante no es el valor exacto, sino que normalmente el mismo dato produzca el mismo resultado.

---

## ¿Por qué esto hace rápidas las búsquedas?

### Sin Hash

Buscar un elemento puede requerir recorrer uno por uno.

```text
Buscar "Pedro"

Juan
Ana
Pedro ← encontrado
```

Costo aproximado:

```text
O(n)
```

---

### Con Hash

Se calcula directamente dónde buscar.

```text
Buscar "Pedro"

"Pedro"
↓
hash()
↓
posición interna
↓
acceso directo
```

Costo promedio:

```text
O(1)
```

Por eso conjuntos y diccionarios suelen ser mucho más rápidos para búsquedas.

---

## Hash y estructuras de Python

### Conjuntos (`set`)

Guardan elementos usando hash.

Ejemplo conceptual:

```text
set = {10, 20, 30}
```

Cuando se pregunta:

```text
20 in set
```

Python calcula el hash de `20` y busca directamente.

---

### Diccionarios (`dict`)

Guardan pares:

```text
clave → valor
```

Ejemplo:

```text
{"nombre": "Ana"}
```

Cuando se consulta:

```text
diccionario["nombre"]
```

Python calcula el hash de `"nombre"`.

---

## ¿Por qué algunos tipos no funcionan en estructuras hash?

Para que el hash funcione correctamente, el valor debe producir siempre el mismo resultado.

A esto se le llama:

```text
Hashable
```

Ejemplos:

| Tipo  | ¿Hashable? |
| ----- | ---------- |
| int   | ✅          |
| float | ✅          |
| str   | ✅          |
| bool  | ✅          |
| tuple | ✅*         |
| list  | ❌          |
| set   | ❌          |
| dict  | ❌          |

* Solo si todos sus elementos también son hashables.

---

## ¿Por qué una lista no puede ser hashable?

Una lista puede cambiar.

Ejemplo conceptual:

```text
[1,2,3]
↓
hash = 100
```

Luego:

```text
[1,2,3,4]
↓
hash = diferente
```

Entonces el sistema perdería la referencia de dónde estaba almacenada.

Por eso las estructuras hash requieren elementos estables.

---

## Idea para recordar

Las estructuras hash reemplazan:

```text
Buscar recorriendo
```

por:

```text
Calcular → ir directo
```

Ese es el motivo principal por el cual conjuntos y diccionarios suelen tener búsquedas muy eficientes.
