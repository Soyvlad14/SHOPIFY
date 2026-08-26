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

## Quitar logo de OXXO (tema borrador `Paulina Montiel - Quitar Logo OXXO`)

- Tema borrador: `Paulina Montiel - Quitar Logo OXXO` (id 156206825658, duplicado del tema principal)
- `snippets/pt-payment-icons.liquid` — se elimina el `<img>` del logo de OXXO; se conserva el de Mercado Pago y los íconos nativos de `shop.enabled_payment_types`
