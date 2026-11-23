# Biblioteca de Anuncios de Meta en headless (2026-11-21)

- La Biblioteca SÍ se renderiza con Chrome headless (chrome.exe --headless=new --remote-debugging-port=9444+ con perfil temporal propio) y se puede leer por CDP desde Node 24 (WebSocket nativo). No hace falta login.
- URL que funciona: facebook.com/ads/library/?active_status=active&ad_type=all&country=BR&media_type=all&search_type=keyword_exact_phrase&q="ebook"&start_date[max]=AAAA-MM-DD (usar >1 mes para validados). Hay que hacer scroll (3-7 veces) para cargar tarjetas.
- view_all_page_id NO devolvió resultados en headless (con ni sin search_type=page). Para contar anuncios de una página: buscar el nombre del anunciante con search_type=keyword_unordered (aproximado) y contar tarjetas de ese anunciante.
- Scripts temporales en C:\Users\AGUSTIN\AppData\Local\Temp\adlib-scripts (scrape.mjs, agg.mjs).
- Usar puertos 9444-9446, nunca 9333 (navegador de trabajo del usuario).
- El usuario quiere rapidez: entregar 3 productos validados (activos +1 mes, escalados) sin tardar de más.
- (2026-11-23) CRITERIO DEL USUARIO: "validado" = anunciante/página con MÁS DE 50 anuncios activos en la Biblioteca (además de +1 mes y sin comida/fitness). Verificar por nombre del anunciante (keyword_unordered) con 5 scrolls: da hasta ~100 tarjetas. agg3.mjs junta todos los .json viejos por anunciante; agg4.mjs resume tandas nuevas.
- (2026-11-23) Con 50+ anuncios y sin comida/fitness salen muy pocos: Clever Poppy (US, bordado, 56), Photzy (US), Pack herrería (ES, 2 páginas: Marcos Vinicius 58 + Daniel Brooks 65), Praxis Studio (ES, 84), Clubinho Católico (BR, 87, físico). IT y FR con "ebook/guida/télécharger/méthode" devolvieron solo apps y corporativos: no vale la pena repetir. Manualidades (crochet, madera, guitarra) en US/MX/BR: nadie pasa de 40 anuncios.
