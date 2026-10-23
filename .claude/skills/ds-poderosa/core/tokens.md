# Valores de Poderosa

Colores de `docs/inputs/design-system-colors.md`. Las variables CSS están en `tokens.css`. Los significados están en
`meanings.md`. Solo modo light: el doc define también modo oscuro y se omitió a propósito (ver `references/README.md`).

No hay valores de tipografía, botones ni retícula: el design system no los define.

## Primitivos

Nunca se usan directamente en componentes; solo alimentan los tokens semánticos.

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

## Semánticos (light)

Los componentes consumen solo estos. Variable CSS: `--bg-canvas`, `--text-primary`, etc. (`tokens.css`).

### Fondo
| Token | Valor |
|---|---|
| `bg/canvas`    | `lilac-200` `#E7C5DD` |
| `bg/surface`   | `sand-50` `#F8F2EE` |
| `bg/surface-2` | `sand-100` `#EFE3DC` |
| `bg/muted`     | `sand-200` `#DCC4B7` |

### Texto
| Token | Valor |
|---|---|
| `text/primary`   | `ink-900` `#171616` |
| `text/secondary` | `ink-700` `#45413E` |
| `text/tertiary`  | `ink-500` `#7A7572` |
| `text/on-accent` | `ink-900` `#171616` |
| `text/on-coral`  | `white` |
| `text/link`      | `cyan-700` `#0F7276` |

### Acento / acción
| Token | Valor | Uso |
|---|---|---|
| `accent/primary`       | `cyan-300` `#5FE0E5` | botón principal, highlight |
| `accent/primary-hover` | `cyan-400` `#2FC9CF` | |
| `accent/secondary`     | `yellow-300` `#F4DD6A` | CTA secundario, énfasis |
| `accent/tertiary`      | `coral-300` `#EA8588` | chips, badges, decoración |

### Estado
| Token | Valor |
|---|---|
| `state/success` | `cyan-500` `#17A8AE` |
| `state/warning` | `mustard-400` `#D9933F` |
| `state/error`   | `coral-500` `#D85D61` |
| `state/info`    | `lilac-500` `#B06E9F` |

### Borde
| Token | Valor |
|---|---|
| `border/subtle` | `sand-200` `#DCC4B7` |
| `border/strong` | `ink-300` `#B5B1AD` |
| `border/focus`  | `cyan-500` `#17A8AE` |

## Contraste (WCAG)

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

## Tailwind (`tailwind.config.js`)

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

El doc también trae un bloque Flutter. Se omitió: la app es una PWA.
