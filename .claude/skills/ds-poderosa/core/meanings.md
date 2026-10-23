# Significados: qué dicen el color, la forma y la proporción

Esto es el estilo de Poderosa según `docs/inputs/design-system-colors.md` y las notas de `docs/inputs/entrevista.md`.
Los valores (hex, tokens) no se repiten aquí: están en `tokens.md` y `tokens.css`. El design system **no define**
tipografía, logotipo, voz, modo oscuro ni estados hover/disabled, y este skill tampoco los inventa.

## Estilo

Pastel, cálido, amigable, con un acento frío (cian) para contraste. La cliente pidió un diseño limpio, minimalista y
sobrio, con calidez de marca. La paleta sale del post "La autoridad que no actúa con rectitud se invalida sola" y de
las redes de la comunidad.

## Color

**El lila es el fondo de marca; el cian es la acción.** Ninguno va solo: el contenido vive sobre crema y el texto es
carbón.

| Familia | Qué dice | Dónde va | Nunca |
|---------|----------|----------|-------|
| Lila | La marca, el fondo original del post | `bg/canvas`: canvas, headers, estados vacíos. `lilac-500` como `state/info` | Fondo de texto largo; el contenido va a `bg/surface` |
| Cian | Acento frío, la acción | `accent/primary`: botón principal, highlight. `cyan-700` para enlaces. `cyan-500` para foco y éxito | `cyan-300` como color de texto sobre fondos claros |
| Amarillo | Acento cálido, énfasis | `accent/secondary`: CTA secundario, destacados | En botones del mismo nivel que el cian |
| Coral | Detalle rosa (diadema, texto curvo de la ilustración) | `accent/tertiary`: chips, badges, decoración. `coral-500` como `state/error` | Texto blanco sobre `coral-300` (solo desde `coral-500`) |
| Arena | Neutro cálido, superficies | `bg/surface` (crema), `bg/surface-2`, `bg/muted` (beige), `border/subtle` | Como color de acción |
| Mostaza | Las hojas, detalle | `state/warning` y pequeños acentos | Como fondo grande |
| Carbón | El texto | `text/primary` (`ink-900`), `text/secondary` (`ink-700`), `text/tertiary`, `border/strong` | Negro puro `#000000` como texto |

Reglas de uso:
- Sobre cian, amarillo, lila y arena, el texto siempre es `ink-900` o `ink-700`.
- **Un solo acento por pantalla** como color de acción principal: cian o amarillo.
- Los componentes consumen solo tokens semánticos; los primitivos quedan en `tokens.css`.
- Las combinaciones válidas de texto y fondo están en la tabla WCAG de `tokens.md`.

## Proporción

60 % lila y arena (fondos) · 25 % crema (superficies) · 10 % cian o amarillo (acción) · 5 % coral y mostaza (detalle).

## Forma

- Las "franjas" del post se traducen a **chips y cards con esquinas muy redondeadas (16–24 px)**.
- Ligera rotación (−2° a 2°) en chips o cards si se quiere conservar el aire editorial. Opcional.
- La ilustración "Poderosa" (caricatura) va solo en la pantalla de inicio: en móvil no hay espacio para más.

## Huecos

No definidos por el design system. Pregunta o declara el hueco antes de decidir:

- Tipografía (familia, pesos, escala).
- Logotipo y tagline.
- Tono de voz.
- Modo oscuro (el doc lo define; se omitió por decisión del proyecto).
- Elevación, sombras y estados hover/disabled más allá de `accent/primary-hover`.
