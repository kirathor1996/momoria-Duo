# Tiendas reales de EE. UU. y Alemania (2026-11-27)

- EE. UU.: Shopify admin `thedesiregame` (la tienda se llama "The Desire Game", en singular; tema shrine-pro-1-3-0-nulled). Alemania: Shopify admin `dasspielderlust` (dominio dasspielderlust.de). Son tiendas EN VIVO con pedidos.
- El usuario está logueado en ellas en su Chrome normal (Profile 2), que no tiene puerto de depuración. Para trabajar abrí un Chrome aparte: perfil `Duo\herramientas\chrome-jdd`, puerto 9446 (ahí tiene que iniciar sesión el usuario).
- Impultienda (Maplish) queda aparte: no se usa para esto.
- Precio pedido por el usuario: base 19,90 (USD en EE. UU., EUR en Alemania) + 35 % = 26,90; comparación 35,90; código 10 % solo la app (NOLIMITS / GRENZENLOS).
- La tienda k01cpa-0y fue solo de prueba.

## Prueba piloto EE. UU. (2026-11-28) — HECHA
- Producto "The Desire Games No Limits" (id 9851050852406, handle the-desire-games-no-limits), 26.90 / 35.90, digital, publicado en Tienda online (ACTIVO en la tienda real).
- Código NOLIMITS (DiscountCodeNode 1355254792246), 10 % solo ese producto, un uso por cliente.
- Sección + popup SOLO en una COPIA del tema: "PRUEBA APP No Limits (no publicar)" id 160360267830, debajo de banner_wbY6AT. El tema publicado (shrine-pro, 156845703222) NO se tocó. Vista previa: thedesiregame.com/?preview_theme_id=160360267830
- Para pasarlo al tema publicado: `python subir_tema.py thedesiregame <tab> gid://shopify/OnlineStoreTheme/156845703222 qu4.json banner_wbY6AT --live` (scripts en %TEMP%\cdpjdd; guarda backup del index antes).

## Prueba piloto ALEMANIA (2026-11-28) — HECHA
- El handle real del admin alemán es `na1byx-1n` (no dasspielderlust). Moneda EUR. Mismo Chrome 9446 (el usuario cambió de cuenta en la pestaña).
- Producto "Das Spiel der Lust Grenzenlos" id 15904498254190, 26,90 € / 35,90 €, publicado en Tienda online (ACTIVO).
- Código GRENZENLOS (DiscountCodeNode 1876908343662).
- Sección + popup SOLO en copia del tema "PRUEBA APP Grenzenlos (no publicar)" id 198274842990, debajo de hero_yHpwDY. Tema publicado 195437068654 sin tocar. Vista previa: dasspielderlust.de/?preview_theme_id=198274842990
- Pasarlo al publicado: subir_tema.py na1byx-1n <tab> gid://shopify/OnlineStoreTheme/195437068654 ql5.json hero_yHpwDY --live
- TRAMPA (2026-11-28): las tiendas tienen mercados con LISTAS DE PRECIOS FIJOS. Un producto nuevo no muestra el precio tachado en esos mercados hasta agregarle precio fijo (priceListFixedPricesAdd). DE: hecho en "Alemania y Austria" (26,90/35,90 EUR) y "Suiza" (27,90/36,90 CHF). EE. UU.: el mercado USD no tiene lista (anda bien); Inglaterra, Canadá, Australia, Nueva Zelanda e Irlanda sí tienen → falta definir precios ahí.
- En la ficha de producto el tema (Shrine) muestra "(xxxx Reviews)" y una línea de envío "Ordered/Order Ready/Delivered": pasa en TODOS los productos de la tienda, no es nuestro.
