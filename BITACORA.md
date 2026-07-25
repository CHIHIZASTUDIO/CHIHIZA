# CHIHIZA — Bitácora de Proyecto

## Información General

- **Proyecto:** CHIHIZA International — Sitio web de inversión inmobiliaria ecológica
- **Países:** Colombia, Costa Rica, Panamá
- **Stack:** HTML5, CSS3, JavaScript vanilla (sin frameworks)
- **Repo:** https://github.com/CHIHIZASTUDIO/CHIHIZA.git (main)
- **Email:** chihizaestudio@gmail.com
- **WhatsApp:** +57 321 993 1029
- **Última sesión:** 24 de julio de 2026

---

## Estructura del Sitio

```
├── index.html              — Página principal
├── about.html              — Nosotros
├── projects.html           — Catálogo de proyectos
├── contact.html            — Contacto
├── guide.html              — Guía "Beyond Buying Property" (descargable)
├── legacy.html             — Marco Legal de Inversión (descargable)
├── projects/
│   ├── natauta.html        — Natautá, Colombia
│   ├── rio-frio.html       — Río Frío, Colombia
│   ├── el-mirador.html     — El Mirador, Colombia
│   ├── costaverde.html     — CostaVerde, Panamá
│   └── nosara.html         — Nosara, Costa Rica
├── assets/
│   ├── css/styles.css      — Estilos globales (~3000 líneas)
│   ├── js/main.js          — Lógica principal
│   ├── favicon.svg         — Favicon
│   ├── images/bg/          — 16 imágenes de fondo (img-1 a img-16)
│   ├── CHIHIZA Secure Investment Framework.pdf
│   └── guide.pdf
├── tools/
│   ├── CHIHIZA_DISCOVERY_V2.html    — Herramienta de descubrimiento
│   ├── CHIHIZA_DUE_DILIGENCE.html   — Due diligence terrain
│   ├── CHIHIZA_FINANCIAL_MODEL.html — Modelo financiero
│   └── digital-twin-campestre/       — Digital Twin (HTML+CSS+JS)
└── proyectos/              — Imágenes de proyectos
    ├── natauta/
    ├── riofrio/
    ├── el-mirador/
    ├── costaverde/
    ├── nosara/
    ├── about-hero.png
    └── images-back/        — Imágenes fuente para backgrounds
```

---

## Paleta de Colores

| Variable | Color | Uso |
|---|---|---|
| `--bg` | `#f8f7f4` | Fondo principal (warm white) |
| `--bg-warm` | `#f3f1ec` | Secciones alternas |
| `--accent` | `#6b8f71` | Sage green (botones, tags, links) |
| `--text` | `#2c2c2c` | Texto principal |
| `--text-secondary` | `#5a5a55` | Texto secundario |
| Hot pink | `#ff0055` | Botón play (parpadeante) |
| WhatsApp green | `#25d366` | Float de WhatsApp |
| Fuchsia | `#d946ef` | Reserva (no activo) |

## Tipografía

- **Display:** Playfair Display (títulos, logo)
- **Body:** Inter (texto general)
- **Mono:** Courier New (botón play)

---

## Historial de Commits (Sesión 24 jul 2026)

| Hash | Descripción |
|---|---|
| `cc7e820` | Comprehensive mobile fixes: divider parallax, slider swipe, play button, spacing, hero bgs |
| `46cbbd9` | 16 images redistributed: hero bgs, dividers across all pages, CTA bgs |
| `567ba10` | Reverted section-bg approach, now using 4 full-width image dividers between sections |
| `d85f8c0` | 10 background images distributed across all pages (no repeats) |
| `f84bcb5` | Fix email: chihizaestudio@gmail.com |
| `3976b6b` | Play button: circle, hot pink #ff0055, blink animation, no text |
| `bda9a30` | START button moved into header nav (fuchsia, no more overlap) |
| `79211ad` | Remove WhatsApp nav-cta, START button now fuchsia |
| `256abf1` | START button fixed top-right (orange, console style) + WhatsApp nav green |

### Commits anteriores (pre-sesión)

| Hash | Descripción |
|---|---|
| `varios` | Rewrite all 11 HTML pages (inline CSS removed, SEO, lazy load) |
| `varios` | Full CSS rewrite: white theme, shadow system, responsive |
| `varios` | main.js rewrite: IntersectionObserver, counters, toast, lightbox |
| `varios` | Copy 4 team tools into tools/ folder, white theme applied |
| `varios` | THE PROCESS panel with 4 tools (Discovery, Due Diligence, Digital Twin, Financial Model) |
| `varios` | Delete dead files (5 stubs, old CSS/JS, .bak) |
| `varios` | OG tags, Twitter Cards, canonical URLs on all pages |
| `varios` | Breadcrumbs on project pages, nav fix |
| `varios` | Email capture forms on guide.html and legacy.html |

---

## Lo que Hicimos en Esta Sesión

### 1. Botón Play (THE PROCESS)
- **Original:** Botón "START" naranja fijo arriba a la derecha
- **Cambio 1:** Movido al nav después de Contact, color fucsia
- **Cambio 2:** Eliminado WhatsApp naranja del nav
- **Final:** Botón circular 44x44px, hot pink `#ff0055`, solo triángulo play ▶, animación parpadeante (`blink-glow`), hover escala x1.1
- **CSS:** `.team-tools-toggle` — border-radius 50%, animation blink-glow 1.5s infinite

### 2. Email Actualizado
- Cambiado de `hello@chihiza.com` a `chihizaestudio@gmail.com` en contact.html (mailto + texto)

### 3. Sistema de Imágenes de Fondo
- **Enfoque 1 (revertido):** `.section-bg` con pseudo-elementos `::before`/`::after`, opacidad 15% — se veía lavado y sucio
- **Enfoque 2 (actual):** Divisores de imagen de ancho completo (`img-divider`) entre secciones
  - Altura: 320px desktop, 200px tablet, 150px móvil
  - `background-attachment: fixed` (parallax) en desktop
  - `background-attachment: scroll` en móvil (iOS compatible)
  - Overlay gradiente sutil en bordes para transición suave
- **16 imágenes** distribuidas en 6 páginas:
  - Hero backgrounds con gradiente semitransparente
  - CTA backgrounds con overlay oscuro + texto blanco
  - Dividers a full opacidad sin overlay

### 4. Distribución de Imágenes

| Página | Tipo | Imagen |
|---|---|---|
| index.html | Hero bg | img-1 |
| index.html | Divider (Stats→Projects) | img-2 |
| index.html | Divider (Projects→Steps) | img-3 |
| index.html | Divider (Form→Testimonials) | img-4 |
| index.html | Divider (FAQ→Team) | img-5 |
| index.html | CTA bg | img-6 |
| projects.html | Hero bg | img-7 |
| projects.html | Divider (Hero→Filter) | img-8 |
| projects.html | Divider (Catalog→CTA) | img-9 |
| projects.html | CTA bg | img-10 |
| about.html | Divider (Content→Stats) | img-11 |
| about.html | Divider (Stats→CTA) | img-12 |
| about.html | CTA bg (verde) | img-13 |
| legacy.html | Divider (Content→CTA) | img-14 |
| legacy.html | CTA bg | img-15 |
| guide.html | Hero bg | img-16 |
| guide.html | Divider (Content→CTA) | img-1* |
| contact.html | Hero bg | img-3* |

*\*Repeticiones menores: img-1 (guide divider) e img-3 (contact hero)*

### 5. Fix Móvil Integral
- **Dividers:** `background-attachment: scroll` para iOS, alturas reducidas
- **Play button:** 56x56px en menú móvil, cierra menú al hacer click
- **Slider proyectos:** `overflow-x: auto` + touch scrolling, animación desactivada en móvil
- **Heroes/CTAs:** `background-size: cover`, `background-attachment: scroll`
- **Formularios:** `font-size: 16px` en inputs (prevenir zoom iOS)
- **Spacing:** Padding reducido en todas las secciones
- **Tipografía:** Tamaños responsive con `clamp()`
- **Botones:** Full-width en móvil

---

## Funcionalidades del Sitio

### Principal (index.html)
- Hero con imagen de fondo + gradiente
- Filosofía (GEA, MOX, HOM)
- Stats animados (IntersectionObserver)
- Slider de proyectos con scroll infinito
- 3 Simple Steps (How to Invest)
- Formulario de inversores (→ WhatsApp)
- Testimonios
- FAQ accordion
- Team grid
- CTA con imagen de fondo
- THE PROCESS (panel lateral con 4 herramientas)
- WhatsApp float

### Herramientas de Equipo (tools/)
1. **Discovery** — Screening de oportunidades de inversión
2. **Due Diligence** — Análisis de terreno y evaluación de riesgo
3. **Digital Twin** — Ficha técnica y configuración paramétrica
4. **Financial Model** — Proyecciones, IRR, rendimientos

### Páginas Secundarias
- **About:** Hero con imagen, valores, stats, CTA
- **Projects:** Filtros por país, catálogo con cards, CTA
- **Contact:** Formulario + métodos de contacto (WhatsApp, email, calendario)
- **Guide:** Hero, contenido, sidebar con 8 temas, descarga PDF, email capture
- **Legacy:** Hero, framework legal, 8 secciones, descarga PDF, email capture
- **5 projetos individuales:** Hero, galería, detalles, ubicación, CTA

### Componentes Reutilizables
- Header fijo con scroll effect
- Menú hamburger móvil (fullscreen overlay)
- Botón play parpadeante
- WhatsApp float
- Toast notifications
- Lightbox de imágenes
- Breadcrumbs
- Email capture forms
- Fade-in on scroll (IntersectionObserver)

---

## Notas Técnicas

### CSS
- Variables CSS para colores, sombras, tipografía
- Sistema de sombras (xs → xl)
- Grid layouts responsive (1-2-4 columnas)
- Animaciones: fade-in, blink-glow, slide (slider)
- Media queries: 1024px, 768px, 480px

### JavaScript
- IIFE auto-ejecutable (sin globals innecesarios)
- IntersectionObserver para lazy loading y fade-in
- Smooth scroll para anchors
- Contadores animados con ease-out cubic
- Lightbox para galerías
- Toast notifications
- FAQ accordion
- Filtros de proyectos por país
- Team tools panel (slide-out)
- Mobile menu toggle

### Performance
- `loading="lazy"` en todas las imágenes
- Ancho/alto explícito en todas las imágenes (prevenir layout shift)
- `font-display: swap` en Google Fonts
- CSS/JS minificado (producción)
- Imágenes optimizadas (WebP donde es posible)

### SEO
- Title y meta description en todas las páginas
- Open Graph tags (og:title, og:description, og:image, og:url)
- Twitter Cards
- Canonical URLs
- Structured headings (h1 → h2 → h3)
- Alt text en todas las imágenes

---

## Próximos Pasos Pendientes

- [ ] Verificar que no queden repeticiones de imagen molestas
- [ ] Agregar más imágenes si el usuario proporciona extras
- [ ] Considerar SPA si se necesita música continua
- [ ] Optimizar tamaño de imágenes (actualmente ~2.5MB cada una)
- [ ] Minificar CSS/JS para producción
- [ ] Agregar analytics (Google Analytics / Plausible)
- [ ] Configurar dominio chihiza.com
