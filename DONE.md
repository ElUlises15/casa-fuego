# Casa Fuego · terminado

Sitio estático multipágina: index.html, carta.html, eventos.html y reservas.html. Sin dependencias de runtime, sin proceso de build y sin git.

## Entrega
- Identidad carbón, brasa, hueso y albahaca; fuentes Barlow Condensed y DM Sans locales.
- Hero de parrilla con partículas que terminan a los 10 segundos; reduced-motion sin partículas.
- Navegación móvil, carta por secciones, preguntas de eventos y formulario demo validado con toast accesible. No hay backend, envíos ni almacenamiento.
- WhatsApp demo: https://wa.me/541155550909.
- Cinco imágenes creadas mediante image_gen integrado: assets/hero-parrilla.png, assets/plato.png, assets/patio.png, assets/vino.png y assets/equipo-cocina.png. WebP comprimidos para carga. Prompts exactos en assets/PROMPTS.md.
- noindex/nofollow en las cuatro páginas. _headers incluye X-Robots-Tag para hosts compatibles; un servidor HTTP simple no interpreta ese archivo. robots.txt permite leer la meta noindex.
- Carta e imágenes identificadas como ilustrativas. Sin horarios, precios, domicilio preciso, reseñas o credenciales inventadas.
- Dirección visual en spec.md. Guías anti-generico, frontend-design, web-review y kit gastro leídas.

## Validación realizada
Chrome con Playwright sobre `python3 -m http.server 4173`.
- Cuatro páginas a 390 y 1280 px: un H1 por página, sin overflow horizontal, imágenes completas, cero errores de JavaScript ni respuestas HTTP >=400.
- Comprobación adicional a 320 px: sin overflow en las cuatro páginas; corregido el tamaño del título de eventos.
- Zoom CSS al 200% sobre viewport de escritorio de 1280 px: sin overflow en las cuatro páginas. La prueba extrema de zoom CSS al 200% sobre viewport de 390 px produce desbordes (ancho efectivo inferior a 200 px); no se garantiza ese tamaño.
- Menú móvil abre y navega; Escape cierra y devuelve foco al botón.
- Tab inicial llega a “Saltar al contenido”. Estilos de foco visibles en controles y enlaces.
- Reduced-motion: cero partículas creadas.
- Formulario vacío bloqueado por validación nativa. Datos de prueba válidos muestran toast; cero solicitudes POST. Fecha pasada limitada; tipo Evento preseleccionado desde eventos.html.
- Inspección visual de capturas de portada desktop/mobile, carta desktop y reservas mobile. Capturas de las cuatro páginas en ambos tamaños en qa/.
- Contraste de botones reforzado con un tono de brasa más oscuro. No se declara auditoría completa de accesibilidad.

## Uso
Abrir index.html o servir esta carpeta con un servidor estático. No se publicó el sitio.
