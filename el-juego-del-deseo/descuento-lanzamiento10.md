# App en Shopify (tienda k01cpa-0y): estado actual = versión EE. UU. (inglés) de prueba (2026-11-26)

- Historial: prueba AR (SINLIMITES, $26.990/$39.990) aprobada y borrada; versión alemana ("Spiel der Begierde Grenzenlos", código GRENZENLOS) cargada y BORRADA el 26-11 para probar la de EE. UU.
- Ahora cargado (inglés): producto "The Desire Games No Limits" (handle the-desire-games-no-limits, vendor The Desire Games, id 15484815212717), 26.90 / comparación 35.90, digital, solo Tienda online, portada en inglés, descripción en inglés. Código NOLIMITS: 10 % solo ese producto, un uso por cliente, no combinable, se escribe en el checkout.
- Moneda de la tienda: USD.
- Sección sections/jdd-nueva-coleccion.liquid en la home debajo de "Banner Hero" (key jdd_nueva_coleccion). Archivos locales en "propuesta web app": jdd-nueva-coleccion.liquid (ES), -alemania-de.liquid (DE), -eeuu-en.liquid (EN). Respaldos de la home: backup-index-antes-de-seccion-2026-11-26.json y backup-index-version-alemana-2026-11-26.json.
- Portadas en "portada producto app": portada-1x1-v1.png (ES), -alemania-de.png, -eeuu-en.png. Scripts scripts/portada_producto(_de|_en).py; capturas traducidas en %TEMP%\apptest\hd_de / hd_en (textos reemplazados en el DOM con hd_de.json / hd_en.json vía run3.mjs). OJO: la app real sigue en español.
- Para recargar la versión alemana: payloads en %TEMP%\cdpjdd q21-q24 (cambiar el título a "Spiel der Begierde Grenzenlos").
- Cómo se hizo: GraphQL del admin desde la pestaña logueada del Chrome 9445 (fetch a /api/shopify/k01cpa-0y?operation=X con el x-csrf-token del HTML). Scripts en %TEMP%\cdpjdd. Subida de imagen: stagedUploadsCreate + curl --form-string. La tienda tiene contraseña: para ver la home, usar el editor de temas.
- TRAMPA: themeFilesUpsert rechaza index.json si alguna sección apunta a un archivo que no existe.
