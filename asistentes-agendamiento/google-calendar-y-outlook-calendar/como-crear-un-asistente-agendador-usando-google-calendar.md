# Cómo crear un asistente agendador usando Google Calendar y Outlook calendar

## Cómo crear un asistente agendador usando Google Calendar y Outlook calendar

En este artículo aprenderás a configurar un **asistente agendador utilizando Google Calendar**, ideal para los casos en que deseas **agendar directamente una cita en Google Calendar**, sin depender de una plataforma externa de agendamiento.

{% hint style="info" %}
Si usas **Outlook calendar** debes seguir las mismas instrucciones pero seleccionando **Outlook calendar**
{% endhint %}

Este flujo es especialmente útil cuando:

* Quieres agendar reuniones internas o externas directamente en Google Calendar.
* Buscas un flujo más simple y directo de agendamiento.

***

### Consideraciones importantes antes de comenzar

Antes de continuar, asegúrate de cumplir con lo siguiente:

* ✅ Tener **Google Calendar conectado** correctamente en Vambe.

> Si aún no lo has hecho, revisa el artículo: **Cómo conectar Google Calendar en Vambe**.

* ✅ Haber creado previamente:
  * Las [**etapas del embudo**](https://academy.vambe.ai/asistentes-agendamiento/parte-3-crear-plataforma-agendamiento/paso-0-crear-las-etapas).
  * El [**asistente inicial**](https://academy.vambe.ai/asistentes-agendamiento/parte-3-crear-plataforma-agendamiento/paso-1-como-crear-tu-primer-asistente-de-agendamiento) (Información y dudas generales).
  * El [**asistente de agendamiento base**](https://academy.vambe.ai/asistentes-agendamiento/parte-3-crear-plataforma-agendamiento/paso-2-asistente-agendador) (Paso 2).
  * El **asistente de Agendados** (Paso 3).

{% hint style="info" %}
La única diferencia entre este asistente y un asistente agendador tradicional (AgendaPro, Reservo, Dentalink, etc.) es que **NO se utiliza el bloque de aplicaciones de reserva**.\
Todo lo demás (estructura general, bloques compartidos, etapas) se mantiene igual.
{% endhint %}

Para revisar la configuración completa del asistente agendador estándar: 👉 [**Paso 2: Cómo crear el asistente agendador**](https://academy.vambe.ai/asistentes-agendamiento/parte-3-crear-plataforma-agendamiento/paso-2-asistente-agendador)

***

### Qué veremos en este artículo

En este artículo **solo nos enfocaremos en el bloque “Pasos a seguir”** del asistente agendador usando Google Calendar, ya que es la única parte que cambia.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/eOxOMuXvSgF6ucXwemvg/image\(7\).png)

***

{% stepper %}
{% step %}
#### Buscar disponibilidad en Google Calendar

El primer paso del asistente será buscar disponibilidad y mostrar opciones al cliente.

Instrucción sugerida:

> Buscar disponibilidad y entregar al cliente 5 fechas disponibles para que pueda escoger.

Configuración de la función

1. Haz clic en **Agregar función**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/dTCGt1BGeFjrC0eLXQ4U/image\(9\).png)

2. Baja hasta la sección **Google Calendar**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/vdRUppRuP7hpGWhPdvgE/image\(10\).png)

3. Crea una nueva función de tipo **Disponibilidad**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/CGBQelbAUMUAyMivyvP5/image\(11\).png)

4. Configura:
   * **Cuenta de Google** (correo conectado).
   * **Calendario** que se usará para buscar disponibilidad.
   * Selecciona el tipo de asignación: Aleatoria, Según criterio de IA, Según agente.
   * (Opcional) **Asignación por agente**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/Qz0auqVxFzJ58QEvRtan/image\(12\).png)

5. Define la duración de la cita:
   * Duración fija (recomendado), o
   * Dejar que la IA decida _(no recomendado si no está bien definido)_.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/BLwMpwiuUy8qjq8Ib4Qv/image\(13\).png)

⚠️ Esta configuración deberá repetirse exactamente igual más adelante al crear el evento.

Una vez creada la función se verá de la siguiente forma:

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/Xgy75NLsHygBgtZBEzK8/image\(15\).png)
{% endstep %}

{% step %}
#### Solicitar datos al cliente

Una vez que el cliente selecciona una fecha, el asistente debe pedir los datos necesarios para crear el evento.

Recomendación mínima de datos:

* Correo electrónico ( **obligatorio**).
* Nombre del cliente.
* Teléfono de contacto.
* Dirección (si aplica).

📌 El correo es indispensable para poder crear correctamente el evento en Google Calendar.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/RFSkM2lwhKFWEtGYNeaU/image\(16\).png)
{% endstep %}

{% step %}
#### Crear el evento en Google Calendar

Cuando el cliente ya eligió fecha y entregó sus datos, se debe crear la cita.

Instrucción sugerida:

> Crear la cita en Google Calendar con los datos entregados por el cliente.

Configuración de la función “Crear evento”

1. Haz clic en **Agregar función**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/dTCGt1BGeFjrC0eLXQ4U/image\(9\).png)

2. Selecciona **Google Calendar**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/vdRUppRuP7hpGWhPdvgE/image\(10\).png)

3. Crea una nueva función de tipo **Crear Evento**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/nMBEFeuDB9CrDtPA7kzX/image\(18\).png)

4. Configura:
   * Calendario donde se creará el evento.
   * (Opcional) Agente asignado.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/nrqS1MnWiWsRR1zY7YWd/image\(19\).png)

5. Define:
   * **Nombre del evento**.
   * **Descripción del evento**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/bumQ7J6YjJ19wvh8g8Bn/image\(21\).png)

6. Configuraciones adicionales:
   * Activar creación automática de descripción.
   * Activar enlace de **Google Meet** (si corresponde).
   * Notificaciones al cliente: si se notifica, cuánto tiempo antes, mensaje de confirmación.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/PCGb6jF3OLt29GCUP70G/image\(22\).png) ![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/lLShhmEpt01zRT4T874P/image\(23\).png)

7. Define **cuándo se ejecuta la función**:
   * Cuando el cliente selecciona fecha y ha entregado todos los datos requeridos.
8. Define duración del evento:
   * Debe ser **idéntica** a la configurada en la búsqueda de disponibilidad.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/i8tTvVBtU6XKldlACxCn/image\(24\).png)

⚠️ Muy importante: Las configuraciones de **disponibilidad y creación del evento deben ser exactamente iguales** (criterio, calendario, duración, asignación).

Una vez creada la función se verá de la siguiente forma:

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/3DtpExTb3XMTBnsU7TLz/image\(25\).png)
{% endstep %}

{% step %}
#### Enviar al cliente a la etapa Agendados

Una vez creada la cita exitosamente, debes ejecutar la función **Cambiar de etapa a Agendados**. Recuerda colocar la función ‘Cambio de etapa’.

Esto permite que el cliente:

* Reciba recordatorios.
* Pueda reagendar o cancelar.
* Consulte información de su cita desde el asistente correspondiente.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/0D2Sv8eWs7wOJSusvOna/image\(27\).png)
{% endstep %}
{% endstepper %}

***

### Resumen final

* Este asistente **agenda directamente en Google Calendar**.
* No utiliza el bloque de aplicaciones de reserva.
* El foco está en:
  * Buscar disponibilidad.
  * Crear evento.
  * Enviar al cliente a la etapa Agendados.
* El resto de la estructura del asistente se mantiene igual que en el asistente agendador estándar.

Para continuar, revisa:

* **Paso 1: Crear tu primer asistente de agendamiento**
* **Paso 3: Crear el asistente de Agendados**
