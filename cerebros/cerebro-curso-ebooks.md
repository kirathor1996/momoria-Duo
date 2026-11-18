# Cerebro del curso "Ebooks de Cero a CEO" (2026-11-18)

- El proyecto cerebros-exey es un cerebro armado con el curso de `C:\Users\AGUSTIN\Desktop\Curso Ebooks` (7 módulos: modelo de negocio, creación de ebook, Facebook, tienda Shopify, creativos, Meta Ads, upsell).
- Estructura: `CLAUDE.md` (entrada) · `cerebro/` (notas por tema, índice en `00-INDICE.md`) · `fuentes/transcripciones` (videos transcriptos con faster-whisper medium en la GPU) · `fuentes/documentos` (PDF/docx/txt extraídos) · `.claude/skills/` (7 skills) · `_scripts/` (extracción y transcripción).
- Trampa ya pagada: faster-whisper en GPU necesitó `pip install nvidia-cublas-cu12 nvidia-cudnn-cu12` y agregar las carpetas `site-packages/nvidia/*/bin` con `os.add_dll_directory` (ya está en `_scripts/transcribir.py`).
- Trampa: Bash de Git no abre archivos con emojis o tildes en el nombre (los del curso tienen); usar Python para esos.
