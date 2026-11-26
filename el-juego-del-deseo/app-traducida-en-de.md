# App "Sin Límites" traducida a inglés y alemán (2026-11-26)

- Carpetas (en la carpeta del proyecto): "app the desire games (EN)" (EE. UU., marca The Desire Games · No Limits) y "app spiel der begierde (DE)" (Alemania, Spiel der Begierde · Grenzenlos).
- Se generan desde la app en español con scripts\app_i18n\traducir_app.py: copia "app el juego del deseo", reemplaza textos de index.html/app.js/manifest/sw y pone cards_en.js / cards_de.js como cards.js. Si se cambia la app en español, volver a correr el script (borra y rehace las dos carpetas). Si un texto en español cambió, el script frena y avisa cuál no encontró.
- Mismo contenido que la versión en español (83 cartas, 10 castigos, 30 fantasías). Mismo sistema de códigos (codes.js y el link general sirven igual; el formato sigue siendo DESEO-XXXX-XXXX).
- Probadas en 360x640: sin desbordes. TRAMPA: en app.js hay textos entre comillas simples; un apóstrofo en inglés (can't) rompe el JS.
- Falta: publicarlas (dominio/hosting), igual que la española.
- (2026-11-26) Links PÚBLICOS DE PRUEBA con Tailscale Funnel (dependen de la PC prendida; apagar con "tailscale funnel --https=8443 off" y "--https=10000 off"): EN https://desktop-bukarmv.tail1fb808.ts.net:8443 (python http.server 8788), DE :10000 (8789). La raíz :443 → 127.0.0.1:8765 es de OTRO programa: no tocarla. Si se reinicia la PC hay que volver a levantar los http.server. Netlify: el usuario todavía no las subió (zips listos: app-the-desire-games-EN.zip / app-spiel-der-begierde-DE.zip).
