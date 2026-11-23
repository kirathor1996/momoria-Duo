(2026-11-23) Pack estoico en inglés "The Stoic Path Collection" (para EE.UU./UK/CA/AU), inspirado en competidor es.mentisclassics.com (EduDigital, AR$, 6 PDFs).
- ESTADO: los 6 PDF terminados en la raíz de "Libros Digitales" (1 Meditations, 2 Seneca On the Shortness of Life +3 ensayos, 3 Enchiridion, 4 Stoicism for Anxiety, 5 Stoicism for Your Emotions, 6 The 21-Day Stoic Challenge). 4-6 son textos originales nuestros; citas solo de traducciones de dominio público (Long, Stewart).
- Para regenerar: "_trabajo_pack_estoico\build.py" (python -I build.py [num]); fuentes HTML de 4-6 en _trabajo_pack_estoico\libros\. Usa Chrome headless --print-to-pdf (sin puerto de depuración).
- EPUB originales en "Libros ingles dominio publico\" (Standard Ebooks, CC0).
- TRAMPA: Project Gutenberg devuelve 503 a curl; usar standardebooks.org.
- Tapas (2026-11-23): estilo blanco tipo competidor (comillas de color + título Oswald grande). Ilustraciones = grabados de dominio público de Wikimedia Commons procesados con _trabajo_pack_estoico/portadas/procesar.py; textos y colores de tapa en COVERS de build.py; build.py también exporta portadas/tapa-N.png. Higgsfield tenía 0,9 créditos (no alcanzó para generar).
- Páginas (con workbooks): 151, 120, 67, 76, 80, 81 + Bonus 21-Day Stoic Journal 32 = 607. Workbooks en libros/*.workbook.html (build.py los agrega al final, estilo compacto .wb); el diario es num=7 en BOOKS con CSS compacto propio.
- Bonus hecho: "Bonus - The 21-Day Stoic Journal.pdf" (tapa con grabado de Séneca, ilu-7).
