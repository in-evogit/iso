# Brief consolidado — Sitio Web SDI Systems (cliente: Ariel)

> Documento de contexto generado a partir de la carpeta de Drive **"Proyecto Sitio Web — Ariel"**.
> Pensado para entregárselo a Claude Code como base del proyecto.

---

## 1. La empresa

- **Nombre de marca:** **SDI Systems** (la referencia anterior era *Element Logic Chile*; la marca real del negocio de Ariel es SDI Systems).
- **Rubro:** Automatización e intralogística para centros de distribución — LATAM / Chile.
- **Propuesta de valor:** "Automatización e Inteligencia Logística para LATAM. Transformamos operaciones logísticas en ventajas competitivas."
- **Modelo:** Proyectos llave en mano (diseño → integración → implementación → soporte). Socio estratégico de largo plazo, con soporte local en español y misma zona horaria.
- **Contacto / dueño del material:** Ariel (arieljaimovicho@gmail.com).

---

## 2. Productos / Soluciones (el corazón del sitio)

Portafolio de tecnologías de clasificación, almacenamiento y picking:

**1. Clasificación unitaria de alta velocidad (Sorters)**
- SORTRAK G4 (Bomb Bay) — caída vertical, clasificación masiva ultraprecisa.
- Tilt Tray Sorter — bandejas inclinables, cargas variadas.
- Crossbelt Sorter — bandas cruzadas, paquetes/sobres/cajas.
- TableSort / T-Sort + 3DSort — alto volumen, pocas unidades por orden, reconfigurable.

**2. Clasificación de cajas y contenedores**
- Narrow Belt Sorter (NBS) — desvíos múltiples.
- Shoe Sorter — alta velocidad, cargas pesadas, confiabilidad.
- Crossbelt / Multibelt Sorter — velocidad + precisión + uso de espacio.

**3. Robóticos y secuenciación**
- AutoStore™ — almacenamiento automatizado de mayor densidad del mercado.
- Joey Pouch Sorter — bolsas colgantes, e-commerce.
- Enzo AGV — vehículos de guiado automático.

**4. Asistencia para picking, clasificación y consolidación**
- Pack-to-Light / Put-to-Store — guiado por luz.
- PTL (Pick-to-Light) — picking de alta rotación.
- PTW (Put-to-Wall / Put-to-Light) — consolidación e-commerce.

---

## 3. Servicios (El Ciclo SDI)

Acompañamiento integral de principio a fin:
1. **Diseño y Consultoría Logística** — análisis de procesos, soluciones a medida, optimización de espacio.
2. **Ingeniería de Sistemas** — arquitecturas de automatización/control/software, integración con WMS/ERP, escalabilidad.
3. **Instalación y Puesta en Marcha** — implementación, pruebas/validación, capacitación.
4. **Soporte y Mantenimiento** — soporte local LATAM, mantenimiento preventivo, gestión de repuestos.

---

## 4. Industrias a las que apuntan

- **E-Commerce** — miles de pedidos diarios, entregas exigentes.
- **Moda y Textil (Apparel)** — catálogos grandes, devoluciones/cambios, prenda colgada y doblada.
- **Grandes cadenas de Retail** — omnicanal, reposición en tienda.
- **Operadores Logísticos (3PL)** — múltiples clientes, plataformas modulares.
- **Consumo Masivo y Farmacéutico** — volumen + trazabilidad + velocidad.

---

## 5. Casos y clientes (de "Caso y clientes.pptx")

Capacidades destacadas: Ingeniería, Software, Controles, Fábrica, Soporte 24/7, Transporte y clasificación, Almacenamiento y picking, Consultoría (data analysis, DC design, network optimization, WMS/WCS/WES).

Ejemplos de soluciones por caso:
- Torres de picking (alta/media rotación), Pick to Pallet (baja rotación), scanners de validación de SKU, sorter de cajas a tiendas.
- Pick-to-Light (alta rotación), picking con RF (media/baja), balanza en línea de validación.
- Sistemas para temperatura fresca (0º a 4º) y congelado (-28º); transelevador 740 posiciones (-28º).
- Secciones: "Algunos clientes en Chile" y "Algunos clientes en LATAM" (logos de clientes — revisar slides finales del pptx).

---

## 6. Estructura propuesta del sitio (landing de una página)

Basada en el brief interno (referencia: elementlogic.net/cl, simplificada):
1. **Hero / Portada** — título, slogan, CTA (Contáctanos / Ver soluciones / Agendar reunión) + imagen de fondo.
2. **Sobre la empresa** — quiénes son, enfoque, respaldo internacional.
3. **Soluciones y productos** — cards por categoría (los 4 grupos de arriba).
4. **Servicios (Ciclo SDI)** — 4 etapas con íconos.
5. **Industrias** — 5 sectores.
6. **Casos de éxito / Clientes** — logos + ejemplos.
7. **¿Por qué elegirnos?** — diferenciadores (respaldo internacional, soporte local, experiencia).
8. **Contacto** — formulario, WhatsApp, email, redes.

---

## 7. Identidad visual y activos

- **Logos disponibles** (carpeta "04 — Logo e identidad visual"): `Iso.png` (isotipo), `Logo1.png`, `Logo2.png`.
- **Colores corporativos:** no entregados como códigos HEX → extraer de los logos al diseñar.

---

## 8. Estado del material (qué hay / qué falta)

| Carpeta | Estado | Contenido |
|---|---|---|
| 01 — El negocio | ✅ Completo | `Página Web.docx` (copy real del sitio, muy completo) |
| 02 — Servicios y productos | ⚠️ Vacía | (info ya está en el docx de "01") |
| 03 — Imágenes y fotos | ❌ Vacía | **Falta:** foto de portada, equipo, instalaciones, productos |
| 04 — Logo e identidad visual | ✅ Parcial | 3 logos PNG. **Falta:** colores HEX / guía de marca |
| 05 — Referencias y otros | ✅ Parcial | `Caso y clientes.pptx` (casos + logos de clientes) |

**Definiciones pendientes con Ariel:** dominio (.cl o .com), botón de WhatsApp (sí/no), idioma (solo español o también inglés), precios (mostrar o no), foto principal de portada.

---

## 9. Notas de implementación (para Claude Code)

- Stack sugerido para una landing estática rápida y demo-able: HTML + Tailwind (o Astro/Next si se quiere escalar). Probablemente **no se necesita Supabase** salvo que el formulario de contacto requiera guardar leads (alternativa: Formspree / email).
- Repo: subir a GitHub bajo la organización **InEvolution**.
- Tono visual: profesional, moderno, tecnológico (industria logística / automatización).
