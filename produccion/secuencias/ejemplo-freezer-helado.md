# Ejemplo de secuencia — el pote del freezer

Estado: **guion y prompts listos para prueba en este branch**. Imágenes aún no generadas; no contar como stock ni post terminado.

## Analista
Referencia editorial aportada por Juan: humor cotidiano con foto realista y audio emotivo usado en contraste. No se atribuyen métricas actuales a esta idea. Evitar la geometría del «último pedazo de pizza» descartado: aquí el remate es un solo contenido claramente visible dentro de un pote.

## Creativo
**Un único chiste:** la ilusión de encontrar helado termina en un pote reutilizado para guardar lentejas congeladas.

**Continuidad fija:** freezer blanco doméstico con manija horizontal y un pequeño imán redondo azul en la esquina superior derecha; cocina modesta de azulejos beige, mesada gris moteada; pote circular blanco con tapa azul lisa y una pequeña marca de desgaste en el borde delantero, sin logos ni texto. Misma luz fría de cocina, perspectiva de cámara de teléfono, fotorrealismo cotidiano. El pote del fondo del cuadro 02 es exactamente el que sale en 03 y se abre en 04. La textura interior es lentejas cocidas y congeladas, inequívocamente comida salada, nunca helado. La marca de desgaste es una pista visual de identidad, no un logo.

| Cuadro | Duración | Imagen / información nueva | Texto para montaje |
| --- | --- | --- | --- |
| 01 | 0,0–1,5 s | Freezer cerrado, expectativa cotidiana | «Cuando te acordás que hay helado...» |
| 02 | 1,5–3,5 s | Freezer abierto; pote azul al fondo | «Y encontrás el pote» |
| 03 | 3,5–5,5 s | Pote sobre mesada, tapa aún cerrada | «Te cambia la noche» |
| 04 | 5,5–9,0 s | Pote abierto: lentejas congeladas | «Eran lentejas.» |

Corte directo 01→02, acercamiento 02→03, pequeño silencio/pausa antes de 04 y sostener el remate 3 segundos. El texto se agrega en el editor, no dentro de las imágenes. Formato sugerido 9:16, 9 s, sin voz generada. El mismo cuadro 04 puede llevar una descripción breve: «La traición venía en pote de helado». No se ha creado video.

**Audio solicitado:** «La noche sin ti» — **Los Huayra**. Título/artista verificados en el canal oficial del grupo: https://www.youtube.com/watch?v=yaxcMQIgzhw . Función: melodrama irónico; introducir suave desde el cuadro 01 y sostener la revelación en el 04. **AUDIO EN TIKTOK NO VERIFICADO**: buscar el sonido exacto en la app al montar, comprobar versión y permisos de la cuenta; no afirmar que se puede seleccionar aún. No copiar letras de la canción ni incrustar audio.

## Prompts aprobados como diseño para prueba

### `freezer-helado-01` — freezer cerrado
```text
Use case: photorealistic-natural
Asset type: frame 01 of four for one short vertical social post
Primary request: Create ONE photorealistic vertical 9:16 candid smartphone image of a modest Argentine kitchen at night. A plain white domestic freezer is completely closed, with a horizontal handle and exactly one small round blue magnet at the upper-right corner. Beige wall tiles and a gray speckled counter edge establish the kitchen. Quiet anticipation: the closed freezer is the unmistakable subject. Natural imperfect cool kitchen light, ordinary wear, unpolished home realism.
Continuity: preserve the same freezer, blue magnet, beige tiles, gray counter and cool lighting for the next frames.
Composition/framing: eye-level vertical view showing the complete closed freezer door and surroundings in one scene.
Constraints: no people, no hands, no visible food or ice-cream tub yet, no logos, no readable text, no embedded caption, no watermark, no collage, no split screen, no multiple panels, one image only.
```

### `freezer-helado-02` — pote al fondo
```text
Use case: photorealistic-natural
Asset type: frame 02 of four for the same short vertical social post
Primary request: Create ONE photorealistic vertical 9:16 candid smartphone image in the exact modest Argentine kitchen from frame 01. The same plain white freezer with horizontal handle and one small round blue magnet at its upper-right corner is now open. Deep on the middle freezer shelf sits one circular plain white food tub with a smooth blue lid and a tiny worn mark on its front rim. Show the tub clearly enough to find it, but keep it at the back so the contents remain completely hidden. Beige wall tiles, gray speckled counter edge, natural imperfect cool kitchen light, ordinary home realism.
Continuity: same freezer geometry, blue magnet, beige tiles and gray counter as frame 01; this exact tub with the blue lid and worn front rim must be moved to the counter in frame 03.
Composition/framing: eye-level vertical view of the open freezer, open door and tub at the back, one scene only.
Constraints: no people, no hands, exactly one blue-lidded tub, do not show its contents or any other ice-cream container, no logos, no readable text, no embedded caption, no watermark, no collage, no split screen, no multiple panels, one image only.
```

### `freezer-helado-03` — pote cerrado en mesada
```text
Use case: photorealistic-natural
Asset type: frame 03 of four for the same short vertical social post
Primary request: Create ONE photorealistic vertical 9:16 candid smartphone image in the exact modest Argentine kitchen from frames 01 and 02. The identical circular plain white food tub with the same smooth blue lid and tiny worn mark on its front rim now rests closed on the gray speckled counter. The same white freezer is visible softly in the background, its single round blue magnet still at the upper-right corner; beige wall tiles and cool imperfect kitchen light remain consistent. The intact lid fully hides the contents. A small damp ring under the cold tub adds ordinary realism and anticipation.
Continuity: same tub, size, lid, worn rim, counter, freezer, magnet, tiles and light as earlier frames; frame 04 reveals this exact tub without changing container.
Composition/framing: vertical close-up of the complete closed tub on the counter with enough recognizable kitchen background, one scene only.
Constraints: no people, no hands, exactly one tub, no view inside it, no other food, no logos, no readable text, no embedded caption, no watermark, no collage, no split screen, no multiple panels, one image only.
```

### `freezer-helado-04` — remate
```text
Use case: photorealistic-natural
Asset type: frame 04 and reveal of the same short vertical social post
Primary request: Create ONE photorealistic vertical 9:16 candid smartphone close-up in the exact modest Argentine kitchen from frames 01–03. The same circular plain white food tub with tiny worn mark on its front rim remains in the same position on the gray speckled counter. Its smooth blue lid now lies immediately beside it, face down. The tub is open and clearly filled to the top with unmistakable cooked brown lentils frozen together, with a little frost at the edge. This is leftover savory food in a reused ice-cream-style tub, not ice cream. The same white freezer and single round blue magnet remain softly visible behind beige tiles. Natural imperfect cool kitchen light, credible food and plastic texture, understated visual disappointment.
Continuity: preserve the exact tub, blue lid, worn rim, counter, freezer, magnet, tiles, lighting and camera direction from frame 03; change only the lid state and reveal the contents.
Composition/framing: vertical close-up with the whole open tub, separate lid and obvious lentils fully visible, one scene only.
Constraints: no people, no hands, exactly one tub and one lid, no ice cream, no other food, no logos, no readable text, no embedded caption, no watermark, no collage, no split screen, no multiple panels, one image only.
```

## Corrector y Validador
- El gag se entiende sin conocer la letra ni generar voz. Cada cuadro revela una sola etapa y reserva el contenido real para el 04.
- Riesgo principal: continuidad exacta del freezer y pote al generar cuadros aislados. Usar cuadro anterior como referencia visual cuando la herramienta lo permita; comparar rasgos antes de aprobar cada salida. Una corrección específica máxima por cuadro.
- Segundo riesgo: el generador confunda lentejas con helado. Inspeccionar contenido visual, rechazar si es ambiguo.
- Cuatro prompts completos, uno por imagen; orden y texto establecidos. **APROBADO COMO DISEÑO PARA PRUEBA**, no equivale a `SECUENCIA COMPLETA` hasta generar, inspeccionar y guardar cuatro PNG individuales.
