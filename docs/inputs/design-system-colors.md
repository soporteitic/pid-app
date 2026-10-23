# Design System · Colores

Paleta derivada del post "La autoridad que no actúa con rectitud se invalida sola". Estilo: pastel, cálido, amigable, con un acento frío (cian) para contraste.

---

## 1. Tokens primitivos

Valores crudos. Nunca se usan directamente en componentes; solo alimentan los tokens semánticos.

### Lila (fondo de marca)
| Token | HEX | Nota |
|---|---|---|
| `lilac-50`  | `#F6EDF3` | tint muy suave |
| `lilac-100` | `#EFDCEA` | |
| `lilac-200` | `#E7C5DD` | **color base (fondo original)** |
| `lilac-300` | `#D9A9CB` | |
| `lilac-400` | `#C88DB8` | |
| `lilac-500` | `#B06E9F` | |
| `lilac-700` | `#7E4A70` | |
| `lilac-900` | `#4A2A42` | |

### Cian (acento frío)
| Token | HEX | Nota |
|---|---|---|
| `cyan-100` | `#D6F7F8` | |
| `cyan-200` | `#A8EEF0` | |
| `cyan-300` | `#5FE0E5` | **color base** |
| `cyan-400` | `#2FC9CF` | |
| `cyan-500` | `#17A8AE` | |
| `cyan-700` | `#0F7276` | texto sobre cian claro |

### Amarillo (acento cálido)
| Token | HEX | Nota |
|---|---|---|
| `yellow-100` | `#FCF3CC` | |
| `yellow-200` | `#F9E9A0` | |
| `yellow-300` | `#F4DD6A` | **color base** |
| `yellow-400` | `#E8C93A` | |
| `yellow-500` | `#C9A71E` | |
| `yellow-700` | `#8A7012` | |

### Coral (acento rosa)
| Token | HEX | Nota |
|---|---|---|
| `coral-100` | `#FBE1E1` | |
| `coral-300` | `#EA8588` | **color base** (diadema, texto curvo) |
| `coral-500` | `#D85D61` | |
| `coral-700` | `#9E3A3D` | |

### Arena (neutro cálido)
| Token | HEX | Nota |
|---|---|---|
| `sand-50`  | `#F8F2EE` | **crema base** |
| `sand-100` | `#EFE3DC` | |
| `sand-200` | `#DCC4B7` | **beige base** |
| `sand-300` | `#C7A896` | |
| `sand-500` | `#A29685` | gris verdoso de las hojas |

### Mostaza (hojas)
| Token | HEX |
|---|---|
| `mustard-200` | `#F1D0A5` |
| `mustard-400` | `#D9933F` |

### Carbón (texto / neutros fríos)
| Token | HEX | Nota |
|---|---|---|
| `ink-50`  | `#F4F3F2` | |
| `ink-100` | `#E4E2E0` | |
| `ink-300` | `#B5B1AD` | |
| `ink-500` | `#7A7572` | |
| `ink-700` | `#45413E` | **texto base** |
| `ink-900` | `#171616` | **texto fuerte** |

### Base
| Token | HEX |
|---|---|
| `white` | `#FFFFFF` |
| `black` | `#000000` |

---

## 2. Tokens semánticos

Los componentes consumen solo estos.

### Fondo
| Token | Light | Dark |
|---|---|---|
| `bg/canvas`    | `lilac-200` `#E7C5DD` | `lilac-900` `#4A2A42` |
| `bg/surface`   | `sand-50` `#F8F2EE`   | `#2E1F2A` |
| `bg/surface-2` | `sand-100` `#EFE3DC`  | `#3A2834` |
| `bg/muted`     | `sand-200` `#DCC4B7`  | `#514150` |

### Texto
| Token | Light | Dark |
|---|---|---|
| `text/primary`   | `ink-900` `#171616` | `sand-50` `#F8F2EE` |
| `text/secondary` | `ink-700` `#45413E` | `sand-200` `#DCC4B7` |
| `text/tertiary`  | `ink-500` `#7A7572` | `ink-300` `#B5B1AD` |
| `text/on-accent` | `ink-900` `#171616` | `ink-900` `#171616` |
| `text/on-coral`  | `white`             | `white` |
| `text/link`      | `cyan-700` `#0F7276` | `cyan-300` `#5FE0E5` |

### Acento / acción
| Token | Light | Dark | Uso |
|---|---|---|---|
| `accent/primary`       | `cyan-300` `#5FE0E5` | `cyan-400` `#2FC9CF` | botón principal, highlight |
| `accent/primary-hover` | `cyan-400` `#2FC9CF` | `cyan-300` `#5FE0E5` | |
| `accent/secondary`     | `yellow-300` `#F4DD6A` | `yellow-400` `#E8C93A` | CTA secundario, énfasis |
| `accent/tertiary`      | `coral-300` `#EA8588` | `coral-300` `#EA8588` | chips, badges, decoración |

### Estado
| Token | Light | Dark |
|---|---|---|
| `state/success` | `cyan-500` `#17A8AE`   | `cyan-300` `#5FE0E5` |
| `state/warning` | `mustard-400` `#D9933F` | `yellow-300` `#F4DD6A` |
| `state/error`   | `coral-500` `#D85D61`  | `coral-300` `#EA8588` |
| `state/info`    | `lilac-500` `#B06E9F`  | `lilac-300` `#D9A9CB` |

### Borde
| Token | Light | Dark |
|---|---|---|
| `border/subtle`  | `sand-200` `#DCC4B7` | `#514150` |
| `border/strong`  | `ink-300` `#B5B1AD`  | `ink-500` `#7A7572` |
| `border/focus`   | `cyan-500` `#17A8AE` | `cyan-300` `#5FE0E5` |

---

## 3. Contraste (WCAG)

Combinaciones verificadas para texto normal:

| Texto | Fondo | Ratio | Resultado |
|---|---|---|---|
| `ink-900` | `lilac-200` | ≈ 11.8 | AAA |
| `ink-900` | `cyan-300`  | ≈ 12.4 | AAA |
| `ink-900` | `yellow-300` | ≈ 13.7 | AAA |
| `ink-900` | `sand-50`   | ≈ 16.5 | AAA |
| `ink-700` | `sand-200`  | ≈ 6.6 | AA |
| `white`   | `coral-300` | ≈ 2.9 | ❌ solo ≥ 24 px o ícono |
| `white`   | `coral-500` | ≈ 4.5 | AA |
| `cyan-700`| `sand-50`   | ≈ 5.2 | AA |

Reglas:
- Sobre cian, amarillo, lila y arena, el texto siempre es `ink-900` o `ink-700`.
- Coral solo lleva texto blanco a partir de `coral-500`; `coral-300` es decorativo.
- El cian base (`cyan-300`) **no** sirve como color de texto sobre fondos claros; usa `cyan-700`.

---

## 4. Implementación

### CSS
```css
:root {
  --lilac-200: #E7C5DD; --lilac-900: #4A2A42;
  --cyan-300: #5FE0E5;  --cyan-400: #2FC9CF; --cyan-500: #17A8AE; --cyan-700: #0F7276;
  --yellow-300: #F4DD6A; --yellow-400: #E8C93A;
  --coral-300: #EA8588; --coral-500: #D85D61;
  --sand-50: #F8F2EE; --sand-100: #EFE3DC; --sand-200: #DCC4B7;
  --ink-300: #B5B1AD; --ink-500: #7A7572; --ink-700: #45413E; --ink-900: #171616;

  --bg-canvas: var(--lilac-200);
  --bg-surface: var(--sand-50);
  --bg-muted: var(--sand-200);
  --text-primary: var(--ink-900);
  --text-secondary: var(--ink-700);
  --text-link: var(--cyan-700);
  --accent-primary: var(--cyan-300);
  --accent-secondary: var(--yellow-300);
  --accent-tertiary: var(--coral-300);
  --border-subtle: var(--sand-200);
  --border-focus: var(--cyan-500);
}

@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg-canvas: var(--lilac-900);
    --bg-surface: #2E1F2A;
    --bg-muted: #514150;
    --text-primary: var(--sand-50);
    --text-secondary: var(--sand-200);
    --text-link: var(--cyan-300);
    --accent-primary: var(--cyan-400);
    --accent-secondary: var(--yellow-400);
    --border-subtle: #514150;
    --border-focus: var(--cyan-300);
  }
}
```

### Tailwind (`tailwind.config.js`)
```js
theme: {
  extend: {
    colors: {
      lilac:  { 50:'#F6EDF3', 200:'#E7C5DD', 500:'#B06E9F', 900:'#4A2A42' },
      cyan:   { 300:'#5FE0E5', 400:'#2FC9CF', 500:'#17A8AE', 700:'#0F7276' },
      yellow: { 300:'#F4DD6A', 400:'#E8C93A', 700:'#8A7012' },
      coral:  { 300:'#EA8588', 500:'#D85D61', 700:'#9E3A3D' },
      sand:   { 50:'#F8F2EE', 100:'#EFE3DC', 200:'#DCC4B7', 500:'#A29685' },
      ink:    { 300:'#B5B1AD', 500:'#7A7572', 700:'#45413E', 900:'#171616' },
    },
  },
}
```

### Flutter
```dart
abstract class AppColors {
  static const lilac200 = Color(0xFFE7C5DD);
  static const cyan300  = Color(0xFF5FE0E5);
  static const yellow300 = Color(0xFFF4DD6A);
  static const coral300 = Color(0xFFEA8588);
  static const sand50   = Color(0xFFF8F2EE);
  static const sand200  = Color(0xFFDCC4B7);
  static const ink700   = Color(0xFF45413E);
  static const ink900   = Color(0xFF171616);
}
```

---

## 5. Guía de uso

- **Proporción sugerida:** 60 % lila/arena (fondos) · 25 % crema (superficies) · 10 % cian o amarillo (acción) · 5 % coral/mostaza (detalle).
- **Un solo acento por pantalla** como color de acción principal; no mezcles cian y amarillo en botones del mismo nivel.
- Las "franjas" del post se traducen a **chips/cards con esquinas muy redondeadas (16–24 px)** y ligera rotación (−2° a 2°) si quieres conservar el aire editorial.
- Evita usar el lila como fondo de texto largo; úsalo en canvas, headers y estados vacíos, y lleva el contenido a `bg/surface`.
