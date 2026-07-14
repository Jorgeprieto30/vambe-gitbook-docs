---
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Paso 1: Cómo crear tu primer asistente de agendamiento

## Paso 1: Cómo crear tu primer asistente de agendamiento

En este artículo aprenderás a crear y configurar el **primer asistente de agendamiento**, enfocado en atender a clientes que llegan con dudas iniciales y guiarlos correctamente hasta el siguiente paso del embudo.

Antes de comenzar, asegúrate de que las **etapas del embudo ya estén creadas** (Información y dudas generales, Agendamiento, Agendados, Ayuda humana, etc.).

Este asistente será asignado a la **etapa inicial** del embudo.

***

### Crear el asistente

{% stepper %}
{% step %}
#### Crear asistente

1. Ve al menú lateral izquierdo y entra en **Asistentes**.
2. Haz clic en **Crear asistente** (arriba a la derecha).

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/SH2hfLIWWJlWMQmazf8y/image%20png%20Dec%2019%202025%2003%2009%2021%206278%20PM.png)

3. Asigna un **nombre claro** (por ejemplo: _Info y dudas generales_).
4. Selecciona el modelo de inteligencia artificial recomendado según tu plan.
5. Haz clic en **Crear asistente**.

Una vez creado, comenzaremos a configurar sus bloques.

Si ya tienes tu asistente creado, debes acceder a él: ["Cómo ingresar al asistente de Inteligencia Artificial"](https://academy.vambe.ai/asistentes-ia/como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial)
{% endstep %}
{% endstepper %}

Para agregar bloques debes ir en el menú de la izquierda y hacer click en "agregar bloque".

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/M05ZjSKjwi9gn1FfCPzO/image%20png%20Dec%2019%202025%2003%2021%2039%206207%20PM.png)

***

### Configurar los bloques de identidad

Los **bloques de identidad** definen quién es el asistente, qué debe lograr y cómo debe responder.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/Vj6XbLvxBvEJBrCwHsg5/image%20png%20Dec%2019%202025%2004%2056%2059%208074%20PM.png)

{% stepper %}
{% step %}
#### Personificación

Aquí defines **quién es el asistente** y cómo debe comportarse.

Ejemplo de enfoque:

* Asistente cordial, claro y profesional.
* Especialista en atención inicial y orientación al cliente.
* Lenguaje cercano y fácil de entender.

Este bloque marca el tono general de toda la conversación.
{% endstep %}

{% step %}
#### Objetivo

Define **qué debe lograr el asistente en esta etapa**.

Objetivo recomendado para este asistente inicial:

* Resolver dudas generales de los clientes sobre los servicios ofrecidos.
* Proveer información clara sobre especialistas y tratamientos disponibles.
* Orientar al cliente respecto a citas, horarios y próximos pasos.

👉 Importante: este asistente **no agenda directamente**, solo prepara al cliente para pasar a la etapa de agendamiento.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/plnFjwo43X6UqEan2nxq/image%20png%20Dec%2019%202025%2003%2023%2050%203952%20PM.png)
{% endstep %}

{% step %}
#### Formato de respuesta

Aquí defines **cómo debe responder** el asistente.

Ejemplos de decisiones habituales:

* Respuestas claras y ordenadas.
* Mensajes breves pero completos.
* Uso moderado de emojis (opcional).
* Preguntas de una en una para no confundir al cliente.

Con este bloque finalizamos los **bloques de identidad**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/5pz1dOL9k5ZWMuan0lTv/image%20png%20Dec%2019%202025%2003%2019%2057%207966%20PM.png)
{% endstep %}
{% endstepper %}

***

### Configurar los bloques de instrucción

Los bloques de instrucción indican **qué hacer y en qué orden**. Son la columna vertebral del comportamiento del asistente.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/QXlHshwkPW4XnqkHC19K/image%20png%20Dec%2019%202025%2004%2056%2012%203911%20PM.png)

{% stepper %}
{% step %}
#### “Pasos a seguir”

Este bloque define el flujo principal de conversación; aquí indicas a la IA las instrucciones que debe seguir.

Ejemplo de estructura para este bloque:

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/3QGI5dYOPZaMRztIOP6j/image%20png%20Dec%2019%202025%2004%2036%2035%200949%20PM.png)

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/rUNUf8uuG5ECjrkYJ2HK/image%20png%20Dec%2019%202025%2004%2037%2005%200380%20PM.png)
{% endstep %}

{% step %}
#### Caso posible: Paso a Agendados

Este bloque detecta clientes que **ya tienen una cita**.

**Nombre del bloque:** Paso a Agendados

**Lado izquierdo (condición):**

* El cliente dice que ya tiene una cita.
* Quiere reagendar.
* Quiere cancelar.
* Pregunta por información de su hora.

**Lado derecho (acción):**

* Ejecutar la función **Cambiar de etapa a Agendados**.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/4sn0ZiplVvt7Ma7zxIqN/image%20png%20Dec%2019%202025%2004%2039%2024%204825%20PM.png)
{% endstep %}

{% step %}
#### Caso posible: Todos

Este bloque debe existir **en todos los asistentes**.

**Nombre del bloque:** Todos

**Lado izquierdo (condición):**

* La duda es muy compleja.
* El cliente solicita hablar con una persona.
* El asistente detecta una urgencia o caso sensible.

**Lado derecho (acción):**

* Ejecutar la función **Cambiar de etapa a Ayuda humana**.
* Informar que un agente del equipo continuará la atención en horario hábil.

Este bloque actúa como **red de seguridad** para el asistente.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/hZY7JW4ZwrKnwoovTEW7/image%20png%20Dec%2019%202025%2004%2058%2012%203756%20PM.png)
{% endstep %}

{% step %}
#### “No hacer”

Aquí defines **límites claros** del asistente.

Ejemplos:

* No prometer resultados médicos.
* No entregar diagnósticos.
* No inventar precios.
* No confirmar citas directamente.

Este bloque reduce errores y alinea expectativas.

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/bvdVm9GMa5rka22s8BDF/image%20png%20Dec%2019%202025%2004%2044%2054%201435%20PM.png)
{% endstep %}
{% endstepper %}

***

### Bloques de información

En esta sección puedes agregar contenidos que el asistente consultará para responder correctamente:

* Información de tratamientos.
* Especialistas.
* Propuesta de valor.
* Cualquier dato relevante para las respuestas.

Una vez agregados todos los bloques se verá de la siguiente forma:

![](https://content.gitbook.com/content/hQjV55x4bDSryBoT4FYC/blobs/P1Vk1UvRmlNDsZnW7Q2Y/image%20png%20Dec%2019%202025%2005%2001%2054%205078%20PM.png)

***

### Guardar y asignar el asistente a la etapa

Sigue estos pasos para activar el asistente en la etapa inicial del embudo.

{% stepper %}
{% step %}
#### Guardar

1. Haz clic en **Guardar** dentro del asistente.
{% endstep %}

{% step %}
#### Ir al Embudo

2. Ve al **Embudo**.
{% endstep %}

{% step %}
#### Editar etapa inicial

3. En la etapa inicial, haz clic en la **tuerca (configuración)**.
4. Selecciona **Editar etapa**.
{% endstep %}

{% step %}
#### Desactivar etapa humana

5. Desactiva el switch **Etapa humana**.
{% endstep %}

{% step %}
#### Seleccionar asistente

6. Selecciona el asistente que acabas de crear.
{% endstep %}

{% step %}
#### Guardar cambios

7. Haz clic en **Guardar cambios** y luego en **Volver**.

✅ Tu primer asistente de agendamiento ya está activo en la etapa inicial del embudo.
{% endstep %}
{% endstepper %}

Siguiente paso: Asistente de Agendamiento — [Paso 2: Asistente Agendador](https://academy.vambe.ai/asistentes-agendamiento/parte-3-crear-plataforma-agendamiento/paso-2-asistente-agendador)

***

{% hint style="success" %}
Tu primer asistente de agendamiento ya está activo en la etapa inicial del embudo.
{% endhint %}
