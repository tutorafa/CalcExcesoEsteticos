# Cálculo importe MULTIMAP

App web instalable (PWA) para calcular los importes de un siniestro y de la asistencia MULTIMAP.

## Desplegar en GitHub Pages
1. Crea un repositorio y sube **todo** el contenido de esta carpeta (incluida `.github`).
2. En *Settings → Pages → Build and deployment*, elige **Source: GitHub Actions**.
3. Haz push a `main`; el workflow publica la app en `https://<usuario>.github.io/<repo>/`.

## Instalar
- **Android (Chrome):** menú ⋮ → *Instalar aplicación*.
- **iOS (Safari):** Compartir → *Añadir a pantalla de inicio*.
- **PC (Chrome/Edge):** icono de instalar en la barra de direcciones.

## Estructura
- `index.html`: aplicación (lógica de cálculo + interfaz)
- `manifest.webmanifest`, `sw.js`: instalación y modo sin conexión
- `icons/`, `favicon.ico`: iconos (any, maskable, apple-touch)

Al cambiar archivos, incrementa `CACHE` en `sw.js` para que los usuarios reciban la actualización.

## Vista previa al compartir (WhatsApp, Telegram, etc.)
`index.html` incluye etiquetas Open Graph y `og-image.jpg` (1200×630). WhatsApp exige una URL absoluta para la imagen: el workflow sustituye `__SITE_URL__` por la dirección real de GitHub Pages al desplegar. Si despliegas sin el workflow, reemplázalo a mano por tu URL (terminada en `/`).
WhatsApp guarda la vista previa en caché: si la cambias, prueba con `?v=2` al final del enlace.
