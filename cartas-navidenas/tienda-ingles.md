# Tienda en inglés "Letters from Santa" (2026-11-19)

- Plan Starter (prueba de 45 días, la activó el usuario el 2026-11-19). 2.ª tienda: https://lettersfromsanta.impultienda.ar (panel /dashboard/lettersfromsanta/...). Creada con "Copiar una tienda que ya tengo" desde Cartas Navideñas.
- Países recomendados: EE.UU., Canadá, Reino Unido, Australia (después Irlanda y Nueva Zelanda).
- Cobro: tienda en USD + Impul Pay (Whop). Checkout probado con ?country=US/GB/CA: US$ 19.90 / £15.12 / CA$ 28.50, en inglés. Idioma de la tienda: English (en-US).
- Productos: principal "Personalized Letters from Santa + 2 Free Gifts" US$ 19.90 (tachado 29.90) → entregables/santa-letters-en.pdf; bono "Free Gifts: Good Behavior Diploma + Christmas Stories" → gifts-diploma-stories-en.pdf; upsell "Letters from Your Christmas Elf" US$ 19.90 (tachado 29.90) → elf-letters-en.pdf (el usuario aceptó el elfo en lugar de los Reyes).
- PDFs en tamaño Letter (también imprimen en A4 con "Fit to page"). Fuente: entregables/fuente/textos_en.json + armar_ingles.py → render con claude-navegador/pdf-letter.js. "Dear ____" sirve para niña y niño, por eso cada pack tiene 15 págs. El elfo se llama Snowflake (= Copito). No usar la marca "Elf on the Shelf".
- Página: impultienda/tienda-ingles-subir.html, generada por impultienda/fuente-en/armar_pagina_en.py (CSS/JS de tienda-unica.html + cuerpo-en.html). Se sube con claude-navegador/pegar-en.js.
- Reseñas: las mismas 5 reales de la tienda en español, traducidas, con la aclaración "translated from Spanish" (pedido del usuario: mismas reseñas en inglés).
- Fotos: rehechas con la carta en inglés (sobre "To: Emma") en entregables/fuente/prev-en/ (foto-santa-en, foto-manana-en, foto-cuentos-en). La foto del chico escribiendo (texto en español) y la de los Reyes no se usan.
- Pendiente: pixel de Meta y email de soporte de esta tienda (no se copian).
- Ojo con los scripts que buscan la pestaña por URL ("/ebooks", "/recursos"): con 2 tiendas pueden agarrar la de la otra tienda. Verificar con `node nav.js tabs` antes.
