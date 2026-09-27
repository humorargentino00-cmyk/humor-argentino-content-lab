# Secuencia — La zapatilla estaba apagada

ID: `secuencias-post-2026-09-27-0130-zapatilla-apagada`

## Analista

Corte Metricool 27/09/2026 01:32 ART: las escenas cotidianas simples y reconocibles sostienen mejor la señal disponible que los objetos absurdos sin acción. Originalidad contrastada con historial de las tres líneas; no repite anteojos, llaves, heladera, tostada, frasco ni carga corta.

## Creativo

**Hook:** celular al 2% antes de dormir.  
**Progresión:** 01 batería baja → 02 conectar el cable → 03 descubrir zapatilla apagada → 04 encender y comenzar la carga.  
**Remate:** todo estaba enchufado excepto la corriente.

**Continuidad:** mismo teléfono rojo, cable blanco, mesa de luz de madera oscura, lámpara gris, pared beige y luz cálida nocturna.

| Cuadro | Tiempo | Texto de montaje |
| --- | --- | --- |
| 01 | 0,0–1,5 s | «2%. Tranquilo.» |
| 02 | 1,5–3,0 s | «Lo enchufé.» |
| 03 | 3,0–5,5 s | «Pasaron veinte minutos...» |
| 04 | 5,5–8,5 s | «La zapatilla: apagada.» |

Audio: **“Electric Feel” — MGMT**, título y artista verificados en el canal oficial del artista; disponibilidad en TikTok **NO VERIFICADA**. Entrar suave en 01 y acentuar el interruptor en 04. Caption: `Todo conectado menos la electricidad.`

## Prompts exactos

### 01

```text
Use case: photorealistic-natural
Asset type: frame 01 of four for one vertical social post, sequence secuencias-post-2026-09-27-0130-zapatilla-apagada
Primary request: Create ONE photorealistic vertical 9:16 candid smartphone photo in a modest Argentine bedroom at night. A single red smartphone lies flat on a dark wooden bedside table beside a plain gray lamp. Its screen is on and clearly shows one large nearly empty red battery icon with the simple number “2%” underneath. A white charging cable lies nearby but is not yet connected to the phone. The low battery is the unmistakable hook.
Continuity: preserve this exact red phone, dark wooden table, gray lamp, white cable, beige wall and warm lamp light for frames 02–04.
Composition/framing: vertical close-up showing the complete phone, cable end, table surface and recognizable lamp base, one scene only.
Constraints: exact text “2%” only, one phone, one cable, no hands, realistic phone proportions, screen and shadows plausible.
Avoid: no other text, no logos, no watermark, no collage, no split screen, no multiple panels, no duplicated cable, no advertising look.
```

### 02

```text
Use case: photorealistic-natural
Asset type: frame 02 of four for sequence secuencias-post-2026-09-27-0130-zapatilla-apagada
Input image role: frame 01 is the strict continuity reference and edit basis.
Primary request: Create ONE photorealistic vertical 9:16 frame in the exact same bedroom, angle, dark wooden bedside table, gray lamp, warm light, red smartphone and white charging cable. Change only the cable state: a normal adult hand enters from the right and plugs the same white connector fully into the phone’s bottom charging port. Keep the phone lying flat in the exact same position. The screen remains on and still shows the same large nearly empty red battery icon with exactly “2%”; do not show a charging symbol yet.
Composition/framing: same close-up and camera direction as frame 01, complete phone and connector visible.
Constraints: one anatomically correct hand, connector aligned with the port, one phone and one cable.
Avoid: no other text, no logos, no watermark, no collage, no extra hands, no duplicated cable, no changed phone color, no changed lamp or table.
```

### 03 — prompt inicial y corrección

```text
Use case: photorealistic-natural
Asset type: frame 03 of four for sequence secuencias-post-2026-09-27-0130-zapatilla-apagada
Input image role: frame 02 is the strict continuity reference.
Primary request: Create ONE photorealistic vertical 9:16 candid smartphone photo lower beside the exact same dark wooden bedside table in the same beige bedroom and warm light. The same white charging cable now runs continuously from above the frame into a plain white USB adapter that is correctly plugged into one socket of a black power strip on the wooden floor. The power strip’s single red rocker switch is unmistakably in the OFF position and its indicator light is dark. Nothing is wrong with the cable connection; the switched-off strip is the new clue. The red phone may appear softly out of focus on the same table above, still connected.
Continuity: preserve red phone, white cable, dark table, gray lamp, beige wall and warm light.
Composition/framing: vertical close-up emphasizing the whole black power strip, white adapter, continuous cable and dark OFF switch, one scene only.
Constraints: one power strip, one adapter, one continuous cable, plausible plug geometry and floor contact, no hands.
Avoid: no readable brand text, no logos, no watermark, no collage, no split screen, no duplicate cables, no glowing switch, no floating plugs, no changed room.
```

Corrección específica aplicada por estado ambiguo del interruptor:

```text
Use case: precise-object-edit
Asset type: corrected frame 03 of four for sequence secuencias-post-2026-09-27-0130-zapatilla-apagada
Primary request: Correct ONLY the power-strip rocker switch so its OFF state is unmistakable. Keep the exact same bedroom, red phone, white cable, adapter, black power strip, camera angle, composition and warm light unchanged. Replace the ambiguous marking with a standard red rocker showing a clean white “I” on one half and “O” on the other; the “O” half must be visibly pressed down and the switch must emit no light. The white adapter remains fully plugged into the strip and the cable remains continuous to the red phone.
Constraints: one power strip, one switch, one adapter, one cable; realistic electrical geometry.
Avoid: no other changes, no new text, no logos, no watermark, no collage, no extra cable, no glowing indicator.
```

### 04

```text
Use case: photorealistic-natural
Asset type: frame 04 and reveal for sequence secuencias-post-2026-09-27-0130-zapatilla-apagada
Input image role: corrected frame 03 is the strict continuity reference and edit basis.
Primary request: Create ONE photorealistic vertical 9:16 image in the exact same bedroom, floor-level angle, warm light, red phone, dark table, gray lamp, white cable, adapter and black power strip. Change only the power state and add one adult hand: a normal index finger has just pressed the red rocker to the ON “I” side. The switch now emits a small plausible red glow. The same red phone remains connected on the table above and its screen now clearly shows a green charging battery icon; no percentage text is necessary. This is the reveal that the strip had been switched off.
Composition/framing: retain the whole power strip and switch in the foreground, continuous cable to the visible phone above, one coherent scene.
Constraints: one anatomically correct hand, one power strip, one adapter, one continuous cable, believable switch pressure and electrical geometry.
Avoid: no other changes, no logos, no watermark, no collage, no split screen, no duplicated cable, no sparks, no floating plug, no changed furniture or phone color.
```

## Corrector y Validador

- 01 y 02 aprobados al primer intento.
- 03 requirió una corrección específica: el interruptor inicial no distinguía bien OFF; la segunda salida muestra `O` y ausencia de luz.
- 04 aprobado al primer intento, con interruptor iluminado y carga verde.
- Continuidad de teléfono, cable, mesa, lámpara y ambiente verificada; geometría de enchufe, adaptador y mano plausible.
- Estado técnico: **SECUENCIA COMPLETA 4/4**, cuatro PNG guardados.
- Aptitud editorial: **UTILIZABLE provisional**, pendiente de revisión de Juan.

Rutas: `/Humor Argentino/Branch 2 - Secuencias/Vida cotidiana/2026-09-27-0130-zapatilla-apagada/`.

No se generó video ni se publicó.
