# Arquitectura y conceptos del sistema — Humor Argentino

Este documento traduce decisiones prácticas del Lab a conceptos técnicos de diseño de sistemas de IA.
Su objetivo es conservar el conocimiento arquitectónico aunque Juan no recuerde los nombres técnicos.

> Estado: documentación de diseño. No reactiva la fábrica ni autoriza publicación o gasto.

## Norte del sistema
**Objetivo final:** lograr monetización rentable de la cuenta de TikTok.
La producción de imágenes, views, likes, seguidores y engagement son medios o señales; no sustituyen el objetivo económico.

## Mapa de conceptos aplicados

### Agente / Skill / Rule / Workflow
- **Agent:** especialista con responsabilidad definida (Analista, Creativo, Corrector, Validador, Curador).
- **Skill:** procedimiento estandarizado para ejecutar una capacidad.
- **Rule:** límite o condición que debe respetarse.
- **Workflow:** secuencia y lógica de pasos, decisiones y handoffs.

### Separation of concerns + Least privilege
Cada agente debe tener una responsabilidad clara y solo los permisos/herramientas necesarios para cumplirla.
Ejemplo: Analista necesita leer métricas; no necesita permiso para borrar publicaciones o modificar la cuenta.

### Orchestration + Supervisor
- **Orchestrator:** componente que hace avanzar la ejecución según el workflow y decide el siguiente paso.
- **Supervisor:** control/auditor que verifica que no se hayan omitido etapas o reglas.
No asumir que son el mismo componente.

### Memory / Context / Retrieval / RAG
- **Memory:** conocimiento persistente entre corridas: ideas usadas, descartes, métricas, errores y aprendizajes.
- **Context:** información efectivamente disponible para el agente durante la tarea actual.
- **Retrieval:** recuperar de la memoria solo lo relevante para la tarea.
- **RAG:** recuperar información relevante y entregarla como contexto antes de generar/decidir.
No cargar todo el historial indiscriminadamente. Antes de crear, consultar ideas semánticamente similares y aprendizajes aplicables.

### Semantic search / Embeddings
Cuando exista volumen suficiente, detectar similitud por significado y no solo por palabras exactas. Esto puede ayudar a prevenir ideas repetidas aunque estén redactadas de otra manera.

### State + Checkpoint
- **State:** situación actual de una corrida (etapa, piezas completadas, intentos usados, pendientes).
- **Checkpoint:** persistencia del estado necesaria para retomar sin empezar desde cero.
Un commit de Git guarda estado del proyecto; un checkpoint guarda por dónde iba una ejecución.

### Human-in-the-loop (HITL)
El control humano se ubica según riesgo, costo y reversibilidad.
Regla de Juan: **todo gasto de dinero requiere autorización**.
La publicación automática no es un veto permanente: podrá automatizarse si deja de implicar costo/riesgo relevante y el Lab demuestra confiabilidad suficiente.

### Guardrails
Autonomía dentro de límites explícitos: intentos máximos, permisos, presupuesto, reglas editoriales, no borrar memoria histórica, no saltar validación y escalar decisiones de riesgo.

### Error handling / Retry / Fallback / Escalation
Definir qué ocurre ante fallos:
1. retry limitado cuando corresponda;
2. fallback seguro si existe;
3. escalation a Juan cuando el sistema no pueda resolver con seguridad.
El máximo de 2 intentos es un techo, no obligación de gastar ambos.

### Idempotency
Repetir una operación no debe crear duplicados no deseados.
Toda pieza/corrida debe tener ID único y, antes de repetir guardado/publicación, verificar si ese ID ya fue procesado.

### Observability
Registrar evidencia para entender qué hizo el sistema.
- **Logs:** qué ocurrió.
- **Metrics:** cómo está rindiendo.
- **Alerts:** cuándo requiere atención.
"Corrida completada" no equivale a "corrida exitosa".

### KPI / Output / Outcome
- **Output:** lo producido (ideas, imágenes, publicaciones).
- **Outcome:** resultado conseguido (audiencia útil, crecimiento, monetización, rentabilidad).
Medir cantidad producida no basta.

### Feedback loop
Producción → resultado real → medición → aprendizaje → actualización de memoria/reglas → nueva producción.
Los descartes deben alimentar aprendizaje, no ser solo basura.

### Evals / Dataset / Benchmark / Regression
Las decisiones humanas sobre piezas deben convertirse gradualmente en datos de evaluación.
Rubrica inicial:
- gracia;
- comprensión rápida del chiste;
- geometría;
- diseño;
- calidad visual;
- resultado final UTILIZABLE / CORREGIR / DESCARTAR;
- motivo.
Conservar casos estables como benchmark para comparar versiones y detectar regresiones.

### Alignment / Objective function / Guardrails
El sistema debe optimizar lo que Juan realmente quiere: **rentabilidad sostenible**, no una métrica sustituta.
Views, likes o cantidad de imágenes pueden ser señales, nunca el objetivo absoluto.

### Goodhart
No convertir una sola métrica intermedia en el objetivo. Maximizar views puede empeorar rentabilidad, identidad o calidad.

### Optimization + Trade-offs
Elegir acciones según objetivo y recursos. Calidad, cantidad, costo, velocidad y riesgo compiten; explicitar los trade-offs.

### Exploration vs Exploitation
- **Exploitation:** usar formatos ya comprobados.
- **Exploration:** reservar capacidad para descubrir formatos mejores.
Nunca convertir automáticamente una señal ganadora en 100% de la producción.

### Confidence + Decision thresholds
La fuerza de la evidencia debe determinar el nivel de autonomía:
- evidencia baja: observar;
- media: experimentar;
- alta: aumentar prioridad;
- decisiones caras/irreversibles: exigir umbral mayor o autorización.

### Multi-armed bandit / Portfolio strategy
Distribuir producción entre líneas conocidas y experimentales, ajustando porcentajes según resultados, sin cerrar exploración prematuramente.

### Local optimum
Una estrategia que funciona muy bien puede impedir descubrir una mejor si se detiene la exploración.

### Concept drift / Recency weighting / Seasonality
El mundo cambia. Dar mayor peso a señales recientes sin borrar el historial.
Conservar datos antiguos porque pueden revelar patrones estacionales o volver a ser relevantes en contextos similares.

### Experimentation / A-B tests / Confounders
Probar hipótesis controlando variables cuando sea posible.
Correlación no implica causalidad: horario, audiencia inicial, audio, distribución y contexto pueden confundir conclusiones.

## Regla de aprendizaje del Lab
Cada nuevo concepto del curso que tenga aplicación real en Humor debe:
1. documentarse aquí con nombre técnico + explicación práctica;
2. vincularse a una regla/workflow/agente solo si cambia comportamiento real;
3. no activarse en producción hasta estar suficientemente definido y evaluado;
4. conservar trazabilidad de por qué se incorporó.

## Pendiente antes de reactivar fábrica
- Diseñar retrieval real contra historial para evitar repeticiones.
- Crear dataset/rúbrica de evaluación a partir de revisión humana del stock.
- Definir KPIs conectados con monetización/rentabilidad.
- Formalizar state/checkpoints e idempotencia.
- Definir observabilidad y alertas.
- Revisar qué componente cumple orquestación y cuál supervisión.
- Establecer política de exploración/explotación y umbrales de confianza.
- Revisar permisos y puntos HITL.


## Línea recurrente de identidad — «Alarma negociada»

«Alarma negociada» no debe evaluarse como una pieza aislada de performance. Su función principal es construir **identidad, reconocimiento y hábito** mediante repetición deliberada.

### Brand consistency / Distinctive assets
La serie conserva activos reconocibles:
- mismo chiste o estructura base;
- mismo audio de referencia;
- composición visual altamente reconocible;
- despertador/alarma como elemento distintivo.

Cambian principalmente:
- día de la semana;
- fecha/contexto cuando corresponda;
- meteorología real del día.

Objetivo buscado: que el follower reconozca inmediatamente la serie y la asocie con Humor Argentino ("esta es la cuenta que todos los días me dice qué día es").

### Serie de identidad vs contenido de performance
No todas las publicaciones cumplen la misma función.
- **Performance content:** prioriza alcance, engagement, adquisición de seguidores y señales hacia monetización.
- **Identity content:** prioriza reconocimiento, familiaridad, hábito y asociación con la cuenta.

Por lo tanto, una publicación individual de «Alarma negociada» con pocas views NO autoriza a descartar automáticamente la serie.

### Evaluación longitudinal
La unidad principal de evaluación es la **serie a lo largo del tiempo**, no una única publicación.
Observar, entre otras señales:
- estabilidad o crecimiento de audiencia recurrente;
- interacción repetida de los mismos seguidores;
- reconocimiento/comentarios asociados a la serie;
- visitas al perfil y follows cuando puedan atribuirse razonablemente;
- evolución de alcance/retención de la serie;
- contribución indirecta al rendimiento general de la cuenta.

### Guardrail de identidad
El optimizador no puede eliminar, reemplazar ni transformar radicalmente esta serie solo porque otro formato tenga mayor rendimiento inmediato.
Cualquier cambio estructural en chiste base, audio o identidad visual debe tratarse como una decisión de producto/identidad y no como una optimización automática de corto plazo.

### Exploration / Exploitation dentro de la serie
La consistencia es parte del producto. La exploración debe hacerse sobre variables periféricas sin destruir los activos distintivos. Si se experimenta, registrar claramente qué variable cambió y comparar longitudinalmente.
