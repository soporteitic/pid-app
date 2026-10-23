# Valores de Interbank

Colores y fuentes del Manual de identidad v1 (`ibk_ds.pdf`, pp. 45-53). Las variables CSS están en `tokens.css`.
Los significados están en `meanings.md`.

## Colores

El manual no da tokens con nombre. Los nombres `ibk-*` son de este skill.

| Color | Token | HEX | RGB | CMYK | Pantone | Grupo |
|---|---|---|---|---|---|---|
| Verde | `ibk-green` | `#05be50` | 5 190 80 | 75 0 100 0 | 360 U (también citado 361 C) | Principal |
| Azul | `ibk-blue` | `#0039a6` | 0 57 166 | 100 75 0 0 | 286 C | Principal |
| Blanco | `ibk-white` | `#ffffff` | 255 255 255 | 0 0 0 0 | n/d | Fondo |
| Crema | `ibk-cream` | `#f0f0dc` | 240 240 220 | 0 0 15 5 | 168 C | Secundaria |
| Amarillo | `ibk-yellow` | `#ffcd00` | 255 205 0 | 0 10 100 0 | 116 C | Secundaria |
| Celeste | `ibk-sky` | `#64b4e6` | 100 180 230 | 55 10 0 0 | 292 C | Secundaria |
| Rosa rojo | `ibk-pink-red` | `#eb0046` | 235 0 70 | 0 100 65 0 | 192 C | Secundaria |
| Azul noche | `ibk-navy` | `#001e5f` | 0 30 95 | 100 95 25 30 | 2757 C | Secundaria |
| Negro | `ibk-black` | `#0f191e` | 15 25 30 | 95 80 55 85 | Black 6 C | Secundaria |

Correcciones sobre el manual:
- El manual imprime el HEX del amarillo como `cd00`. Se usa `#ffcd00`, que sale de su RGB.
- El verde aparece como Pantone 360 U en la tabla y como 361 C en el texto. El HEX de pantalla es el mismo.
- El manual separa en sus pp. 56-57 los "colores de realce" y los "tonos neutros" (crema y negro) sin nombrar cada color en el texto. Para saber cuáles son de realce, mirar la imagen de esas páginas.

## Texto sobre cada color

El manual solo fija: texto azul sobre blanco, y blanco o azul sobre fotografía. El resto se **calculó con WCAG** y no es
una regla del manual. Se elige el primer par que llega a 4,5:1.

| Fondo | Texto | Contraste |
|---|---|---|
| Verde `#05be50` | Negro `#0f191e` | 7,2:1 (azul solo da 3,97, blanco 2,47: no sirven) |
| Azul `#0039a6` | Blanco | 9,8:1 |
| Crema `#f0f0dc` | Azul | 8,5:1 |
| Amarillo `#ffcd00` | Azul | 6,5:1 (negro 11,9:1) |
| Celeste `#64b4e6` | Negro `#0f191e` | 7,8:1 (azul da 4,31: no llega) |
| Rosa rojo `#eb0046` | Blanco | 4,5:1 (justo en el límite) |
| Azul noche `#001e5f` | Blanco | 15,5:1 |
| Negro `#0f191e` | Blanco | 17,8:1 |
| Blanco `#ffffff` | Azul (regla del manual) | 9,8:1 |

## Opacidad

Todos los colores van al 100 %. El manual permite 20, 40, 60, 80 % solo de forma excepcional, y
nunca añadir tonos nuevos. Para fondos neutros, negro Black 6 C entre 5 y 100 %, mejor desde 20 %.
Negro como color de texto: solo por razones técnicas y al 70 %.

## Fuentes

| Familia | Pesos permitidos | Uso | Nunca |
|---|---|---|---|
| Geometria | Medium, Regular, Extra Light | Toda la comunicación | Otros pesos, negrita, cursiva, subrayado |
| Montserrat | Medium, Light, Extra Light | Sustituta cuando hay que usar una Google Font | Cuando se puede usar Geometria |
| Verdana | Regular | Solo emailings HTML (fuente de sistema) | Cualquier otro caso |

Stack: `'Geometria', 'Montserrat', sans-serif`. Las normas de uso de Montserrat son las de Geometria. Mapa de pesos:
Medium → Medium, Regular → Light, Extra Light → Extra Light.

## Niveles tipográficos

X es el tamaño base del titular. No hay px fijos: todo es múltiplo o fracción de X.

| Nivel | Fuente y peso | Tamaño | Caja |
|---|---|---|---|
| Descriptor | Regular | ½ X | MAYÚSCULAS |
| Titular | Medium | X o múltiplo de X | minúsculas |
| Subtitular | Regular | ½ X | minúsculas |
| Cuerpo de texto | Extra Light | ¼ X | minúsculas |
| Destacado | Extra Light | múltiplos de X | minúsculas |

## Interfaz

| Elemento | Valor |
|---|---|
| Retícula | 12 columnas en escritorio, 6 en tablet, 2 en móvil |
| Base | 8 dp. Íconos y texto pueden alinearse a 4 dp |
| Botón S / M / L | 40 / 56 / 72 dp de alto |
| Botón: margen lateral | 32 dp a cada lado del texto |
| Énfasis de botón | Alto = primary, medio = secondary, bajo = text |
| Campo de texto y desplegable | 56 dp de alto, 16 dp de separación |
