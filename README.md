# Guía docente · «La etiqueta sin nombre»

## 1. Datos

| Campo | Valor |
|---|---|
| Unidad didáctica | Producción y publicación de piezas gráficas |
| Tipo | Actividad gamificada DUA-Experiencial (skill gamificacion-dua-idc) |
| Duración | 40 min · individual o en parejas |
| Archivos | `etiqueta-sin-nombre.html` (estudiante), `etiqueta-sin-nombre-docente.html` (con respuestas) |
| Plano | Plantilla SP074 (388 × 398 pt), mismo troquel que la landing EC |

## 2. Objetivo y resultado de aprendizaje

- **Objetivo:** leer la información obligatoria de una etiqueta de alimentos y deducir de ella la naturaleza del producto, para comprobar por qué la denominación no puede faltar.
- **Resultado:** interpreta advertencias, tabla nutricional, ingredientes y alérgenos de un rotulado y decide qué advertencias corresponden a un alimento nuevo.

## 3. Narrativa y uso del prompt de arte

En la imprenta falló la plancha de la denominación y de la ilustración. Las cuatro etiquetas se generan en SVG con el estilo del prompt del arte navideño (tapa carmesí con filigrana dorada, laterales verde bosque con acebo y piñas, octógonos arriba a la derecha, base con tabla nutricional, ingredientes, código de barras, QR, fabricante y espacios de LOTE y vencimiento en blanco, sangrado de 3 mm sobre SP074). En lugar de la denominación aparece «DENOMINACIÓN NO IMPRESA»; al resolver cada caso se imprime la denominación y la ilustración del producto.

**Caja 1 (versión 2):** usa la etiqueta raster aportada por el docente (`assets/caja1.jpg`, 2048 × 2048 px, comprimida desde el original). La tabla nutricional y los ingredientes de esa imagen traen texto ilegible o mezclado con inglés («Amount per serving», «Soiúm 128 g»), así que al revelarse se cubren con un parche vectorial con los datos correctos del caso (560 kcal, 23 g grasa saturada, 40 g azúcares, 40 mg sodio). La ilustración de bombones queda cubierta hasta resolver el caso; al resolverlo se añade la cinta «BOMBONES DE CHOCOLATE». La imagen muestra «Chocolates del Perú S.A.» como fabricante, a diferencia de las cajas 2 a 4 («Alimentos del Sur S.A.»).

## 4. Estaciones y puntaje (100 XP)

| # | Estación | Kolb | Mecánica | XP |
|---|---|---|---|---|
| 0 | Registro | — | Datos en memoria (no se guardan al recargar) | 0 |
| 1 | Caso de entrenamiento | EC | Predicción + lupa gratis + identificación con evidencia | 10/7/4 (2) |
| 2 | ¿Qué le faltaba? | OR → CA | Definición por contraste (4 formulaciones) + clasificación sí/no | 8/5/2 + 7 |
| 3 | Laboratorio | EA | 3 cajas: 2 lupas gratis, −2 por lupa extra (máx. −6), −4 por error, respuesta tras 3 errores (3) | 3 × 15 |
| 4 | Anagramas | CA | ROTULADO, ALÉRGENO, DENOMINACIÓN, ADVERTENCIA | 4 × 3 |
| 5 | Rotula un producto | EA + reflexión | Octógonos de una barra de cereal + denominación + «Dos hallazgos y una duda» | 10/6/3 + 4 + 4 |

Niveles: Aprendiz de etiquetas (0) · Lector de rótulos (25) · Detective de rotulado (50) · Inspector de rotulado (75) · Jefe de control (95). Cinco insignias, una por estación.

## 5. Respuestas

| Caja | Marca | Producto | Octógonos | Evidencias decisivas |
|---|---|---|---|---|
| 1 | Amor de Navidad | Bombones de chocolate | Azúcar, grasas saturadas | Masa y manteca de cacao; 40 g azúcares, 23 g grasa sat., 40 mg sodio |
| 2 | Brisa del Puerto | Galletas de soda | Sodio, grasas saturadas | 820 mg sodio y 4 g azúcares; harina, sal, bicarbonato; envase hermético |
| 3 | Dulce Herencia | Alfajores de manjar blanco | Azúcar, grasas saturadas | Manjar blanco, harina, mantequilla, yema; alérgenos leche, huevo, gluten |
| 4 | Jardín Andino | Infusión de manzanilla | Ninguno | Preparación con agua hervida; manzanilla 100 %; 1 kcal/100 ml |

Trampa didáctica: las cajas 1 y 3 tienen los mismos octógonos; solo ingredientes y alérgenos las distinguen. La caja 4 no lleva octógonos y su ausencia es evidencia.

Estación 2: formulación correcta «nombre que indica la verdadera naturaleza del alimento, de forma específica y no genérica»; solo «Bombones de chocolate» es denominación. Estación 5: solo ALTO EN AZÚCAR (24 g ≥ 10 g; sodio 85 mg, grasa sat. 1,5 g y trans 0 g bajo umbral); cara frontal 96 cm² → octógono 2,0 × 2,51 cm según el proyecto de Manual notificado a la OMC (2017) `[CONFIRMAR con la versión aprobada]`.

## 6. Ayudas

Narración 🔈 de la misión, cada consigna, cada caso y cada anagrama; 🗣️ Voz lee avisos y zonas reveladas; señales sonoras con transcripción; fichas de evidencia en texto grande junto a la etiqueta; vistas Tapa/Base/Plano y ampliación; 🎯 ¿Qué me falta?; mapa; panel Pausa · Pista · Dato clave · Contexto · Reintento en cada error; temporizadores que no bloquean.

## 7. Fidelidad y ficción

Marcas, fabricante («Alimentos del Sur S.A.»), RUC, registro sanitario y valores nutricionales son ficticios y aproximados `[CONFIRMAR]`. Las mecánicas (escena para examinar, deducción por eliminación, candado, anagrama) se tomaron como tipo de juego de los libros de referencia, sin reproducir su contenido; de los cuatro libros extensos solo se revisaron títulos y encabezados.

## 8. Técnica

Un solo HTML por versión, sin dependencias externas (qrcode-generator incrustado), estado en memoria (sin `localStorage`), constancia imprimible con `@media print` (una página A4), probado con Playwright: recorrido completo (87/100 con errores intencionales; docente 100/100), sin desborde a 375 px.
