# Cómo crear un asistente agendador usando Google Calendar

En este artículo aprenderás a configurar un **asistente agendador utilizando Google Calendar**, ideal para los casos en que deseas **agendar directamente una cita en Google Calendar**, sin depender de una plataforma externa de agendamiento.

Este flujo es especialmente útil cuando:

* Quieres agendar reuniones internas o externas directamente en Google Calendar.
* Buscas un flujo más simple y directo de agendamiento.

***

## Consideraciones importantes antes de comenzar

Antes de continuar, asegúrate de cumplir con lo siguiente:

* ✅ Tener **Google Calendar conectado** correctamente en Vambe.

> Si aún no lo has hecho, revisa el artículo: [**Cómo conectar Google Calendar en Vambe**.](como-iniciar-sesion-y-vincular-google-calendar-en-vambe.md)

* ✅ Haber creado previamente:
  * Las [**etapas del embudo**](https://academy.vambe.ai/v1/docs/paso-0-crear-las-etapas).
  * El [**asistente inicial**](https://academy.vambe.ai/v1/docs/paso-1-c%C3%B3mo-crear-tu-primer-asistente-de-agendamiento) (Información y dudas generales).
  * El [**asistente de agendamiento base**](https://academy.vambe.ai/v1/docs/paso-2-asistente-agendador) (Paso 2).
  * El **asistente de Agendados** (Paso 3).

{% hint style="info" %}
La única diferencia entre este asistente y un asistente agendador tradicional (AgendaPro, Reservo, Dentalink, etc.) es que **NO se utiliza el bloque de aplicaciones de reserva**.\
Todo lo demás (estructura general, bloques compartidos, etapas) se mantiene igual.
{% endhint %}

Para revisar la configuración completa del asistente agendador estándar: 👉 [**Paso 2: Cómo crear el asistente agendador**](https://academy.vambe.ai/v1/docs/paso-2-asistente-agendador)

***

## Qué veremos en este artículo

En este artículo **solo nos enfocaremos en el bloque “Pasos a seguir”** del asistente agendador usando Google Calendar, ya que es la única parte que cambia.

![](../.gitbook/assets/image\(7\).png)

***

{% stepper %}
{% step %}
### Buscar disponibilidad en Google Calendar

El primer paso del asistente será buscar disponibilidad y mostrar opciones al cliente.

Instrucción sugerida:

> Buscar disponibilidad y entregar al cliente 5 fechas disponibles para que pueda escoger.

Configuración de la función

1. Haz clic en **Agregar función**.

![](../.gitbook/assets/image\(9\).png)

2. Baja hasta la sección **Google Calendar**.

![](../.gitbook/assets/image\(10\).png)

3. Crea una nueva función de tipo **Disponibilidad**.

![](../.gitbook/assets/image\(11\).png)

4. Configura:
   * **Cuenta de Google** (correo conectado).
   * **Calendario** que se usará para buscar disponibilidad.
   * Selecciona el tipo de asignación: Aleatoria, Según criterio de IA, Según agente.
   * (Opcional) **Asignación por agente**.

![](../.gitbook/assets/image\(12\).png)

5. Define la duración de la cita:
   * Duración fija (recomendado), o
   * Dejar que la IA decida _(no recomendado si no está bien definido)_.

![](../.gitbook/assets/image\(13\).png)

⚠️ Esta configuración deberá repetirse exactamente igual más adelante al crear el evento.

Una vez creada la función se verá de la siguiente forma:

![](../.gitbook/assets/image\(15\).png)
{% endstep %}

{% step %}
### Solicitar datos al cliente

Una vez que el cliente selecciona una fecha, el asistente debe pedir los datos necesarios para crear el evento.

Recomendación mínima de datos:

* Correo electrónico ( **obligatorio**).
* Nombre del cliente.
* Teléfono de contacto.
* Dirección (si aplica).

📌 El correo es indispensable para poder crear correctamente el evento en Google Calendar.

![](../.gitbook/assets/image\(16\).png)
{% endstep %}

{% step %}
### Crear el evento en Google Calendar

Cuando el cliente ya eligió fecha y entregó sus datos, se debe crear la cita.

Instrucción sugerida:

> Crear la cita en Google Calendar con los datos entregados por el cliente.

Configuración de la función “Crear evento”

1. Haz clic en **Agregar función**.

![](../.gitbook/assets/image\(9\).png)

2. Selecciona **Google Calendar**.

![](../.gitbook/assets/image\(10\).png)

3. Crea una nueva función de tipo **Crear Evento**.

![](../.gitbook/assets/image\(18\).png)

4. Configura:
   * Calendario donde se creará el evento.
   * (Opcional) Agente asignado.

![](../.gitbook/assets/image\(19\).png)

5. Define:
   * **Nombre del evento**.
   * **Descripción del evento**.

![](../.gitbook/assets/image\(21\).png)

6. Configuraciones adicionales:
   * Activar creación automática de descripción.
   * Activar enlace de **Google Meet** (si corresponde).
   * Notificaciones al cliente: si se notifica, cuánto tiempo antes, mensaje de confirmación.

![](../.gitbook/assets/image\(22\).png) ![](../.gitbook/assets/image\(23\).png)

7. Define **cuándo se ejecuta la función**:
   * Cuando el cliente selecciona fecha y ha entregado todos los datos requeridos.
8. Define duración del evento:
   * Debe ser **idéntica** a la configurada en la búsqueda de disponibilidad.

![](../.gitbook/assets/image\(24\).png)

⚠️ Muy importante: Las configuraciones de **disponibilidad y creación del evento deben ser exactamente iguales** (criterio, calendario, duración, asignación).

Una vez creada la función se verá de la siguiente forma:

![](../.gitbook/assets/image\(25\).png)
{% endstep %}

{% step %}
### Enviar al cliente a la etapa Agendados

Una vez creada la cita exitosamente, debes ejecutar la función **Cambiar de etapa a Agendados**. Recuerda colocar la función ‘Cambio de etapa’.

Esto permite que el cliente:

* Reciba recordatorios.
* Pueda reagendar o cancelar.
* Consulte información de su cita desde el asistente correspondiente.

![](../.gitbook/assets/image\(27\).png)
{% endstep %}
{% endstepper %}

***

## Resumen final

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
