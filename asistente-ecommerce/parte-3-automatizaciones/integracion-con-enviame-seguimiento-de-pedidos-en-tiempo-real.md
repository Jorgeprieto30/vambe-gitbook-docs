---
description: >-
  Conecta Vambe con Envíame para que tu asistente pueda consultar el estado de
  envío de cualquier pedido directamente desde la conversación, usando los
  principales couriers del mercado.
---

# Integración con Envíame: Seguimiento de pedidos en tiempo real

Conecta Vambe con Envíame para que tu asistente pueda consultar el estado de envío de cualquier pedido directamente desde la conversación, usando los principales couriers del mercado.

### ¿Qué es Envíame y por qué integrarlo?

Envíame es una plataforma que conecta e-commerces con múltiples transportistas (couriers), permitiendo **rastrear envíos** en tiempo real desde un solo lugar. Al integrarlo en Vambe, potencias tu sistema de postventa: tu asistente podrá responder preguntas de seguimiento de pedidos con información actualizada, sin que el cliente tenga que salir de la conversación.

**Lo que obtienes con esta integración:**

* **Seguimiento multicarrier:** El asistente consulta el estado del envío a través de la red de couriers de Envíame.
* **Complemento inteligente:** Si Envíame no encuentra el estado, el sistema hace fallback automático al `get_order_status` del e-commerce conectado.
* **Postventa reforzada:** Menos tickets manuales, respuestas más precisas para tus clientes.

***

### Paso 1: Conectar Envíame en Vambe

Ve a **Ajustes → Integraciones**. En la sección **Ecommerce** encontrarás la tarjeta de **Envíame**.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

Haz clic en la tarjeta para abrir el detalle de la integración y luego presiona el botón **Conectar**.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

***

### Paso 2: Autenticar la conexión

Se abrirá el formulario de autenticación. Debes completar dos campos:

1. **Nombre de la conexión:** Un nombre identificador, por ejemplo `demo-enviame-1`.
2. **Token:** El token de API de tu cuenta en Envíame.

💡 **¿No sabes dónde encontrar tu token?** Envíame dispone de documentación y tutoriales en su plataforma para obtenerlo. También puedes hacer clic en el enlace **"**[**¿Cómo obtener mis credenciales?**](https://app.vambeai.com/token/create?imagePath=/logos/enviame-logo.png\&integrationType=enviame\&description=enviame_description\&fields=name,token\&videoPath=https://assets.vambe.ai/videos/enviame-api-key-demo-2.mp4\&integrationTitle=Enviame)**"** dentro del mismo formulario.

Una vez completados los campos, haz clic en **Siguiente**. La conexión quedará autenticada y lista para usarse.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

***

### Paso 3: Vincular Envíame a la función "Get Order Status"

Con la conexión creada, el siguiente paso es asociarla al asistente que consulta el estado de pedidos.

1. Dirígete al **asistente** de e-commerce que tenga configurada la función `Get order status` (también llamada _Obtener Estado de Orden_).
2. En el caso posible o pasos a seguir agregar la función.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

1. Haz clic en el ícono de configuración (⚙️) junto a **Get order status**.

***

### Paso 4: Configurar el proveedor de seguimiento

Dentro del modal de configuración de la función verás los campos habituales (Nombre, Descripción, E-commerce). Ahora hay un campo nuevo:

* **Proveedor de seguimiento (opcional):** Selecciona aquí la conexión de Envíame que creaste en el paso anterior (ej. `demo-enviame-1`).

Haz clic en **Guardar**.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

***

### ¿Cómo funciona la lógica de consulta?

Una vez configurado, el asistente sigue este orden al recibir una pregunta sobre el estado de un pedido:

1. **Primero consulta Envíame** usando el número de orden y el proveedor configurado.
2. **Si Envíame no tiene datos disponibles**, hace fallback y consulta el estado directamente desde el e-commerce conectado (comportamiento anterior).

Esto garantiza que el cliente siempre reciba la información más precisa posible, aprovechando la red de couriers de Envíame cuando está disponible.
