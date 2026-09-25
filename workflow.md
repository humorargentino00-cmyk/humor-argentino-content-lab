# Branch 1 — Prompts listos para Gemini

Este es el branch Git `experimental`. Corre a la misma frecuencia horaria que `main` y Branch 2, con inventario y destino exclusivos. El entregable de cada corrida son **cuatro prompts diferentes, completos y listos para pegar en Gemini**, cada uno para un post distinto. **No genera imágenes ni videos y no usa créditos de Gemini.**

## Flujo
1. **Analista:** consultar métricas recientes verificables de @humor.argentino97 cuando estén disponibles; si no, usar el último corte confirmado, con fecha y limitaciones. Revisar historial de publicaciones, descartados, Main y Branch 2 para evitar repeticiones.
2. **Creativo:** proponer cuatro conceptos originales y distintos entre sí, cada uno con hook de 0–1 s, una acción realizable, remate visual, duración sugerida 7–8 s y un prompt Gemini autocontenido. Incluir formato vertical 9:16, realismo cotidiano, escena, sujeto, acción, encuadre, iluminación, continuidad, restricciones y qué resultado aceptar. Incluir texto exacto y timing de montaje fuera de la generación, caption breve y audio con título y artista; marcar disponibilidad TikTok no verificada cuando corresponda.
3. **Corrector:** revisar originalidad, física, anatomía, claridad, probabilidades de generación y costo humano de editar. Corregir cada prompt **antes** de entregarlo. Máximo una propuesta de reemplazo por concepto si falla el filtro; no gastar generación.
4. **Validador:** confirmar cuatro prompts íntegros, separados, originales y copiables, con análisis y corrección registrados. Estado final `PROMPTS LISTOS PARA GEMINI` o `PENDIENTE` con causa exacta.
5. **Curador:** crear un archivo Markdown de corrida con cuatro secciones independientes, prompts exactos, instrucciones de uso, audio y texto, en `/Humor Argentino/Branch 1 - Prompts Gemini/<tema o mixtos>/`; confirmar guardado y registrar el mismo contenido, ruta y estado en GitHub bajo `produccion/corridas/`. Actualizar `datos/inventario-prompts.md` con paquetes y prompts aprobados por temática. No contar un archivo .md como imagen ni como video.

## Regla de costo y alcance
No llamar a generadores de imagen o video, ni abrir Gemini, ni contratar o conectar herramientas pagas. Juan elegirá qué prompts copiar y ejecutará Gemini con sus créditos cuando quiera. No publicar ni enviar contenido a redes. Si falta una métrica o un audio verificable, declararlo; no bloquear un buen prompt por indisponibilidad de generación.

## Aislamiento
La carpeta de este branch es `/Humor Argentino/Branch 1 - Prompts Gemini`. `main` utiliza `/Humor Argentino/Main` y Branch 2 utiliza `/Humor Argentino/Branch 2 - Secuencias`. Cada corrida usa ID único por fecha/hora ART; evitar duplicados y mantener contadores separados.
