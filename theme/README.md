# Cambios de diseño — Product Page + Carrito

Este repositorio no tenía archivos del tema; el tema Shopify (Horizon) se edita
directamente en la tienda vía Admin API. Estos archivos son un espejo, para
historial en git, de los cambios aplicados a la tienda **Paulina Montiel**
(zv001c-im.myshopify.com).

Los cambios se publicaron en un **tema borrador** (no en el tema principal),
para poder revisarlos antes de que queden visibles a los clientes:

- Tema borrador: `Paulina Montiel - Diseño Product Page + Carrito`
- Vista previa: https://paulinamontiel.com/products/laia?preview_theme_id=156093219002
- Editor: https://zv001c-im.myshopify.com/admin/themes/156093219002/editor

## Archivos modificados

- `snippets/product-rating-line.liquid` — estrellas verdes, 4.9, línea divisoria
- `snippets/product-social-proof.liquid` — franja de confianza (DHL, devolución, familiar) + subrayado en "últimas unidades"
- `templates/product.json` — reconecta el bloque de confianza a `product-social-proof`
- `snippets/cart-drawer-topbar.liquid` — quita banner de reserva y barra de envío gratis, centra el logo
- `snippets/cart-drawer-trust.liquid` — botón de pago y garantía en tonos café de la marca

# Rediseño — Carrusel de reseñas (Home)

Duplicado del tema en vivo (`Paulina Montiel - Diseno Product Page + Carrito`,
que era el tema `MAIN` en el momento de este cambio) para rediseñar únicamente
la sección **Carrusel de reseñas** de la página de inicio, sin tocar el tema
publicado.

- Tema borrador: `Paulina Montiel - Carrusel de Resenas Draft`
- Vista previa: https://paulinamontiel.com/?preview_theme_id=156099215546
- Editor: https://zv001c-im.myshopify.com/admin/themes/156099215546/editor

## Qué cambió (v1)

`sections/reviews-carrusel.liquid` — rediseño completo pensado para transmitir
confianza:

- Tarjetas más pequeñas y compactas (antes 260–300px de ancho, ahora 218–252px),
  con texto recortado a 4 líneas para que todas midan lo mismo.
- Estrellas en SVG doradas en vez de los cuadros negros originales — acabado
  más limpio y premium.
- Resumen de valoración rediseñado al estilo "insignia de confianza": número
  grande + estrellas + etiqueta, con un ícono de check verde junto al texto de
  reseñas verificadas.
- Insignia "Compra verificada" (chip verde) en cada tarjeta, más un avatar
  circular con la inicial de cada clienta — refuerza que son personas reales.
- Tarjetas con sombra suave en capas y borde sutil (antes sombra pesada única),
  degradados en los bordes del carrusel para insinuar que hay más contenido al
  deslizar, y una barra de scroll más discreta.
- Nuevos ajustes editables desde el editor de temas: color de acentos/estrellas
  (`accent_color`) y texto de la insignia verificada (`verified_text`). Los
  ajustes existentes (color de fondo, título, valoración, etc.) se mantienen
  intactos.
- Sigue sin JavaScript (scroll nativo con snap), igual que el original.

## Ajustes (v2), a pedido de la clienta

- **Quitado el degradado de las orillas del carrusel** (el efecto difuminado
  ya no está).
- **Todo más pequeño**: tarjetas de 190–222px (antes 218–252px), texto
  recortado a 3 líneas, tipografía y espaciados reducidos en todo el bloque.
- **Quitado el fondo café**: `bg_color` default ahora es blanco (`#FFFFFF`).
  Los textos del encabezado (título, valoración, "reseñas verificadas") ahora
  tienen colores oscuros explícitos para que se sigan viendo bien sobre
  cualquier fondo, en vez de heredar el color del tema.
- **Las 5 reseñas ahora son bloques editables** en `templates/index.json`
  (`type: review`), cada uno con: **Foto de la clienta** (`image_picker`,
  opcional), Título, Texto y Nombre. Se puede subir una foto real por reseña
  directamente desde el editor de temas — clic en la tarjeta → "Foto de la
  clienta" → Seleccionar imagen. Mientras no haya foto, se muestra un avatar
  con la inicial del nombre (como estaba). También se pueden agregar, quitar
  o reordenar reseñas como cualquier otro bloque.
- La clienta ya subió sus propias fotos (`AVATAR_1.jpg`…`AVATAR_6.jpg`) desde
  el editor y renombró una reseña ("David L." → "Rosa L."). `templates/index.json`
  en este repo refleja ese estado más reciente.

## Ajustes (v3) — carrusel también en la página de producto

A pedido de la clienta: mismo carrusel de reseñas (con sus fotos ya subidas),
colocado en la **página de producto**, arriba del bloque "Prueba social"
(los 3 avatares + "Laura S., Marta T. y +5.748 confían en Paulina Montiel").

- `templates/product.json` — se agregó una nueva instancia de la sección
  `reviews-carrusel` (`reviews_carrusel_product_9F3xQ2`) justo después de
  `main` y antes de `social_proof_banner_TCBqXx` en el `order`. Usa los mismos
  5 bloques/fotos que la versión de la página de inicio.
- No se tocó `social-proof-banner` — sigue debajo del carrusel, tal como se
  pidió (carrusel arriba, ese abajo).
- `sections/reviews-carrusel.liquid` no cambió en esta iteración; es la misma
  sección reutilizada en dos plantillas distintas.
