# Branch 2 — Secuencias de fotos para un post

Este branch parte de `main` y conserva el circuito Analista → Creativo → Corrector → Validador → generación → Curador. Su diferencia es la unidad creativa: **una historia original por corrida, contada en cuatro imágenes independientes y ordenadas**, destinadas a formar un solo post o video corto. No se mezcla con el stock de cuatro conceptos independientes de `main`.

## 1. Analista
Consultar las métricas recientes de @humor.argentino97 cuando estén disponibles, con fuente y fecha. Si no, usar el último corte verificado y declarar su antigüedad. Detectar el tipo de situación, hook y remate que merece una secuencia; no atribuir desempeño a métricas inexistentes. Revisar historial de publicaciones, aprobados, descartados y secuencias para evitar repetir el chiste.

## 2. Creativo
Entregar **un concepto y cuatro cuadros**: situación inicial, pista o expectativa, acercamiento y remate. Cada cuadro debe aportar información nueva al mismo chiste. Definir un objeto protagonista, escenario, iluminación, utilería y rasgos visuales invariantes para mantener continuidad. Escribir cuatro prompts completos, uno por cuadro, con identificadores `<fecha>-<secuencia>-01` a `04`. Imágenes fotorrealistas verticales 9:16, individuales, sin mosaicos ni textos integrados salvo decisión justificada.

Entregar además: hook, texto breve exacto por cuadro o en montaje, duración sugerida (preferencia 7–10 s), transición y momento del remate, nombre y artista del audio recomendado, y qué función cumple. Verificar título y artista en una fuente confiable. La disponibilidad de ese audio dentro de TikTok debe verificarse aparte; si no se pudo, marcar **AUDIO EN TIKTOK NO VERIFICADO**. No generar ni incrustar música.

## 3. Corrector
Revisar los cuatro cuadros **como una sola historia**. Comprobar que el primer cuadro atraiga, que cada cambio sea legible, que el remate no aparezca antes de tiempo, que objetos, tamaño, posición, fondo, luz y encuadre mantengan continuidad y que el texto se lea en el tiempo sugerido. Revisar originalidad frente al historial, realismo y facilidad de montar desde el teléfono. Marcar APROBADO o CORREGIR y entregar el prompt completo corregido del cuadro afectado.

## 4. Validador
Aprobar únicamente cuando existan cuatro prompts completos y ordenados, una sola historia original, texto y audio identificados, revisión del Corrector y una vía real de generación/guardado. Registrar incertidumbres y estado por cuadro. Resultado: APROBADO PARA GENERAR o BLOQUEADO con etapa y motivo.

## 5. Producción
Procesar **cuadro por cuadro y en orden**. Para cada cuadro, enviar a la herramienta el texto completo de SU prompt aprobado, pedir UNA imagen vertical 9:16 y conservar identificador, prompt exacto y archivo devuelto asociados. Cuando la herramienta admita referencia a la imagen anterior, usarla para continuidad visual, sin perder el prompt explícito. Si no admite referencia, repetir los invariantes visuales en cada prompt.

Inspeccionar visualmente sujeto, acción, encuadre, continuidad con los cuadros anteriores, legibilidad del remate y ausencia de collage. Permitir una sola corrección específica y una nueva generación por cuadro. Si vuelve a fallar, marcarlo pendiente y continuar los restantes; **la secuencia no está completa ni lista para montar** hasta que haya cuatro cuadros correctos. No sustituir un cuadro por una imagen de otro concepto.

Guardar cada imagen aprobada como archivo individual en `/Humor Argentino/Branch 2 - Secuencias`, con fecha, ID de secuencia y número de cuadro. Confirmar cada archivo antes de contarla. Registrar en GitHub prompt exacto enviado, intentos, revisión, estado generado/aprobado/guardado o pendiente, ruta y motivo de fallo. Conservar un manifiesto del post con el orden 01–04, textos, tiempos y audio. Los prompts no sustituyen a los PNG. No publicar ni generar video automáticamente.

## 6. Curador
Aplicar `agentes/05-curador.md` después del guardado. Clasificar la secuencia por **una temática principal** y mantener sus cuatro imágenes juntas en `/Humor Argentino/Branch 2 - Secuencias/<tema>/<id>/`, en orden numérico. Contrastar cada alta con Biblioteca y registrar dos contadores distintos: imágenes individuales verificadas y secuencias completas de cuatro cuadros. Una secuencia incompleta queda pendiente aunque tenga imágenes parciales guardadas; no se presenta como post listo.

## Cadencia y aislamiento
La regla heredada de cuatro imágenes por corrida significa aquí cuatro cuadros de un post. La tarea horaria específica de este branch ejecuta esta línea de forma independiente de `main` y Branch 1. Cada corrida usa un ID único e idempotente para evitar duplicados. La serie diaria «Alarma negociada» y su prioridad matinal siguen en `main`; este branch produce su secuencia propia en la corrida horaria. Branch 1 sólo entrega prompts para Gemini; sus archivos Markdown y contadores no forman parte de esta línea.

## Ejemplo de referencia
Ver `produccion/secuencias/ejemplo-freezer-helado.md`: freezer cerrado → abierto con pote al fondo → pote afuera → pote abierto con otra comida. El video propuesto usaría «La noche sin ti» de Los Huayra como contraste dramático; verificar el sonido seleccionable en TikTok antes del montaje.
