# Spect - Carrito y Checkout de VELUNE

## Objetivo

Definir el prototipo de las vistas Carrito (`carrito.html`) y Checkout (`checkout.html`) de VELUNE, con una estructura semántica, accesible y responsive que muestre el cierre de la compra de forma clara y coherente con la identidad visual de la marca.

Ambas vistas son estáticas: presentan un pedido de ejemplo y no procesan compras reales.

## Usuarios

- Clientes que quieren revisar los productos elegidos, sus tallas, cantidades y el total antes de comprar.
- Clientes que quieren indicar sus datos de contacto, envío y método de pago para completar el pedido.

## Identidad de marca aplicada

- Dirección visual editorial, sobria y sofisticada, en línea con Home, catálogo y producto.
- Paleta principal: negro carbón `#171315`, rojo burdeos `#8F243C`, marfil `#F1E9E2` y gris seda `#D7C8BC`.
- Tratamiento cromático: `header` y `footer` con fondo `#D7C8BC` y texto `#8F243C`; `body` con fondo `#F1E9E2`, títulos `#8F243C` y párrafos `#171315`.
- Títulos con fuente serif y etiquetas pequeñas en mayúsculas, como en las vistas existentes.
- Formularios sobrios, con bordes finos y sin esquinas redondeadas, siguiendo los campos de la vista de producto.
- Se evitará una apariencia prediseñada de tienda genérica o de contraste blanco/negro.

## Historias de usuario

- Como cliente, quiero ver los productos de mi carrito con su imagen, nombre, talla, cantidad y precio.
- Como cliente, quiero conocer el subtotal, el envío y el total antes de continuar.
- Como cliente, quiero pasar del carrito al checkout o volver al catálogo para seguir comprando.
- Como cliente, quiero introducir mis datos de contacto y de envío en un formulario claro.
- Como cliente, quiero elegir un método de pago y revisar el resumen de mi pedido antes de confirmarlo.
- Como cliente, quiero saber que este prototipo no realiza compras reales.

## Pedido de ejemplo

Las dos vistas muestran el mismo pedido. Los precios son ilustrativos y coinciden con los del catálogo.

| Producto | Talla | Cantidad | Precio unitario | Importe |
| --- | --- | --- | --- | --- |
| Vestido Camille | M | 1 | 189,00 € | 189,00 € |
| Pantalón Juliette | S | 2 | 145,00 € | 290,00 € |

| Concepto | Valor |
| --- | --- |
| Subtotal | 479,00 € |
| Envío estándar | Gratuito |
| Total (IVA incluido) | 479,00 € |

## Requisitos funcionales

### Comunes

- Las páginas deben usar HTML semántico, con un único `h1`, encabezados en orden y un enlace "Saltar al contenido".
- Deben incluir el `header` y el `footer` reutilizables, con el contenido definido en `Spect-Home.md`.
- El contador del menú debe mostrar `Carrito (3)` y describir "3 artículos" a lectores de pantalla, para coincidir con el pedido de ejemplo.
- Las páginas deben incluir `<meta name="robots" content="noindex">`, porque carrito y checkout no son contenido para buscadores.
- Los productos deben marcarse con Schema.org (`Product` y `Offer`, con `price` y `priceCurrency` en EUR).
- Los importes deben mostrarse en formato europeo (`189,00 €`) y usar `<data value="189.00">` para el valor legible por máquina.
- El layout debe adaptarse a móvil, tablet y escritorio usando CSS con Tailwind.
- No se utilizará JavaScript.
- No se mostrarán controles que parezcan funcionar sin hacerlo. Las acciones no disponibles irán deshabilitadas, con un aviso visible.

### Carrito (`carrito.html`)

- Debe tener un título "Carrito" y el número de artículos.
- Debe existir una lista de productos con imagen, nombre, talla, cantidad, precio unitario e importe.
- La talla y la cantidad se mostrarán como texto, porque editarlas requiere lógica que este prototipo no tiene.
- Debe existir un resumen con subtotal, envío y total.
- Debe existir un enlace principal "Finalizar compra" hacia `checkout.html`.
- Debe existir un enlace secundario "Seguir comprando" hacia el catálogo.

### Checkout (`checkout.html`)

- Debe tener un título "Checkout" y un enlace "Volver al carrito".
- Debe existir un `form` con tres grupos, cada uno en un `fieldset` con `legend`:
  - Contacto: correo electrónico y teléfono.
  - Envío: nombre, apellidos, dirección, código postal, ciudad y país.
  - Pago: selección de método entre tarjeta, PayPal y transferencia, mediante `radio`.
- Cada campo debe tener un `label` visible y los atributos `type`, `name`, `required` y `autocomplete` que correspondan.
- No se incluirán campos de número de tarjeta, caducidad ni CVV, para que el prototipo no solicite datos de pago.
- Debe existir un resumen del pedido con productos, cantidades, subtotal, envío y total.
- Debe existir un botón "Confirmar pedido" deshabilitado, acompañado de un aviso visible: "Este prototipo no procesa pedidos ni pagos."
- Deben mostrarse enlaces a términos y condiciones y a política de privacidad.

### Responsive

- En móvil y tablet, las vistas se presentan en una columna y el resumen aparece después de los productos o del formulario.
- En escritorio, se presentan en dos columnas: contenido principal a la izquierda y resumen a la derecha.
- La página no debe tener desplazamiento horizontal en ningún ancho.

## Criterios de aceptación

1. `carrito.html` muestra los dos productos del pedido de ejemplo con imagen, nombre, talla, cantidad, precio unitario e importe.
2. El resumen del carrito muestra subtotal, envío y total, y los importes coinciden con el pedido de ejemplo.
3. Desde el carrito se puede ir a `checkout.html` y al catálogo; desde el checkout se puede volver al carrito.
4. `checkout.html` incluye contacto, envío y pago en grupos `fieldset` con `legend`, y todos los campos tienen `label`.
5. El checkout no solicita número de tarjeta, caducidad ni CVV.
6. "Confirmar pedido" está deshabilitado y un aviso visible explica que el prototipo no procesa pedidos ni pagos.
7. Ambas vistas incluyen `header` y `footer` coherentes con el resto del sitio, y el menú muestra `Carrito (3)`.
8. Ambas vistas mantienen legibilidad, jerarquía y navegación en móvil, tablet y escritorio, sin desplazamiento horizontal.
9. La navegación por teclado alcanza todos los enlaces y campos, con foco visible.
10. Los colores cumplen lo definido en la identidad de marca, y las vistas funcionan sin JavaScript.

## Fuera de alcance

- Pagos, creación de pedidos, gestión real del carrito o backend.
- Agregar, editar o eliminar productos, y recalcular totales.
- Códigos de descuento, opciones de envío, impuestos por país y gastos de envío reales.
- Autenticación y compra con cuenta de usuario.
- Vistas de carrito vacío, pedido confirmado y errores de pago.
- Textos legales definitivos, precios, inventario y datos reales de contacto.

## Decisiones pendientes del equipo

- Nombre del catálogo: los enlaces de Home y producto apuntan a `catalogo.html`, pero el archivo se llama `catalog.html`. Estas vistas enlazarán a `catalog.html` hasta que el equipo lo unifique.
- Header y footer: Home usa una inclusión del lado del servidor, mientras que catálogo y producto los copian en cada página. Estas vistas los copiarán, porque así funcionan al abrir el archivo directamente.
- Enlace de entrada: "Agregar al carrito" sigue deshabilitado en `product.html`. Hay que acordar si pasa a ser un enlace a `carrito.html` para completar el recorrido del prototipo.
