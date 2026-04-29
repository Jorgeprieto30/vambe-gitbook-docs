# ¿Cómo corregir a la IA cuando se equivoca en una conversación?

Cuando la inteligencia artificial comete un error en una conversación real con un cliente —por ejemplo, entrega un dato incorrecto, responde algo fuera de contexto, interpreta mal una intención, o genera una **alucinación** definida por Vambe— puede corregirla directamente desde esa misma conversación utilizando PandaAI. Este proceso es rápido, guiado y permite mejorar el comportamiento del asistente sin tener que buscar el bloque manualmente.

{% stepper %}
{% step %}
### Ubicar el mensaje que contiene el error

Dentro del ticket, identifica el mensaje enviado por la IA que deseas corregir.

A la izquierda de ese mensaje verás un ícono de **estrellitas**. Haz clic en esas estrellitas.

![Ícono de estrellitas](<../.gitbook/assets/image png Dec 02 2025 02 06 15 1958 PM.png>)
{% endstep %}

{% step %}
### Indicarle a PandaAI qué estuvo mal

Al hacer clic, se abrirá una ventana donde podrás escribirle a PandaAI detallando lo que ocurrió.

PandaAI ahora tiene una comprensión mejorada de las **alucinaciones**, entendiendo que son respuestas fuera de los parámetros definidos por los `guard rails` del asistente. Puede indicarle, por ejemplo:

*   “La IA entregó información incorrecta o inventada.”
*   “El asistente recomendó un producto que no ofrecemos (una alucinación).”
*   “Respondió algo que no correspondía a la pregunta, ignorando un `guard rail` clave.”
*   “Quiero saber de dónde sacó esta información.”
*   “La IA omitió un paso importante del flujo.”

Mientras más claro sea, mejor será la sugerencia que PandaAI podrá darte.

{% hint style="info" %}
Ejemplo: describe qué parte fue incorrecta, por qué lo es y, si es posible, qué respuesta esperabas. Esto ayuda a que PandaAI identifique el bloque (incluyendo los `guard rails` en "No Hacer") y proponga correcciones más precisas para evitar futuras **alucinaciones**.
{% endhint %}

![Ventana para escribir a PandaAI](<../.gitbook/assets/image png Dec 02 2025 02 07 49 3305 PM.png>)
{% endstep %}

{% step %}
### PandaAI analiza y propone correcciones

Una vez envías tu comentario, se abrirá un chat con PandaAI.

Ahí verás:

*   La explicación del error.
*   De dónde tomó la información el asistente (si lo preguntas).
*   Qué bloque podría estar generando el problema (ahora con mayor énfasis en la configuración de `guard rails` y "No Hacer").
*   Recomendaciones específicas para corregirlo.
*   Opciones sugeridas para reescribir el prompt afectado.

PandaAI revisa el comportamiento del asistente y te guía para dejar la instrucción correcta.

![Chat con PandaAI mostrando análisis y sugerencias](<../.gitbook/assets/image png Dec 02 2025 02 09 03 1520 PM.png>)
{% endstep %}

{% step %}
### Aplicar las mejoras sugeridas

PandaAI puede:

*   Redactar una versión mejorada del bloque.
*   Señalar instrucciones contradictorias.
*   Detectar carencias en los Pasos a Seguir o Casos Posibles.
*   Indicar si falta metadata, información o un bloque clave, o si un `guard rail` necesita ser ajustado.

Luego solo debes copiar la corrección y pegarla en el bloque correspondiente del asistente.
{% endstep %}
{% endstepper %}

<details>

<summary>¿Para qué sirve este proceso?</summary>

*   Detectar errores que no se ven a simple vista, incluyendo las **alucinaciones** según la definición de Vambe.
*   Mejorar el asistente mientras los clientes interactúan, fortaleciendo sus **`guard rails`**.
*   Evitar respuestas incorrectas y **alucinaciones** en el futuro.
*   Mantener la coherencia del flujo sin perder tiempo revisando todo.

PandaAI actúa como un supervisor del asistente, ayudándote a perfeccionarlo conversación por conversación y a asegurar el cumplimiento de sus **`guard rails`** para minimizar las **alucinaciones**.

</details>
