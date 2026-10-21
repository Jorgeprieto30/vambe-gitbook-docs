# Cómo conectar tu tienda PrestaShop con Vambe

Al conectar tu tienda **PrestaShop** con Vambe, tu asistente de IA trabaja con la información real de tu tienda: tu catálogo, tus precios, tu stock y los pedidos de tus clientes. Así puede recomendar productos, cerrar ventas y responder por el estado de los pedidos por WhatsApp, sin que tu equipo tenga que copiar datos ni actualizar nada a mano cuando cambia un precio.

La conexión se hace una sola vez, toma unos minutos y se realiza con un módulo de Vambe que se instala en tu tienda. En este artículo verás qué puede hacer tu asistente con PrestaShop, qué información utiliza y cómo conectar tu tienda paso a paso.

> Para entrar: en Vambe, ve a **Configuración**, luego a **Integraciones** y selecciona **PrestaShop**.

***

## Qué puede hacer tu asistente con tu tienda

Con tu tienda conectada, el asistente de IA cuenta con estas capacidades:

* **Recomendar y vender productos**: busca en tu catálogo y responde con el nombre, la variante, la foto, el precio vigente (con impuestos y descuentos), el stock y el link al producto.
* **Enviar links de checkout**: comparte un link que abre el checkout de tu tienda con los productos, las variantes y las cantidades conversadas ya cargados. El cliente solo tiene que pagar.
* **Revisar el stock en tiempo real**: antes de armar un link consulta el stock real. Si piden más unidades de las disponibles, ajusta la cantidad; si un producto se agotó, lo deja fuera y se lo explica al cliente.
* **Informar el estado de un pedido**: con el número o la referencia del pedido, consulta tu tienda en ese momento y le indica al comprador si está pagado, en camino, entregado o cancelado.
* **Medir las ventas del asistente**: cada pedido que nace de un link de Vambe queda asociado a la conversación que lo originó, para que sepas qué ventas generó tu asistente.
* **Recuperar carritos abandonados**: detecta los carritos que quedaron sin comprar y le escribe al cliente por WhatsApp con un link que le rearma el carrito. Esta capacidad se activa de forma opcional.

***

## Qué información utiliza Vambe

Vambe lee la información de tu tienda para que el asistente responda siempre con datos actualizados:

| Información          | Qué incluye                                                                                                                                                                | Cuándo se actualiza                                |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| Productos            | Nombre, descripción, variantes (tallas, colores, etc.), precio final como lo ve un visitante, imágenes y link al producto. Solo productos activos.                         | Todos los días, y cuando lo solicites              |
| Stock                | Unidades disponibles de cada producto y variante.                                                                                                                          | En tiempo real, al momento de la consulta          |
| Pedidos              | Número, referencia, fecha, productos, total, estado, dirección de envío y datos de contacto del cliente. Solo pedidos pagados; al conectar se importan los del último año. | Al instante, cada vez que entra o cambia un pedido |
| Estado de un pedido  | Lo que ves en tu panel para ese pedido.                                                                                                                                    | En tiempo real, cuando el cliente pregunta         |
| Carritos abandonados | Productos del carrito, nombre y teléfono del cliente, y el link para retomar la compra.                                                                                    | Cada hora, solo si activas la recuperación         |

### Qué cambia en tu tienda

Vambe accede a tu tienda en modo de **solo lectura**: nunca modifica tus productos, precios, stock, pedidos ni clientes, y el pago se completa siempre en tu checkout. Lo único que interviene es el módulo de Vambe (**Batch Cart**): cuando un cliente abre un link de Vambe, el módulo le arma el carrito en su navegador y registra de qué conversación vino. Al conectar, Vambe deja configurado el módulo automáticamente, por lo que no necesitas ajustar nada en él.

***

## Conecta tu tienda paso a paso

{% hint style="info" %}
**Antes de comenzar**

* Necesitas acceso al panel de administración de tu tienda PrestaShop y a tu cuenta de Vambe.
* La integración funciona con PrestaShop 1.7 y versiones superiores, incluida la versión 8.
* Vambe nunca te pedirá tu usuario ni tu contraseña de administrador.
{% endhint %}

{% stepper %}
{% step %}
### Instala el módulo de Vambe

1. En Vambe, ve a **Configuración → Integraciones → PrestaShop** y descarga el **Módulo de Vambe para PrestaShop** (`batchcart.zip`).
2. En tu tienda, ve a **Módulos → Gestor de módulos → Subir un módulo** y selecciona ese archivo.

{% hint style="info" %}
Si ya tenías instalada una versión anterior del módulo en **PrestaShop 1.7**, después de subir el archivo busca **Batch Cart** en la lista de módulos y haz clic en **Actualizar**. En PrestaShop 8 este paso no es necesario.
{% endhint %}
{% endstep %}

{% step %}
### Activa el webservice y crea la clave

1. En tu tienda, ve a **Parámetros avanzados → Webservice**, deja **Activar el webservice de PrestaShop** en **Sí** y guarda.
2. Haz clic en **Añadir nueva clave** y luego en **Generar**. Escribe `Vambe` en la descripción y deja el estado en **Sí**.
3. Marca los siguientes permisos en la tabla, haz clic en **Guardar** y copia la clave:

| Recursos                                                                                                                       | Permiso         | Para qué                       |
| ------------------------------------------------------------------------------------------------------------------------------ | --------------- | ------------------------------ |
| `products`, `combinations`, `product_option_values`, `product_options`, `categories`, `tags`, `image_types`, `specific_prices` | Ver (GET)       | Catálogo y precios             |
| `configurations`, `currencies`, `groups`, `tax_rules`, `tax_rule_groups`, `taxes`                                              | Ver (GET)       | Monedas e impuestos            |
| `stock_availables`                                                                                                             | Ver (GET)       | Stock                          |
| `orders`, `order_states`, `customers`, `addresses`, `countries`                                                                | Ver (GET)       | Pedidos                        |
| `batchcart_attributions`                                                                                                       | Ver (GET)       | Medir las ventas del asistente |
| `batchcart_abandoned_carts`                                                                                                    | Ver (GET)       | Recuperar carritos abandonados |
| `batchcart_webhook`                                                                                                            | Modificar (PUT) | Recibir avisos de pedidos      |

{% hint style="warning" %}
Los tres recursos `batchcart_…` aparecen después de instalar el módulo del paso anterior. Si vas a recuperar carritos, no olvides marcar `batchcart_abandoned_carts`: sin ese permiso la tienda se conecta igual, pero Vambe no puede ver los carritos. Trata la clave como una contraseña.
{% endhint %}
{% endstep %}

{% step %}
### Conecta tu tienda en Vambe

En la misma pantalla de PrestaShop en Vambe, completa estos dos campos y haz clic en **Conectar**:

* **URL de la tienda**: la dirección de tu tienda con `https://`, por ejemplo `https://mitienda.cl`.
* **Clave del Webservice**: la clave de 32 caracteres que copiaste en el paso anterior.

Tu tienda aparecerá en **Conectados** y la sincronización del catálogo comenzará automáticamente. Cuando termine, se importarán tus pedidos. Si a la clave le falta algún permiso, la pantalla te indicará cuáles.

{% hint style="info" %}
**Si aparece el mensaje «Tu servidor no le está entregando la clave a PrestaShop»:** ocurre con algunos proveedores de hosting. Ve a **Parámetros avanzados → Webservice**, deja **Activar modo CGI para PHP** en **Sí** y guarda. Luego entra a **Parámetros de la tienda → Tráfico y SEO**, haz clic en **Guardar** sin cambiar nada y vuelve a conectar.
{% endhint %}
{% endstep %}

{% step %}
### Activa la recuperación de carritos (opcional)

Ve a **Ecommerce → Recuperación de carritos**, elige tu tienda PrestaShop, crea el flujo y actívalo.

Desde ese momento, Vambe revisa cada hora los carritos abandonados y le escribe al cliente entre una y tres horas después de que dejó su carrito. Si compra desde el link, la venta queda marcada como recuperada. Si apagas el flujo, Vambe deja de revisarlos.

Para personalizar las plantillas, los reintentos y las condiciones de envío, revisa [Recuperación de carrito abandonado: configura tu flujo desde Vambe](../parte-3-automatizaciones/recuperacion-de-carrito-abandonado-configura-tu-flujo-desde-vambe.md).
{% endstep %}
{% endstepper %}

***

## Seguridad de tu información

La conexión está diseñada para que mantengas siempre el control sobre los datos de tu tienda:

* **Tu clave está cifrada.** Vambe la guarda encriptada y solo tiene los permisos que marcaste. Puedes cambiarlos cuando quieras sin generar una clave nueva.
* **Los avisos de pedidos están protegidos.** Cada aviso viaja con una clave secreta propia de tu tienda, y Vambe vuelve a leer el pedido directamente desde ella.
* **Puedes cortar el acceso cuando quieras.** Desde **Parámetros avanzados → Webservice**, desactiva o elimina la clave de Vambe. El corte es inmediato.
* **Tus datos son solo tuyos.** Ningún otro cliente de Vambe puede ver la información de tu tienda.

***

## Consideraciones de la integración

Ten en cuenta el alcance de la integración al planificar la atención de tus clientes:

* **Precios**: el asistente muestra el precio que ve un visitante de tu tienda. Los precios para clientes con sesión iniciada, por cantidad o por región pueden ser distintos.
* **Stock**: el asistente utiliza el stock total de cada producto, no el stock por sucursal.
* **Devoluciones y reembolsos**: se siguen gestionando desde tu tienda.
* **Carritos sin teléfono**: no se pueden recuperar, porque no hay un número al cual escribir.
* **Avisos de pedidos**: si tu servidor no logra enviar un aviso, por ejemplo por una caída momentánea, ese pedido no llega a Vambe. El error queda registrado en **Parámetros avanzados → Registros** de tu tienda.

***

## Preguntas frecuentes

<details>

<summary>¿Tengo que instalar algo en mi PrestaShop?</summary>

Sí, el módulo de Vambe (**Batch Cart**). Es liviano, no cambia tu tema y no modifica tus productos ni tus pedidos.

</details>

<details>

<summary>¿Vambe puede cambiar precios o stock?</summary>

No. Vambe solo lee esa información.

</details>

<details>

<summary>¿La clave vence?</summary>

No. Si la desactivas o la eliminas, la conexión se corta y debes crear una nueva para volver a conectar.

</details>

<details>

<summary>¿Qué versiones de PrestaShop funcionan?</summary>

PrestaShop 1.7 y versiones superiores, incluida la versión 8.

</details>

<details>

<summary>¿Y si mi tienda está detrás de Cloudflare o un firewall?</summary>

La pantalla de conexión de Vambe te muestra la IP de Vambe y los pasos para autorizarla.

</details>

<details>

<summary>Conecté todo y no funciona. ¿Qué reviso?</summary>

Revisa que la URL incluya `https://`, que **Batch Cart** esté instalado y activo, que la clave tenga todos los permisos del paso 2 y, en PrestaShop 1.7, que hayas hecho clic en **Actualizar** en el módulo.

</details>

{% hint style="info" %}
¿Tienes dudas? Escríbenos a **soporte@vambe.ai**. Podemos coordinar una demo o una llamada con tu equipo técnico para revisar tu tienda antes de conectarla.
{% endhint %}

***

## En resumen

Con PrestaShop conectado, tu asistente de IA conoce tu catálogo y tus precios al detalle, responde por el estado de los pedidos, cierra ventas con links de checkout y recupera las compras que quedaron a medio camino. Solo necesitas instalar el módulo de Vambe y crear una clave con los permisos indicados para que todo funcione con la información real de tu tienda.
