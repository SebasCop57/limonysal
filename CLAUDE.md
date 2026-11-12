# Web de Limón y Sal

Web del restaurante **Limón y Sal** (pescados y mariscos, Villa El Salvador, Lima, Perú).
Todo el sitio es un solo archivo: `index.html` (HTML + CSS + JavaScript, sin frameworks ni paso de compilación).
Se publica en Netlify, conectado a este repositorio de GitHub: cada `git push` a la rama principal actualiza la web en 1–2 minutos.

## Publicación
- Repositorio GitHub: https://github.com/SebasCop57/limonysal (rama `main`)
- Proyecto de Netlify: `limonysal-ves` (el nombre `limonysal` estaba ocupado)
- Web pública: https://limonysal-ves.netlify.app

## Datos del negocio
- Teléfono / WhatsApp de pedidos: 924 879 011 (en el código: `51924879011`)
- Dirección: Calle Villa del Mar con Av. Revolución, Sector 2, Grupo 12, Mz. A, Lt. 09, Villa El Salvador, Lima
- Horario: lunes a domingo, 10:00 a.m. – 5:30 p.m. Miércoles cerrado.
- Delivery: Villa El Salvador y zonas aledañas; costo aparte según distancia, se confirma por WhatsApp.
- Métodos de pago: Yape, Plin, efectivo y tarjeta (Visa, Mastercard).
- Buzón de sugerencias (Google Forms): https://forms.gle/dCYmFCPFaUrjuMTC7

## Dónde está cada cosa en index.html
- **Carta (platos y precios):** constante `MENU` en el `<script>`. Cada categoría tiene `items` con el formato `["Nombre", precio, "nota opcional"]`. Para cambiar un precio o agregar/quitar un plato, edita solo esa lista; la carta, el buscador y el pedido se generan solos.
- **Horario y aviso "Abierto/Cerrado":** constantes `OPEN_MIN`, `CLOSE_MIN` y `CLOSED_DAY` (0 = domingo … 3 = miércoles) en el bloque "Horario". Usa la hora de Lima. Si cambia el horario, actualiza también el texto de la sección de contacto.
- **Portada de carta cerrada:** elemento `#cover` y el bloque JS "Portada de carta cerrada". Se muestra una vez por visita (sessionStorage).
- **Pedido por WhatsApp:** función `buildLink()` arma el mensaje (platos, total, tipo, nombre, dirección, pago, nota).
- **Imágenes:** logo, ceviche y arroz están embebidos como `data:` URIs en base64 dentro del HTML.

## Estilo (respetar siempre)
- Colores: verde lima `#84B12E` (oscuro `#5E8A17`), azul marino `#1E3557`, celeste acuarela `#BFDCEA` / `#6FA9C6`, fondo blanco.
- Tipografías: Montserrat (títulos, con letras espaciadas) y Nunito Sans (texto).
- Títulos de sección en verde, en mayúsculas, subrayados. Estilo inspirado en la carta impresa de Canva.
- Debe verse bien en celular (la mayoría de clientes entra desde el teléfono).

## Reglas de trabajo
- Escribe y explica en español.
- No uses logos oficiales de marcas (Yape, Plin, Visa, etc.) dibujados o descargados; solo archivos que el dueño entregue.
- Después de cada cambio: revisa que el JavaScript no tenga errores, haz commit con un mensaje claro en español y `git push`.
