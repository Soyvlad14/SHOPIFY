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

## Qué cambió

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
