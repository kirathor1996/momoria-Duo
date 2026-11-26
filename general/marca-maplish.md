# Marca del producto de mapas de inglés: MAPLISH (2026-11-25)

El usuario definió que la marca de los 300 mapas de inglés es **MAPLISH** (antes "INGLÉS ORDENADO", nombre provisorio, ya no va).
Ya aplicada en: marca de agua de los videos, pack, tapas y pie de cada mapa, y nombres de los PDF.
Detalle técnico en Desktop/video para mapas de ingles/VIDEOS_NUESTROS/LEEME.md.

## Página de Facebook (2026-11-25)
- Creada desde el Facebook de Agustina: https://www.facebook.com/profile.php?id=61596679392923 — categoría Educación, tipo Empresa, correo maplish.oficial@gmail.com (corregido 2026-11-25), con logo, portada y presentación.
- WhatsApp no conectado e invitaciones a amigos no enviadas (a decidir por el usuario).
- Logo/portada: Desktop/video para mapas de ingles/FACEBOOK_MAPLISH (crear_fb.py).
- Navegador usado: Chrome visible en puerto 9445, perfil herramientas/chrome-maplish (sesión de Agustina). Helper CDP: herramientas/cdp/cdp.mjs (node). Subir archivos: Page.setInterceptFileChooserDialog + click + DOM.setFileInputFiles con ruta con barras "/" (con "\" falla).

## Píxel en Impultienda (2026-11-25)
- maplish.impultienda.ar (antes thestoicpath) tiene DOS píxeles (Configuración > Meta / Tracking): el estoico 2281492459348205 (no tocar, lo usan las campañas estoicas) + el de Agustina 920973110537874 ("Lacocinadealba", portfolio "La cocina de alba" 4377696989216783), cada uno con su token CAPI. Verificado: ambos disparan PageView e InitiateCheckout.
- Cuenta publicitaria de Agustina 1596834421363646 se llama "La Cocina De Alba".
- Pendiente: Meta bloquea sumar la página Maplish al portfolio y ver activos del píxel hasta que Agustina verifique identidad (login Microsoft con su hotmail) en el Chrome del puerto 9445.
- (2026-11-25) Mercado Pago conectado en maplish.impultienda.ar (antes thestoicpath) con la cuenta MP de Agustina Luna Suarez (seller 252085739). Modo Multidivisa: argentinos ven ARS y MP primero; resto, Impul Pay. Verificado en el checkout.

## Drive de entrega (2026-11-25)
- Producto subido al Drive de maplish.oficial@gmail.com (con "i"): carpeta "MAPLISH - 300 mapas de inglés (A1 a C2)" https://drive.google.com/drive/folders/1EW3obpSOkGHqfyqKA-_q1F5KNJ4-_dum (pública, lector). Subcarpetas "1 - Mapas en PDF" (6 PDF) y "2 - Audios" (16 zip). Este es el link para Impultienda.
- La copia anterior (folders/1T_oohijEv6rjwP0j4heR_Y1p48bhjfSJ) quedó en el Drive personal del usuario: no usarla.
- TRAMPA CDP: en el Chrome 9445 hay 2 pestañas de Drive (una es la carpeta compartida The Stoic Path). cdp.mjs elige la primera que matchea: usar un patrón de URL exacto.

## Landing en Impultienda (2026-11-25)
- La tienda maplish.impultienda.ar (antes thestoicpath) ahora vende MAPLISH (el plan Starter permite 2 tiendas y están ocupadas: esta + Cartas Navideñas). Nombre "Maplish", idioma es-AR, mail soporte maplish.oficial@gmail.com, favicon M. Subdominio sigue "thestoicpath" (sin cambiar).
- Producto principal: precio USD 11.90 / tachado 37.90 (Multidivisa → AR$ 18.946 / 60.338), link externo = Drive de maplish.oficial. Bonus estoico eliminado. Sin upsells.
- HTML de la landing: Desktop/video para mapas de ingles/LANDING_MAPLISH/landing.html (con IMG/ placeholders) y landing_final.html (con URLs cdn.impultienda.ar). Imágenes subidas en Diseño > Recursos (prefijo maplish-). Backups del HTML estoico: BACKUP_tienda_stoic_path.html y _2.html.
- TRAMPAS CDP en Impultienda: si la pestaña no está activa, Runtime/screenshot se cuelgan → curl /json/activate/<id> antes. "Eliminar" usa confirm(): sobreescribir window.confirm=()=>true. El textarea de Contenido solo toma cambios con foco + Ctrl+A + Input.insertText (no con setter). El "Contexto para la IA" tiene su propio botón "Guardar contexto".
- (2026-11-26) Tienda en modo de cobro "Pesos argentinos" (solo Argentina, el usuario testea solo en AR): precio AR$ 19.990, tachado AR$ 59.990, cargado directo en el ebook. Cobra Mercado Pago (redirección o tarjeta). Markets/Multidivisa desactivados. Si algún día se sale a otros países, hay que volver a Multidivisa y recargar precios en USD (no se convierten solos).
- (2026-11-26) Subdominio cambiado a maplish.impultienda.ar (thestoicpath.impultienda.ar ya no abre nada; dashboard: impultienda.ar/dashboard/maplish). Píxel: SOLO el de Agustina 920973110537874 con token CAPI (se quitó el estoico 2281492459348205). Garantía SACADA de la landing por pedido del usuario (no prometer garantía/devolución). Backup con garantía: LANDING_MAPLISH/landing_final_con_garantia.bak.html.
- (2026-11-26) Los 4 videos del test (C1-1, C1-2, C2-2, C3-1) están en Desktop/video para mapas de ingles/VIDEOS_NUESTROS/FINALES, con voz real de Agustina y marca MAPLISH.
- (2026-11-26) La landing final de maplish.impultienda.ar la armó el usuario, con el mismo formato que la de la competencia; no reemplazarla con la mía. Test solo en Argentina (tienda en modo Pesos argentinos, anuncios segmentados solo AR). 4 videos de gancho listos en VIDEOS_NUESTROS/FINALES (C1-1, C1-2, C2-2, C3-1).

## Campaña de test en Meta (2026-11-26)
- Cuenta de Agustina act_1596834421363646 (moneda USD, zona AR). Página Maplish para anuncios: ID 1392227443981721 (no figura en promote_pages pero Agustina tiene ADVERTISE).
- Campaña "MAPLISH | ABO testeo 4 ganchos | AR" (120250347376630491), PAUSADA: 4 conjuntos ABO de USD 5/día (regla del usuario: 1 conjunto por video, USD 5 c/u) (compra, píxel 920973110537874, AR, Advantage+ 18-65), uno por gancho. 4 creativos de video creados (1157493276997362, 3079112029095961, 1139037442347931, 4385108108293411).
- (2026-11-26) Medio de pago cargado; 4 anuncios creados PAUSADOS, uno por conjunto (IDs 120250347553880491, 120250347554610491, 120250347555960491, 120250347556700491). Inicio del calendario: 26/11 09:09 (se ofreció reprogramar a 7 am del día siguiente). Pendiente: el usuario revisa y prende.
- Truco: la API se usa desde la pestaña de Ads Manager con el token EAA del HTML, contra adsmanager-graph.facebook.com con credentials:'include' (graph.facebook.com da "Invalid request"). Videos: input file + DOM.setFileInputFiles + FormData a /advideos.
- OJO: en la cuenta hay 3 borradores viejos ("Revisar y publicar (3)", ej. "conjunto 1" de ABO testeo): no tocar ese botón sin revisar.
- (2026-11-26) Campaña REHECHA con identidad @maplishoficial (IG 17841476193328034, vinculado a la página Maplish). Vieja 120250347376630491 = ELIMINADA. Nueva: 120250348029710491 "MAPLISH | ABO testeo 4 ganchos | AR", 4 conjuntos USD 5/día (1 video c/u), todo PAUSADO. Script: herramientas/cdp/rehacer.js. Ojo: DELETE por Graph no borra; usar POST status=DELETED. Solo La Cocina De Alba tiene el IG; las otras 4 cuentas no.
- (2026-11-26) Instagram @maplishoficial: 6 carruseles publicados (imágenes y textos en Escritorio/video para mapas de ingles/INSTAGRAM_MAPLISH). TRAMPA: la API (token de Ads Manager) no tiene permiso para publicar en IG (#10); se publica por la web de IG con CDP 9445: herramientas/cdp/igpost.js (IGN=n), recorte 4:5 obligatorio (por defecto corta 1:1). Fijar publicaciones no está en la web, solo en la app.
- (2026-11-26) Conjuntos rehechos con inicio 27/11 00:00 (AR), mismos creativos con IG; los anteriores ELIMINADOS. TRAMPA: start_time no se puede editar si ya pasó; poner la fecha AL CREAR el conjunto.
- (2026-11-26) Pie de la landing: íconos Instagram (@maplishoficial), Facebook (página Maplish) y mail, en círculos azules (mismo bloque .soc que la landing estoica). Backup previo: LANDING_MAPLISH/landing_usuario_antes_iconos.bak.html. Editor: impultienda.ar/dashboard/maplish/personalizacion/diseno/contenido → textarea + "Guardar cambios".
