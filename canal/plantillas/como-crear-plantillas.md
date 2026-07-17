---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Como crear plantillas

## Como crear plantillas

En esta guía aprenderás a **crear, categorizar y configurar plantillas de WhatsApp en Vambe** para responder más rápido, abrir conversaciones cerradas (más de 24 h sin actividad), enviar campañas masivas cumpliendo las políticas de Meta o para enviar mensajes rápidos.

***

**¿Qué es una plantilla y para qué sirve?**

Una **plantilla** es un mensaje preaprobado por Meta que te permite:

* [Responder más rápido mensajes repetitivos.](https://academy.vambe.ai/canal/plantillas/como-enviar-mensajes-rapidos-y-plantillas)
* **Abrir conversaciones cerradas** (cuando pasaron más de 24 h desde el último mensaje del cliente).
* Iniciar chats desde cero (por ejemplo, leads que llegan desde formularios).
* Enviar **campañas masivas** a decenas, cientos o miles de contactos.
* Enviar mensajes de recordatorio de citas para agendamientos.

⚠️ Importante:

* Las plantillas de **WhatsApp** requieren aprobación de Meta.
* En **Instagram**, las plantillas no requieren aprobación y están listas de inmediato.

***

**Requisitos previos**

Para usar plantillas necesitas:

* Tener un [**número de WhatsApp Business API**](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/como-conectar-whatsapp-api-oficial) o [número híbrido conectado](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/guia-de-conexion-whatsapp-api-metodo-qr) en Vambe.
* Tener un [**método de pago activo**](https://academy.vambe.ai/canal/configuracion-en-meta/como-agregar-un-metodo-de-pago-y-configurar-el-perfil-de-tu-numero-de-whatsapp-api) en tu cuenta de WhatsApp dentro de Meta (obligatorio para enviar plantillas y campañas).

***

{% stepper %}
{% step %}
**Ingresar a la sección de Plantillas**

* En Vambe, ve al menú izquierdo.
* Haz clic en **Canales**.
* En el submenú, selecciona **Plantillas**.
* Haz clic en **Crear**.

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/kPSlFrnU0n3aJZ8nv1LN/image%20png%20Dec%2001%202025%2012%2047%2007%203673%20PM.png)
{% endstep %}

{% step %}
**Crear la plantilla**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/n6Rsqh8pnNvYSoRcoTAi/image%20png%20Dec%2001%202025%2012%2048%2055%206076%20PM.png)

Completa los siguientes campos:

**Nombre de la plantilla**

* Debe ser técnico, sin espacios ni caracteres especiales.
* Ejemplos: `recordatorio_cita`, `seguimiento_pago`, `promo_blackfriday`

**Categoría**

Selecciona:

* **Utilidad**, para recordatorios, códigos, información importante.
* **Marketing**, para promociones y acciones comerciales.

_(Meta podría ajustar la categoría si considera que no coincide.)_

**Idioma**

Selecciona **Español** u otro idioma según lo necesites.

**Canales**

* Activa **WhatsApp**.
* Activa también **Instagram** si deseas que la plantilla funcione en ambos canales.
{% endstep %}

{% step %}
**Definir el contenido de la plantilla**

Aquí defines la estructura del mensaje:

**Encabezado (opcional)**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/6CHYCF5mpq2s66VmmKR7/image%20png%20Dec%2001%202025%2001%2018%2027%209729%20PM.png)

Puede ser:

* Texto (incluye negrita si deseas)
* Imagen
* Video
* Documento PDF

**Cuerpo del mensaje (Body)**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/Woa5EMTC4G9GwJUk7lVY/image%20png%20Dec%2001%202025%2001%2019%2044%201147%20PM.png)

Es el contenido principal.

Recomendaciones:

* Claro y directo
* Profesional pero cercano

Puedes incluir variables:

* Ej.: `Hola {{1}}, tu cita está agendada para el {{2}}.`

**Pie de mensaje (opcional)**

Texto breve, generalmente informativo.

**Botones (opcional)**

Puedes agregar:

* **Respuestas rápidas**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/BT2f9ggfP2nR5vw3NDxG/image%20png%20Dec%2001%202025%2001%2025%2046%201538%20PM.png)

* **Botón con URL**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/75P3aSCJgHD0tbyuLXwC/image%20png%20Dec%2001%202025%2001%2022%2025%207995%20PM.png)

* **Botón para llamar por teléfono**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/JaujkVOVfNYsMSLdQ47z/image%20png%20Dec%2001%202025%2001%2027%2044%204166%20PM.png)

Tip: Las variables permiten personalizar masivamente:

* `{{1}} = nombre del cliente`
* `{{2}} = fecha`
* `{{3}} = dirección`, etc.
{% endstep %}

{% step %}
**Completar los ejemplos para revisión de Meta**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/vgq8RIDvW6jUYPKu70ur/image%20png%20Dec%2001%202025%2001%2029%2023%207618%20PM.png)

Antes de guardar, debes completar valores de ejemplo para cada variable. Esto permite que Meta entienda el contexto del mensaje.

Ejemplo:

* `{{1}} = Felipe`
* `{{2}} = 25 de enero`
* `{{3}} = Av. Kennedy 1234`

Luego revisa la vista previa y guarda.
{% endstep %}

{% step %}
**Estado, asociación y aprobación de la plantilla**

Una vez creada la plantilla, todavía **no quedará lista para usar**. Antes debe ser asociada a los canales correspondientes y enviada a revisión por Meta.

**Pasos para habilitarla correctamente:**

* Hacer clic en **Asociar canales** en la plantilla creada

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/tcD891rFs2qzsYg9Joje/image%20png%20Dec%2001%202025%2001%2033%2010%209326%20PM.png)

* Seleccionar el canal donde quieres usar la plantilla (por ejemplo, WhatsApp API).
* Hacer clic en **Habilitar**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/kTExsn6PWMZL0Hnxec5D/image%20png%20Dec%2001%202025%2001%2035%2022%208917%20PM.png)

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

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/ThWEAndiAOFNQM7GOvwt/image%20png%20Dec%2001%202025%2001%2038%2027%208770%20PM.png)
{% endstep %}
{% endstepper %}

***

### Uso de las plantillas

#### ¿Cuándo se debe usar una plantilla?

Debes utilizar una plantilla cuando:

* **Ya pasaron más de 24 horas** desde el último mensaje del cliente (chat cerrado).
* **Necesitas iniciar una conversación desde cero**, por ejemplo, al contactar leads de formularios o bases externas.
* **Deseas enviar campañas masivas** a decenas, cientos o miles de contactos.
* **Quieres responder de forma rápida** con mensajes predefinidos.

⚠️ Importante: La conversación solo se abre cuando **el cliente responde**. Por eso, siempre se recomienda incluir **toda la información clave en el primer mensaje de la plantilla**, evitando depender de respuestas adicionales.

***

#### 💲 Costo por envío de plantillas

El envío de plantillas tiene un costo definido por Meta. Cada vez que envías una plantilla para iniciar o reactivar una conversación (fuera de la ventana de 24 horas), se genera un cobro según:

* **El país del cliente:** Las tarifas varían dependiendo de la región geográfica del número receptor.
* **El tipo de conversación:** El costo se determina por la categoría aprobada (marketing, utilidad o autenticación).
* **Las tarifas vigentes:** Los precios son establecidos directamente por Meta y pueden sufrir ajustes.

Este cobro no depende de si el cliente responde o no; se genera de forma automática al momento de enviar la plantilla desde el sistema.

👉 Te recomendamos revisar periódicamente las [tarifas oficiales de Meta](https://business.whatsapp.com/products/platform-pricing?lang=es_LA) para entender el impacto en tu facturación.

***

#### Plantillas en acciones automáticas

Las plantillas también pueden usarse en:

* Seguimientos automáticos
* Reenvíos
* Flujos de nurturing
* Mensajes programados

Solo debes elegir la plantilla que corresponda dentro de la acción automática que configures.

***

#### Buenas prácticas

* Sé breve y directo.
* Usa variables, pero siempre asegúrate de que tendrán valor.
* No intentes “camuflar” mensajes promocionales como utilidad.
* Usa nombres técnicos simples.
* Antes de campañas masivas, prueba enviándote la plantilla a ti.
* Evita links sospechosos o claims engañosos (Meta los rechaza).

***

### Solución de problemas frecuentes

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
