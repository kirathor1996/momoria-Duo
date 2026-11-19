# Objetivo de testeo (actualizado 2026-11-18)

- El producto es SOLO DIGITAL (carta personalizada en PDF).
- La tienda va en "Impul tienda" (el usuario la llama así; no la encontré en internet, falta que pase el link) y se cobra con el método de pago que trae Impul tienda. La idea es no tener que abrir una LLC en EE.UU. Mercado Pago queda para Argentina.
- Mercados: Argentina, EE.UU. y "todo lo que se pueda" de LATAM. El usuario quiere probar con una campaña de prueba en Meta con una imagen que va a pasar.
- El usuario quiere que Claude cargue las campañas "como enseña Agu Frederick" (no sé cuál es ese método; pedirle sus notas). Quiere que Claude entre a Impul tienda y a Meta y cargue todo.
- Al 2026-11-18 no hay herramientas de navegador ni de control de la PC activas en la sesión, así que Claude no puede entrar a esas cuentas. Hay que activar "Claude en Chrome" o "control del equipo" en Duo. Las contraseñas no se pasan por el chat: el usuario inicia sesión él mismo.
- Idiomas, según lo que propuse: una página en español para LATAM y los latinos de EE.UU., una en inglés para EE.UU. y, si se quiere sumar Brasil, una en portugués. Cada página tiene su versión del producto en su idioma. No conviene la traducción automática, y la VPN no traduce nada: solo sirve para ver la página como la ve alguien de otro país.

## Decisión 2026-11-18
- Dos campañas y dos páginas: ARGENTINA (index.html, en español, en pesos, con Mercado Pago, solo digital) e INGLÉS (en/index.html, "Letters from Santa", en US$, para EE.UU., Reino Unido, Canadá y Australia, cobrando con el método de Impul tienda).
- La página en inglés no tiene Reyes Magos: tiene Santa, Elf y el combo de hermanos. Las capturas están en captura-ar.png y captura-en.png.

## Cerebro "Capitan America" (curso del usuario), 2026-11-18
- Impultienda: según la clase del Módulo 4, se conecta con Mercado Pago o con Stripe, y para vender al exterior hace falta una LLC. CORRECCIÓN 2026-11-18: el usuario aclara que Impultienda permite cobrar con WHOP para vender al exterior sin LLC. Plan: Argentina con Mercado Pago y la página en inglés con Whop. La IA de Impultienda arma la página, los textos y los bonos; la entrega es automática; tiene upsells, y el upsell post-compra no está disponible con Mercado Pago de Argentina.
- La estructura de página que enseña el curso: ganchos visuales, dolores, beneficios, garantía y bonus. Ya la apliqué a las dos páginas (2026-11-18).
- Ojo: la entrega automática manda un PDF fijo, y el producto es una carta personalizada. Propuse vender una plantilla editable, donde los padres ponen el nombre.

## Imágenes (2026-11-18)
- El usuario pasó las imágenes de cartasencantadas.com (fotos de sus cartas y sus personajes: los pajes Anita, Federico, Sofía y Tomás) para ponerlas en la página. NO las usé, porque son productos y personajes de otra marca.
- Lo que propuse: generar imágenes propias con el mismo estilo general (carta sobre un escritorio de madera, velas, sello de lacre), pero con ilustraciones y personajes nuestros.
- 2026-11-18: hice imágenes propias con HTML renderizado en Edge (sin IA): la carta y el sobre sobre madera, el diploma, la portada de los cuentos y anuncios de 1080x1080 y 1080x1920, en ES y EN. Están en el proyecto, en imagenes/. Ya están puestas en impultienda/*.html con rutas ../imagenes/; al subirlas a Impultienda (Recursos) hay que cambiar esas rutas por las URL que dé Impultienda. Pendiente: el bonus "Foto mágica" es un trabajo manual y choca con la entrega automática.

## Precios y PDF (2026-11-18)
- Papá Noel y Reyes Magos salen AR$ 19.990 cada una (Reyes = upsell en el checkout). En la página, el precio de los Reyes está escrito a mano porque {{price}} solo trae el del producto principal.
- Precio tachado AR$ 29.990 (lo eligió el usuario el 2026-11-18), escrito a mano en el HTML porque {{original_price}} mostraba "AR$ 0". Los carteles dicen "33% OFF".
- Sección "¿Qué recibís exactamente?" (#contenido): mosaicos con las páginas reales de los PDF (imagenes/contenido-*.jpg, armados con PIL desde Temp/capcartas/pdf/prev) y la lista de las cartas y los cuentos.
- PDF en entregables/: pack-papa-noel.pdf, pack-reyes-magos.pdf, regalos-diploma-cuentos.pdf. Todos en español; la tienda en inglés todavía no tiene PDF.

## Estado de cobro (revisado 2026-11-19)
- Configuración → Pagos: la tienda cobra en ARS solo con Mercado Pago ("Pagos locales · solo cuentas de Argentina"). NO está lista para LATAM. Opciones del panel: USD (Stripe/PayPal), Multidivisa (Stripe internacional + MP Argentina), dLocal Go (cobros locales LATAM), Whop (tarjeta en 80+ monedas). La página está en voseo y con precios AR$ escritos a mano. Falta que el usuario elija el procesador y lo conecte.
- 2026-11-19: Whop en Impultienda = "Impul Pay" (menú Impul Pay, /dashboard/cartasnavidenas/impulpay). Se activa una vez por cuenta: el usuario acepta los términos de Whop y verifica su identidad él mismo; después se prende por tienda en Configuración → Pagos. Según el panel, Mercado Pago sigue para Argentina en pesos y Impul Pay cobra al exterior en la moneda del comprador. Pendiente: que el usuario lo active.
