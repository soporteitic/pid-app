# Referencias: procedencia y huecos

## Procedencia

- Fuente única: `ibk_ds.pdf` (raíz del repo), "Manual de identidad, versión 1". Algunas páginas llevan pie "Versión 0.2".
- Extracción: `pdftotext -layout -enc UTF-8`, el 2026-10-22. Las muestras visuales (combinaciones de realce, cajas,
  ejemplos de interfaz) son imágenes y no salen en el texto.
- Este skill es una variación de `../../ds-mentorium/`. No comparte archivos con él ni se publica desde ningún frontend.
  `core/` se edita aquí a mano.

## Qué se leyó y qué no

| Capítulo del manual | Estado |
|---------------------|--------|
| 1 Estrategia (pp. 6-30) | Leído |
| 2.1 Logotipo, 2.2 Tipografía, 2.3 Color (pp. 32-61) | Leído |
| 2.4 Pictogramas, 2.8 Interfaz (pp. 62-67, 104-119) | Leído en parte |
| 2.5 Fotografía, 2.6 Ilustración, 2.7 Patterns | Solo la premisa de fotografía |
| 3 Principios de diseño: cajas, márgenes, titulares (pp. 122-156) | Leído |
| 3.5-3.7 Caja flotante, caja secundaria, la ventana (pp. 159-183) | **Pendiente** |
| 4-5 Convivencia de marcas, submarcas, cobranding (pp. 184-209) | **Pendiente** |
| 5 Tono de voz con ejemplos (pp. 210-243) | Solo el resumen de los cuatro pilares |
| 6 Aplicaciones (p. 244 en adelante) | **Pendiente** |

## Huecos del manual

El manual no define, y este skill no inventa:

- Modo oscuro.
- Estados (activo, pendiente, cancelado…) y colores de error o éxito.
- Notas o calificaciones.
- Superficies, elevación y sombras.
- Radios de producto (solo la esquina de la caja de logotipo).
- Tamaños de fuente en px (todo va en múltiplos de X).
- Términos oficiales del producto (estudiante, cliente, etc.).

## Dudas conocidas

| Duda | Qué se hizo |
|------|-------------|
| Amarillo impreso como `cd00` | Se usó `#ffcd00`, sacado de su RGB 255 205 0 |
| Verde: Pantone 360 U en la tabla, 361 C en el texto | Se anotaron ambos. El HEX de pantalla no cambia |
| Qué colores secundarios son "realce" | El texto no los nombra uno a uno. Ver imagen de pp. 56-57 |
| Contraste de texto sobre cada color | Calculado con WCAG aquí, no viene del manual (`core/tokens.md`) |
| Medidas de selector y navegación | No se transcribieron: el texto extraído sale desordenado. Ver pp. 115-116 |

## Para ampliar

Releer los capítulos pendientes con `pdftotext -layout -enc UTF-8 ibk_ds.pdf salida.txt`. Para las partes que son
imagen, abrir el PDF y mirar la página citada.
