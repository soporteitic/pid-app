# Micro App de Devocionales · Alcance y características técnicas

**Cliente:** comunidad de mujeres "Poderosa" (emprendedora independiente)
**Proveedor:** ITIC · ventas@itic.com.pe · +51 945 032 612
**Fuente:** Propuesta económica, versión inicial — Lima, 19 de octubre de 2026
**Estado del alcance:** referencial; se confirma con las respuestas de la sección 7.

---

## 1. Resumen del proyecto

Micro app para sondear una comunidad orgánica de mujeres, con tres ejes:

1. **Devocionales** diarios con notificaciones al celular.
2. **Biblia incorporada**, enlazada desde cada devocional.
3. **Tienda en línea** para vender libros y devocionales.

Todo en **tres idiomas** (español, inglés, portugués) y administrado desde un **panel** propio.

### Objetivos

| # | Objetivo |
|---|---|
| 01 | Sondear la comunidad orgánica con una micro app simple, rápida y de bajo costo |
| 02 | Acompañar el día a día de cada mujer con devocionales y avisos en su celular |
| 03 | Monetizar libros y devocionales con compra en línea segura |
| 04 | Ampliar el alcance en español, inglés y portugués |

---

## 2. Tipo de solución

| Atributo | Definición |
|---|---|
| Plataforma | **Webapp instalable (PWA)** |
| Instalación | Desde el navegador, a la pantalla de inicio del celular |
| Tiendas de apps | **No aplica.** Sin publicación, aprobación ni costos de App Store / Google Play |
| Acceso | Por URL con dominio propio y HTTPS |
| Licenciamiento | Sin licencias ni costo por usuaria |

**Justificación:** inversión baja y predecible, sin dependencia de procesos de revisión de terceros, apta para una emprendedora independiente.

---

## 3. Alcance funcional

### 3.1 Matriz de entregables

| Entregable | Nivel técnico | Descripción |
|---|---|---|
| App instalable (webapp) | Intermedio | Se instala desde el navegador en la pantalla de inicio, sin tiendas |
| Devocionales | Básico | Devocional del día y archivo de lecturas anteriores |
| Notificaciones al celular | Intermedio | Aviso al publicar un devocional o contenido nuevo |
| Biblia incorporada | Intermedio | Lectura por libro y capítulo, enlazada desde cada devocional |
| Tres idiomas | Intermedio | Interfaz y contenidos en español, inglés y portugués |
| Tienda y pasarela de pagos | Intermedio | Compra en línea de libros y devocionales con tarjeta |
| Panel de administración | Básico | Publicar devocionales, programar avisos y gestionar productos |

### 3.2 Módulo: Devocionales

- **Pantalla de inicio** con saludo personalizado por nombre y fecha del día.
- **Devocional del día:** título, cita bíblica de referencia (ej. Hebreos 4:12), extracto y acción "Leer devocional".
- **Archivo de anteriores:** listado cronológico con título y fecha relativa (Ayer, 17 oct…).
- Cada devocional **enlaza al pasaje** correspondiente en la Biblia incorporada.
- Contenido disponible en el idioma seleccionado por la usuaria.

### 3.3 Módulo: Biblia incorporada

- Navegación **por libro y capítulo**.
- Texto versiculado (número + versículo).
- **Versiones de dominio público** (referencia mostrada: Reina-Valera 1909). Versiones con derechos quedan fuera del alcance (ver sección 6).
- Versión por idioma pendiente de definir con la cliente.
- Acceso directo desde el devocional del día.

### 3.4 Módulo: Notificaciones push

| Tipo de aviso | Disparador | Control de la usuaria |
|---|---|---|
| Devocional diario | Publicación programada (ej. 7:00 a. m.) | Activar/desactivar y hora |
| Novedades de tienda | Alta de un producto nuevo | Activar/desactivar |

- Las notificaciones llegan al centro de notificaciones del celular con título, cuerpo y acceso directo a la app.
- Se programan desde el panel de administración.

### 3.5 Módulo: Tienda y pagos

- **Catálogo** con filtros: Todo · Libros · Devocionales.
- Ficha de producto con título, formato (ej. digital) y precio (referencia en USD).
- **Checkout** con pago con tarjeta: número, vencimiento (MM/AA), CVV y total.
- **Entrega digital por correo** tras la compra.
- Confirmación de compra por correo electrónico.
- La pasarela de pagos la define y contrata el proveedor; su **comisión por venta** la cobra la pasarela y no está incluida.
- Historial "Mis compras" en el perfil de la usuaria.

Productos de ejemplo en la propuesta (títulos y precios referenciales): Cápsula Poderosa USD 9.90 · Devocional 30 días USD 12.90 · Libro impreso USD 24.90 · Guía de oración USD 7.90.

### 3.6 Módulo: Internacionalización (i18n)

- Tres idiomas: **Español, English, Português**.
- Aplica a **interfaz y contenidos** (devocionales, Biblia, tienda).
- Selector de idioma en el perfil de la usuaria.
- Los contenidos **llegan traducidos** por la cliente; la traducción no forma parte del desarrollo.

### 3.7 Módulo: Perfil de usuaria

- Selección de idioma.
- Preferencias de notificaciones (devocional diario con hora; novedades de tienda).
- Mis compras.

### 3.8 Módulo: Panel de administración

| Función | Detalle |
|---|---|
| Devocionales | Crear, publicar y archivar devocionales en los tres idiomas |
| Avisos | Programar notificaciones push (fecha/hora y tipo) |
| Productos | Alta, edición y baja de productos; precio y formato |
| Capacitación | Incluida en el pase a producción |

---

## 4. Diseño

- Vistas de referencia basadas en la **paleta visual de Poderosa**.
- Diseño final con la identidad de la cliente, **aprobado en la semana 1–2** (Hito 1).
- La cliente provee los recursos gráficos (portadas, imágenes, audios, textos).

---

## 5. Infraestructura y operación

Incluido en el fee mensual (USD 180 / mes desde el pase a producción):

| Componente | Alcance |
|---|---|
| Hosting en la nube | Servidor y base de datos administrados |
| Dominio | Registro y renovación anual |
| Notificaciones push | Servicio de envío a los celulares de las usuarias |
| Correo transaccional | Bienvenida y confirmaciones de compra |
| Certificado SSL | Conexión HTTPS, requerida para pagos |
| Copias de seguridad | Respaldo periódico de la información |
| Mantenimiento | Actualizaciones y corrección de errores |
| Soporte | Atención en horario laboral |

- Sin licencias ni costos por usuaria.
- Si la comunidad crece muy por encima de lo estimado, se revisa el plan de infraestructura.

---

## 6. Exclusiones

No forman parte del alcance; cualquiera puede incorporarse como **adenda con cotización propia**:

1. Publicación en App Store y Google Play.
2. Traducción de contenidos (los devocionales llegan traducidos a los tres idiomas).
3. Licencias de versiones bíblicas con derechos de autor (se usan versiones de dominio público).
4. Comisiones de la pasarela de pagos (las cobra el proveedor en cada venta).
5. Envío de libros físicos y su logística.
6. Suscripciones o membresías con cobro recurrente.
7. Producción de contenido: textos, portadas, audios e imágenes (los provee la cliente).

---

## 7. Definiciones pendientes para cerrar el alcance

Estas respuestas pueden ajustar funcionalidades, cronograma e inversión:

| Tema | Pregunta |
|---|---|
| Comunidad actual | ¿Cuántas mujeres tiene hoy la comunidad y en qué redes está? |
| Proyección a 2 años | ¿Cuántas usuarias se esperan en la app en los próximos 2 años? |
| Devocionales | ¿Con qué frecuencia se publicará? ¿Ya existen en los tres idiomas? |
| Versión de la Biblia | ¿Qué versión se prefiere en cada idioma? Algunas requieren licencia |
| Tienda y pagos | ¿Cuántos productos? ¿Digitales o físicos? ¿En qué moneda se cobra? |
| Acceso | ¿App gratuita con registro, con contenido de pago o con suscripción? |

---

## 8. Metodología y cronograma

### Fases

| Fase | Costo | Descripción |
|---|---|---|
| Diagnóstico | Sin costo | Conversación sobre comunidad, contenidos y objetivos |
| Borrador inicial | Sin costo | Primera versión de pantallas y alcance para validar la idea |
| Análisis | Desarrollo | Cierre de funcionalidades, idiomas, productos y versión de la Biblia |
| Diseño | Desarrollo | Diseño visual con la identidad de la cliente, para aprobación |
| Desarrollo | Desarrollo | Devocionales, Biblia, tienda, notificaciones y panel |
| Pase a producción | Desarrollo | Publicación, pruebas finales y capacitación en el panel |
| Mantenimiento | Fee mensual | Hosting, dominio, avisos, correos, soporte y mejoras |

### Cronograma · 4 semanas

| Semana | Actividad | Entregable |
|---|---|---|
| 1 | Análisis | Funcionalidades, idiomas y productos cerrados |
| 2 | Diseño | Pantallas con identidad visual · **Hito 1: aprobación del diseño** |
| 3 | Desarrollo | Devocionales, Biblia, tienda, avisos y panel |
| 4 | Pase a producción | Pruebas, publicación y capacitación · **Hito 2: app en producción** |

- Antes de la semana 1: diagnóstico y borrador inicial, sin costo.
- El cronograma arranca al aprobar el borrador y pagar el primer 50 %.

---

## 9. Resumen económico (referencia)

| Concepto | Modalidad | USD |
|---|---|---|
| Diagnóstico y borrador inicial | Sin costo | 0 |
| Desarrollo de la micro app | 50 % al aprobar borrador · 50 % en producción | 800 |
| Fee mensual (hosting, dominio, notificaciones, correos, mantenimiento) | Mensual desde producción | 180 |
| Fee mensual × 12 | Primer año | 2,160 |
| **Total primer año** | | **2,960** |

Montos en dólares americanos, no incluyen IGV. La comisión por venta de la pasarela la cobra el proveedor de pagos.

---

## 10. Próximos pasos

1. Agendar el diagnóstico sin costo y responder las preguntas de alcance.
2. Revisar el borrador inicial de pantallas y alcance.
3. Confirmar con el 50 % del desarrollo (USD 400).
4. Iniciar el análisis: semana 1 del cronograma.
