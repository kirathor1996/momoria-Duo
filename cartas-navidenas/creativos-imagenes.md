# Creativos en imagen (2026-11-19)

- Al usuario NO le gustó la voz de IA del video ("muy IA"). Pidió creativos en imagen, de Navidad y de Reyes, todos nuevos (sin reutilizar lo ya hecho).
- Tanda 1: 8 imágenes de 1080x1350 (4:5) en creativos/ como "imagen 1..8.png". Las 1 a 5 son de Navidad: oferta 33% OFF, qué recibes, reseña real de Sol L., "la noche del 24 se acerca" y una nota adhesiva estilo "ugly ad". Las 6 a 8 son de Reyes: oferta, "noche del 5 de enero, junto a sus zapatos" y qué recibes.
- Hechas con HTML, usando las páginas reales del PDF (creativos/paginas, renderizadas a 150 dpi con pymupdf) y el nombre en letra Caveat sobre la línea "Querida ____". Generador: creativos/fuente/armar.py. Render: claude-navegador/render-creativos.js <html> <salida>.
- Texto en español neutro (tú). No hay precios en moneda, porque cambian según el país: solo dice "33% OFF".
- Ojo: Reyes hoy es solo upsell del checkout. Los anuncios de Reyes llevan a la página de Papá Noel.
