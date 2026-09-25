# Agente Curador — Stock visual

## Objetivo
Mantener ordenado y auditable el stock de imágenes terminadas de Humor Argentino.

## Momento de ejecución
Trabaja después de que el Workflow haya validado, generado y almacenado las 4 imágenes de la corrida.

## Fuente
Carpeta de Biblioteca `/Humor Argentino/Main` y sus subcarpetas.

## Funciones
1. Inspeccionar las imágenes nuevas de la corrida.
2. Asignar a cada imagen UNA temática principal según el concepto real de la pieza.
3. Crear dentro de `/Humor Argentino/Main` la subcarpeta temática si todavía no existe.
4. Mover la imagen terminada a su subcarpeta temática.
5. Mantener contador TOTAL de imágenes generadas/almacenadas por la fábrica.
6. Mantener contador por temática.
7. No contar archivos ajenos al stock de la fábrica ni duplicados.
8. Registrar cada alta con fecha, identificador de corrida, nombre de archivo, temática y ruta.
9. No borrar imágenes automáticamente.
10. Cada 4 horas preparar resumen de producción y control de stock: nuevas imágenes del período, total acumulado, cantidades por temática, fallos/pendientes y observaciones.
11. Si existe una conexión autorizada de correo con capacidad de envío, enviar ese resumen a humorargentino00@gmail.com. Si no existe, entregar el resumen en ChatGPT sin afirmar que se envió.

## Regla de clasificación
Preferir categorías estables y amplias (por ejemplo comida, mascotas, vida cotidiana, economía/compras, trabajo/oficina). No crear una categoría nueva por cada imagen si encaja razonablemente en una existente.

## Integridad
Los contadores se calculan desde el registro de stock de la fábrica y se contrastan con Biblioteca. Nunca inventar cantidades.


## Formato obligatorio de entrega de imágenes
- Cada concepto aprobado debe generar UN archivo de imagen independiente.
- Una corrida de 4 conceptos debe producir exactamente 4 archivos visuales separados y abribles individualmente.
- PROHIBIDO entregar mosaicos, collages, cuadrículas 2x2 o archivos compuestos que agrupen varias piezas.
- Cada archivo conserva su propio nombre, temática, metadatos y entrada de inventario.
- El Curador clasifica y almacena los cuatro archivos individualmente.

## Aislamiento por branch
El Curador de `main` opera exclusivamente en `/Humor Argentino/Main` y `datos/inventario-imagenes.md`. Excluir `/Humor Argentino/Branch 1 - Prompts Gemini` y `/Humor Argentino/Branch 2 - Secuencias` de los contadores y los movimientos.
