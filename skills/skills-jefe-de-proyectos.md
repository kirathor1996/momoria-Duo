# Skills del Jefe de proyectos (2026-11-21)

- Los agentes de Duo (config.json → agentes; "Jefe de proyectos" id mwr1ja0xhdz6o) NO tienen skills propias: toda skill activa en Duo vale para todos los chats, agentes y tareas.
- Importadas y activas desde Escritorio\skill jefe de proyectos (.skill = ZIP): metodologia-3qs, analizador-ads-estaticos, excel-de-estrategia, monitor-pixel, sugeridor-productos-test. Los "(1)" eran copias idénticas.
- TRAMPA: el importador de Duo rechaza ("name debe tener hasta 64 letras minúsculas...") los SKILL.md cuya cabecera usa `id:` en vez de `name:`. Arreglo: agregar `name: <id>` en una copia (Downloads\duo-skills-jefe\fix), sin tocar los originales.
