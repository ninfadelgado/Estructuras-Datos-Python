# Resumen-Estructuras-Datos-Python

Sitio de documentación **Estructuras de Datos en Python — ITBA**, construido con [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

---

## Instalación

```bash
pip install mkdocs-material
```

## Ejecución local

```bash
mkdocs serve
```

Luego abrir: [http://127.0.0.1:8000](http://127.0.0.1:8000)

## Build estático

```bash
mkdocs build
```

El sitio se genera en la carpeta `site/`.

---

## Publicación en GitLab Pages

Agregar este archivo como `.gitlab-ci.yml` en la raíz del repositorio:

```yaml
pages:
  image: python:3.11-slim
  script:
    - pip install mkdocs-material
    - mkdocs build --site-dir public
  artifacts:
    paths:
      - public
  only:
    - main
```

El sitio quedará disponible en:
`https://ninfadelgado.gitlab.io/Resumen-Estructuras-Datos-Python/`

---

## Estructura del proyecto

```
docs/
├── index.md
├── fundamentos/
│   ├── introduccion.md
│   └── big-o.md
├── estructuras-secuenciales/
│   ├── listas.md
│   └── tuplas.md
├── estructuras-hash/
│   ├── conjuntos.md
│   └── diccionarios.md
├── estructuras-lineales/
│   ├── pilas.md
│   ├── colas.md
│   └── listas-enlazadas.md
├── estructuras-especializadas/
│   └── arrays-numpy.md
├── estructuras-jerarquicas/
│   └── bst.md
└── referencia/
    ├── guia-seleccion.md
    ├── tabla-comparativa.md
    └── conclusiones.md
```
