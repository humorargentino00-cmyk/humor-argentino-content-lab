# Workflow principal — MAIN

1. **Agente Analista** obtiene todas las métricas disponibles de @humor.argentino97, registra limitaciones y entrega señales verificables.
2. **Agente Creativo** recibe el análisis, usa Instagram como radar de formatos transferibles y produce exactamente 4 propuestas nuevas sin copiar piezas.
3. **Agente Corrector** revisa las 4 antes de gastar créditos y marca APROBADO o CORREGIR.
4. **Agente Creativo** incorpora las correcciones.
5. **Agente Validador** verifica orden, reglas, evidencia y herramientas/APIs/MCP disponibles. Solo marca APROBADO PARA GENERAR cuando corresponde.
6. **Producción/publicación** genera únicamente aprobados, máximo 2 intentos por concepto, revisa antes de publicar, registra el resultado y vuelve al Analista.

No se saltean etapas.


## Producción continua de stock
- Main debe ejecutarse como workflow productivo recurrente una vez por hora.
- Cada corrida: Analista → Creativo (4 ideas nuevas) → Corrector → corrección → Validador → guardar stock aprobado.
- No requiere una orden manual del usuario para cada corrida.
- Generar stock NO implica publicar contenido ni gastar créditos de generación de video automáticamente.
- Conservar historial suficiente para impedir repeticiones entre corridas.


## Generación y Biblioteca — MAIN
- Después de APROBADO PARA GENERAR, las piezas de imagen deben pasar de prompt a imagen final generada.
- El entregable de stock visual es la IMAGEN, no solamente el prompt.
- Cada imagen final debe guardarse en la Biblioteca del usuario cuando la ejecución disponga de generación de imagen y acceso de escritura a Biblioteca.
- Conservar prompt/metadatos en el repositorio para trazabilidad, pero el inventario consumible por el usuario debe ser el archivo visual final.
- No publicar automáticamente.


## Salida obligatoria por corrida horaria — MAIN
1. El workflow produce exactamente 4 propuestas nuevas.
2. Las 4 deben pasar Analista → Creativo → Corrector → corrección → Validador.
3. Solo cuando las 4 queden verificadas como originales, viables y APROBADAS PARA GENERAR, generar las 4 imágenes finales.
4. No considerar completada la corrida con prompts: el entregable son 4 archivos de imagen.
5. Guardar automáticamente las 4 imágenes finales en la carpeta de Biblioteca `/Humor Argentino/Main`.
6. Usar nombres únicos y descriptivos para evitar sobrescrituras, incluyendo fecha/hora o identificador de corrida.
7. Mantener prompts y metadatos en GitHub únicamente como trazabilidad.
8. Si alguna imagen falla la generación o el guardado, registrar cuál quedó pendiente; no sustituirla por una idea repetida ni afirmar que fue almacenada.
9. No publicar automáticamente.


## Curaduría posterior
Después de guardar las 4 imágenes finales de cada corrida en `/Humor Argentino/Main`, ejecutar `agentes/05-curador.md`. El Curador clasifica y mueve las imágenes a subcarpetas temáticas, actualiza inventario total y por temática y deja el stock auditable. La generación termina antes de la curaduría; la curaduría no modifica el concepto ni la imagen.


## Formato obligatorio de entrega de imágenes
- Cada concepto aprobado debe generar UN archivo de imagen independiente.
- Una corrida de 4 conceptos debe producir exactamente 4 archivos visuales separados y abribles individualmente.
- PROHIBIDO entregar mosaicos, collages, cuadrículas 2x2 o archivos compuestos que agrupen varias piezas.
- Cada archivo conserva su propio nombre, temática, metadatos y entrada de inventario.
- El Curador clasifica y almacena los cuatro archivos individualmente.

## Primera corrida de la mañana — serie «Alarma negociada»
- En la corrida de las 06:30, antes de generar el resto del stock, producir primero una versión diaria de la serie «Alarma negociada», lista para publicar antes de las 08:00 ART. Esta serie recurrente es una excepción explícita a NO REPETIR: cambia el día real del calendario y el fondo según el pronóstico; no cuenta como un concepto original nuevo.
- Usar fecha y día de semana de America/Buenos_Aires para el día de publicación. El día debe estar integrado y legible en la imagen, en español (viernes, sábado, domingo, etc.), sin depender de un texto que Juan agregue después. No usar un día fijo en el prompt ni reciclar el archivo del día anterior.
- Consultar el pronóstico actualizado para Ciudad Evita, Buenos Aires, para ese día. Lluvia → lluvia visible por ventana y luz gris; nublado → cielo cubierto y luz difusa; despejado → luz de amanecer y cielo claro. Si no hay pronóstico confiable, mantener fondo neutro y marcar clima no verificado. No presentar un pronóstico inventado.
- Conservar la composición reconocible: dormitorio realista, cama, mano que se estira hacia el celular, alarmas 07:00/07:05/07:10/07:15/07:20. Cambiar solamente el rótulo del día y el clima del exterior/iluminación. Un archivo individual vertical 9:16, sin collage; inspeccionar visualmente día, horarios, situación y clima. Si el texto del día sale mal, corregir una sola vez y, si persiste, marcar pendiente sin afirmar que está listo para publicar.
- Usar el texto breve del estilo publicado («jueves...», adaptado al día correcto) y registrar el audio de referencia «me levanto temprano a las 7am...» como referencia aportada por Juan. Verificar nombre/disponibilidad exactos en TikTok antes de recomendarlo como audio seleccionable; no incrustar audio en la imagen.
- Guardar la imagen aprobada con fecha local y `alarma-negociada-<dia>` en `/Humor Argentino/Main`; confirmar el archivo y registrar prompt exacto, pronóstico/fuente, revisión y estado en GitHub. Avisar a Juan con el archivo individual antes de las 08:00 cuando esté listo. No publicar automáticamente.
- La corrida matinal conserva cuatro archivos totales: la imagen diaria de la serie + tres conceptos nuevos que siguen Analista → Creativo → Corrector → Validador. Las otras corridas horarias conservan cuatro conceptos originales nuevos, sin repetir la serie durante el mismo día.

## Aislamiento de líneas
Esta línea guarda solamente su stock en `/Humor Argentino/Main/<temática>/`. Las otras líneas del repositorio tienen carpetas e inventarios propios: `/Humor Argentino/Branch 1 - Prompts Gemini` y `/Humor Argentino/Branch 2 - Secuencias`. No contar ni reclasificar archivos de esas líneas. Una sola tarea horaria activa invoca Main, Branch 1 y Branch 2; esta sección define únicamente el trabajo de Main. Cada línea conserva sus rutas y contadores propios.
