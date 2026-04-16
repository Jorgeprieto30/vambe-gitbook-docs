---
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Paso 3: Crear el asistente Agendados

En este artículo aprenderás a crear y configurar el asistente de **Agendados**, el cual se encarga de atender a clientes que **ya tienen una cita creada** y escriben para:

* Confirmar su cita
* Reagendar
* Cancelar
* Consultar información sobre su hora, profesional o tratamiento
* Responder luego de un recordatorio o confirmación automática

Este asistente es clave para mantener una buena experiencia post-agendamiento.

Antes de comenzar

* Haber creado las etapas del embudo:
  * Información y dudas generales
  * Agendamiento
  * Agendados
  * Ayuda humana\
    (Referencia [aquí](https://academy.vambe.ai/paso-0-crear-las-etapas))
* Haber creado y configurado:
  * [El asistente Información y dudas generales](https://academy.vambe.ai/paso-1-c%C3%B3mo-crear-tu-primer-asistente-de-agendamiento)
  * [El asistente Agendamiento](https://academy.vambe.ai/paso-1-c%C3%B3mo-crear-tu-primer-asistente-de-agendamiento)

El asistente que construiremos en este artículo se asigna **exclusivamente a la etapa Agendados**.

{% hint style="info" %}
Consideración clave: este asistente NO tiene “Pasos a seguir”\
El asistente Agendados no debe tener un bloque de “Pasos a seguir”. Los clientes en esta etapa no siguen un único flujo lineal; llegan con múltiples intenciones (cancelar, reagendar, confirmar, consultar). Por eso este asistente funciona principalmente mediante **bloques de Casos posibles**.
{% endhint %}

{% stepper %}
{% step %}
### Paso 1: Crear el asistente

1. Ve al menú lateral izquierdo y entra en **Asistentes**.
2. Haz clic en **Crear asistente** (arriba a la derecha).

![](../.gitbook/assets/image\(2\).png)

3. Asigna un **nombre claro** (por ejemplo: _Info y dudas generales_).
4. Selecciona el modelo de inteligencia artificial recomendado según tu plan.
5. Haz clic en **Crear asistente**.

Una vez creado, comenzaremos a configurar sus bloques.\
Si ya tienes tu asistente creado, debes acceder a él [aquí](https://academy.vambe.ai/c%C3%B3mo-ingresar-al-asistente-de-inteligencia-artificial?hsLang=es)
{% endstep %}

{% step %}
### Paso 2: Configurar los bloques de identidad

#### Bloque de Personificación (bloque compartido)

* Agrega un bloque de tipo **Personificación**.
* Selecciona el **mismo bloque** utilizado en los asistentes anteriores.

Esto asegura consistencia en el tono, estilo y personalidad del asistente en todo el embudo.

#### Bloque de Objetivo (bloque nuevo)

Crea un nuevo bloque de tipo **Objetivo** con los siguientes puntos:

* **Atender a clientes ya agendados**, respondiendo consultas sobre su cita (fecha, horario, doctor, estado) mediante la validación del RUT y la búsqueda de información del paciente.
* **Gestionar correctamente el estado de la cita**, confirmándola cuando el cliente lo indique y guiando el proceso de cancelación o reprogramación según la intención expresada.
* Derivar de forma controlada a Agendamiento, enviando al cliente a la etapa correspondiente cuando quiera agendar una nueva cita, evitando reprocesos o conflictos con citas existentes.

![](<../.gitbook/assets/image png Dec 22 2025 02 47 28 0363 PM.png>)

{% hint style="warning" %}
Este asistente **no agenda nuevas citas desde cero**. Si un cliente desea agendar una nueva cita, debe ser derivado al asistente de **Agendamiento**.
{% endhint %}

#### Bloque de Formato de respuesta (bloque compartido)

* Agrega un bloque de **Formato de respuesta**.
* Selecciona el mismo bloque usado en los asistentes anteriores.

Con esto finalizamos los bloques de identidad.
{% endstep %}

{% step %}
### Paso 3: Configurar los bloques de instrucción

#### Bloque de Casos posibles “Todos” (bloque compartido)

* Agrega el bloque **Todos**, que debe existir en todos los asistentes.
* Cubre situaciones como dudas muy complejas, solicitud explícita de hablar con una persona y casos sensibles o urgentes.

Acción: Ejecutar la función **Cambiar de etapa a Ayuda humana**, informando que un agente continuará la atención en horario hábil.

#### Bloque de Casos posibles “Casos: Agendados” (bloque nuevo)

Este es el bloque más importante de este asistente.

Nombre del bloque: **Casos: Agendados**

Lado izquierdo (condiciones):

* El cliente quiere cancelar su cita.
* El cliente quiere reagendar su cita.
* El cliente pregunta por la hora, fecha o profesional de su cita.
* El cliente quiere confirmar su cita.
* El cliente pregunta por información relacionada a una cita ya existente.
* El cliente quiere agendar una nueva cita (teniendo ya una previa).

Lado derecho (acciones):

* Ejecutar funciones correspondientes para:
  * Obtener información del cliente o de la cita.
  * Cambiar estado de la cita (confirmar / cancelar).
  * Reagendar según corresponda.
* Si el cliente quiere **agendar una nueva cita**, ejecutar la función **Cambiar de etapa a Agendamiento**.

Es fundamental que las funciones estén correctamente creadas y asociadas a cada caso, siguiendo la estructura recomendada como se muestra en las imágenes:

![](/broken/files/7e3c0028f24ceba60521e6413b32abf90d27c3f2)

![](<../.gitbook/assets/image png Dec 22 2025 02 49 19 0965 PM.png>)

![](<../.gitbook/assets/image png Dec 22 2025 02 49 41 0936 PM.png>)

![](<../.gitbook/assets/image png Dec 22 2025 02 49 54 5815 PM.png>)

#### Bloque “No hacer” (bloque compartido)

* Agrega el bloque compartido de **No hacer**, que define los límites del asistente.

Ejemplos:

* No confirmar citas nuevas.
* No inventar información.
* No prometer resultados médicos.
* No entregar diagnósticos.
{% endstep %}

{% step %}
### Paso 4: Bloques de información

Agrega los mismos bloques de información utilizados en los asistentes anteriores, por ejemplo:

* Tratamientos
* Especialistas
* Propuesta de valor
* Información general del negocio

{% hint style="danger" %}
No agregues el bloque “Aplicaciones de reserva” en este asistente.\
El asistente **Agendados no agenda nuevas citas**. Para eso, siempre debe derivar al asistente de **Agendamiento**.
{% endhint %}

Así se verá una vez agregados todos los bloques:

![](<../.gitbook/assets/image png Dec 22 2025 02 52 16 8660 PM.png>)
{% endstep %}

{% step %}
### Paso 5: Guardar y asignar el asistente a la etapa Agendados

1. Haz clic en **Guardar** dentro del asistente.
2. Ve al **Embudo**.
3. En la etapa **Agendados**, haz clic en la tuerca (configuración).
4. Selecciona **Editar etapa**.
5. Desactiva el switch **Etapa humana**.
6. Selecciona el asistente **Agendados**.
7. Guarda los cambios y vuelve al embudo.

Si tienes dudas de cómo asignar el asistente a una etapa, lee:\
https://academy.vambe.ai/c%C3%B3mo-asignar-un-asistente-de-inteligencia-artificial-a-una-etapa-del-embudo?hsLang=es

✅ Listo.\
Ya tienes configurado el asistente **Agendados**, preparado para gestionar confirmaciones, reagendamientos, cancelaciones y consultas posteriores a la cita.

Como siguiente paso recomendado, revisa:

* Configuración de notificaciones y recordatorios: https://academy.vambe.ai/paso-1-configuraciones-recordatorio
{% endstep %}
{% endstepper %}
