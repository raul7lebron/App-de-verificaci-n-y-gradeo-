---
name: card-grading-appraiser
description: Estima el estado de conservación y la posible nota de gradeo (PSA o Beckett/BGS) de una carta coleccionable a partir de fotos o una descripción visual. Úsalo cuando el usuario pida "gradear", "evaluar el estado", "qué nota le pondría PSA/Beckett" o "verificar autenticidad" de una carta.
---

# Card Grading Appraiser

Esta skill ayuda a estimar de forma orientativa el estado de conservación de una carta coleccionable (deportiva, TCG, etc.) y a situarla en las escalas de gradeo profesional más habituales: **PSA** y **Beckett/BGS**.

No sustituye un gradeo profesional real: el objetivo es dar una estimación razonada al usuario antes de que decida enviar (o no) la carta a una casa de gradeo.

## Flujo de trabajo

1. **Reúne evidencia visual.** Pide (o revisa, si ya las tienes) fotos del **frente y el dorso completos**, más **primeros planos de las 4 esquinas** si el estado general parece alto (a partir de ~PSA 8 / BGS 8.5 los defectos de esquina son difíciles de juzgar en una foto general). Pide luz uniforme y sin reflejos directos sobre la carta — el brillo de un flash puede ocultar rayones reales o simular defectos de superficie que no existen.
   - Si las fotos están borrosas, mal iluminadas, incompletas (falta el dorso, falta una esquina) o el reflejo impide ver la superficie, **pide fotos mejores antes de estimar** en vez de adivinar. Es preferible decir "no puedo evaluar la superficie con esta foto" que dar una nota poco fiable.
   - Pregunta o identifica el **tipo de carta** (deportiva, TCG, vintage) y si tiene **acabado foil/holo/refractor**: estos acabados hacen más difícil detectar micro-rayones y merecen mención explícita de esa limitación en el informe.
2. **Aclara qué escala interesa** si no es evidente por el pedido del usuario: PSA, Beckett/BGS, o ambas en paralelo. Si no lo especifica, ofrece ambas notas por defecto — son las dos referencias más buscadas.
3. **Evalúa las 4 categorías clásicas** de forma independiente, describiendo el defecto concreto observado en cada una (no te limites a poner un número):
   - Centrado (centering)
   - Esquinas (corners)
   - Bordes (edges)
   - Superficie (surface): rayones, brillo, defectos de impresión
4. **Consulta la escala de referencia correspondiente antes de dar una nota** — no inventes los criterios de memoria:
   - Para PSA (nota única 1-10, con posibles qualifiers), usa `references/psa-scale.md`.
   - Para Beckett/BGS (4 subgrados + nota final), usa `references/beckett-scale.md`.
5. **Revisa la sección de autenticidad de ambas guías** (recorte, recoloreado, limpieza/restauración, reencolado, falsificación) antes de cerrar la estimación. Si hay indicios, esto tiene prioridad sobre la nota numérica.
6. **Aplica la regla del "eslabón más débil"**: un defecto grave en una sola categoría puede bajar la estimación general aunque el resto esté impecable (más acusado aún en BGS, donde el subgrado más bajo pesa más que la media).
7. **Presenta el informe final** siguiendo esta estructura:
   - **Resumen**: 1-2 frases con la impresión general y la nota estimada.
   - **Por categoría**: centrado, esquinas, bordes y superficie, cada una con el defecto concreto observado (o "sin defectos apreciables").
   - **Nota estimada**: PSA y/o BGS (con subgrados si aplica Beckett), dejando claro que es orientativa.
   - **Alertas de autenticidad**: solo si detectaste algo de la sección de descalificación; si no hay nada, se puede omitir esta sección o indicar "sin indicios de alteración".
   - **Limitaciones**: menciona si alguna zona no se pudo evaluar bien (ángulo, luz, reflejo, foil) y qué fotos ayudarían a confirmar la estimación.
   - **Disclaimer**: recuerda siempre que es una estimación y que la nota real puede variar frente al gradeo oficial de la casa correspondiente.

## Archivos de referencia

- `references/psa-scale.md` — guía de correspondencia entre estado visual y nota PSA (1-10), qualifiers y motivos de descalificación.
- `references/beckett-scale.md` — guía de los 4 subgrados de Beckett/BGS, cómo se combinan en la nota final y motivos de descalificación.

Carga el archivo de referencia relevante antes de dar una estimación numérica, en lugar de inventar los criterios de memoria.
