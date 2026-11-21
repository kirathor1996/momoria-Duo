# Biblioteca de Anuncios de Meta en headless (2026-11-21)

- La Biblioteca SÍ se renderiza con Chrome headless (chrome.exe --headless=new --remote-debugging-port=9444+ con perfil temporal propio) y se puede leer por CDP desde Node 24 (WebSocket nativo). No hace falta login.
- URL que funciona: facebook.com/ads/library/?active_status=active&ad_type=all&country=BR&media_type=all&search_type=keyword_exact_phrase&q="ebook"&start_date[max]=AAAA-MM-DD (usar >1 mes para validados). Hay que hacer scroll (3-7 veces) para cargar tarjetas.
- view_all_page_id NO devolvió resultados en headless (con ni sin search_type=page). Para contar anuncios de una página: buscar el nombre del anunciante con search_type=keyword_unordered (aproximado) y contar tarjetas de ese anunciante.
- Scripts temporales en C:\Users\AGUSTIN\AppData\Local\Temp\adlib-scripts (scrape.mjs, agg.mjs).
- Usar puertos 9444-9446, nunca 9333 (navegador de trabajo del usuario).
- El usuario quiere rapidez: entregar 3 productos validados (activos +1 mes, escalados) sin tardar de más.
