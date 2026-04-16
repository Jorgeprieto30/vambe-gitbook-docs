---
description: >-
  Evita respuestas automáticas incómodas. Configura a tu Asistente IA para que
  ignore reacciones, emojis o elogios cortos a tus historias de Instagram sin
  cortar la conversación.
---

# ¿Cómo evitar que la IA responda a las reacciones en Instagram?

Cuando conectas tu cuenta de Instagram a Vambe, es muy común que tus clientes reaccionen a tus Historias (Stories) con un simple emoji (🔥, 😍, 👏) o un elogio corto.

Por defecto, la Inteligencia Artificial intentará ser educada y responder a esa interacción, lo que puede generar una conversación forzada o poco natural. Para solucionar esto, usaremos un "truco" en el bloque de Casos Posibles para obligar a la IA a guardar silencio ante estas reacciones.



***

#### Configuración Paso a Paso

Sigue estos pasos para crear esta regla de excepción en tu bot:

**Paso 1: Ingresar al Asistente**

1. Ve al menú [Asistente](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md) en la barra lateral izquierda.
2. Selecciona el asistente que está conectado a tu canal.
3. Haz clic en **+ Agregar otro bloque** (si no lo tienes) y selecciona **Casos Posibles**, o entra al que ya tienes creado.

**Paso 2: La Condición (Lado Izquierdo)**

En el recuadro de la izquierda, debes explicarle a la IA exactamente qué tipo de comportamiento debe identificar como una simple "reacción".

Copia y pega este texto exacto:

> **Si el cliente reacciona desde Instagram con un solo emoji o envía un mensaje elogiando a la empresa, considera que está mostrando una reacción positiva o emocional. Esto aplica cuando el cliente envía cualquiera de los siguientes emojis: 🥹 (emotivo) 😯 (sorprendido) 😍 (enamorado / encantado) 😂 (divertido) 👏 (aplauso / aprobación) 🔥 (entusiasmo / emoción)**

**Paso 3: La Acción de Silencio (Lado Derecho)**

En el recuadro de la derecha (donde le decimos a la IA qué hacer), vamos a darle una instrucción estricta para que responda con un "espacio en blanco".

Copia y pega este texto (asegúrate de incluir los espacios en blanco entre las comillas):

> **SIEMPRE responde el siguiente texto: "                      "**

_**¿Por qué hacemos esto?**_ Al obligar a la IA a responder solo con un espacio vacío, el sistema detecta que no hay un mensaje real que enviar y, en la práctica, la IA no le enviará nada al cliente, dejándolo en "visto" de forma natural.

**Paso 4: Verificación Visual**

Asegúrate de que tu bloque de Casos Posibles se vea exactamente como en este ejemplo, con la condición a la izquierda y el texto en blanco a la derecha. Luego, haz clic en Guardar (botón azul abajo a la derecha).

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
