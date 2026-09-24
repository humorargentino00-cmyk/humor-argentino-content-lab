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
