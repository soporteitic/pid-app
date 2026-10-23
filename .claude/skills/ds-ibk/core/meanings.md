# Significados: qué dicen el color, la tipografía y la forma

Esto es el estilo de Interbank según el Manual de identidad v1 (`ibk_ds.pdf`). Los valores (hex, fuentes) no se
repiten aquí: están en `tokens.md` y `tokens.css`. El manual **no define** modo oscuro, estados, notas, superficies
ni colores por tipo de registro, y este skill tampoco los inventa.

## Color

**El verde es la seña de identidad.** Casi nunca va solo: se combina con blanco (fondo) y azul (títulos y cuerpo).

| Color | Qué dice | Dónde va | Nunca |
|-------|----------|----------|-------|
| Verde | La marca corporativa | Elementos de marca y de interacción, junto al blanco | Como color del isotipo (el isotipo no se usa en verde) |
| Azul | La voz | Titulares y cuerpo de texto sobre blanco | Sustituirlo por negro, salvo razón técnica (negro al 70 %) |
| Blanco | El fondo | Fondo por defecto y caja de logotipo | Caja de logotipo de otro color |
| Crema y negro | Tonos neutros | Fondos de composiciones; negro desde 20 % de opacidad para no endurecer | Negro puro como fondo grande |
| Amarillo, celeste, rosa rojo, azul noche | Realce | Destacados, llamadas de atención, interacción, jerarquías de varios niveles (infografías) | Usarlos solos, sin la paleta principal |

Reglas de uso:
- Los colores van al **100 % de opacidad**. Los porcentajes (20, 40, 60, 80) solo se usan cuando la paleta no alcanza.
- **No se añaden tonos nuevos** a la paleta.
- Texto sobre blanco: azul. Excepción técnica: negro al 70 %.
- Texto sobre fotografía: azul o blanco, con el máximo contraste. Si no se lee, se usa una caja de titular.
- Solo valen las combinaciones de realce que muestra el manual (pp. 60-61). Cualquier otra se evita.

## Tipografía

| Familia | Rol | Nunca |
|---------|-----|-------|
| Geometria | La fuente de la marca, en Medium, Regular y Extra Light | Otros pesos, negrita, cursiva, subrayado |
| Montserrat | Sustituta digital cuando hace falta una Google Font | Cuando se puede usar Geometria |
| Verdana | Emailings en HTML | Cualquier otro caso |

Cada texto cae en uno de cinco niveles: descriptor, titular, subtitular, cuerpo y destacado (`tokens.md`).
No se mezclan: un titular tiene un solo peso y un solo tamaño. Para resaltar una palabra o cifra se añade un
**destacado** junto al titular, no se cambia el estilo de la palabra.

## Forma

- La esquina curva del isotipo se repite en la **caja de logotipo**: esquina inferior derecha, radio = altura del isotipo.
- Los pictogramas reproducen esa curva en uno de sus ángulos. Debajo de 50 px se simplifican y pierden la inclinación.
- La caja de titular es blanca al 100 %, crece en horizontal y vertical según el texto, y nunca es de otro color.
- Módulo X: la altura del isotipo. Márgenes y separaciones se miden en X.
- En interfaz todo se apoya en una retícula de 8 dp (4 dp para íconos y texto).

## Voz

Todo mensaje cumple al menos uno de cuatro pilares:

| Pilar | Cómo suena |
|-------|-----------|
| Empático y humano | De tú a tú, lenguaje comprensible, natural e inclusivo |
| Resolutivo y dinámico | Directo, simple y claro; valora el tiempo de quien lee |
| Ingenioso | Compacto pero expresivo; creatividad, emoción y toques de humor |
| Didáctico | Pedagógico, transmite seguridad, transparencia y sencillez |

Personalidad: empática, resolutiva, retadora, dinámica, didáctica, humana.
