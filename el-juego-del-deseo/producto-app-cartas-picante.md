# Idea de producto: app de cartas "sin límites" (2026-11-19)

- El usuario quiere sacar un producto nuevo: una app de cartas como la que ya tienen, pero mucho más explícita y "sin límites", con prendas.
- Lo que se recomendó: que sea una web app (PWA) con link y QR, no una app de App Store o Google Play, porque las tiendas rechazan las apps con contenido sexual explícito. El cobro tiene que ir por Shopify o el checkout que ya usan, no por las tiendas de apps. En los anuncios de Meta, la app se muestra censurada, con el mismo formato de la carta tachada.
- Funciones que se propusieron: niveles, ruleta, prendas y castigos, una palabra de seguridad con filtro de límites para cada pareja, temporizador, modo "a ciegas", reto 30 noches, packs extra y una versión de regalo.
- Estado: ver abajo (primera versión ya armada).
- 2026-11-19: se armó la primera versión, una web app (PWA) sin dependencias. Está en la carpeta "app el juego del deseo" (index.html, styles.css, app.js y cards.js con todo el contenido, más sw.js y el manifest). Usa los colores de la marca: negro, bordó y dorado. Tiene +18, PIN, botón de pánico, termómetro de 5 niveles, prendas y castigos, doble o nada con comodines, temporizador, modo a ciegas, rol de quién manda, 7 mazos, ruleta y dados, fantasías en secreto, cartas propias y límites con palabra de seguridad. Todo se guarda en el celular (localStorage). TRAMPA: no usar la clase .back para el dorso de la carta, porque choca con el botón "volver".
- Falta: publicarla con https (Netlify o Vercel) y ponerle un acceso pago (código o login después de comprar en Shopify). Hoy cualquiera que tenga el link puede usarla.

- 2026-11-19: adaptada a celular chico (320-412 px): la pantalla de juego entra sin scroll desde 360x640; en pantallas bajas los 4 botones van en una fila. Pruebas: 0 desbordes laterales en todas las pantallas.

- 2026-11-20: el logo de la app es el oficial de la carpeta Escritorio\Logo JDD (logo_v2_borgona.png), vectorizado. app/logo.svg = version oro. En CSS va como mascara (--logo) en .logo-amp, .amp-wm, .back-amp, .card-logo; icon.svg tambien. OJO: al cambiar proporciones con regex no tocar el aspect-ratio:5/7.2 de .card-wrap.


- 2026-11-20: acceso con código único (opción A elegida por el usuario). 5000 códigos DESEO-XXXX-XXXX en 'codigos app juego del deseo (NO SUBIR)'; la app guarda solo huellas cyrb53 en codes.js; link directo ?c=CODIGO activa solo. Generador: scripts/generar_codigos.mjs (conserva los viejos). Hosting elegido: Cloudflare Pages + subdominio propio (falta cuenta y dominio). Falta: conectar Shopify para mandar un código por compra (preguntar qué app usa para entregar PDFs).
