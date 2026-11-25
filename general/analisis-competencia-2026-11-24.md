# Análisis de competencia — tanda 1 (2026-11-24)

Biblioteca de Meta (country=ALL, activos) leída con Chrome headless en el puerto 9444. Los scripts están en entornos/general/analisis-paginas (cdp.mjs, parse.mjs, quiz.mjs).

- ingles.atrilestudio.com ("Inglés en Mapas", PDF con +300 mapas A1-C2, USD 17 / 15 €): ~100 anuncios, desde el 22/10/2026, sin "X anuncios usan" pero con 93 variantes. Veredicto: ARMAR MEJORADO (la mejor de la tanda).
- calisteniamilitar.site (quiz + VSL de 12 min + /salespage, USD 7,90, tachado 49,90): ~110 anuncios, desde el 22/07/2026, 42 con duplicados. Validado, pero es fitness: ARMAR MEJORADO solo si el usuario confirma que quiere entrar en fitness.
- kit-para-adolescentes.impultienda.ar (kit para psicólogos, US$16): 31 anuncios propios desde el 09/11/2026, más otros 6 kits para terapeutas en Impultienda. VIGILAR (nicho caliente pero muy nuevo).
- magiatienda.com/bonita (plantillas de packaging para joyería en Canva, Hotmart, USD 12): 19 anuncios. NO ARMAR.
- escuelavegetariana.com (cursos en video de cocina vegana, marca personal de Alejandra Schvartz): ~37 anuncios desde dic 2025. NO ARMAR.

## Inglés en Mapas a fondo (2026-11-24)
- Atril pauta en MX (~81), CO (~79), ES (~100) y US (~81). En AR tiene 0 anuncios.
- El formato "300 mapas mentales de inglés" ya lo venden muchos: Inglés en Mapas Visuales (desde 01/09, duplicados), Tus Clases Online (+100 videos), 300mapas.online (USD 9,99 con 6 bonus), OferteiHoje y Biblioteca Digital (por WhatsApp), Mapas Pro.
- En AR, desde el 15/11 hay un clon casi idéntico de Atril (ingles-en-mapas.impultienda.ar, AR$ 19.999, mismos 4 bonus) y otro desde el 20/11 (idiomapa.impultienda.ar, AR$ 19.990, cero a intermedio).
- Conclusión: la demanda está validada pero el formato genérico se está saturando. Entrar solo anichado y con audio.

## Material armado (2026-11-24)
- Carpeta: Escritorio\video para mapas de ingles: 102 videos de Atril, transcripciones, landing (1_), guiones de Atril desarmados (2_) y nuestros guiones UGC (3_).
- Hallazgo: Atril usa un solo guion base con 25 ganchos distintos; los que más usa son "Mirá cómo repaso todo el inglés A1-C2" (32 videos) y "Si entendés inglés y después se te olvida" (24). No muestran a nadie a cámara ni tienen audio.
- Plan acordado con el usuario: landing con la misma estructura y texto propio, creativos UGC (3 bases × 12 ganchos), test primero en AR y después MX.

## Producto Inglés en Mapas armado (2026-11-24)
- Carpeta: Escritorio\video para mapas de ingles\PRODUCTO_300_mapas (LEEME.md explica todo). 6 PDF (A1-C2, 300 mapas), 300 MP3 (edge-tts voces Jenny/Guy), contenido en JSON editable y scripts para regenerar.
- Español neutro sin vos/tú (para AR, MX y ES). Marca provisoria INGLÉS ORDENADO (variable MARCA).
- Pendiente: hosting de audios + QR por mapa, 4 bonus, revisión humana del contenido, testimonios.

## Videos de anuncios gratis (2026-11-25)
- Escritorio\video para mapas de ingles\VIDEOS_NUESTROS: 9 anuncios de la 1ra tanda hechos sin gastar (edge-tts voz es-AR + páginas de mapas animadas con PIL/ffmpeg + subtítulos karaoke ASS). Script crear_videos.py.
- TRAMPA TTS: "del A1" suena "de la 1"; "sin cuotas" suena "cinco cuotas". Verificar siempre con faster-whisper.

- (2026-11-25) Voz clonada de Agustina GRATIS en la PC: Chatterbox Multilingual (MIT, uso comercial OK; XTTS y F5 son no comerciales). Entorno en C:\Users\AGUSTIN\AppData\Roaming\Duo\herramientas\clonar-voz (.venv Python 3.11, torch 2.6.0+cu124 en la RTX 3060 Ti; hizo falta setuptools<81 para perth). Script clonar_frases.py <muestra.wav> <salida.wav> <frases.txt> [intentos]: genera frase por frase, Whisper elige la toma más fiel. Trampas: con texto largo inventa palabras al final; escribir "a uno"/"ce dos" en vez de A1/C2. Muestra: VIDEOS_NUESTROS\VOZ_AGUSTINA\muestra_agustina.mp3 (la original de Cartas Navideñas se borró; se recuperó de Higgsfield media 3ce8e1be…). Créditos Higgsfield: 0,9.
- (2026-11-25) Los 10 videos de Inglés Ordenado ya usan la voz clonada de Agustina (FINALES; los viejos en VERSION_VIEJA_voz_robot). Flujo en VIDEOS_NUESTROS\LEEME.md. Frases copiadas de Atril reescritas. Duran 17-37 s.
