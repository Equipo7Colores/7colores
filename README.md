# Siete Colores — Equipo Terapéutico

Landing one-page para el equipo interdisciplinario **Siete Colores** (Burzaco, Almirante Brown).
Sitio estático, sin frameworks ni CDNs, optimizado para carga instantánea y SEO local.

## Estructura

| Archivo / Carpeta | Descripción |
| :-- | :-- |
| `index.html` | Página completa: HTML semántico, SEO Local Schema.org y JavaScript. |
| `estilos.css` | CSS de producción con tokens de diseño. |
| `assets/` | Imágenes en producción (WebP optimizado, favicons, OG image). |
| `imagenes/` | Imágenes originales y fuentes sin uso (backup y archivo de material gráfico). |
| `robots.txt` | Directivas de rastreo de motores de búsqueda. |
| `sitemap.xml` | Mapa de sitio indexable canónico. |
| `vercel.json` | Cabeceras de seguridad y caché inmutable de assets. |

### Assets usados por la página

| Archivo | Uso | Dimensiones |
| :-- | :-- | :-- |
| `assets/hero-salas.webp` | Hero principal (LCP, `fetchpriority="high"`) | 900 × 600 |
| `assets/servicio-*.webp` | Fotos de cada especialidad | 700 × ~470 |
| `assets/adriana-rotela.webp` | Ficha Lic. Adriana Rotela | 400 × 400 |
| `assets/monica-belottini.webp` | Ficha Lic. Mónica Belottini | 400 × 400 |
| `assets/jimena-delmoral.webp` | Ficha Lic. Jimena Delmoral | 400 × 400 |
| `assets/isotipo.webp` | Logo del header en móvil | 120 × 91 |
| `assets/logo-horizontal.webp` | Logo del header en desktop y hero | 768 × 191 |
| `assets/og-image.jpg` | Open Graph / JSON-LD | 1200 × 630 |

## Imágenes provisorias

> **Importante:** las fotos actuales de `assets/` son **provisorias**. Se usan imágenes de stock
> y las fotos originales del equipo mientras el cliente envía el material definitivo.

Cuando lleguen las fotos finales:

1. Guardarlas en `assets/` con el **mismo nombre de archivo** (recomendado WebP, ancho ≤ 1200 px).
2. Mantener las proporciones o actualizar `width`/`height` en `index.html` para evitar CLS.
3. Regenerar `assets/og-image.jpg` a 1200 × 630.

Los logos están en WebP con transparencia porque no se dispone de vectoriales (SVG). Si el
cliente entrega el logo en SVG, reemplazar `isotipo.webp` y `logo-horizontal.webp` por el SVG
y actualizar las rutas en el `<head>` y en el sprite.

## Cómo editar los estilos

`estilos.css` se genera con Tailwind CSS a partir del contenido de `index.html`.
Si se agregan clases nuevas:

```bash
npx tailwindcss -c tailwind.config.js -i input.css -o estilos.css --minify
```

Los tokens de color (`brand-*`), tipografías del sistema, iconos SVG, `safe-area` y
`prefers-reduced-motion` viven en `input.css`.

## Cómo publicar

Es un sitio estático: basta con servir la carpeta.

- **Vercel / Netlify / GitHub Pages:** subir `index.html`, `estilos.css` y `assets/`.
- **Local:** cualquier servidor estático (por ejemplo `npx serve .`).
- No requiere build en producción ni variables de entorno.

## Checklist rápido

- [x] Zero-CDN: sin Tailwind CDN, FontAwesome ni Google Fonts.
- [x] Todas las imágenes locales, con `width`/`height` y `loading="lazy"` (salvo el hero).
- [x] Iconos como sprite SVG inline (`currentColor`, sin librería externa).
- [x] WhatsApp contextual por profesional y por sección.
- [x] FAQ con `aria-expanded` / `aria-controls`.
- [x] Formulario abre WhatsApp en el mismo gesto del usuario.
- [x] Navegación inferior con `safe-area` para iPhone con notch.
- [x] JSON-LD `MedicalClinic` + Open Graph con imagen local.
