# App en Shopify (tienda k01cpa-0y): estado actual = versión ALEMANA de prueba (2026-11-26)

- Prueba AR (producto "El Juego del Deseo Sin Límites" $26.990/$39.990 + código SINLIMITES) se hizo, el usuario la aprobó y se BORRÓ.
- Ahora cargado (alemán): producto "El Juego del Deseo – Grenzenlos (App 18+)" (handle el-juego-del-deseo-grenzenlos, id 15484802957485), 26.90 / comparación 35.90, digital, solo Tienda online, portada alemana. Código GRENZENLOS: 10 % solo ese producto, un uso por cliente, no combinable, se escribe en el checkout.
- Moneda de la tienda: USD (el bloque muestra $26.90, no €).
- Sección sections/jdd-nueva-coleccion.liquid en la home debajo de "Banner Hero" (key jdd_nueva_coleccion), ahora con textos en alemán. Archivos locales en "propuesta web app": jdd-nueva-coleccion.liquid (ES) y jdd-nueva-coleccion-alemania-de.liquid (DE). Respaldo de la home: backup-index-antes-de-seccion-2026-11-26.json.
- Portada DE: "portada producto app\portada-1x1-alemania-de.png", con el script scripts/portada_producto_de.py y las capturas en alemán de %TEMP%\apptest\hd_de (textos de la app reemplazados en el DOM con de_tr.js, hd_de.json). OJO: la app real sigue en español.
- Cómo se hizo: GraphQL del admin desde la pestaña logueada del Chrome 9445 (fetch a /api/shopify/k01cpa-0y?operation=X con el x-csrf-token del HTML). Scripts en %TEMP%\cdpjdd. La tienda tiene contraseña: para ver la home, usar el editor de temas.
- TRAMPA: themeFilesUpsert rechaza index.json si alguna sección apunta a un archivo que no existe.
