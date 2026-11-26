# App en Shopify AR: producto, código y sección (2026-11-26, prueba piloto)

- Tienda admin k01cpa-0y (moneda de la tienda: USD, pero los precios están cargados en pesos). Tema activo: shrine-pro-1-3-0-nulled (id 158311317677).
- Producto "El Juego del Deseo Sin Límites" (handle el-juego-del-deseo-sin-limites, id 15484789162157): $26.990, comparación $39.990, digital (sin envío, sin inventario), publicado solo en Tienda online, portada 1:1 como imagen.
- Código SINLIMITES: 10 % solo en ese producto, un uso por cliente, no combinable. El cliente lo escribe en el checkout (decisión del usuario: nunca aplicar solo). LANZAMIENTO10 y "picante" ya se borraron.
- Sección sections/jdd-nueva-coleccion.liquid en la home, justo debajo de "Banner Hero" (key jdd_nueva_coleccion). Si no hay imagen elegida, usa la del producto. Respaldo de la home anterior: propuesta web app\backup-index-antes-de-seccion-2026-11-26.json.
- Cómo se hizo: GraphQL del admin desde la pestaña logueada del Chrome 9445 (fetch a /api/shopify/k01cpa-0y?operation=X con el header x-csrf-token que está en el HTML). Scripts en %TEMP%\cdpjdd (gql.mjs, cdp.mjs). La tienda tiene contraseña: para ver la home, usar el editor de temas.
- TRAMPA: themeFilesUpsert rechaza index.json si hay una sección cuyo archivo no existe.
