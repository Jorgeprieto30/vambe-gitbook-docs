# Llamadas con IA

### ¿Para qué sirve esta función?

Vambe Phone te permite realizar y recibir llamadas con tus contactos directamente desde Vambe, potenciadas por un asistente de IA. En lugar de necesitar un equipo de agentes humanos para hacer seguimiento masivo, la IA puede contactar a cientos de leads de forma automática, calificar su interés, agendar citas y registrar cada interacción — todo sin intervención manual.

El asistente de voz opera igual que el asistente de chat: su comportamiento lo define la etapa del embudo en la que se encuentra el ticket al momento de la llamada.

{% hint style="info" %}
💡 **¿Cuándo usar llamadas con IA?** Es especialmente útil para campañas de reactivación, seguimientos post-formulario, confirmación de citas o cualquier flujo donde el contacto rápido y a escala marque la diferencia.
{% endhint %}

***

### ¿Qué puedes lograr?

* **Escalar el contacto inicial** sin ampliar tu equipo: llama a cientos de leads en minutos.
* **Automatizar seguimientos** usando Workflows para gatillar llamadas al instante cuando entra un lead.
* **Monitorear cada interacción** con transcripción automática, resumen de la llamada, grabación de audio y análisis de satisfacción.
* **Controlar horarios y reintentos** para proteger la reputación de tu empresa frente a llamadas fuera de horario.

***

### Requisitos previos

Antes de usar llamadas con IA, necesitas tener un número de teléfono activo en Vambe Phone y configurarlo correctamente.

#### Configurar tu teléfono

1. Ve a **Canales → Teléfonos** en el menú lateral.
2. Haz clic en el ícono de edición junto al número que quieres configurar.
3. En el panel de configuración, ajusta los siguientes campos:

| Campo                  | Descripción                                                                                                          |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Asociar a canal**    | Define qué embudo recibirá los contactos entrantes de este número. Si el contacto no existe, se creará en ese canal. |
| **Llamadas entrantes** | Activa este toggle para que el número también pueda recibir llamadas.                                                |
| **Llamadas con IA**    | Selecciona la voz que usará tu asistente (Fernanda, Pablo, Tomás, Valeria, Ana María, Sofía, entre otras).           |
| **Mensaje de inicio**  | El saludo por defecto que usará la IA al comenzar la llamada (puede sobreescribirse desde Campañas o Workflows).     |

> ⚠️ **Importante:** La voz y el mensaje de inicio configurados aquí son el valor por defecto. Si lanzas una campaña o un workflow con un mensaje distinto, ese mensaje sobreescribe el de la configuración del teléfono.

***

### Formas de activar una llamada con IA

Hay tres maneras de gatillar una llamada desde Vambe:

***

#### 1. Campaña masiva de llamadas

Úsala cuando quieras contactar a una lista grande de personas de forma simultánea.

1. Ve a **Canales → Campañas** y haz clic en **+ Crear campaña**.
2.  Selecciona el tipo **Llamadas con IA**.\
    <br>

    <figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>
3. Completa los campos del formulario:

**Campos obligatorios:**

* **Teléfono Vambe:** el número desde el que se realizarán las llamadas.
* **Etapa de entrada (opcional):** la etapa del embudo a la que entrará el ticket. Esto determina qué asistente manejará la llamada.
* **Primer mensaje (opcional):** el mensaje de inicio de la llamada. Puedes agregar variables dinámicas (nombre del contacto, empresa, etc.) con el botón **Agregar Variable**.

<figure><img src="../.gitbook/assets/image (73).png" alt=""><figcaption></figcaption></figure>

**Carga de contactos:**

* **Excel:** descarga la plantilla de ejemplo, complétala y cárgala.
* **Contactos en Vambe:** filtra contactos existentes con las vistas del embudo.

4. Expande **Configuración Avanzada** para ajustar:

| Parámetro                            | Descripción                                         |
| ------------------------------------ | --------------------------------------------------- |
| **Máximo de Reintentos**             | Cuántas veces intentará llamar si no hay respuesta. |
| **Minutos Entre Reintentos**         | Tiempo de espera entre cada intento.                |
| **Inicio / Fin Horario de Llamadas** | Rango horario en que se permitirán las llamadas.    |
| **Duración Máxima de Llamada**       | Límite en minutos por llamada.                      |

{% hint style="danger" %}
⚠️ **Configura siempre el horario de llamadas.** Las campañas intentan paralelizar las llamadas al máximo, por lo que sin un límite horario podrías estar contactando clientes a horas inapropiadas. Recomendamos un rango de 9:00 AM a 7:00 PM.
{% endhint %}

5. Haz clic en **Crear** y luego en **Enviar** para lanzar la campaña.

<figure><img src="../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

***

#### 2. Workflow automático

Úsala cuando quieras que la IA llame automáticamente al cumplirse una condición (por ejemplo, cuando un lead entra a una etapa específica).

1. Ve a **Workflows → Flows** y crea o edita un flow existente.
2. Agrega la acción **Activar llamada IA**.
3. Configura:
   * **Teléfono de voz:** el número desde el que se realizará la llamada.
   * **Primer mensaje (opcional):** mensaje de inicio personalizado.
   * **Duración máxima:** límite en minutos.

**Ejemplo de reintento automático con Workflows:**

Si quieres reintentar la llamada cuando no hay respuesta, agrega una **Condición** posterior a la acción de llamada que evalúe el estado de la llamada. Si el estado es `fallida`, conecta esa rama a una nueva acción **Activar llamada IA**.

{% hint style="info" %}
💡 En Workflows tienes control total sobre los **reintentos** y la lógica de ramificación, lo que te da más flexibilidad que en campañas.
{% endhint %}

***

#### 3. Llamada manual desde el ticket

Úsala cuando un agente humano quiera pedirle a la IA que llame a un contacto específico, directamente desde el chat.

1. Abre el ticket del contacto en el embudo.
2. Haz clic en el ícono de llamada en la barra superior del ticket.
3. En el panel **Opciones de Llamada**, selecciona el número de Vambe y haz clic en el ícono de **Llamar con IA** (ícono de robot).
4. La IA iniciará la llamada de inmediato.

<figure><img src="../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

***

### Qué pasa después de la llamada

Cada llamada queda registrada en el ticket del contacto. Al abrirla, verás:

* **Transcripción:** el diálogo completo entre la IA y el cliente, con timestamps por turno.
* **Resumen:** un resumen automático generado por IA sobre qué ocurrió en la llamada.
* **Resultado:** si el objetivo de la llamada se logró, fue parcial o no se logró.
* **Calificación de satisfacción:** evaluación automática de la experiencia del cliente (escala 1–5).
* **Grabación de audio:** reproducible directamente desde el ticket para auditoría y mejora de calidad.

***

### Métricas de la campaña

Al ingresar a una campaña de llamadas, la pestaña **Métricas** te muestra:

| Métrica                                    | Descripción                                                           |
| ------------------------------------------ | --------------------------------------------------------------------- |
| **Total Contacts / Calls Made / Answered** | Embudo de alcance de la campaña con porcentajes.                      |
| **Tasa de Conversión**                     | % de contactos que lograron el objetivo definido.                     |
| **Estado de Llamadas**                     | Desglose por estado: Completed, No-Answer, Failed, In-Progress, Busy. |
| **Duración Promedio**                      | Distribución de duración de llamadas (P25, P50, P75).                 |
| **Satisfacción**                           | Promedio de calificación IA en escala 1–5.                            |
| **Efectividad de Reintentos**              | % de éxito en primer intento vs. reintentos.                          |
| **Logro de Objetivo**                      | Desglose entre Logrado, Parcial y No Logrado.                         |

***

### Configuración del asistente de voz

El asistente que maneja la llamada es el mismo que está asignado a la etapa del embudo donde entra el ticket. La lógica de configuración es idéntica a la del asistente de chat:

* Define el **objetivo** de la llamada con claridad (ej: "agendar una demo", "confirmar interés", "inscribir en lista de espera").
* Usa un **formato breve** en las instrucciones: en voz, respuestas largas generan fricción.
* Puedes usar **funciones** (como cambiar etapa, crear tarea, etc.) igual que en chat.

> 💡 Para llamadas, se recomienda indicar explícitamente en el asistente que se trata de un canal de voz y que las respuestas deben ser concisas y naturales.

***

### Preguntas frecuentes

**¿La IA puede recibir llamadas entrantes?** Sí, si activas el toggle de **Llamadas entrantes** en la configuración del teléfono. El asistente asignado a la etapa del ticket manejará la llamada.

**¿Qué pasa si el contacto no existe en Vambe al recibir una llamada entrante?** Se crea automáticamente un nuevo contacto en el canal asociado al número.

**¿Puedo usar variables personalizadas en el mensaje de inicio?** Sí, tanto en campañas como en workflows puedes agregar variables dinámicas desde el botón **Agregar Variable**.

**¿Las llamadas desde workflows tienen las mismas métricas que las campañas?** Las transcripciones, resúmenes y grabaciones están disponibles a nivel de ticket. Las métricas agregadas (tasa de conversión, efectividad de reintentos) aplican solo a campañas.
