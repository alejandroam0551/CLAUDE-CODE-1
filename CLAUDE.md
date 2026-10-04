# CLAUDE.md

Este repositorio es una base de conocimiento personal. La información entra en bruto, se organiza en una wiki y de ahí salen los entregables.

```
raw/  →  wiki/  →  output/
fuentes   conocimiento   entregables
```

## Carpetas

### `raw/`: fuentes originales
Material tal como llega: artículos, PDFs, transcripciones, notas sueltas, capturas, exportaciones.

- **Solo lectura para Claude.** Nunca editar, renombrar ni borrar archivos aquí.
- Se agregan archivos nuevos sin procesarlos.
- Es la fuente de verdad: si la wiki y `raw/` se contradicen, manda `raw/`.

### `wiki/`: conocimiento procesado
Notas en Markdown que Claude escribe y mantiene a partir de `raw/`.

- Un archivo por tema o concepto, con nombre en `kebab-case.md` (ej. `estrategia-de-precios.md`).
- Cada nota cita sus fuentes con la ruta del archivo en `raw/` (ej. `Fuente: raw/entrevista-cliente-2026-09.pdf`).
- Enlazar notas relacionadas con enlaces relativos (`[precios](estrategia-de-precios.md)`).
- `wiki/index.md` lista todas las notas con una línea de descripción. Actualizarlo al crear o borrar una nota.
- Al procesar una fuente nueva, actualizar las notas existentes antes que crear duplicadas.

### `output/`: entregables
Productos terminados que se generan a partir de la wiki: informes, resúmenes, presentaciones, correos, respuestas a preguntas concretas.

- Se basan en `wiki/`, no directamente en `raw/` (si falta algo, primero se agrega a la wiki).
- Nombre con fecha y tema: `AAAA-MM-DD-tema.ext` (ej. `2026-10-04-resumen-mercado.md`).
- Son desechables: se pueden regenerar desde la wiki.

## Flujo de trabajo

1. **Ingerir**: el usuario deja material en `raw/`.
2. **Compilar**: Claude lee las fuentes nuevas y crea o actualiza las notas de `wiki/` y `wiki/index.md`.
3. **Producir**: a pedido, Claude genera entregables en `output/` usando la wiki.
4. **Mantener**: de vez en cuando, revisar la wiki para detectar contradicciones, notas huérfanas o temas sin fuente.

## Reglas generales

- Responder en español.
- Si un dato no está respaldado por `raw/`, marcarlo como `[sin fuente]` en vez de inventarlo.
