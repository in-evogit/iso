# Instrucciones para Claude Code — Sitio Web Corporativo SDI Systems

> **Este archivo es autocontenido.** Tiene todo lo que Claude Code necesita: contexto, stack, contenido real, estructura y pasos. No requiere acceso a Google Drive.
> Cliente: **Ariel** · Empresa: **SDI Systems** (antes la representación en Chile operaba bajo *Element Logic*) · Agencia: **InEvolution**.

> **📍 Ubicación local del proyecto:** `…/Documents/Claude/Projects/web ariel/`
> Carpeta de activos ya creada: `public/assets/logos/`, `public/assets/clientes/`, `public/assets/img/`.
>
> **⚠️ Dos reglas que no se negocian:**
> 1. **El texto del sitio se usa TEXTUAL** tal como lo entregó Ariel (sección 4). No inventar productos, datos ni claims. Pulir redacción/ortografía está OK; cambiar el contenido no.
> 2. **La paleta de colores se saca de los logos de SDI** (sección 5). Los colores del sitio deben seguir las tonalidades de la marca, no colores arbitrarios.

---

## ▶️ Cómo usar este archivo (workflow)

1. Abre una terminal y entra a la carpeta del proyecto:
   ```bash
   cd "ruta/a/pagina-ariel"
   ```
2. Inicia Claude Code:
   ```bash
   claude
   ```
3. Pega este primer mensaje:

   > Lee el archivo `INSTRUCCIONES-CLAUDE-CODE.md` completo. Es la especificación del proyecto. Vamos a construir un sitio corporativo estático de una sola página para SDI Systems con **Astro** + CSS (sin frameworks pesados). Sigue el plan de "Pasos de construcción" en orden, empezando por el Paso 1 (inicializar el proyecto Astro). Antes de escribir código, muéstrame tu plan y la estructura de carpetas para confirmar.

4. A partir de ahí Claude Code arma todo. Tú vas confirmando cada paso.

---

## 1. Contexto del proyecto

**Qué es:** sitio web corporativo (landing de una sola página, scroll vertical) para **SDI Systems**, empresa de **automatización e intralogística** para centros de distribución en LATAM/Chile. Reemplaza la página antigua de Element Logic.

**Objetivo del sitio:** presencia corporativa profesional que comunique quiénes son, qué soluciones/productos ofrecen, sus servicios e industrias, casos/clientes, y un canal de contacto. No es e-commerce, no necesita login.

**Tono:** profesional, moderno, tecnológico, industrial. Serio pero limpio. Público B2B (gerentes de logística, operaciones, retail, e-commerce).

---

## 2. Stack técnico

- **Framework:** Astro (sitio estático — ideal porque es contenido mayormente fijo, carga rápido y SEO-friendly).
- **Estilos:** CSS con variables (custom properties) en un `global.css`. Tailwind es opcional; si lo usas, que sea con `@astrojs/tailwind`. Mantenerlo simple.
- **Sin backend / sin base de datos.** No se necesita Supabase. El formulario de contacto se resuelve con un servicio externo tipo **Formspree** o un `mailto:`, o un link directo a **WhatsApp**.
- **Responsive** (mobile-first), accesible y con buen rendimiento (Lighthouse alto).
- **Idioma:** español. Dejar la estructura preparada por si después se agrega inglés (i18n), pero v1 solo español.

---

## 3. Estructura del sitio (secciones, en orden)

Una sola página con navegación ancla (navbar fijo que hace scroll a cada sección).

1. **Navbar** — logo + links a secciones + botón CTA "Contáctanos".
2. **Hero / Portada** — título, slogan, CTA, imagen/fondo.
3. **Sobre la empresa** — quiénes son + respaldo internacional.
4. **Soluciones y Productos** — 4 categorías en cards.
5. **Servicios (El Ciclo SDI)** — 4 etapas con íconos.
6. **Industrias** — 5 sectores en cards.
7. **Casos y Clientes** — ejemplos + logos de clientes.
8. **¿Por qué elegirnos?** — diferenciadores.
9. **Contacto** — formulario / WhatsApp / email.
10. **Footer** — logo, links, datos de contacto.

---

## 4. Contenido real (copy proporcionado por Ariel — usar tal cual, pulir redacción si hace falta)

### Hero / Portada
- **Título:** Automatización e Inteligencia Logística para LATAM
- **Subtítulo:** Transformamos operaciones logísticas en ventajas competitivas
- **CTA:** "Contáctanos" / "Ver soluciones"

### Sobre la empresa
> En SDI Systems impulsamos la evolución de la cadena de suministro en Latinoamérica mediante soluciones de automatización e intralogística de clase mundial. Diseñamos, integramos e implementamos proyectos llave en mano que permiten a nuestros clientes optimizar sus centros de distribución, aumentar su productividad y prepararse para los desafíos del crecimiento futuro.
>
> Respaldados por décadas de experiencia internacional y por un profundo conocimiento de las realidades operativas de la región, nos convertimos en un socio estratégico capaz de acompañar cada etapa de la transformación logística, desde el diseño conceptual hasta el soporte permanente de la operación.

### Soluciones y Productos
Encabezado: **Tecnología de Vanguardia para Centros de Distribución.** "Nuestro portafolio integra tecnologías líderes a nivel mundial, seleccionadas para responder con flexibilidad, eficiencia y escalabilidad a las exigencias de los mercados actuales."

**1. Clasificación Unitaria de Alta Velocidad (Sorters)**
- **SORTRAK G4 (Bomb Bay):** tecnología propia de caída vertical para clasificación masiva ultraprecisa.
- **Tilt Tray Sorter:** bandejas inclinables de alta resistencia, cargas variadas y flujos constantes.
- **Crossbelt Sorter:** bandas cruzadas para paquetes, sobres, cajas y contenedores de distintos tamaños.
- **TableSort / T-Sort + 3DSort:** alto volumen con pocas unidades por orden, reconfiguración rápida.

**2. Clasificación de Cajas y Contenedores**
- **Narrow Belt Sorter (NBS):** desvíos en múltiples configuraciones.
- **Shoe Sorter:** altas velocidades, cargas pesadas, máxima confiabilidad.
- **Crossbelt / Multibelt Sorter:** velocidad, precisión y aprovechamiento del espacio.

**3. Robóticos y Sistemas de Secuenciación**
- **AutoStore™:** almacenamiento automatizado de mayor densidad del mercado.
- **Joey Pouch Sorter:** clasificador de bolsas colgantes, ideal e-commerce.
- **Enzo AGV:** vehículos de guiado automático para transporte interno autónomo.

**4. Asistencia para Picking, Clasificación y Consolidación**
- **Pack-to-Light / Put-to-Store:** guiado por luz, reduce errores.
- **PTL (Pick-to-Light):** picking de alta rotación.
- **PTW (Put-to-Wall / Put-to-Light):** consolidación rápida y escalable para e-commerce.

### Servicios — El Ciclo SDI
Encabezado: **Un acompañamiento integral de principio a fin.**
1. **Diseño y Consultoría Logística** — análisis de procesos e indicadores, soluciones a medida, optimización del espacio, eliminación de cuellos de botella.
2. **Ingeniería de Sistemas** — arquitecturas de automatización/control/software, integración con WMS/ERP, infraestructura escalable.
3. **Instalación y Puesta en Marcha** — implementación por especialistas, pruebas/validación, capacitación.
4. **Soporte y Mantenimiento** — soporte local en LATAM (mismo idioma y zona horaria), mantenimiento preventivo, gestión de repuestos y actualizaciones.

### Industrias
Encabezado: **Soluciones Adaptadas a Cada Industria.**
- **E-Commerce** — miles de pedidos diarios con tiempos de entrega exigentes → almacenamiento automatizado, clasificación de alta velocidad, picking.
- **Moda y Textil (Apparel)** — catálogos grandes, devoluciones/cambios → soluciones para prenda colgada y doblada.
- **Grandes Cadenas de Retail** — omnicanal → clasificación, secuenciación y consolidación para reposición en tienda.
- **Operadores Logísticos (3PL)** — múltiples clientes → plataformas modulares y escalables.
- **Consumo Masivo y Farmacéutico** — volumen + trazabilidad → software + automatización con control en tiempo real.

### Casos y Clientes
Capacidades de la empresa: **Ingeniería · Software · Controles · Fábrica · Soporte 24/7 · Transporte y Clasificación · Almacenamiento y Picking · Consultoría** (data analysis, DC design, network optimization, WMS/WCS/WES).

Ejemplos de soluciones implementadas:
- Torres de picking (alta/media rotación), Pick-to-Pallet (baja rotación), scanners de validación de SKU, sorter de cajas a tiendas.
- Pick-to-Light (alta rotación), picking con RF (media/baja), balanza en línea de validación.
- Sistemas independientes para temperatura fresca (0° a 4°) y congelado (-28°); transelevador de 740 posiciones (-28°).
- Bloques: **"Algunos clientes en Chile"** y **"Algunos clientes en LATAM"** → grilla de logos + fotos reales de proyectos.
- **Clientes reales con foto** (del PPT, ver sección 12): **Dimerc** (picking de cajas y de unidades), **Soprole** (picking de cajas/unidades), **PF Alimentos** (picking de cajas y packing de pallets). Usar estas fotos en las cards de casos, cada una con el nombre del cliente y la solución implementada.

### ¿Por qué elegirnos? (diferenciadores)
- Respaldo y experiencia internacional de décadas.
- Soporte local en LATAM (mismo idioma y zona horaria).
- Proyectos llave en mano de principio a fin.
- Soluciones modulares y escalables.
- Tecnología líder a nivel mundial.

### Contacto
Formulario (nombre, empresa, email, mensaje) + botón de WhatsApp + email. *(Datos exactos: pendientes de Ariel — dejar placeholders.)*

---

## 5. Identidad visual y paleta

- **Logos de SDI** (ya en `public/assets/logos/`): `Iso.png` (isotipo — disco con tres segmentos **azul / gris / dorado** y un triángulo tipo "play" al centro), `Logo1.png` y `Logo2.png` (logo completo, wordmark en azul marino). Usar la versión que mejor se lea sobre cada fondo.

- **Paleta oficial — YA EXTRAÍDA de los logos. Usar estos HEX exactos:**

| Variable | HEX | Rol |
|---|---|---|
| `--brand-blue` | `#426E9A` | Primario (azul corporativo) — links, íconos, secciones destacadas |
| `--brand-gold` | `#DC9A16` | Acento (dorado/ámbar) — botones CTA, subrayados, highlights |
| `--brand-gray` | `#848484` | Gris de marca — texto secundario, líneas, fondos neutros |
| `--brand-navy` | `#2C2C42` | Azul marino oscuro — títulos, texto principal, navbar, footer |
| `--bg-light` | `#F4F6F8` | Fondo claro de secciones |
| `--white`     | `#FFFFFF` | Fondo base / texto sobre oscuro |

  ```css
  :root{
    --brand-blue:#426E9A;
    --brand-gold:#DC9A16;
    --brand-gray:#848484;
    --brand-navy:#2C2C42;
    --bg-light:#F4F6F8;
    --white:#FFFFFF;
  }
  ```

  **Uso (contraste/accesibilidad):**
  - Texto de cuerpo: `--brand-navy` sobre blanco (contraste alto, ✅).
  - Botones CTA: fondo `--brand-gold` con texto `--brand-navy` (NO texto blanco sobre dorado).
  - `--brand-blue` para hero/secciones destacadas; texto encima en blanco.
  - Dorado y gris solo como acentos, no para párrafos largos.

- **Tipografía:** sans-serif moderna y legible (Inter, Manrope o similar vía `@fontsource`).
- **Fotos reales:** ver **sección 12** (fotos de casos reales que se extraen del PPT de Ariel). Donde falten, placeholders marcados como temporales.

---

## 6. Estructura de carpetas sugerida (Astro)

```
pagina-ariel/
├── public/
│   └── assets/
│       ├── logos/        (Iso.png, Logo1.png, Logo2.png)
│       ├── clientes/     (logos de clientes — pendiente)
│       └── img/          (fotos / placeholders)
├── src/
│   ├── components/
│   │   ├── Navbar.astro
│   │   ├── Hero.astro
│   │   ├── SobreEmpresa.astro
│   │   ├── Soluciones.astro
│   │   ├── Servicios.astro
│   │   ├── Industrias.astro
│   │   ├── Casos.astro
│   │   ├── PorQue.astro
│   │   ├── Contacto.astro
│   │   └── Footer.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css     (variables de color + base)
├── astro.config.mjs
├── package.json
└── README.md
```

---

## 7. Pasos de construcción (para Claude Code, en orden)

1. **Inicializar Astro:** `npm create astro@latest .` (plantilla "Empty" o "Minimal"), TypeScript opcional. Instalar dependencias.
2. **Base:** crear `Layout.astro` (head, meta SEO, fuentes) y `global.css` con las variables de color (extraídas de los logos).
3. **Navbar + Footer** con navegación por anclas y el logo.
4. **Hero** con título, slogan y CTA.
5. **Secciones de contenido** una por una usando el copy de la sección 4: Sobre la empresa → Soluciones (cards) → Servicios → Industrias → Casos/Clientes → Por qué elegirnos.
6. **Contacto:** formulario (Formspree o `mailto:`) + botón WhatsApp.
7. **Responsive + pulido:** breakpoints, hover states, espaciados, animaciones sutiles al hacer scroll.
8. **README** con instrucciones de desarrollo y despliegue.
9. **Verificación:** `npm run build` sin errores, revisar en mobile y desktop, Lighthouse.

---

## 8. Git / GitHub

**Repo ya creado:** https://github.com/in-evogit/iso  (org `in-evogit`, repo `iso`).

```bash
git init
git add .
git commit -m "init: estructura base del sitio SDI Systems (Astro) + assets"
git branch -M main
git remote add origin https://github.com/in-evogit/iso.git
git push -u origin main
```
- `referencias/` está en `.gitignore` (material fuente pesado: PPT, extracciones, videos originales — no va al repo).
- Despliegue para mostrarle a Ariel: **Vercel**, **Netlify** o **Cloudflare Pages** (deploy automático desde el repo, soportan Astro).

---

## 9. Cómo correr local

```bash
npm install
npm run dev      # servidor local (http://localhost:4321)
npm run build    # build de producción → carpeta dist/
npm run preview  # previsualizar el build
```

---

## 10. Pendientes / definiciones de Ariel

- Fotos reales (portada, equipo, instalaciones, productos) — carpeta venía vacía.
- Logos de clientes para la sección de Casos.
- Dominio definitivo (.cl o .com) y datos de contacto reales (email, teléfono, WhatsApp).
- ¿Mostrar precios? (no obligatorio).
- ¿Solo español o también inglés?
- Confirmar nombre/marca final: usar **SDI Systems** salvo indicación contraria.

---

## 11. Referencia: la página antigua (Element Logic Chile)

El sitio que SDI reemplaza es el de **Element Logic Chile** (`elementlogic.net/cl`). Sirve como referencia de **estructura, arquitectura de información y tono B2B**, NO de colores (la paleta de SDI sale de sus propios logos).

Qué tomar de ahí:
- **Menú / arquitectura:** "Soluciones y Servicios" (AutoStore, Diseño y Consultoría, Instalación, Software), "Casos" (customer cases), "Noticias", e industrias (3PL, e-commerce, retail). → Calza con las secciones que ya definimos en la sección 3.
- **Enfoque:** AutoStore y automatización de bodegas como producto estrella, casos de éxito con clientes reales, foco en densidad de almacenamiento y eficiencia de picking.
- **Estilo:** corporativo, mucho espacio en blanco, fotos grandes de bodegas/sistemas, secciones de "solución por industria", llamados a "agendar" o "contactar".
- **Diferencia clave:** Element Logic se centra solo en AutoStore; **SDI tiene un portafolio más amplio** (sorters, AGVs, picking, etc., ver sección 4). El sitio de SDI debe reflejar ese catálogo más amplio.

URLs de referencia (estructura/casos):
- https://www.elementlogic.net/cl/soluciones-y-servicios/diseno-y-consultoria/
- https://www.elementlogic.net/cl/soluciones-y-servicios/autostore/
- https://www.elementlogic.net/cl/soluciones-y-servicios/software/
- https://www.elementlogic.net/cl/cases/un-gran-almacen-autostore-para-un-ecommerce-de-moda-lider-en-europa/

> Nota: revisar estas páginas para inspirarse en layout y orden de la información. Reescribir todo con el copy de SDI (sección 4) — no copiar textos de Element Logic.

---

## 12. Fotos reales de casos (extraídas del PPT "Caso y clientes")

Ariel entregó un PPT con **fotos reales de proyectos** en clientes de Chile/LATAM. Esas fotos se extraen del `.pptx` (que internamente es un ZIP: las imágenes viven en `ppt/media/`) y se guardan en `public/assets/img/casos/` con nombres claros.

Clientes y soluciones documentadas:
- **Dimerc** — picking de cajas y picking de unidades.
- **Soprole** — picking de cajas / unidades.
- **PF Alimentos** — picking de cajas y packing de pallets.

**✅ YA EXTRAÍDAS Y LISTAS** (archivos reales en el repo):

Fotos de proyectos → `public/assets/img/casos/`
```
dimerc-picking-cajas.png       (601x399)   — Dimerc, sortación/clasificación de cajas
dimerc-picking-unidades.png    (680x489)   — Dimerc, picking de unidades
soprole-picking.jpg            (1280x720)  — Soprole, líneas de conveyor con cajones (la mejor calidad)
pf-alimentos-layout.png        (1038x788)  — PF Alimentos, render del centro de distribución (cajas + pallets, frío/congelado)
```

Logos de cliente (24, limpios y nombrados) → `public/assets/clientes/`
```
dimerc · dimerc-office · soprole · pf-alimentos · ripley · hites · belcorp ·
concha-y-toro · artel · chilexpress · dimeiggs · axo-chile · dinet ·
farmacias-peruanas · renner · hering · levis · alpargatas · flexi ·
farmacorp · belleza-express · continental · bosch · flex
```
→ Úsalos en una sección **"Empresas que confían en nosotros"** (grilla de logos en gris/monocromo o a color, sobre fondo claro).

Video para el hero → `public/assets/video/`
```
hero-broll.mp4    (~12 MB, b-roll de un sorter en movimiento — fondo del hero)
globo-latam.mp4   (~3 MB, globo animado — opcional)
```
> El `hero-broll.mp4` puede ir como fondo del hero (con overlay oscuro + texto encima, `muted autoplay loop playsinline`). **Conviene comprimirlo** (objetivo < 3–4 MB, ej. con ffmpeg/HandBrake) antes de producción. Si aparece branding viejo de Element Logic, se puede re-editar con Higgsfield.

Estas fotos van en la sección **Casos y Clientes** (sección 3, punto 7): una card por cliente con foto + logo + nombre + solución implementada. Mapea cada caso con su texto:
- **Dimerc** → "Picking de Cajas (torres de picking, pick-to-pallet, sorter a tiendas) + Picking de Unidades (pick-to-light, RF, balanza de validación)".
- **Soprole** → "Picking de Cajas (pick-to-belt, sorter a tiendas) + Picking de Unidades (pick-to-light)".
- **PF Alimentos** → "5 torres de picking, sorter a rutas, sistemas para fresco (0–4°) y congelado (-28°), transelevador de 740 posiciones (pallets)".

> **Material fuente completo** (todo lo extraído del PPT) está en `referencias/ppt-extraido/` con su `_INDICE.md`. Esa carpeta NO va al repo (`.gitignore`), es solo para consulta.
> **Importante (marca):** el PPT usa la identidad ANTIGUA "Element Logic" (roja). En el sitio nuevo se reutilizan **fotos de casos y logos de clientes**, pero NO el branding rojo de Element Logic — la web va con la marca **SDI Systems** (azul/dorado, sección 5).
