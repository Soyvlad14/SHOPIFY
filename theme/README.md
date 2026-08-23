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

## Cambio — recuadro de envío bajo el selector de talla (agosto 2026)

El recuadro debajo del botón "Agregar al carrito" que calculaba automáticamente
"Envío [día, fecha]" (siempre 2 días después de hoy) ahora dice
**"Procesamiento de pedido [día, fecha]"**. El cálculo de fecha, la fila
"Envío Gratuito" y todo el resto del diseño quedan exactamente igual.

- `snippets/shipping-date-banner.liquid` — cambia la etiqueta "Envío" por "Procesamiento de pedido"

Publicado en un **tema borrador nuevo**, duplicado del tema principal en vivo:

- Tema borrador: `Paulina Montiel - Procesamiento de Pedido Draft`
- Vista previa: https://paulinamontiel.com/products/laia?preview_theme_id=156127985850
- Editor: https://zv001c-im.myshopify.com/admin/themes/156127985850/editor
