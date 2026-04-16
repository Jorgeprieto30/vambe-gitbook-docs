---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Como crear plantillas

En esta guía aprenderás a **crear, categorizar y configurar plantillas de WhatsApp en Vambe** para responder más rápido, abrir conversaciones cerradas (más de 24 h sin actividad), enviar campañas masivas cumpliendo las políticas de Meta o para enviar mensajes rápidos.

***

#### ¿Qué es una plantilla y para qué sirve?

Una **plantilla** es un mensaje preaprobado por Meta que te permite:

* [Responder más rápido mensajes repetitivos.](https://academy.vambe.ai/como-enviar-mensajes-r%C3%A1pidos-y-plantillas)
* **Abrir conversaciones cerradas** (cuando pasaron más de 24 h desde el último mensaje del cliente).
* Iniciar chats desde cero (por ejemplo, leads que llegan desde formularios).
* Enviar **campañas masivas** a decenas, cientos o miles de contactos.
* Enviar mensajes de recordatorio de citas para agendamientos.

⚠️ Importante:

* Las plantillas de **WhatsApp** requieren aprobación de Meta.
* En **Instagram**, las plantillas no requieren aprobación y están listas de inmediato.

***

#### Requisitos previos

Para usar plantillas necesitas:

* Tener un [**número de WhatsApp Business API**](https://academy.vambe.ai/c%C3%B3mo-conectar-whatsapp-api-oficial) o [número híbrido conectado](https://academy.vambe.ai/c%C3%B3mo-conectar-un-n%C3%BAmero-de-whatsapp-business-a-vambe-mediante-el-m%C3%A9todo-h%C3%ADbrido-api-qr) en Vambe.
* Tener un [**método de pago activo**](https://academy.vambe.ai/c%C3%B3mo-agregar-un-m%C3%A9todo-de-pago-y-configurar-el-perfil-de-tu-n%C3%BAmero-de-whatsapp-api) en tu cuenta de WhatsApp dentro de Meta (obligatorio para enviar plantillas y campañas).

***

{% stepper %}
{% step %}
### Ingresar a la sección de Plantillas

* En Vambe, ve al menú izquierdo.
* Haz clic en **Canales**.
* En el submenú, selecciona **Plantillas**.
* Haz clic en **Crear**.

![](<../.gitbook/assets/image png Dec 01 2025 12 47 07 3673 PM.png>)
{% endstep %}

{% step %}
### Crear la plantilla

![](<../.gitbook/assets/image png Dec 01 2025 12 48 55 6076 PM.png>)

Completa los siguientes campos:

#### Nombre de la plantilla

* Debe ser técnico, sin espacios ni caracteres especiales.
* Ejemplos: `recordatorio_cita`, `seguimiento_pago`, `promo_blackfriday`

#### Categoría

Selecciona:

* **Utilidad**, para recordatorios, códigos, información importante.
* **Marketing**, para promociones y acciones comerciales.

_(Meta podría ajustar la categoría si considera que no coincide.)_

#### Idioma

Selecciona **Español** u otro idioma según lo necesites.

#### Canales

* Activa **WhatsApp**.
* Activa también **Instagram** si deseas que la plantilla funcione en ambos canales.
{% endstep %}

{% step %}
### Definir el contenido de la plantilla

Aquí defines la estructura del mensaje:

#### Encabezado (opcional)

![](<../.gitbook/assets/image png Dec 01 2025 01 18 27 9729 PM.png>)

Puede ser:

* Texto (incluye negrita si deseas)
* Imagen
* Video
* Documento PDF

#### Cuerpo del mensaje (Body)

![](<../.gitbook/assets/image png Dec 01 2025 01 19 44 1147 PM.png>)

Es el contenido principal.

Recomendaciones:

* Claro y directo
* Profesional pero cercano

Puedes incluir variables:

* Ej.: `Hola {{1}}, tu cita está agendada para el {{2}}.`

#### Pie de mensaje (opcional)

Texto breve, generalmente informativo.

#### Botones (opcional)

Puedes agregar:

* **Respuestas rápidas**

![](<../.gitbook/assets/image png Dec 01 2025 01 25 46 1538 PM.png>)

* **Botón con URL**

![](<../.gitbook/assets/image png Dec 01 2025 01 22 25 7995 PM.png>)

* **Botón para llamar por teléfono**

![](<../.gitbook/assets/image png Dec 01 2025 01 27 44 4166 PM.png>)

Tip: Las variables permiten personalizar masivamente:

* `{{1}} = nombre del cliente`
* `{{2}} = fecha`
* `{{3}} = dirección`, etc.
{% endstep %}

{% step %}
### Completar los ejemplos para revisión de Meta

![](<../.gitbook/assets/image png Dec 01 2025 01 29 23 7618 PM.png>)

Antes de guardar, debes completar valores de ejemplo para cada variable. Esto permite que Meta entienda el contexto del mensaje.

Ejemplo:

* `{{1}} = Felipe`
* `{{2}} = 25 de enero`
* `{{3}} = Av. Kennedy 1234`

Luego revisa la vista previa y guarda.
{% endstep %}

{% step %}
### Estado, asociación y aprobación de la plantilla

Una vez creada la plantilla, todavía **no quedará lista para usar**. Antes debe ser asociada a los canales correspondientes y enviada a revisión por Meta.

#### Pasos para habilitarla correctamente:

* Hacer clic en **Asociar canales** en la plantilla creada

![](<../.gitbook/assets/image png Dec 01 2025 01 33 10 9326 PM.png>)

* Seleccionar el canal donde quieres usar la plantilla (por ejemplo, WhatsApp API).
* Hacer clic en **Habilitar**

![](<../.gitbook/assets/image png Dec 01 2025 01 35 22 8917 PM.png>)

Qué ocurre después:

* Al habilitarla, **Vambe envía automáticamente la plantilla a revisión de Meta**.
* El estado cambiará a **Pendiente** mientras Meta la evalúa.
* Una vez aprobada por Meta, la plantilla quedará **lista para usar** tanto en:
  * Envíos manuales
  * Mensajes rápidos
  * Acciones automáticas
  * Campañas

Para actualizar el estado:

* Haz clic en **Sincronizar**.
* Meta suele responder en minutos.

![](<../.gitbook/assets/image png Dec 01 2025 01 38 27 8770 PM.png>)
{% endstep %}
{% endstepper %}

***

## Uso de las plantillas

### ¿Cuándo se debe usar una plantilla?

Debes utilizar una plantilla cuando:

* **Ya pasaron más de 24 horas** desde el último mensaje del cliente (chat cerrado).
* **Necesitas iniciar una conversación desde cero**, por ejemplo, al contactar leads de formularios o bases externas.
* **Deseas enviar campañas masivas** a decenas, cientos o miles de contactos.
* **Quieres responder de forma rápida** con mensajes predefinidos.

⚠️ Importante: La conversación solo se abre cuando **el cliente responde**. Por eso, siempre se recomienda incluir **toda la información clave en el primer mensaje de la plantilla**, evitando depender de respuestas adicionales.

***

### 💲 Costo por envío de plantillas

El envío de plantillas tiene un costo definido por Meta. Cada vez que envías una plantilla para iniciar o reactivar una conversación (fuera de la ventana de 24 horas), se genera un cobro según:

* **El país del cliente:** Las tarifas varían dependiendo de la región geográfica del número receptor.
* **El tipo de conversación:** El costo se determina por la categoría aprobada (marketing, utilidad o autenticación).
* **Las tarifas vigentes:** Los precios son establecidos directamente por Meta y pueden sufrir ajustes.

Este cobro no depende de si el cliente responde o no; se genera de forma automática al momento de enviar la plantilla desde el sistema.

👉 Te recomendamos revisar periódicamente las [tarifas oficiales de Meta](https://business.whatsapp.com/products/platform-pricing?lang=es_LA) para entender el impacto en tu facturación.

***

### Plantillas en acciones automáticas

Las plantillas también pueden usarse en:

* Seguimientos automáticos
* Reenvíos
* Flujos de nurturing
* Mensajes programados

Solo debes elegir la plantilla que corresponda dentro de la acción automática que configures.

***

### Buenas prácticas

* Sé breve y directo.
* Usa variables, pero siempre asegúrate de que tendrán valor.
* No intentes “camuflar” mensajes promocionales como utilidad.
* Usa nombres técnicos simples.
* Antes de campañas masivas, prueba enviándote la plantilla a ti.
* Evita links sospechosos o claims engañosos (Meta los rechaza).

***

## Solución de problemas frecuentes

<details>

<summary>❌ Meta rechazó mi plantilla</summary>

* Ajusta el texto o la categoría.
* Evita promociones agresivas, claims falsos o confusos.

</details>

<details>

<summary>❌ No aparece WhatsApp como canal</summary>

* Verifica que tu número WhatsApp Business API esté correctamente conectado.

</details>

<details>

<summary>❌ Las variables aparecen vacías</summary>

* Debes mapearlas al momento de enviar o configurar la campaña.

</details>

<details>

<summary>❌ El estado no actualiza</summary>

* Pulsa **Sincronizar** y espera unos minutos.

</details>
