# ASSET MANIFEST — KMLS 41 Arvida Proposal

## 1. RENDERS DEL ESTUDIO (41 Arvida) — van en las secciones narrativas de arriba

Estos son los renders que ellos/el estudio nos pasan. NO son fotos genéricas.
Cada uno llena un slot que YA EXISTE en el HTML. Solo hay que nombrarlos así:

| Slot / archivo                  | Sección en la propuesta            | Qué render va acá |
|---------------------------------|------------------------------------|-------------------|
| assets/arvida/approach.jpg      | 02 — The Approach · i              | Render CÁLIDO: interior al atardecer, una sola fuente baja, cinematográfico |
| assets/arvida/cinema.jpg        | 02 — A Shared Language · ii        | INTERIOR REAL KMLS en clave baja (no render, no still de película). Una sola fuente dura de un lado, negro real en el encuadre, temperatura fría/neutra, geometría limpia, sin gente. Es EVIDENCIA de autoría en el lenguaje claroscuro. En post: bajar calidez, subir contraste para oponerse al Approach cálido. Test: ¿un DP asentiría? |
| assets/arvida/material.jpg      | Reading Arvida 01 — Material first | Render o close-up: plaster / iroko / microcement / felt en contexto |
| assets/arvida/mood.jpg          | Reading Arvida 02 — Screening room | Render de la screening room / booth / studio |
| assets/arvida/plaster.jpg       | 05 — Our Craft (card Plaster)      | Detalle plaster curvo con grazing light |
| assets/arvida/wood.jpg          | 05 — Our Craft (card Wood)         | Detalle iroko & teak, grain iluminado |
| assets/arvida/microcement.jpg   | 05 — Our Craft (card Microcement)  | Detalle microcement mate |
| assets/arvida/felt.jpg          | 05 — Our Craft (card Acoustic felt)| Detalle felt acústico |
| assets/arvida/hero.jpg          | HERO (portada)                     | 41 Arvida al atardecer, cálido, cinematográfico |

Nota: "son referencia, no protagonizan" — encajan en el rol que estas imágenes ya
cumplen: acompañan el texto. No hace falta rediseñar nada, solo cargar los archivos.

## 2. KAREN
- assets/studio/karen.jpg  → retrato Founder & Creative Director (vertical, 3/4). ⚠️ El archivo actual tiene nombre random → renombrar a `karen.jpg`.

## 3. GALERÍAS DE PROYECTOS (lightbox)

⚠️ **REGLA CLAVE:** dentro de cada carpeta, las fotos deben llamarse `1.jpg`, `2.jpg`, … `N.jpg` (la `1.jpg` es la portada). Hoy tienen nombres random (WhatsApp…, Proyecto Garcia…, etc.) → Claude Code las renombra. `N` debe coincidir con `photos:N` del objeto PROJECTS en el HTML.

| Proyecto         | Carpeta                | photos:N | Material hoy | Extra |
|------------------|------------------------|----------|--------------|-------|
| Neymar           | assets/neymar/         | 8        | 8            |       |
| Gusttavo Lima    | assets/gustavo/        | 5        | vacía        |       |
| Superyacht       | assets/yacht/          | 4        | vacía        |       |
| Private Jet      | assets/jet/            | 4        | vacía        |       |
| Saadiyat         | assets/saadiyat/       | 5        | vacía        | + video.mp4 (primer slide) |
| Art Collector    | assets/collector/      | 6        | vacía        |       |
| Four Seasons     | assets/fourseasons/    | 8        | 18 → elegir 8 |       |
| Fisher Island    | assets/fisher/         | 5        | vacía        |       |
| Key Biscayne     | assets/keybiscayne/    | 8        | 15 → elegir 8 |       |
| Golden Beach     | assets/golden/         | 6        | vacía        |       |
| Palm Beach       | assets/palmbeach/      | 5        | vacía        |       |
| Private Villa    | assets/privatevilla/   | 6        | 6            |       |
| Private Family   | assets/residence-1/    | 4        | vacía (era `kathy`) | renombrar carpeta |
| Private Apt      | assets/residence-2/    | 4        | vacía (era `mariana`) | renombrar carpeta |
| Poseidón         | assets/poseidon/       | 8        | 8            |       |
| Pezet 1          | assets/pezet1/         | 8        | 8            |       |
| Pezet 2          | assets/pezet2/         | 8        | 10 → elegir 8 |       |
| Pezet 3          | assets/pezet3/         | 6        | 1 → faltan   | sumar fotos o bajar photos:6 |
| Blas Cerdeña     | assets/blascerdena/    | 8        | 15 → elegir 8 |       |
| Viva Gym         | assets/vivagym/        | 4        | vacía        |       |

**Para cambiar un conteo:** editar `photos:N` en el objeto PROJECTS del HTML. Si falta una foto, el `onerror` la oculta (no rompe).

### ⚠️ Renombrar 2 carpetas (nombres de cliente → genéricos)
- `assets/kathy/`   → `assets/residence-1/`
- `assets/mariana/` → `assets/residence-2/`
(Ambas están vacías, así que es solo renombrar la carpeta.)

## 4. VIDEO
- assets/saadiyat/video.mp4 → aparece como PRIMER slide de la galería de Saadiyat (con ícono play en el thumbnail)

## 5. REGLAS TÉCNICAS
- Fotos/renders: JPG, ~1600–2000px lado largo, calidad ~80, idealmente <300KB c/u
- Video: MP4 H.264, 1080p, <15MB
- El `onerror` oculta cualquier imagen faltante → no rompe si falta una
- Mismo origen para todo (HTML + assets juntos) = cero CORS

## 6. DEPLOY
1. Carpeta: index.html (este HTML renombrado) + assets/ adentro
2. Vercel: arrastrar la carpeta o conectar repo GitHub → link instantáneo
3. Dominio custom: Settings → Domains → agregar dominio.com
4. Un solo link compartible, sin zip, sin fricción
