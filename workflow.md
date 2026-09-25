# Workflow experimental — video

Esta línea corre por separado de `main` y `secuencias-post`, con la misma frecuencia horaria. Su destino exclusivo es `/Humor Argentino/Experimental/` y sus registros propios del branch. Una corrida apunta a **cuatro conceptos de video distintos**. No contar sus productos en los inventarios de otras líneas.

## Etapas
1. Analista: consultar métricas recientes verificables o declarar último corte y limitaciones; revisar historial de los tres branches para no repetir el chiste.
2. Creativo: proponer exactamente cuatro clips originales 9:16, de preferencia 7–8 s, con hook, una acción, remate, prompt de video completo, texto exacto y tiempos, audio específico (título y artista verificables), caption y condiciones de aprobación.
3. Corrector: revisar originalidad, acción, continuidad, física, claridad, duración, audio y montaje mínimo. Entregar APROBADO o CORREGIR y el prompt completo corregido.
4. Validador: verificar los cuatro y la vía real para producir un archivo de video individual guardable. Marcar APROBADO PARA GENERAR VIDEO o BLOQUEADO con motivo concreto.
5. Producción: procesar cada clip por separado y en orden. Enviar el prompt completo a una herramienta de video que lo acepte explícitamente. Inspeccionar el video devuelto por objeto, acción, encuadre, duración, ausencia de mosaico y remate. Una corrección específica y una regeneración máxima por clip; si vuelve a fallar, marcar pendiente y seguir. Nunca usar el archivo de otro concepto.
6. Curador: guardar cada clip aprobado como archivo de video individual en `/Humor Argentino/Experimental/<tema>/`, con fecha, ID y extensión real. Confirmar existencia, registrar prompt exacto, estado, archivo, intentos y fallo en `datos/inventario-videos.md` y corrida de GitHub. Sólo cuatro archivos correctos y guardados completan la corrida. No publicar.

## Capacidad y costo
Antes de generar, comprobar si hay una herramienta de video disponible, con entrada explícita y salida individual guardable. No contratar servicios, introducir APIs pagas ni gastar créditos externos adicionales. Si sólo se pueden crear imágenes, no llamarlas videos terminados; registrar BLOQUEADO y explicar qué falta. Una generación de video imposible no se sustituye por un prompt o un clip de otro concepto. El audio se recomienda para seleccionar en TikTok al publicar; no incrustar una canción sin archivo o licencia disponible.

## Aislamiento
La programación horaria es independiente y el ID de corrida debe ser único por fecha/hora local y branch. Evitar duplicados si una ejecución tarda más de una hora. Los informes del Curador de esta línea usan sólo su inventario y sus archivos. Mantener los tres contadores separados.
