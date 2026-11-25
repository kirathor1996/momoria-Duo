# Marca del producto de mapas de inglés: MAPLISH (2026-11-25)

El usuario definió que la marca de los 300 mapas de inglés es **MAPLISH** (antes "INGLÉS ORDENADO", nombre provisorio, ya no va).
Ya aplicada en: marca de agua de los videos, pack, tapas y pie de cada mapa, y nombres de los PDF.
Detalle técnico en Desktop/video para mapas de ingles/VIDEOS_NUESTROS/LEEME.md.

## Página de Facebook (2026-11-25)
- Creada desde el Facebook de Agustina: https://www.facebook.com/profile.php?id=61596679392923 — categoría Educación, tipo Empresa, correo cargado maplish.ofical@gmail.com (SIN la i, mal: el real es maplish.oficial@gmail.com; pendiente corregir), con logo, portada y presentación.
- WhatsApp no conectado e invitaciones a amigos no enviadas (a decidir por el usuario).
- Logo/portada: Desktop/video para mapas de ingles/FACEBOOK_MAPLISH (crear_fb.py).
- Navegador usado: Chrome visible en puerto 9445, perfil herramientas/chrome-maplish (sesión de Agustina). Helper CDP: herramientas/cdp/cdp.mjs (node). Subir archivos: Page.setInterceptFileChooserDialog + click + DOM.setFileInputFiles con ruta con barras "/" (con "\" falla).

## Píxel en Impultienda (2026-11-25)
- thestoicpath.impultienda.ar tiene DOS píxeles (Configuración > Meta / Tracking): el estoico 2281492459348205 (no tocar, lo usan las campañas estoicas) + el de Agustina 920973110537874 ("Lacocinadealba", portfolio "La cocina de alba" 4377696989216783), cada uno con su token CAPI. Verificado: ambos disparan PageView e InitiateCheckout.
- Cuenta publicitaria de Agustina 1596834421363646 se llama "La Cocina De Alba".
- Pendiente: Meta bloquea sumar la página Maplish al portfolio y ver activos del píxel hasta que Agustina verifique identidad (login Microsoft con su hotmail) en el Chrome del puerto 9445.
- (2026-11-25) Mercado Pago conectado en thestoicpath.impultienda.ar con la cuenta MP de Agustina Luna Suarez (seller 252085739). Modo Multidivisa: argentinos ven ARS y MP primero; resto, Impul Pay. Verificado en el checkout.

## Drive de entrega (2026-11-25)
- Producto subido al Drive de maplish.oficial@gmail.com (con "i"): carpeta "MAPLISH - 300 mapas de inglés (A1 a C2)" https://drive.google.com/drive/folders/1EW3obpSOkGHqfyqKA-_q1F5KNJ4-_dum (pública, lector). Subcarpetas "1 - Mapas en PDF" (6 PDF) y "2 - Audios" (16 zip). Este es el link para Impultienda.
- La copia anterior (folders/1T_oohijEv6rjwP0j4heR_Y1p48bhjfSJ) quedó en el Drive personal del usuario: no usarla.
- TRAMPA CDP: en el Chrome 9445 hay 2 pestañas de Drive (una es la carpeta compartida The Stoic Path). cdp.mjs elige la primera que matchea: usar un patrón de URL exacto.
