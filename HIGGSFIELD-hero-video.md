# Hero video con Higgsfield — guía + prompts

Objetivo: generar un video corto, cinematográfico y **en loop** para el fondo del hero del sitio SDI Systems. Debe verse moderno/tecnológico (bodega automatizada, conveyors, sorters), en tonos **azul/ámbar** de la marca (NO el rojo de Element Logic), con movimiento de cámara lento para que el texto encima se lea bien.

---

## 1. Cómo usar Higgsfield (desde cero)

1. Entra a **https://higgsfield.ai/ai/video** y crea tu cuenta (login con Google sirve).
2. Elige el modo **Image-to-Video** (imagen a video) — da más control porque el video hereda la composición y los colores de la imagen que subas.
3. **Sube tu imagen de inicio (Start frame)** — ver punto 2 más abajo qué imagen conviene.
4. Pega el **prompt** (punto 3). Los prompts van mejor **en inglés**.
5. Configura (punto 4): modelo, formato **16:9**, duración.
6. Genera. Tarda de segundos a un par de minutos.
7. Revisa y **itera cambiando una sola cosa por vez** (presupuesta 2–3 intentos para 1 clip bueno).
8. Descarga el MP4.

> Tip: una imagen de entrada nítida, con buena luz y poco desorden = mucho mejor resultado. La imagen "pone el techo" de calidad del video.

---

## 2. Qué imagen/frame subir

Tienes 3 caminos:

- **A) Recomendado — usar una foto real limpia como Start frame:** sube **`public/assets/img/casos/soprole-picking.jpg`** (1280×720, es la más nítida y luminosa, muestra conveyors reales). Higgsfield le da movimiento.
- **B) Generar la imagen desde cero** dentro de Higgsfield (Image generator / texto a imagen) con el prompt de imagen del punto 3, y luego animarla. Útil si quieres un look 100% a tu gusto y en azul/ámbar.
- **C) Restyle del video rojo actual:** si quieres conservar el movimiento del b-roll que ya tienes (`public/assets/video/hero-broll.mp4`) pero cambiarle el color/marca, busca el modo **Video-to-Video / "Recast"** y súbelo con el prompt de restyle (punto 3). Así le quitas el rojo de Element Logic.

---

## 3. Prompts listos (copiar/pegar)

### ▶️ Prompt A — Image-to-Video (subiendo la foto de Soprole)
```
Wide cinematic shot, eye level. Automated conveyor sorters move boxes and totes
through a modern distribution center. Slow dolly-in, smooth and subtle motion.
Cool blue and warm amber accent lighting, polished high-tech industrial atmosphere,
soft depth of field, premium and calm mood.
```

### ▶️ Prompt B — Text-to-Image (para generar la imagen base en azul/ámbar) y luego animarla
```
Wide establishing shot of a futuristic automated warehouse. Rows of conveyor belts
and high-speed parcel sorters, robotic AGVs gliding across a clean polished floor.
Cinematic blue and amber lighting, volumetric light beams, sleek modern technology,
ultra-detailed, 16:9, cinematic.
```
Y para animarla (Image-to-Video):
```
Slow lateral tracking camera moving right. Boxes glide along the conveyors,
AGVs move smoothly in the background. Calm, premium, high-tech mood. Subtle motion.
```

### ▶️ Prompt C — Video-to-Video / Recast (rebrandear el b-roll rojo)
```
Restyle this footage: replace the red lighting with cool blue and warm amber tones.
Sleek modern warehouse-automation look, cinematic, clean and premium. Keep the motion.
```

### 🚫 Negative prompt (pégalo en el campo "negative" si aparece)
```
text, logos, watermark, brand names, red branding, people staring at camera,
fast cuts, flicker, distortion, low quality, jitter
```

---

## 4. Configuración recomendada

- **Modelo:** para realismo, **Veo 3.1**; si quieres más control de cámara/secuencia, **Kling 3.0**. Cualquiera sirve para esto.
- **Formato:** **16:9** (es fondo de hero a pantalla completa).
- **Duración:** 5–8 s (se reproducirá en loop, no necesita ser largo).
- **Cámara:** un solo movimiento lento (dolly-in o tracking lateral). Nada brusco.
- **Sin audio** (el hero va en mute).

---

## 5. Para que funcione bien como fondo del hero

- Que sea **oscuro o de medio tono** para que el texto blanco encima se lea (o se le agrega un overlay oscuro por CSS).
- **Loop:** elige una toma con movimiento continuo (conveyor avanzando) para que el corte sea poco notorio.
- **Comprime el MP4** antes de producción (objetivo < 3–4 MB) para que cargue rápido. Ej. con HandBrake o ffmpeg.
- En la web va con `muted autoplay loop playsinline`.

---

## 6. Dónde dejar el video final

Cuando tengas el clip listo y comprimido, guárdalo como:
```
public/assets/video/hero.mp4
```
y avísale a Claude Code para que lo use de fondo en el hero (reemplaza al `hero-broll.mp4` actual).

---

## 7. Recrear el VIDEO ORIGINAL en la paleta nueva (azul/ámbar)

El video original es un montaje cinematográfico oscuro de automatización (robots en rieles, robot AutoStore, brazo robótico, bin de picking) con luz **roja** y cierra en un **globo con la "E" roja de Element Logic**. Acá lo recreamos con la **marca nueva**: luz azul + ámbar, sin rojo, y un frame final distinto (sin la E).

### ▶️ Prompt principal (recrea el video, paleta nueva) — Text-to-Video o Image-to-Video
```
Cinematic product film of a high-tech automated warehouse, dark and moody, shallow depth of field. A montage of slow macro shots: autonomous robots gliding on rails, a cube-shaped AutoStore-style robot moving across a grid, a precision robotic arm with a gripper, and a top-down view of a storage bin filled with parcels and products. Brushed metal and matte-black machinery, glossy reflections, floating dust particles, volumetric light, soft lens flares. Lighting in deep blue key light with warm amber and gold accents — NO red. Cool grey tones. Smooth slow dolly and rack-focus camera moves. Premium, futuristic, corporate-tech mood. 16:9, cinematic.
```

### 🚫 Negative prompt
```
red lighting, red branding, letter E, text, logos, watermark, brand names, people staring at camera, fast cuts, flicker, distortion, low quality, jitter
```

### 🎬 Frame final (End frame) — globo "similar pero no copia"
El original termina en un globo gris 3D con la **"E" roja**. Hacemos uno parecido pero claramente distinto: mismo globo, **sin la E**, en paleta nueva, y encima va el símbolo de SDI.

**Paso 1 — generar el globo limpio** (Text-to-Image, sin logos):
```
A 3D glossy globe, brushed silver-grey sphere with subtle light-grey continents and country borders, Americas facing forward, soft studio reflections, clean white background, cool blue and warm amber rim light, corporate, minimal. No text, no letters, no logos.
```
**Paso 2 — ponerle el símbolo de SDI:** sobre ese globo, compón el isotipo real **`public/assets/logos/Iso.png`** (el disco azul/gris/dorado con el triángulo) donde antes iba la "E". Así queda marca SDI, no Element. (Se hace en cualquier editor, o pídeselo a Higgsfield como overlay.)

### Cómo armarlo en Higgsfield
- **Start frame:** una toma de bodega/robot (puedes subir `soprole-picking.jpg`, o generar una con el prompt principal).
- **End frame:** el globo del Paso 1+2.
- Higgsfield rellena el movimiento entre ambos → arranca en la bodega y cierra en el globo SDI, igual que el original pero rebrandeado.
- Modelo Veo 3.1 / Kling 3.0 · 16:9 · 6–8 s · sin audio.
