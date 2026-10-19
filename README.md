# Arnasa · web estática

Misma idea que `jokai-web`: HTML + JS + CSS sin compilación. Todo el contenido está en
`content.eu.md` y `content.es.md`; se edita el texto, se guarda y se recarga el navegador.

## Probar en local

    python3 -m http.server 8000

y abre http://localhost:8000 (no sirve abrir `index.html` con doble clic: `fetch()` falla con `file://`).

## Estructura

- `index.html` · `app.js` · `styles.css` — motor y estilo (compartidos con jokai-web)
- `content.eu.md` / `content.es.md` — contenido por idioma (cada marcador `<!-- @id -->` es una sección)
- `vendor/marked.umd.js` — render de markdown, en local
- `img/hero.jpg` — fondo del hero

## Notas

- **Contenido provisional:** copiado de Mugarri (textos, créditos, fotos y vídeos) hasta que haya el de Arnasa.
  Hay que reescribir `content.eu.md` y `content.es.md`.

- Las fotos de la galería apuntan por ahora a `jokai.eus/wp-content/...`. Para independizar la web,
  descárgalas a `img/` y cambia las rutas en la sección `@galeria`.
- Los vídeos usan `youtube-nocookie.com`.
