# Cambios de diseño — Product Page + Carrito

Este repositorio no tenía archivos del tema; el tema Shopify (Horizon) se edita
directamente en la tienda vía Admin API. Estos archivos son un espejo, para
historial en git, de los cambios aplicados a la tienda **Paulina Montiel**
(zv001c-im.myshopify.com).

**Nota:** el tema `Paulina Montiel - Diseno Product Page + Carrito` (id 156093219002)
ya es el tema **MAIN** (publicado, en vivo).

## Tema borrador actual

Los cambios más recientes se publicaron en un **tema borrador nuevo** (no en el
tema principal), para poder revisarlos antes de que queden visibles a los clientes:

- Tema borrador: `Paulina Montiel - Ocultar Pago Express` (duplicado del tema en vivo)
- Vista previa: https://paulinamontiel.com/products/laia?preview_theme_id=156094660794
- Editor: https://zv001c-im.myshopify.com/admin/themes/156094660794/editor

### Archivos modificados en este borrador

- `sections/main-cart.liquid` — oculta los botones de pago express (Shop Pay / Apple Pay / Google Pay / PayPal) en la página de carrito (`/cart`). Antes solo estaban ocultos en el cart drawer.
- `snippets/buy-buttons-styles.liquid` — oculta el botón de pago acelerado (Shop Pay/Apple Pay/Google Pay/PayPal) en la página de producto y en el quick-add de colección, dejando solo "Agregar al carrito".

⚠️ Ojo: los datos de analytics de la tienda muestran que el cuello de botella real
está en sesión → agregar al carrito (86% del tráfico es "social"/ads y casi no
llega ni al carrito), no en el paso de pago. Ocultar los botones express reduce
opciones justo para el 91% de tráfico que es mobile, donde esos botones suelen
bajar la fricción. Vale la pena revisar esto con datos (A/B) antes de publicarlo
en el tema principal.

## Historial anterior

- Tema: `Paulina Montiel - Diseño Product Page + Carrito` (ahora MAIN)
- `snippets/product-rating-line.liquid` — estrellas verdes, 4.9, línea divisoria
- `snippets/product-social-proof.liquid` — franja de confianza (DHL, devolución, familiar) + subrayado en "últimas unidades"
- `templates/product.json` — reconecta el bloque de confianza a `product-social-proof`
- `snippets/cart-drawer-topbar.liquid` — quita banner de reserva y barra de envío gratis, centra el logo
- `snippets/cart-drawer-trust.liquid` — botón de pago y garantía en tonos café de la marca, oculta los botones de pago express y el total estimado dentro del cart drawer
