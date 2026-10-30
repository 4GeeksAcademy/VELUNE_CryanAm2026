# Spect - Home de VELUNE

## Objetivo

Definir el prototipo de la página de inicio de VELUNE, marca de moda francesa, con una estructura semántica, indexable y responsive que presente campañas y productos de forma elegante y coherente con su identidad visual.

## Usuarios

- Personas interesadas en descubrir la marca, sus campañas y sus productos.
- Clientes que buscan acceder rápidamente a novedades, productos más vendidos, búsqueda, cuenta y categorías.

## Identidad de marca aplicada

- Dirección visual editorial, sobria y sofisticada, con sensación de sensualidad contenida, movimiento, tacto y misterio.
- Se evitarán plantillas o diseños prediseñados basados únicamente en contraste blanco/negro. El diseño debe ser elegante, con alto contraste controlado para resaltar la identidad visual de VELUNE.
- Paleta principal: negro carbón `#171315`, rojo burdeos `#8F243C`, marfil `#F1E9E2` y gris seda `#D7C8BC`.
- Tratamiento cromático: `header` con fondo `#D7C8BC` y texto `#8F243C`; `body` con fondo `#F1E9E2`, títulos `#8F243C` y párrafos `#171315`.
- Uso del logotipo VELUNE según la guía, con alto contraste, espacios generosos y composición limpia.
- Imágenes y textos del Home deben priorizar cortes precisos, materiales, siluetas y atmósferas; evitar una presentación estridente o saturada.

## Historias de usuario

- Como visitante, quiero identificar VELUNE y entender su campaña principal al entrar en la Home.
- Como visitante, quiero buscar productos desde la navegación principal.
- Como visitante, quiero explorar los nuevos lanzamientos y los productos más vendidos mediante listados horizontales de cards.
- Como visitante, quiero acceder a mi cuenta, al catálogo completo y al carrito desde el menú principal.
- Como visitante, quiero encontrar información legal y de contacto en el footer.

## Requisitos funcionales

- La página debe usar HTML semántico y el modelo Schema.org para representar la organización de la página, la marca y los productos mostrados.
- El `header` reutilizable debe incluir el logotipo, una barra de búsqueda y un menú con acceso a la cuenta de usuario, la tienda completa o catálogo y el carrito.
- El hero debe destacar una campaña o productos especiales con contenido textual indexable y una llamada a la acción vinculada al contenido presentado.
- Debe existir una sección titulada “Nuevos lanzamientos” con un listado horizontal de cards de producto.
- Debe existir una sección titulada “Más vendidos” con un listado horizontal de cards de producto.
- Las cards deben presentar contenido de producto legible e indexable, sin depender de JavaScript.
- El `footer` reutilizable debe incluir las categorías calzado, camisas, pantalones y accesorios; los enlaces legales términos y condiciones, política de privacidad y sobre la marca; y un bloque de contacto.
- El layout debe adaptarse a móvil, tablet y escritorio usando CSS con Tailwind.
- No se utilizará JavaScript.

## Criterios de aceptación

1. La Home presenta un `header` con logotipo, búsqueda y un menú con cuenta, Catálogo y Carrito, además de un `footer` con todas las secciones exigidas.
2. El hero comunica una campaña o selección especial con texto indexable, imagen o composición visual coherente con la identidad y una llamada a la acción.
3. Se muestran las secciones “Nuevos lanzamientos” y “Más vendidos”, ambas con cards de producto en disposición horizontal.
4. La estructura usa HTML semántico y datos Schema.org aplicables a la organización y a los productos visibles.
5. La página mantiene legibilidad, jerarquía y navegación en móvil, tablet y escritorio mediante Tailwind CSS.
6. El `header` usa fondo `#D7C8BC` y texto `#8F243C`; el `body` usa fondo `#F1E9E2`, títulos `#8F243C` y párrafos `#171315`.
7. El diseño evita una apariencia prediseñada de contraste blanco/negro, usa un contraste elegante que resalta la identidad visual de VELUNE y funciona como contenido estático sin JavaScript con contenidos principales indexables.

## Fuera de alcance

- Catálogo, vista de producto, carrito y checkout.
- Implementación de autenticación, búsqueda funcional, pagos, gestión de carrito o backend.
- JavaScript, animaciones interactivas y lógica de negocio.
- Creación o edición de fotografías, ilustraciones o piezas audiovisuales definitivas.
- Definición de campañas, precios, inventario, textos legales definitivos o datos reales de contacto.
