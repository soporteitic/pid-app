---
name: ds-poderosa
description: Design system de Poderosa (micro app de devocionales de la comunidad "Poderosa en la Intimidad con Dios"). Úsalo para cualquier decisión visual en la app: paleta pastel cálida con acento cian, tokens semánticos (fondo, texto, acento, estado, borde), contraste WCAG, proporción de color, chips y cards redondeados, uso de la ilustración. Si el design system no define algo (tipografía, logotipo, voz, modo oscuro, estados hover/disabled), dilo en vez de inventarlo.
argument-hint: [colors|tokens|contrast|usage] [pregunta o tarea]
---

# Design system de Poderosa

Este skill es la **única fuente** para entender el estilo de la micro app Poderosa. Resume
`docs/inputs/design-system-colors.md` (paleta y tokens) y las notas de marca de `docs/inputs/entrevista.md`,
y lo deja listo para agentes.

| Parte | Qué es |
|-------|--------|
| `core/` | El estilo: qué significa cada color y forma (`meanings.md`), cliente, ilustración y referencias (`brand.md`), todos los valores (`tokens.md`, `tokens.css`) |
| `references/` | De dónde sale cada dato y qué falta. Empieza por `references/README.md` |

`core/` se mantiene a mano en este repo. Si `docs/inputs/design-system-colors.md` cambia, se actualiza `core/` y la
procedencia en `references/README.md`.

## Las reglas

1. **Los componentes consumen solo tokens semánticos** (`bg/*`, `text/*`, `accent/*`, `state/*`, `border/*`). Los primitivos (`lilac-200`, `cyan-300`…) solo alimentan a los semánticos.
2. **Tokens, nunca valores.** Usa la variable de `core/tokens.css`, no un hex suelto.
3. **El lila es el fondo de marca** (`bg/canvas`): canvas, headers y estados vacíos. Nunca fondo de texto largo; el contenido va en `bg/surface` (crema).
4. **Sobre cian, amarillo, lila y arena el texto es siempre `ink-900` o `ink-700`.**
5. **Coral:** `coral-300` es decorativo. Texto blanco solo a partir de `coral-500`.
6. **El cian base (`cyan-300`) no es color de texto** sobre fondos claros. Enlaces en `cyan-700`.
7. **Un solo acento de acción por pantalla:** cian o amarillo, nunca ambos en botones del mismo nivel.
8. **Proporción 60 / 25 / 10 / 5:** lila y arena (fondos) · crema (superficies) · cian o amarillo (acción) · coral y mostaza (detalle).
9. **Chips y cards con esquinas de 16–24 px.** Rotación opcional de −2° a 2° para conservar el aire editorial del post.
10. **Lo que el design system no dice, no se inventa.** No define tipografía, logotipo, voz, modo oscuro, elevación ni px de fuente. La ilustración "Poderosa" va solo en la pantalla de inicio. Pregunta o declara el hueco.

## Dónde mirar

| Necesidad | Lee |
|-----------|-----|
| Qué significa un color o una forma, proporción, estilo | `core/meanings.md` |
| Un valor (hex, token semántico, contraste, Tailwind) | `core/tokens.md`, o `core/tokens.css` para variables CSS |
| Cliente, producto, ilustración, pantallas de referencia | `core/brand.md` |
| De dónde sale un dato y qué huecos hay | `references/README.md` |
