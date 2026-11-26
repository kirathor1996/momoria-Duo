# Propuesta de sección para vender la app en eljuegodeldeseo.com (2026-11-26)

- La home de la tienda es una landing de un solo producto (tema Shrine PRO, secciones: hero oferta, dolor, mazos, qué vas a lograr, producto, bonos, FAQ, reseñas, dónde).
- Propuesta: agregar UNA sección nueva "Colección Sin Límites" (app) entre Bonos y FAQ, sin tocar las demás. Bloque "Liquid personalizado"/Custom liquid.
- Archivos (solo maqueta, no se subió nada): Desktop\Ebook new juego del deseo\propuesta web app\ (seccion-nueva.html, PNG celular/compu, página completa).
- Falta definir precio (quedó $XX.XXX) y el link del producto/colección en Shopify.

## Análisis de la tienda (2026-11-26, 2da vuelta)
- La home NO tiene menú ni header de navegación; solo 1 colección (frontpage). Compra por formularios /cart/add (variantes Digital 52277098709287 y Física 52277093564711).
- El carrito lateral ya tiene 4 upsells del tema (Kamasutra, 100 Juegos, De Cero a Mil, Cofre). Lo más limpio: sumar la app como 5º upsell (primero) => cero cambio de estructura. Maqueta: propuesta web app\carrito-con-app.png.
- Para anuncios: página de producto propia de la app (/products/...), sin tocar la home.

## Código para pegar a mano (2026-11-26)
- El usuario NO quiere que toquemos la tienda real: lo pega él en una página borrador.
- Archivo: propuesta web app\codigo-nueva-coleccion-y-popup.txt (Liquid personalizado: bloque "Nueva colección" arriba + popup 10% una vez por sesión).
- Supone: producto con handle app-sin-limites, código de descuento LANZAMIENTO10 (10%, solo la app), imagen subida a Contenido>Archivos como portada-app.png. El botón usa /discount/CODIGO?redirect=... para que el descuento se aplique solo.
