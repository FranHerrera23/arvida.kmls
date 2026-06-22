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
- assets/studio/karen.jpg  → retrato Founder & Creative Director (vertical, 3/4)

## 3. GALERÍAS DE PROYECTOS (lightbox) — fotos numeradas 1.jpg … N.jpg

| Proyecto      | Carpeta              | Nº fotos | Extra |
|---------------|----------------------|----------|-------|
| Neymar        | assets/neymar/       | 6        |       |
| Gusttavo Lima | assets/gustavo/      | 5        |       |
| Superyacht    | assets/yacht/        | 4        |       |
| Private Jet   | assets/jet/          | 4        |       |
| Saadiyat      | assets/saadiyat/     | 5        | + video.mp4 (primer slide) |
| Art Collector | assets/collector/    | 6        |       |
| Palm Beach    | assets/palmbeach/    | 5        |       |
| Pezet 3       | assets/pezet3/       | 6        |       |
| La Moraleja   | assets/moraleja/     | 5        |       |
| Private Apt   | assets/mariana/      | 4        |       |
| Family Res    | assets/kathy/        | 4        |       |
| Viva Gym      | assets/vivagym/      | 4        |       |
| Blas Cerdeña  | assets/blascerdena/  | 5        |       |
| Poseidón      | assets/poseidon/     | 5        |       |
| Fisher Island | assets/fisher/       | 5        |       |
| Golden Beach  | assets/golden/       | 6        |       |

**Total fotos de proyecto: ~79**  ·  Para cambiar un conteo: editar `photos:N` en el objeto PROJECTS del HTML.

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
