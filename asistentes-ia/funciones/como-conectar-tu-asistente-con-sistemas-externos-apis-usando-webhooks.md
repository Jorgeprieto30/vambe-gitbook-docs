---
description: >-
  Nivel Avanzado. Conecta Vambe con tu software. Aprende a configurar Webhooks
  para que tu IA consulte stock, estados de pedido o envíe datos a tu ERP en
  tiempo real.
---

# ¿Cómo conectar tu Asistente con sistemas externos (APIs) usando Webhooks?

{% embed url="https://www.youtube.com/watch?v=ifqEe40b5W8" %}

La función Llamada Webhook es la herramienta que permite a tu Inteligencia Artificial "hablar" con otros sistemas fuera de Vambe.

¿Para qué sirve? Permite enviar o traer datos.

* Consultar datos (GET): La IA puede ir a tu sistema, preguntar "¿Dónde está el pedido 123?" y responderle al cliente "Tu pedido fue entregado ayer".
* Enviar datos (POST): La IA puede tomar los datos del chat y enviarlos a tu base de datos o CRM externo.

***

#### ⚠️ Requisito: Conocimiento Técnico

Esta función requiere manipular conceptos de programación como APIs, Endpoints, JSON y Métodos HTTP (GET, POST, etc.). Si no te manejas con estos términos, te recomendamos pedir ayuda a tu equipo de desarrollo.

***

#### Configuración Paso a Paso: Ejemplo "Estado del Pedido"

En este ejemplo, configuraremos a la IA para que, cuando un cliente pregunte por su compra, la IA consulte una API externa y le dé la respuesta.

**Paso 1: Instrucción en el Asistente**

1. [Ve a tu Asistente](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md) y entra en **Casos Posibles** (ideal para preguntas que pueden surgir en cualquier momento).
2. Define la lógica en el texto: _"Cuando el cliente necesite saber el estado de su pedido, pídele el número de seguimiento, una vez te lo entrega ejecuta la función webhook"_.

**Paso 2: Configuración Básica del Webhook**

Haz clic en + Agregar Función y selecciona Llamada Webhook.

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Configura los datos base:

1. **Nombre**: Ej: "Estado del Pedido".
2. **Descripción (Vital)**: Dile a la IA cuándo usarla. Ej: _"Cuando el cliente pregunte el estado de su pedido y ya sepas el número del pedido"_.
3. **Método**: Selecciona el verbo HTTP (GET, POST, PUT, DELETE). Para consultar datos, usaremos GET.
4. **URL (Endpoint)**: Pega la dirección de tu API.

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

**Paso 3: Configuración de Parámetros y Variables**

Aquí es donde conectas los datos. Tienes pestañas para Body, Headers, Params y Route.

**A. Autenticación (Headers)**: Si tu API requiere una clave (Token), agrégala en _Headers_.

* _Importante:_ Si el token es fijo, DESACTIVA el interruptor de "Use AI". Esto le dice al sistema que es un valor estático y la IA no debe intentar inventarlo o buscarlo en el chat.

**B. Variables Dinámicas (La magia de la IA)**: Si necesitas insertar un dato que el cliente dio en el chat (como el `order_id`) dentro de la URL, usa llaves dobles: `{{order_id}}`.

* Al hacerlo, se creará automáticamente una pestaña de Route (o Params/Body según corresponda).
* **ACTIVA el interruptor "Use AI"**: Esto le permite a la IA buscar ese número en la conversación.
* **Descripción del parámetro:** Escribe qué es (Ej: "El número de pedido").

Así se ve una configuración correcta con variables dinámicas: Observa cómo el campo `order_id` tiene el switch de IA activado (azul), permitiendo que el asistente extraiga ese dato del chat.

**Paso 4: Verificación Visual (¿Cómo debe verse?)**

Antes de probar, confirma que la función quedó correctamente vinculada al paso.

Revisa la estructura: Debes ver el texto de tu instrucción y, justo debajo, una tarjeta blanca que dice "🔗 Llamada Webhook" (o el nombre que le pusiste, como "Informacion Pedido").

* Si ves el texto pero NO ves la tarjeta debajo, la IA leerá la instrucción pero no podrá ejecutar nada. ¡Asegúrate de darle clic a "Crear"!

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

***

#### 💡 Otra Alternativa: Webhooks en Workflows

¿Buscas disparar un Webhook cuando ocurre un evento (ej: entra un cliente nuevo, cambia de etapa, o se etiqueta) y no necesariamente en una conversación?

Para esos casos de automatización pura, no uses las funciones del Asistente. Debes usar los Workflows.

👉 [\[Haz clic aquí para ver el artículo completo sobre Workflows y Automatizaciones\]](https://app.gitbook.com/o/9CuC7LM0j6YJ7xZrMGfk/s/0xCLgfGby0xiCWJaqr57/)
