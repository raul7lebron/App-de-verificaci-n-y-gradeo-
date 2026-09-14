---
name: card-grading-appraiser
description: Estima el estado de conservación y la posible nota de gradeo (PSA o Beckett/BGS) de una carta coleccionable a partir de fotos o una descripción visual. Úsalo cuando el usuario pida "gradear", "evaluar el estado", "qué nota le pondría PSA/Beckett" o "verificar autenticidad" de una carta.
---

# Card Grading Appraiser

Esta skill ayuda a estimar de forma orientativa el estado de conservación de una carta coleccionable (deportiva, TCG, etc.) y a situarla en las escalas de gradeo profesional más habituales: **PSA** y **Beckett/BGS**.

No sustituye un gradeo profesional real: el objetivo es dar una estimación razonada al usuario antes de que decida enviar (o no) la carta a una casa de gradeo.

## Flujo de trabajo

1. **Reúne evidencia visual**: pide o revisa fotos del frente y dorso de la carta, con buena luz y sin reflejos, si aún no las tienes.
2. **Evalúa las 4 categorías clásicas** de forma independiente:
   - Centrado (centering)
   - Esquinas (corners)
   - Bordes (edges)
   - Superficie (surface): rayones, brillo, defectos de impresión
3. **Consulta la escala de referencia correspondiente**:
   - Para una nota estilo PSA (nota única 1-10), usa `references/psa-scale.md`.
   - Para una nota estilo Beckett/BGS (4 subgrados + nota final), usa `references/beckett-scale.md`.
4. **Aplica la regla del "eslabón más débil"**: un defecto grave en una sola categoría puede bajar la estimación general aunque el resto esté impecable (más acusado aún en BGS, donde el subgrado más bajo pesa más que la media).
5. **Presenta el resultado al usuario** con:
   - Una estimación por categoría (con el defecto concreto observado en cada una, no solo un número).
   - Una nota final estimada, dejando claro que es orientativa y puede variar frente al gradeo real de la casa correspondiente.
   - Si la carta muestra daño estructural (dobleces, grietas, rasgones, escritura) o indicios de alteración/reacondicionamiento, señálalo explícitamente como un problema de autenticidad/elegibilidad, no solo de nota.

## Archivos de referencia

- `references/psa-scale.md` — guía de correspondencia entre estado visual y nota PSA (1-10).
- `references/beckett-scale.md` — guía de los 4 subgrados de Beckett/BGS y cómo se combinan en la nota final.

Carga el archivo de referencia relevante antes de dar una estimación numérica, en lugar de inventar los criterios de memoria.
