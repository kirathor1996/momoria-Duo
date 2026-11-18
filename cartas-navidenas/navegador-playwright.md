# Navegador controlable (2026-11-18)

- En Duo no hay herramientas de Chrome, así que usamos Playwright. Está instalado en C:\Users\AGUSTIN\claude-navegador (playwright-core), fuera del proyecto.
- Se abre Chrome con un perfil propio y depuración remota:
  `chrome.exe --remote-debugging-port=9333 --user-data-dir=C:\Users\AGUSTIN\claude-navegador\perfil`
- Para manejarlo: `node C:\Users\AGUSTIN\claude-navegador\nav.js ver|ir <url>|nueva <url>|click <selector o texto>|escribir <selector> <texto>|scroll|tabs|tab <n>|eval <js>`. Guarda una captura en pantalla.png y lista los elementos visibles.
- El usuario inicia sesión él mismo en esa ventana; las contraseñas nunca pasan por el chat. Las sesiones quedan guardadas en ese perfil.
- Impultienda está en https://impultienda.ar. Su página principal dice que trabaja con MercadoPago, Stripe, PayPal y Whop, y "Cobrá del exterior sin LLC" (confirmado el 2026-11-18).

## Cuenta de Impultienda (2026-11-18)
- Plan Free, 1 tienda. El 2026-11-18 el usuario autorizó reemplazar "El Club del Squishy": ahora es "Cartas Navideñas", https://cartasnavidenas.impultienda.ar (panel: /dashboard/cartasnavidenas/...). Mercado Pago conectado, cobra en ARS. Backup de lo squishy en el proyecto: impultienda/backup/.
- Imágenes subidas en Recursos (sb.impultienda.ar/.../store-resources/...webp). HTML publicado: impultienda/tienda-argentina-subir.html.
- Productos (Diseño de ebooks), todos "Listo" y verificados 2026-11-18: principal "Carta de Papá Noel personalizada + 2 regalos" $19.990 → PDF pack-papa-noel.pdf; bono → regalos-diploma-cuentos.pdf; upsell "Carta de los Reyes Magos personalizada" $19.990 → pack-reyes-magos.pdf (aparece en el checkout como "Sumá a tu compra"). Se quitaron los links de Drive de squishy (están en impultienda/backup/*.json; PDF viejo en backup/squishy-pdf-principal.pdf). Email de soporte sigue siendo el de squishy.
- Producto decidido por el usuario (2026-11-18): opción A. Cada pack = 6 cartas con textos distintos, saludo "Querida/Querido ______" para escribir el nombre a mano, + sobre para recortar y armar + sello de lacre. PDFs en el proyecto: entregables/. Fuente: Temp\capcartas\pdf\textos.py y armar.py; render con claude-navegador\pdf.js (Chrome headless).
- Reseñas (2026-11-18): 5 cargadas como postales navideñas, nombre completo; desde la 4.ª llevan class="testi extra" (botón Ver más/Ocultar). No cargar reseñas inventadas, copiadas de otra marca ni de otro producto (el usuario lo pidió varias veces y se le dijo que no).
- PDFs (2026-11-18): packs de 16 págs; se sumaron "Mi carta para Papá Noel/los Reyes" (escribe + dibuja) antes del sobre. Fuente: entregables/fuente/hojas_ninos.py; originales de 14 págs en entregables/originales. Subida a Impultienda: claude-navegador/reemplazar2.js idx x archivo (idx 0 Papá Noel, 2 Reyes); verificación: verpdf2.js.
- 2026-11-18: landing revisada en celular (390px) con movil.js: sin scroll lateral; se agregó bloque CSS "Ajustes para celular" (menos espacio, botones anchos). Pendientes de texto: reseñas dicen "Nombre del cliente", paso 2 y "menos de 24 h" suponen opción B, bonus dice "audiocuentos", pie menciona Reyes Magos.
- 2026-11-18: se sacó el bonus "Foto mágica" (pedido del usuario). En "Nuestras cartas" se agregó la Carta de los Reyes Magos con imagen propia (imagenes/carta-reyes-es.png, hecha con make_reyes.py en Temp\capcartas\imgs; el usuario había pedido usar la foto de cartasencantadas y se le dijo que no). El botón dice "la sumás en el checkout": PENDIENTE crear el upsell de Reyes (Plan Free permite 1) cuando el usuario diga el precio.
- Scripts en C:\Users\AGUSTIN\claude-navegador: render.js (HTML→PNG), movil.js (capturas en tamaño celular), subir.js (Recursos), pegar.js (HTML), producto.js (título/portada/descripción del ebook con el diálogo abierto).
- El usuario pidió usar tal cual las fotos de cartasencantadas.com; se le explicó dos veces que no (son de otra marca). Usar imágenes propias o generadas imitando el estilo.
- Cada tienda es una sola landing con un solo producto. Se carga en Personalización → Contenido → "HTML completo de la tienda".
- Botón de compra: `<a href="/checkout">`. Precio con tokens: {{price}}, {{original_price}}, {{savings}}, {{currency}}. Cupones: /checkout?cupon=X. El precio se muestra en la moneda del comprador.
- Los HTML listos para pegar están en el proyecto, en impultienda/tienda-argentina.html y impultienda/tienda-ingles.html.
- 2026-11-18: Recursos está en /dashboard/cartasnavidenas/personalizacion/diseno/recursos (la URL /recursos sola no carga). Después de pegar el HTML, la tienda pública tarda unos 30 s en mostrar el cambio.
- Sello de garantía: Openclipart 346882 (dominio público), traducido al español → imagenes/garantia-es.svg/.png, subido a Recursos.
