---
name: ds-ibk
description: Design system de Interbank (IBK) según su Manual de identidad v1. Úsalo para cualquier decisión visual o de voz en una pieza de Interbank: colores y su significado, tipografía Geometria, logotipo y caja de logotipo, titulares, botones y campos de interfaz, tono de voz. Si el manual no define algo (modo oscuro, estados, notas), dilo en vez de inventarlo.
argument-hint: [colors|type|shape|brand|layout|ui|voice] [pregunta o tarea]
---

# Design system de Interbank

Este skill es la **única fuente** para entender el estilo de Interbank. Resume el Manual de identidad v1
(`ibk_ds.pdf`, en la raíz de este repo) y lo deja listo para agentes.

| Parte | Qué es |
|-------|--------|
| `core/` | El estilo: qué significan color, fuente y forma (`meanings.md`), logo, caja y voz (`brand.md`), todos los valores (`tokens.md`, `tokens.css`) |
| `references/` | De dónde sale cada dato y qué falta. Empieza por `references/README.md` |

`core/` se mantiene a mano en este repo. Si el manual cambia, se actualiza `core/` y la procedencia en `references/README.md`.

## Las reglas

1. **El verde es la marca.** Casi nunca va solo: se combina con blanco (fondo) y azul (títulos y cuerpo).
2. **Texto azul sobre blanco.** Excepción técnica: negro Black 6 C al 70 %.
3. **Colores al 100 % y sin tonos nuevos.** Los porcentajes de opacidad son excepcionales.
4. **Tokens, nunca valores.** Usa la variable de `core/tokens.css`, no un hex suelto.
5. **Geometria en tres pesos:** Medium, Regular y Extra Light. Montserrat solo si hay que usar una Google Font; Verdana solo en emails HTML.
6. **Un titular, un peso, un tamaño.** Sin negritas, cursivas ni subrayados: para resaltar se usa un destacado.
7. **El logotipo va siempre dentro de la caja blanca** en piezas de comunicación, anclada a una esquina. El isotipo nunca va en verde y el wordmark nunca va sin isotipo.
8. **Retícula de 8 dp** en interfaz (12 columnas en escritorio, 6 en tablet, 2 en móvil).
9. **Texto en español (es-PE), de tú a tú.** El código va en inglés.
10. **Lo que el manual no dice, no se inventa.** No define modo oscuro, estados, notas ni superficies. Pregunta o declara el hueco.

## Dónde mirar

| Necesidad | Lee |
|-----------|-----|
| Qué significa un color, una fuente o una forma | `core/meanings.md` |
| Un valor (hex, Pantone, fuente, medida de botón) | `core/tokens.md`, o `core/tokens.css` para variables CSS |
| Logotipo, caja, titulares, contacto, voz | `core/brand.md` |
| De dónde sale un dato y qué huecos hay | `references/README.md` |
