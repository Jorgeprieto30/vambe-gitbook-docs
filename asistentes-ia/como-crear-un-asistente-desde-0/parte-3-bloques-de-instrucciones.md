---
description: >-
  Defina el comportamiento de su asistente. Aprenda a configurar los Bloques de
  Instrucciones (Pasos a seguir, Casos Posibles, No hacer y Etiquetas) para
  guiar a la IA y controlar el flujo.
---

# Parte 3: Bloques de Instrucciones

Una vez que la Inteligencia Artificial tiene definida su personalidad y objetivos (Bloques de Identidad), es momento de establecer las reglas del juego. Los **Bloques de Instrucciones** le indican a la IA exactamente qué debe hacer, en qué orden hacerlo y qué escenarios debe evitar por completo.

A continuación, analizaremos los cuatro bloques fundamentales que controlan el flujo de la conversación:

***

#### 1. Pasos a seguir (La columna vertebral)

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Este es el bloque **más importante de su asistente**. Representa la **ruta principal** que usted desea que recorran todos los clientes (por ejemplo, el proceso lineal para calificar a un prospecto o realizar una venta).

Se estructura mediante una secuencia lógica y ordenada (Paso 1, Paso 2, Paso 3) y permite el uso de subpasos (1.1, 2.1) para ramificar la conversación.

**Regla de Oro: La Secuencialidad** Para que la IA **no se salte preguntas ni envíe toda la información de golpe**, las instrucciones deben estar condicionadas al paso anterior.

* **Paso 1:** Saludar amablemente al cliente y preguntarle su nombre.
* **Paso 2:&#x20;**_**Únicamente** una vez que tengas su nombre_, debes preguntarle en qué producto está interesado.

**Uso de Funciones en los Pasos** Dentro de este flujo, usted puede ordenar a la IA que ejecute acciones técnicas. La más común es el [**Cambio de Etapa**](../funciones/como-cambiar-un-ticket-de-una-etapa-a-otra-de-forma-automatica.md). Por ejemplo:

* _Subpaso 2.1:_ Si el requerimiento del cliente es Venta, debes ejecutar la función Cambiar etapa a Venta.
* _Subpaso 2.2:_ Si el requerimiento es Servicio al cliente, debes ejecutar la función Cambiar etapa a Servicio al cliente.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
⚠️ **Importante**: Para que estas acciones se cumplan, debe asegurarse de agregar correctamente la función utilizando el botón "**+ Agregar función**". 👉 [**\[Visite la sección de Funciones aquí para más detalles\]**](/broken/pages/KsYXjY1ljbT0miwhmAIg)
{% endhint %}

**¿Cuándo usar más de un Asistente?** Si nota que sus "Pasos a seguir" se vuelven excesivamente largos o complejos (por ejemplo, intentando que un solo asistente califique, venda, cobre y agende), la IA podría confundirse. En estos casos, la mejor práctica es dividir el flujo creando múltiples asistentes. Un "Asistente Inicial" puede encargarse de la derivación, enviando al cliente mediante un Cambio de Etapa a un "Asistente de Ventas" dedicado exclusivamente a esa labor.

**¿Que no se debe colocar en los pasos a seguir?** Nunca debes colocar acciones por tiempo, por ejemplo "Si el cliente no contesta en 5 minutos" o "despues de 10 minutos vuelve a enviar mensaje" ya que los **pasos a seguir y casos posibles** **responden a mensajes del cliente, no al tiempo transcurrido.** Para enviar mensajes de seguimiento por tiempo debes revisar las [secuencias](https://academy.vambe.ai/workflows/secuencias/como-automatizar-seguimientos-y-tareas-usando-secuencias)

***

#### 2. Casos Posibles (Las excepciones a la regla)

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Si los "Pasos a seguir" son la ruta principal, los **Casos Posibles son los desvíos.** Sirven para atender situaciones específicas que no aplican a todos los clientes, pero que pueden ocurrir en cualquier momento (ej: un reclamo, una pregunta sobre empleo, o un cliente que solicita hablar con un humano).

Este bloque no utiliza pasos secuenciales; funciona bajo una lógica directa de **Causa y Efecto** dividida en dos columnas:

* **Lado Izquierdo (El Gatillante):** Define la condición. _Ejemplo:_ "Si el cliente pregunta por el estado de su pedido".
* **Lado Derecho (La Acción):** Define qué debe hacer la IA. _Ejemplo:_ "Ejecuta la función Get Order Status" o "Deriva a asistencia humana".

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

***

#### 3. No Hacer (Las restricciones absolutas)

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Este bloque es una medida de seguridad crítica. Aquí se listan las acciones que la Inteligencia Artificial tiene estrictamente prohibido realizar.

**Casos de uso comunes:**

* **Clasificación silenciosa:** Usted puede pedirle a la IA que clasifique internamente a los clientes en categorías (A, B o C) según su presupuesto, pero en este bloque debe indicarle: _"NUNCA le digas al cliente en qué categoría fue clasificado"_.
* **Seguridad de datos:** _"No debes enviar datos bancarios de transferencia ni tampoco enviar números de contacto que no estén en tu base de información"_.
* **Prevención de errores:** _"NUNCA debes inventar información"_, _"NO ofrezcas descuentos que no aparecen explícitamente en tu base"_.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

***

#### 4. Etiquetas (Clasificación automática)

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

El bloque de Etiquetas permite automatizar la segmentación de sus contactos y tickets en el CRM, facilitando el orden y la futura creación de campañas.

Al igual que los Casos Posibles, se divide en dos secciones:

* **Lado Izquierdo:** Se seleccionan las etiquetas previamente creadas en el sistema (Ej: "Pequeño", "Mediano", "Grande", o "Santiago").
* **Lado Derecho (Descripción):** Se redacta la instrucción de cuándo la IA debe aplicar dichas etiquetas. _Ejemplo:_ "Debes etiquetar al cliente si dice que es de Santiago" o "Si la cantidad es entre 1 a 3 debes usar Pequeño".

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

***

Con los bloques de Instrucciones configurados, su asistente ya sabe cómo guiar una venta y qué reglas respetar. El último paso es dotarlo de conocimiento para que pueda responder preguntas técnicas.
