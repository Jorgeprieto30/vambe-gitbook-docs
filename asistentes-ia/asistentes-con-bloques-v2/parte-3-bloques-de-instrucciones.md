---
description: >-
  Asistente con Bloques (V2). Configure los Bloques de Instrucciones (Pasos a
  seguir, Casos Posibles, No hacer y Etiquetas) para guiar a la IA y controlar
  el flujo.
---

# Parte 3: Bloques de Instrucciones

{% hint style="warning" %}
**Este artículo corresponde al Asistente con Bloques (V2), la versión anterior de los Asistentes IA de Vambe.**

Los bloques de Pasos a seguir y Casos Posibles existen únicamente en los asistentes V2. En los **Asistentes con Escenarios (V3)** el flujo de la conversación se define mediante Escenarios y Rutas.

[Conocer los Asistentes con Escenarios (V3)](../asistentes-con-escenarios-v3/asistentes-con-escenarios-v3-que-son-y-cuando-usarlos.md)
{% endhint %}

Una vez que la Inteligencia Artificial tiene definida su personalidad y objetivos (Bloques de Identidad), es momento de establecer las reglas del juego. Los **Bloques de Instrucciones** le indican a la IA exactamente qué debe hacer, en qué orden hacerlo y qué escenarios debe evitar por completo.

A continuación, analizaremos los cuatro bloques fundamentales que controlan el flujo de la conversación:

***

#### 1. Pasos a seguir (La columna vertebral)

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2F8cgKywNCSz0T9BXRKFJT%2Fimage.png?alt=media&#x26;token=9c9bcb23-8dd3-4d2e-ac62-85f6d32492fc" alt=""><figcaption></figcaption></figure>

Este es el bloque **más importante de su asistente**. Representa la **ruta principal** que usted desea que recorran todos los clientes (por ejemplo, el proceso lineal para calificar a un prospecto o realizar una venta).

Se estructura mediante una secuencia lógica y ordenada (Paso 1, Paso 2, Paso 3) y permite el uso de subpasos (1.1, 2.1) para ramificar la conversación.

**Regla de Oro: La Secuencialidad** Para que la IA **no se salte preguntas ni envíe toda la información de golpe**, las instrucciones deben estar condicionadas al paso anterior.

* **Paso 1:** Saludar amablemente al cliente y preguntarle su nombre.
* **Paso 2:** _**Únicamente** una vez que tengas su nombre_, debes preguntarle en qué producto está interesado.

**Uso de Funciones en los Pasos** Dentro de este flujo, usted puede ordenar a la IA que ejecute acciones técnicas. La más común es el **Cambio de Etapa**. Por ejemplo:

* _Subpaso 2.1:_ Si el requerimiento del cliente es Venta, debes ejecutar la función Cambiar etapa a Venta.
* _Subpaso 2.2:_ Si el requerimiento es Servicio al cliente, debes ejecutar la función Cambiar etapa a Servicio al cliente.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FkVYrloV0PKilSoccoRDf%2Fimage.png?alt=media&#x26;token=288f5cc0-9175-4f96-b309-ea551dfaba7a" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
⚠️ **Importante**: Para que estas acciones se cumplan, debe asegurarse de agregar correctamente la función utilizando el botón "**+ Agregar función**". 👉 **\[Visite la sección de Funciones aquí para más detalles]**
{% endhint %}

{% hint style="info" %}
Las **Funciones son independientes de la versión del asistente**: están disponibles tanto en los asistentes V2 como en los Asistentes con Escenarios (V3), y se configuran de la misma forma.
{% endhint %}

**¿Cuándo usar más de un Asistente?** Si nota que sus "Pasos a seguir" se vuelven excesivamente largos o complejos (por ejemplo, intentando que un solo asistente califique, venda, cobre y agende), la IA podría confundirse. En estos casos, la mejor práctica es dividir el flujo creando múltiples asistentes. Un "Asistente Inicial" puede encargarse de la derivación, enviando al cliente mediante un Cambio de Etapa a un "Asistente de Ventas" dedicado exclusivamente a esa labor.

**¿Que no se debe colocar en los pasos a seguir?** Nunca debes colocar acciones por tiempo, por ejemplo "Si el cliente no contesta en 5 minutos" o "despues de 10 minutos vuelve a enviar mensaje" ya que los **pasos a seguir y casos posibles** **responden a mensajes del cliente, no al tiempo transcurrido.** Para enviar mensajes de seguimiento por tiempo debes revisar las [secuencias](https://academy.vambe.ai/workflows/secuencias/como-automatizar-seguimientos-y-tareas-usando-secuencias)

***

#### 2. Casos Posibles (Las excepciones a la regla)

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2Fs0u43g4jk8BpwJSdSrp4%2Fimage.png?alt=media&#x26;token=f3f137b7-7b84-4b21-b3ee-5ebefca2a974" alt=""><figcaption></figcaption></figure>

Si los "Pasos a seguir" son la ruta principal, los **Casos Posibles son los desvíos.** Sirven para atender situaciones específicas que no aplican a todos los clientes, pero que pueden ocurrir en cualquier momento (ej: un reclamo, una pregunta sobre empleo, o un cliente que solicita hablar con un humano).

Este bloque no utiliza pasos secuenciales; funciona bajo una lógica directa de **Causa y Efecto** dividida en dos columnas:

* **Lado Izquierdo (El Gatillante):** Define la condición. _Ejemplo:_ "Si el cliente pregunta por el estado de su pedido".
* **Lado Derecho (La Acción):** Define qué debe hacer la IA. _Ejemplo:_ "Ejecuta la función Get Order Status" o "Deriva a asistencia humana".

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FWPbkmNh1axRBN823TkDU%2Fimage.png?alt=media&#x26;token=af5adf0a-6062-4f1b-bb2f-3bc8b362d3ad" alt=""><figcaption></figcaption></figure>

***

#### 3. No Hacer (Las restricciones absolutas y `guard rails`)

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2Fy2iuBeYHPKS7gZtpJm5H%2Fimage.png?alt=media&#x26;token=1960f2f5-7ab0-4c60-b110-ada40e6aa235" alt=""><figcaption></figcaption></figure>

Este bloque es una medida de seguridad crítica. Aquí se listan las acciones que la Inteligencia Artificial tiene estrictamente prohibido realizar. Funciona como un **`guard rail`** esencial, estableciendo los límites y el comportamiento no deseado para su asistente. Esto es fundamental para prevenir **alucinaciones**, asegurando que la IA siempre se mantenga dentro de los parámetros de información y acción definidos por usted.

**Casos de uso comunes:**

* **Clasificación silenciosa:** Usted puede pedirle a la IA que clasifique internamente a los clientes en categorías (A, B o C) según su presupuesto, pero en este bloque debe indicarle: _"NUNCA le digas al cliente en qué categoría fue clasificado"_.
  * Este `guard rail` evita que la IA revele información interna que podría ser sensible o generar confusión, previniendo una alucinación por divulgación de datos internos.
* **Seguridad de datos:** _"No debes enviar datos bancarios de transferencia ni tampoco enviar números de contacto que no estén en tu base de información"_.
  * Un `guard rail` crucial para la privacidad y seguridad, deteniendo a la IA de inventar o compartir datos financieros.
* **Prevención de errores e información incorrecta:** _"NUNCA debes inventar información"_, _"NO ofrezcas descuentos que no aparecen explícitamente en tu base"_.
  * Estos `guard rails` son directrices explícitas para evitar las **alucinaciones** de la IA, asegurando que solo opere con datos verificados y permitidos.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FWPbkmNh1axRBN823TkDU%2Fimage.png?alt=media&#x26;token=af5adf0a-6062-4f1b-bb2f-3bc8b362d3ad" alt=""><figcaption></figcaption></figure>

***

#### 4. Etiquetas (Clasificación automática)

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FzyEd9dT3JLaUOVGeA5xd%2Fimage.png?alt=media&#x26;token=5ebdc839-4402-4618-a4b5-66df173e3fb1" alt=""><figcaption></figcaption></figure>

El bloque de Etiquetas permite automatizar la segmentación de sus contactos y tickets en el CRM, facilitando el orden y la futura creación de campañas.

Al igual que los Casos Posibles, se divide en dos secciones:

* **Lado Izquierdo:** Se seleccionan las etiquetas previamente creadas en Vambe (Ej: "Pequeño", "Mediano", "Grande", o "Santiago").
* **Lado Derecho (Descripción):** Se redacta la instrucción de cuándo la IA debe aplicar dichas etiquetas. _Ejemplo:_ "Debes etiquetar al cliente si dice que es de Santiago" o "Si la cantidad es entre 1 a 3 debes usar Pequeño".

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2Fc3917aQXiw24ch7Od3Nm%2Fimage.png?alt=media&#x26;token=a2fa6476-c343-4064-8a1d-fec4cd8f9343" alt=""><figcaption></figcaption></figure>

***

Con los bloques de Instrucciones configurados, su asistente ya sabe cómo guiar una venta y qué reglas respetar. El último paso es dotarlo de conocimiento para que pueda responder preguntas técnicas.
