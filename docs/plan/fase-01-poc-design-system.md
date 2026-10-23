# Fase 1: PoC de 3 opciones de design system

**Spec:** [poc-design-system-spec.md](../specs/poc-design-system-spec.md)
**Estado:** entregada · 23 de octubre de 2026

## Idea en sencillo

Tenemos 6 pantallas aprobadas por Caro. Queremos probar tres "vestidos" distintos sobre esas mismas pantallas, sin mover nada de sitio, para elegir con cuál seguir. Un solo archivo HTML muestra un celular simulado; un botón A/B/C cambia colores, tipografía y bordes en vivo.

## Parte técnica

- Entregable: `app/poc-design-system/index.html`, vanilla HTML + CSS + JS, sin build. Ilustración copiada a la misma carpeta.
- Primitivos de color copiados de `docs/inputs/design-system-colors.md` (familias lilac, coral, sand, ink). Cada opción define tokens semánticos bajo `:root[data-theme="a|b|c"]`; los componentes consumen solo semánticos.
- Un contenedor `.screen` con 6 `section[data-screen]`; `go(screen)` muestra una y marca la tab activa. Tienda abre Pago al tocar un producto; la flecha atrás vuelve; el botón externo abre la pantalla de push y oculta la tab bar.
- `setTheme(id)` cambia `data-theme` y rellena el panel lateral: nombre, intención, 8 swatches y par tipográfico. Fuentes desde Google Fonts en un solo `<link>`; sin red caen a serif/sans del sistema.
- Contraste verificado con ratios WCAG; los ajustes resultantes están en la spec.

## Ejercicio con resultado esperado

1. Abrir `app/poc-design-system/index.html` con doble click. Resultado: panel oscuro a la izquierda con "A · Lila cálida" y un celular con la pantalla Inicio, saludo "Hola, María" y la ilustración junto al chip "ES".
2. Pulsar "B" y luego "C". Resultado: el celular recolorea sin recargar; el panel cambia nombre, intención, swatches y fuentes.
3. Tocar la tab Tienda y luego el producto "Cápsula Poderosa". Resultado: aparece "Tu compra" con el botón "Pagar USD 9.90"; la flecha "<" devuelve a Tienda.
4. Pulsar "Ver notificación push". Resultado: pantalla de bloqueo con "7:00", dos tarjetas y sin tab bar; tocar la primera tarjeta vuelve a Inicio.
5. Reducir la ventana a 390 px de ancho. Resultado: el panel queda arriba del celular, sin scroll horizontal.
