---
description: >-
  Envía y programa mensajes de WhatsApp desde sistemas externos. Guía técnica de
  la API de Vambe para envíos inmediatos, Smart Templates con IA y agendamiento.
---

# Integración API: Enviar y Programar Mensajes desde Otro Sistema

La API de Vambe permite que tus sistemas externos (CRM, ERP, Web) disparen mensajes de WhatsApp de forma programática. Puedes realizar envíos inmediatos con control manual, usar la IA para rellenar variables o dejar mensajes programados para el futuro.

{% hint style="warning" %}
⚠️ Advertencia Técnica: Este artículo requiere conocimientos de desarrollo y consumo de APIs REST. Si no eres desarrollador, comparte esta guía con tu equipo técnico. Para todos los casos, necesitarás tu x-api-key, disponible en la sección de Desarrolladores.
{% endhint %}

***

#### 1. Requisitos Previos

Antes de usar cualquier endpoint, asegúrate de cumplir con lo siguiente:

* **API Key**: La llave de autenticación de tu cuenta. Puedes encontrarla [aquí](https://www.vambeai.com/developers)
* **Plantilla (Template)**: El mensaje debe ser una plantilla aprobada. Si no tienes una, créala antes de continuar. 👉 [_\[Guía: Cómo crear y aprobar plantillas de WhatsApp\]_](https://academy.vambe.ai/canal/plantillas/como-crear-plantillas)

***

#### 2. Envíos Inmediatos (Immediate Sending)

| **Endpoint**    | **¿Cuándo usarlo?**                                       | **¿Cómo se llenan las variables?**                          |
| --------------- | --------------------------------------------------------- | ----------------------------------------------------------- |
| Code Based (V2) | Tienes los datos estructurados y ordenados en tu sistema. | Manual: Tú envías la lista exacta `["Juan", "Pedido #10"]`. |
| Smart (Single)  | Tienes un texto desordenado o un párrafo largo.           | IA: Le das el texto a la IA y ella busca qué dato sirve.    |
| Smart (Bulk)    | Quieres enviar a muchas personas a la vez usando IA.      | IA: Igual que el anterior, pero optimizado para volumen.    |

Existen tres formas de enviar un mensaje ahora mismo, dependiendo del nivel de control y volumen que necesites.

**A. Envío Manual con Variables (Code Based V2)**

Usa este endpoint si quieres **definir exactamente qué valor va en cada variable**, en el orden específico de la plantilla.

* Endpoint: `Send WhatsApp Template (Code Based v2)`
* 🔗 Documentación Oficial: [Clic aquí para ver docs](https://docs.vambe.me/reference/whatsapp-message/send-a-template-message-1)

Parámetros Obligatorios:

* `variables`: Lista de valores en el orden exacto de la plantilla.
* `metadata`: Información adicional del contacto.
* `phone`: Número de teléfono del destinatario (To).
* `template_name`: Nombre exacto de la plantilla.
* `from_phone_number`: Número de origen conectado a Vambe.

**Parámetros Opcionales:**

* `contact_name`: Para asignar nombre al contacto en Vambe.
* `stage_id`: Define en qué etapa aparecerá el cliente o ticket tras el envío.
* `agent_id`: Asigna el ticket a un agente específico.

<details>

<summary><strong>Logistica Variable &#x3C;> Plantilla</strong></summary>

**💡 Concepto Visual:**

Tu Plantilla en Vambe:\
"Hola \{{1\}}, confirmamos tu cita para el día \{{2\}}."

Tu Código (Array de variables):\
"variables": \[\
"Carlos", <-- Rellena el \{{1\}}\
"Martes 15" <-- Rellena el \{{2\}}\
]

**⚠️ El orden en la lista debe ser exacto.**

</details>

**Curl Ejemplo**

```
curl --request POST \
  --url https://api.vambe.me/v1/whatsapp/message/send-template \
  --header 'Content-Type: application/json' \
  --header 'x-api-key: TU_API_KEY_AQUI' \
  --data '{
  "phone": "56912345678",
  "template_name": "nombre_exacto_plantilla",
  "from_phone_number": "56987654321",
  "variables": [
    "Juan Pérez",
    "Tu pedido #5501"
  ],
  "metadata": {
    "cliente_id": "CLI-999"
  },
  "stage_id": "uuid-de-la-etapa-destino"
}'
```

**B. Envío Inteligente: Un solo destinatario (Smart Template Single)**

En este método, el Template ID se envía directamente en la URL del endpoint. La Inteligencia Artificial utilizará la información que envíes en el `body` (JSON) para rellenar las variables de la plantilla automáticamente.

* Endpoint: `POST /api/public/whatsapp/message/send/template/{templateId}`
* 🔗 Documentación Oficial: [Referencia API aquí](https://docs.vambe.me/reference/whatsapp-message/send-a-template-message-with-unstructured-data)

**Parámetros en URL (Query Params):**

* `x-api-key`: Tu llave de API (Obligatorio).
* `from-phone-number`: El número conectado a Vambe desde donde envías (Obligatorio).
* `stage`: ID de la etapa destino (Opcional).

**Cuerpo de la Solicitud (Body JSON)**: Envía un objeto JSON con los datos que la IA debe procesar. Si necesitas asociar datos de una integración externa, usa la estructura `integrationData`.

```
{
  "contexto_clave": "valor",
  "integrationData": {
    "integrationContactId": "id_externo_123",
    "integrationDealId": "id_negocio_456",
    "additionalData": { "saldo": "5000" }
  }
}
```

**Ejemplo de Código (cURL):**

```
curl --request POST \
  --url 'https://api.vambe.me/api/public/whatsapp/message/send/template/TU_TEMPLATE_ID?x-api-key=TU_API_KEY&from-phone-number=56912345678' \
  --header 'Content-Type: application/json' \
  --data '{
  "nombre": "Carlos",
  "motivo": "Confirmación de cita médica",
  "integrationData": {
     "integrationContactId": "crm_user_88"
  }
}'
```

**C. Envío Inteligente: Masivo (Smart Template Bulk)**

Similar al anterior, pero diseñado para enviar a múltiples personas en una sola petición. El Template ID sigue yendo en la URL, pero el body recibe un Array de objetos.

* **Endpoint**: `POST /api/public/whatsapp/message/send/template/{templateId}/many`
* 🔗 **Documentación Oficial**: [Referencia API aquí](https://docs.vambe.me/reference/whatsapp-message/send-a-template-message-with-unstructured-data-1)

Parámetros en URL (Query Params):

* `x-api-key` (Obligatorio)
* `from-phone-number` (Obligatorio)
* `stageId` (Opcional - Recomendado sobre `stage`)

Cuerpo de la Solicitud (Body JSON): Un arreglo (lista) de objetos, donde cada objeto representa los datos para un destinatario específico.

**Ejemplo de Código (cURL):**

```
curl --request POST \
  --url 'https://api.vambe.me/api/public/whatsapp/message/send/template/TU_TEMPLATE_ID/many?x-api-key=TU_API_KEY&from-phone-number=56912345678&stageId=uuid_etapa' \
  --header 'Content-Type: application/json' \
  --data '[
  {
    "phone": "56911111111",
    "nombre": "Ana",
    "integrationData": { "integrationContactId": "001" }
  },
  {
    "phone": "56922222222",
    "nombre": "Beto",
    "integrationData": { "integrationContactId": "002" }
  }
]'
```

***

#### 3. Programar Mensajes (Scheduling)

Si necesitas que el mensaje se envíe en una fecha futura, utiliza el endpoint de creación de programados.

> ⚠️ Atención al formato: A diferencia de los endpoints anteriores, aquí los parámetros del body deben usar formato camelCase (ej: `scheduledDate`, `templateId`).

* **Endpoint**: `POST /api/public/whatsapp/message/programmed/create`
* 🔗 **Documentación Oficial**: [Referencia API aquí](https://docs.vambe.me/reference/whatsapp-message/send-a-program-a-template-message-to-send-at-a-specific-time)

**Parámetros del Body (JSON):**

* `scheduledDate`: Fecha en formato ISO 8601 (ej: `2023-12-25T09:00:00Z`).
* `templateId`: ID de la plantilla.
* `contactIdentifier`: Número del destinatario.
* `channel`: `whatsapp` (API) o `web_whatsapp` (QR).
* `isSmart`: `true` para usar IA en el relleno de variables.
* `fromPhoneNumber`: Número de origen.
* `stageId`: ID de la etapa destino.
* `meta_data`: Objeto con los datos para la IA.

**Ejemplo de Código (cURL):**

```
curl --request POST \
  --url https://api.vambe.me/api/public/whatsapp/message/programmed/create \
  --header 'Content-Type: application/json' \
  --header 'x-api-key: TU_API_KEY' \
  --data '{
  "scheduledDate": "2023-12-25T09:00:00Z",
  "templateId": "uuid-template-id",
  "contactIdentifier": "56912345678",
  "channel": "whatsapp",
  "isSmart": true,
  "fromPhoneNumber": "56987654321",
  "stageId": "uuid-etapa-id",
  "meta_data": {
    "nombre": "Cliente Ejemplo",
    "producto": "Servicio Premium"
  }
}'
```

***

#### 4. Cancelar un Mensaje Programado

Si necesitas detener un envío que ya programaste (por ejemplo, el cliente ya compró y no quieres enviarle el recordatorio), puedes cancelarlo vía API.

* Endpoint: `Cancel Scheduled WhatsApp Message`
* 🔗 Documentación Oficial: [Clic aquí para ver docs](https://docs.vambe.me/reference/whatsapp-message/cancel-a-programmed-message-by-scheduled-message-id)

Requisito: Necesitas el `scheduled_message_id`. Este ID es retornado por la API en la respuesta (response) cuando creas el agendamiento en el paso anterior. Guárdalo si planeas tener la opción de cancelar.

**Curl Ejemplo**

```
curl --request POST \
  --url https://api.vambe.me/v1/whatsapp/message/schedule/cancel \
  --header 'Content-Type: application/json' \
  --header 'x-api-key: TU_API_KEY_AQUI' \
  --data '{
  "scheduled_message_id": "uuid-retornado-al-programar"
}'
```
