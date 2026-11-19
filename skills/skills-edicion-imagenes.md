# Skills de edición de imágenes (2026-11-19)

- Duo guarda las skills en %APPDATA%\Duo\skills (una carpeta por id + registro.json, que relee en cada consulta). Para importar sin la pantalla: usar el propio módulo de Duo (app.asar → skills.js: crearSkills({dir}).revisarArchivo(ruta) → confirmar(token) → activar(id,true)), nunca editar registro.json a mano. Límites: 25 MB, 500 archivos, 20 activas.
- 2026-11-19: las 3 skills de abajo quedaron importadas y activas en Duo.
- Preparadas para importar en C:\Users\AGUSTIN\Downloads\duo-skills-imagen\listas: image-editing (jlouage, adaptada para usar `python` en vez de `uv`), image-annotations (github/awesome-copilot), image-enhancer (ComposioHQ).
- En la PC: Python 3.14 + pillow, pillow-heif, numpy instalados. No hay uv ni ImageMagick (por eso se descartó la skill de ImageMagick).
