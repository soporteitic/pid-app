# Spec: PoC de 3 opciones de design system

**Estado:** aprobada · 23 de octubre de 2026
**Entregable:** `app/poc-design-system/index.html`
**Plan:** [Fase 1](../plan/fase-01-poc-design-system.md)

## Contexto

La micro app devocional "Poderosa" (ver [entrevista](../inputs/entrevista.md) y [alcance técnico](../inputs/alcance-tecnico-micro-app-devocionales.md)) tiene 6 vistas móviles aprobadas por la cliente en `docs/inputs/referencias/`. Antes de cerrar el diseño (Hito 1, semana 2) el equipo compara 3 propuestas de design system sobre esas mismas pantallas.

## Audiencia y acabado

Evaluación interna, con acabado suficiente para reenviarla a Caro sin retrabajo. Archivo HTML estático que abre sin servidor.

## Decisiones

- Entre opciones cambian tokens (color, tipografía, radios, sombras) y el estilo de los componentes (relleno, borde, indicador activo, tratamiento de texto). Layout, posiciones, medidas, textos y las 6 pantallas son idénticos a las referencias. Decisión del 23 de octubre de 2026: el usuario pidió más diferencia entre opciones manteniendo el layout.
- Paleta: únicamente tokens de [design-system-colors.md](../inputs/design-system-colors.md). Rosado = familia `lilac`, rojo = familia `coral`, negro = familia `ink`, neutros = `sand`. Cian, amarillo y mostaza quedan fuera.
- Las 3 opciones se diferencian por dominancia de color y rol del acento, más un par tipográfico propio.
- Un solo celular con tab bar funcional. Selector A/B/C recolorea en vivo.
- Pago se abre tocando un producto en Tienda; la flecha atrás vuelve. Notificaciones se abre con un botón fuera del celular.
- Panel lateral con nombre de la opción, intención en una frase, swatches de tokens y par tipográfico.
- Ilustración `docs/inputs/ilustracion_mujer.png` solo en Inicio, sutil.
- Stack: un `index.html` vanilla (HTML + CSS variables + JS mínimo). Fuentes desde Google Fonts, íconos SVG inline.

## Las 3 opciones

Reglas de contraste heredadas del doc de colores: texto sobre lila o arena siempre `ink-900` o `ink-700`; blanco solo sobre `coral-500` o más oscuro; `coral-300` es decorativo.

| Token semántico | A · Lila cálida | B · Crema serena | C · Editorial |
|---|---|---|---|
| `--bg-canvas` | `lilac-200` #E7C5DD | `sand-50` #F8F2EE | `lilac-50` #F6EDF3 |
| `--bg-surface` | `sand-50` #F8F2EE | `white` #FFFFFF | `white` #FFFFFF |
| `--bg-surface-2` | `sand-100` #EFE3DC | `lilac-100` #EFDCEA | `sand-50` #F8F2EE |
| `--bg-muted` | `lilac-100` #EFDCEA | `lilac-200` #E7C5DD | `ink-100` #E4E2E0 |
| `--text-primary` | `ink-900` | `ink-900` | `ink-900` |
| `--text-secondary` | `ink-700` | `ink-700` | `ink-700` |
| `--text-brand` | `coral-700` #9E3A3D | `coral-700` #9E3A3D | `coral-700` #9E3A3D |
| `--cta-bg` / `--cta-text` | `ink-900` / `sand-50` | `coral-500` / `white` | `ink-900` / `white` |
| `--chip-active-bg` / texto | `ink-900` / `sand-50` | `coral-500` / `ink-900` | `coral-300` / `ink-900` |
| `--accent-soft` | `lilac-300` | `lilac-200` | `coral-100` #FBE1E1 |
| `--border-subtle` | `sand-200` | `lilac-100` | `ink-100` |
| `--radius-card` / `--radius-cta` | 24px / 999px | 20px / 16px | 12px / 8px |
| Tipografía título / cuerpo | Fraunces / Nunito | Lora / Inter | Playfair Display / DM Sans |

Intención de cada opción:

- **A · Lila cálida:** cálida y envolvente. El lila es el fondo de toda la app, el negro manda en la acción.
- **B · Crema serena:** luminosa y sobria. Crema como lienzo, lila en superficies, coral solo en el botón que importa.
- **C · Editorial:** editorial y limpia. Casi blanco, negro en acción y títulos, coral pastel como detalle.

## Estilo de componentes por opción

| Componente | A · Lila cálida | B · Crema serena | C · Editorial |
|---|---|---|---|
| Card devocional | Relleno lila, radio 24, sin borde | Blanca, borde 1px lila, sombra suave | Sin caja: filetes negros arriba y abajo, radio 0 |
| CTA | Pastilla negra con sombra | Coral relleno, radio 16, ancho completo en la card | Negro, radio 4, texto en mayúsculas con tracking |
| Chips de filtro | Pastilla; activo negro relleno | Delineado 1.5px; activo coral-100 con borde coral | Pestañas de texto sobre filete; activo con subrayado 3px |
| Campos | Rellenos sand-100, sin borde | Delineados 1.5px, ícono coral | Solo línea inferior negra, sin fondo |
| Selector de capítulo | Relleno lila | Delineado | Título serif con línea inferior |
| Versículo resaltado | Relleno lila | Relleno lila claro con anillo | Relleno coral-100 plano; números en itálica voladita |
| Tiles de producto | Rellenos redondeados | Tarjeta blanca con borde y sombra, precio en coral | Planos con filete, radio 0, precio con línea superior |
| Radios | Círculo lila relleno; activo negro | Anillo lila; activo anillo coral con check coral | Anillo negro fino; activo negro relleno |
| Toggle | Negro | Coral | Negro, esquinas de 4px |
| Tab bar | Óvalo lila detrás del ícono activo | Ícono activo coral con punto debajo, sin óvalo | Filete negro superior y barra de 3px sobre el ícono activo |
| Wordmark | Sans en mayúsculas con tracking | Sans en mayúsculas con tracking | Serif itálica en minúsculas |
| Ilustración | Recortada en círculo lila | Sin recorte | Ligeramente desaturada |

## Ajustes por contraste

Ratios calculados sobre los tokens (WCAG, texto normal 4.5:1, texto grande 3:1):

- `coral-500` sobre fondos claros queda entre 2.4 y 3.7. Por eso `--text-brand` es `coral-700` en las 3 opciones (4.9 sobre `lilac-100`, 6.7 sobre blanco).
- `ink-500` sobre `sand-50` da 4.1. Por eso la opción C usa `ink-700` como texto secundario.
- Blanco sobre `coral-500` da 3.7: válido solo para el CTA de B (18 px bold). Los chips de B llevan `ink-900` (4.9).
- En A la card del devocional usa `lilac-100` en vez de `lilac-300` para que el eyebrow coral alcance 4.5.

## Interacciones y datos de prueba

Decisión del 23 de octubre de 2026: el prototipo simula los flujos con datos mock en el propio `index.html` (constantes `DEVOCIONALES`, `BIBLIA`, `VERSIONES`, `PRODUCTOS`, `IDIOMAS`, `HORAS`). Sin backend ni persistencia; el botón "Reiniciar demo" vuelve al estado inicial.

| Pantalla | Interacción |
|---|---|
| Inicio | "Leer devocional" y cada ítem de Anteriores abren la lectura. El chip de idioma lleva a Perfil. Los leídos muestran check. |
| Lectura | Etiquetas, cuerpo en 3 párrafos, enlace al pasaje que abre la Biblia en ese capítulo con el versículo resaltado, "Marcar como leído" con toast. |
| Biblia | Desplegable de pasajes (5 capítulos), desplegable de versión (RV 1909 activa; RV 1960, KJV y ARA marcadas "Próximamente"), tocar un versículo lo resalta, botones Anterior/Siguiente. |
| Tienda | Chips filtran por categoría. Ícono de bolsa con contador y acceso a Mis compras. Tocar un producto abre Pago con sus datos. |
| Pago | Inputs reales con formato automático (tarjeta en bloques de 4, MM / AA, CVV). Validación con mensaje y campo en error. "Procesando…" y pantalla de confirmación. |
| Confirmación | Mensaje según formato (descarga o entrega física), resumen, botones a Mis compras o Tienda. |
| Perfil | Radios de idioma seleccionables (con aviso de que la traducción es de la app real), toggles con animación, hora del devocional en desplegable, enlace a Mis compras. |
| Mis compras | Lista con compras previas y nuevas; estado vacío si no hay. |
| Push | La primera tarjeta abre la lectura de hoy; la segunda, la Tienda. |

Los desplegables se renderizan dentro del celular, anclados al control, y adoptan el estilo de cada opción (A relleno, B contorno, C filetes).

## Pantallas

Contenido copiado tal cual de las 6 referencias: Inicio, Biblia, Notificaciones, Tienda, Pago, Perfil.

Los tiles de producto de la referencia usan 4 colores; en el PoC cada opción usa `accent-soft`, `bg-surface-2`, `bg-muted` y `coral-100`, en ese orden.

## Fuera de alcance

- Modo oscuro.
- Inglés y portugués. Solo español.
- Cambios de layout o de componentes entre opciones.
- Tokens que no existan en el doc de colores.
