# IRATA Consulting — sitio web

Sitio estático (HTML + CSS + JS). **Sin build, sin dependencias, sin CDN**: las fuentes y las imágenes van dentro de la carpeta.
Funciona en cualquier hosting (cPanel, Hostinger, GoDaddy, Netlify, Vercel, GitHub Pages, S3, etc.).

## Cómo publicarlo
1. Sube **todo el contenido** de esta carpeta a la raíz del hosting (`public_html`, `www` o equivalente), de modo que `index.html` quede en la raíz.
2. Netlify / Vercel / Cloudflare Pages: arrastra la carpeta o conéctala a un repositorio; no requiere configuración.
3. WordPress: si ya tienes WP, sube esta carpeta a un subdominio o ruta aparte (p. ej. `/irata/`), o usa un plugin de "página estática/HTML". No está pensado como tema.

## Lo único que debes editar (en `index.html`, bloque `IRATA_CONFIG`, cerca del inicio)
- `email`: correo real de contacto (hoy: `hola@irata.consulting`, tomado de la propuesta anterior; confírmalo).
- `whatsapp`: número con código de país, sin `+` (ej. `573001234567`). Vacío = el botón no aparece.
- `linkedin` / `instagram`: URL completas. Vacío = no aparecen.
- `formEndpoint`: URL de un servicio de formularios (Formspree, Getform, Formsubmit…). Vacío = el formulario abre el correo del visitante con el mensaje ya redactado. **Recomendado configurarlo** para recibir los mensajes directamente.

## Otros ajustes
- **Foto del fundador:** guarda `ramon.jpg` (cuadrada, mínimo 1000×1000 px) en `assets/img/`. Si no existe, se muestra el monograma "RB".
- **Dominio:** reemplaza `https://irata.consulting` en `index.html` (canonical, Open Graph, JSON-LD), `robots.txt` y `sitemap.xml` si usas otro.
- **Privacidad:** `privacidad.html` es un borrador base; revísalo con un asesor legal.
- **Analítica** (GA4, Plausible, etc.): no está incluida. Si la agregas, actualiza la política de privacidad.

## Logos e imágenes (calidad)
- `assets/img/*-original.jpg` son tus archivos **sin modificar**.
- Para la web se generaron variantes WebP de alta calidad (≈46 dB PSNR frente al original, visualmente idénticas) en varios tamaños (`srcset`): el navegador elige la que corresponde a la pantalla y a su densidad (1x, 2x, 3x, 4K).
- Los diseños no se redibujaron ni recolorearon. Las variantes `*-marca-*` solo recortan el margen vacío para usarlas pequeñas (menú, favicon).
- Si cambias un logo, vuelve a exportarlo en los mismos nombres/tamaños.

## Estructura
```
index.html · privacidad.html · robots.txt · sitemap.xml
assets/css/styles.css · assets/js/main.js
assets/fonts/ (Bricolage Grotesque, Instrument Serif, Figtree — licencia OFL, autoalojadas)
assets/img/ (logos, isotipos, favicons, og-image)
```
