# Correcciones: enseña a tu asistente con ejemplos reales

Las **correcciones** son ejemplos concretos que le muestran a tu asistente cómo debe responder en una situación específica. Cada corrección toma un mensaje real de un cliente, la respuesta que dio la IA y la respuesta que debió dar, junto con una nota opcional que explica el porqué. Cuando llega una conversación parecida, el asistente recibe ese ejemplo como referencia y responde de la forma correcta.

Su gran ventaja es la precisión: Vambe no le entrega al asistente todas las correcciones que tienes guardadas, sino solo las que realmente se parecen a lo que está preguntando el cliente en ese momento. Así puedes acumular muchas correcciones sin que interfieran en conversaciones que no tienen relación con ellas. En este artículo verás cómo se eligen, cómo revisarlas en cada mensaje y cómo se crean.

> Para revisarlas: abre una conversación atendida por un asistente (o una prueba en el **Playground**) y haz clic en el ícono de actividad que aparece junto a cualquier mensaje. Se abrirá el **Monitor de Actividad** al costado derecho.

***

## Cómo se eligen las correcciones para cada mensaje

Cada vez que el asistente va a responder, Vambe toma los últimos mensajes del cliente y los compara con todas las correcciones del asistente. A cada corrección le asigna un puntaje de **relevancia** entre 0 y 1, según qué tanto se parece su caso al de la conversación actual.

Solo las correcciones que superan la **relevancia mínima de 0,6** se le entregan al asistente. El resto se descarta para ese mensaje, por lo que no influye en la respuesta.

Por ejemplo, si un asistente tiene 200 correcciones y un cliente pregunta si puede arrendar una raqueta de tenis en el club, Vambe puede encontrar dos que superan el umbral: una con relevancia 0,88 (otro cliente que hizo exactamente la misma pregunta) y otra con relevancia 0,78 (un cliente que preguntó por arriendo de raquetas y pelotas al reservar cancha). Las otras 198, que tratan temas distintos, quedan fuera.

{% hint style="info" %}
Como la búsqueda se hace por similitud con el mensaje del cliente, las correcciones funcionan mejor cuando cada una resuelve un caso concreto. Una corrección clara y específica tiene más probabilidades de activarse justo cuando corresponde.
{% endhint %}

***

## Cómo ver qué correcciones usó el asistente

En el **Monitor de Actividad** puedes revisar paso a paso qué tuvo en cuenta el asistente antes de responder un mensaje. Además del asistente y el modelo que respondieron, verás la sección **Correcciones seleccionadas**, que muestra:

* **Cuántas correcciones superaron la relevancia mínima**, sobre el total que tiene el asistente (por ejemplo, "2 de 200 correcciones superaron la relevancia mínima (0.6)").
* **Mensajes del cliente usados para buscar**: los mensajes de la conversación que Vambe utilizó para encontrar correcciones parecidas.
* **Cada corrección seleccionada**, con su puntaje de relevancia, el mensaje del cliente, la respuesta original de la IA (tachada), la respuesta corregida y, cuando existe, una nota en cursiva con el contexto que explica la corrección.

Al final del recorrido aparece el **Mensaje enviado**, para que puedas comparar lo que el asistente recibió como referencia con lo que finalmente respondió.

Esta vista es especialmente útil cuando una respuesta no es la que esperabas: te permite confirmar si el asistente tenía una corrección relevante disponible o si el caso aún no está cubierto.

***

## Cómo se crean las correcciones

Las correcciones se crean a partir de conversaciones reales en las que la IA no respondió como debía, con ayuda de **PandAI**. Desde el mensaje con el error, abre **Soporte con IA**, indica qué salió mal y pídele a PandAI que lo analice. Cuando el caso se resuelve mejor con un ejemplo concreto, PandAI te recomendará crear una corrección a partir de esa conversación.

De esta forma, cada corrección nace de un caso real, con la respuesta esperada y su contexto bien redactados, lo que permite que el asistente la encuentre y la aplique cuando aparezca una situación parecida.

{% hint style="info" %}
👉 Revisa el paso a paso en [**Cómo corregir a la IA cuando se equivoca en una conversación**](https://academy.vambe.ai/pandai/como-corregir-a-la-ia-cuando-se-equivoca-en-una-conversacion).
{% endhint %}

***

## En resumen

Las correcciones convierten cada error de la IA en un aprendizaje concreto. Se crean desde la conversación con apoyo de PandAI, se aplican solo cuando el mensaje del cliente se parece de verdad al caso corregido y quedan registradas en el Monitor de Actividad, para que siempre sepas qué tuvo en cuenta tu asistente antes de responder.
