# UcuTeria

Pagina web para una cafeteria

## Objetivo

Objetivo

Construir una página donde el usuario:

Explora un menú de cafetería

Filtra/busca productos,

Agrega ítems a un carrito

Ve el total (con impuestos y cupones)

Completa un formulario de checkout (sin enviar)

Puede recuperar su carrito al recargar la página.

## Requisitos funcionales

Ver el menú

Como usuario, quiero ver tarjetas de productos con nombre, precio, categoría (Café, Té, Pastelería, Sándwiches) y una imagen/emoji.
Filtrado y búsqueda

●	Filtrar por categoría con botones/checkbox.

●	Buscar por texto (nombre o descripción) con input instantáneo (oninput).

Ordenar

●	Orden asc/desc por precio o alfabéticamente (select).

Agregar/Quitar

Cada tarjeta tiene “Agregar”. El carrito muestra cantidad por ítem, subtotal por ítem y Total general.

Se puede incrementar/decrementar cantidad desde el carrito y vaciar todo.

Cupones

Campo “Cupón” que acepte:

DESC10 → 10% sobre subtotal
Impuestos y envío

●	IVA 22% (uruguayo) calculado sobre el subtotal luego del cupón.

●	Envío: $0 si el subtotal ≥ $600; si no, $120 fijo.

●	Formulario de checkout (no se envía)

●	Nombre, Email, Teléfono, Dirección, Método de pago (radio), Acepto términos (checkbox).

●	Validación en cliente: campos obligatorios, email con patrón, teléfono numérico. Si todo ok, mostrar modal/alert “¡Pedido confirmado!” y vaciar carrito.

Persistencia

●	El carrito y el cupón aplicado se guardan en localStorage y se restauran al recargar.

Accesibilidad

●	Etiquetas <label> vinculadas, contraste suficiente, alt en imágenes, etc
Dark/Light mode

●	Toggle que cambia variables CSS (colores) y persiste la preferencia en localStorage.


## Requisitos de diseño responsivo

Mobile-first.

Breakpoints sugeridos:

<= 480px: 1 columna de tarjetas.

481–768px: 2 columnas.

●	>= 769px: 3–4 columnas.

●	El carrito en mobile se presenta como panel deslizable (off-canvas) o sección colapsable.

●	Usar Flex/Grid y media queries; evitar medidas fijas donde no sea necesario.

## Catálogo

A modo de ejemplo, pueden usar la siguiente colección:

export const PRODUCTS = [
  { id: "c1", name: "Espresso",      price: 120, category: "Café",       img: "☕️", desc: "Corto e intenso." },
  { id: "c2", name: "Latte",         price: 180, category: "Café",       img: "🥛☕️", desc: "Con leche espumada." },
  { id: "t1", name: "Té Verde",      price: 140, category: "Té",         img: "🍵", desc: "Suave y herbal." },
  { id: "t2", name: "Té Chai",       price: 160, category: "Té",         img: "🫖", desc: "Especias aromáticas." },
  { id: "p1", name: "Medialuna",     price: 90,  category: "Pastelería", img: "🥐", desc: "Mantecosas y doradas." },
  { id: "p2", name: "Torta Choc",    price: 220, category: "Pastelería", img: "🍰", desc: "Fudge intenso." },
  { id: "s1", name: "Sándwich Jamón",price: 260, category: "Sándwiches", img: "🥪", desc: "Clásico de la casa." },
  { id: "s2", name: "Veggie Grill",  price: 280, category: "Sándwiches", img: "🥗", desc: "Verduras asadas." }
];
