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
- Productos (Diseño de ebooks): principal "Carta de Papá Noel personalizada + 2 regalos" $19.990 y bono "Diploma + Cuentos". PENDIENTE: los dos siguen con el LINK EXTERNO de Drive de los squishies (se entregaría el pack equivocado) hasta tener el PDF de la carta. Email de soporte sigue siendo el de squishy.
- Scripts en C:\Users\AGUSTIN\claude-navegador: subir.js (Recursos), pegar.js (HTML), producto.js (título/portada/descripción del ebook con el diálogo abierto).
- El usuario pidió usar tal cual las fotos de cartasencantadas.com; se le explicó dos veces que no (son de otra marca). Usar imágenes propias o generadas imitando el estilo.
- Cada tienda es una sola landing con un solo producto. Se carga en Personalización → Contenido → "HTML completo de la tienda".
- Botón de compra: `<a href="/checkout">`. Precio con tokens: {{price}}, {{original_price}}, {{savings}}, {{currency}}. Cupones: /checkout?cupon=X. El precio se muestra en la moneda del comprador.
- Los HTML listos para pegar están en el proyecto, en impultienda/tienda-argentina.html y impultienda/tienda-ingles.html.
