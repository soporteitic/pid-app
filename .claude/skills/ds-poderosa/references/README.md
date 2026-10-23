# Referencias: procedencia y huecos

## Procedencia

| Dato | Fuente |
|------|--------|
| Paleta, tokens semánticos, contraste WCAG, Tailwind, guía de uso | `docs/inputs/design-system-colors.md` |
| Estilo pedido (limpio, minimalista, sobrio, cálido), uso de la ilustración, origen de la paleta | `docs/inputs/entrevista.md`, sección "Diseño y Marca" |
| Cliente, producto, idiomas, módulos | `docs/inputs/alcance-tecnico-micro-app-devocionales.md` |
| Ilustración y pantallas de referencia | `docs/inputs/ilustracion_mujer.png`, `docs/inputs/referencias/` |

Resumen hecho el 2026-10-23. `core/` se edita a mano en este repo. Este skill sustituye al `ds-ibk` del scaffold
(Interbank); no comparte archivos con él.

## Qué se omitió a propósito

| Qué | Por qué | Cómo recuperarlo |
|-----|---------|------------------|
| Modo oscuro | Decisión del proyecto: solo light | El doc lo define en la sección 2 (columna Dark) y 4 (bloque `@media (prefers-color-scheme: dark)`). Copiarlo a `tokens.css` y `tokens.md` |
| Bloque Flutter | La app es una PWA | Sección 4 del doc |

## Huecos del design system

El doc no define, y este skill no inventa:

- Tipografía: familia, pesos, escala.
- Logotipo y tagline.
- Tono de voz.
- Elevación y sombras.
- Estados de componente (hover, disabled, pressed), salvo `accent/primary-hover`.
- Tamaños de fuente y espaciado en px.
- Términos oficiales del producto (usuaria, devocional, cápsula…).

## Dudas conocidas

Ninguna por ahora.

## Para ampliar

Releer `docs/inputs/design-system-colors.md`. Si la cliente entrega tipografía o logotipo, añadirlos a `core/` y
registrar aquí la fuente.
