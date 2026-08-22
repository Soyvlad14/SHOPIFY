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

## Rediseño de Home estilo ELARA (2026-08-22)

Réplica del diseño de la página de inicio de https://elarashowroom.com/ adaptada a
los productos y la campaña actual de la tienda (cierre por liquidación), en un
**tema borrador** para revisar antes de publicar:

- Tema borrador: `Paulina Montiel - Home Estilo Elara`
- Vista previa: https://paulinamontiel.com/?preview_theme_id=156098625722
- Editor: https://zv001c-im.myshopify.com/admin/themes/156098625722/editor

Se conservó la carta de despedida de Paulina y el framing de liquidación
(decisión del cliente) como hero/pull-quote, y se aplicó encima la estructura y
paleta cálida (crema/café) de Élara:

### Archivos nuevos/modificados

- `config/settings_data.json` — paleta de color cambiada a tonos crema (`#FFFDF8`) /
  café (`#6B4A3A`, `#2C211D`, `#E8D9C8`) en vez de blanco/negro.
- `sections/countdown-bar.liquid` — nueva barra de cuenta regresiva diaria
  (estilo Élara) con el mensaje de liquidación.
- `templates/index.json` — reordena y reconfigura la home:
  1. Barra de cuenta regresiva (nueva)
  2. Hero "Liquidación por cierre" (existente, sin cambios)
  3. Carta de despedida de Paulina (existente, sin cambios)
  4. Carrusel "Tendencias 2026" — antes desactivado, ahora activo con la
     colección Vestidos
  5. Grid de colecciones "Nuestras colecciones más destacadas" — Vestidos,
     Conjuntos y Enterizos, Calzado, Ropa de Hombre
  6. Carrusel "También podría interesarte" — colección Liquidación final
  7. Banner de confianza (existente, sin cambios)
  8. Carrusel de reseñas (existente, retitulado "Reseñas verificadas")

Pendiente de revisión del cliente antes de publicar como tema principal.
