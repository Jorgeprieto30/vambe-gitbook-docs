---
description: >-
  Asistente con Bloques (V2). Aprenda el modelo mental, la regla de los
  múltiples asistentes y cómo escribir instrucciones "a prueba de balas".
---

# Parte 1: La Mentalidad

{% hint style="warning" %}
**Este artículo corresponde al Asistente con Bloques (V2), la versión anterior de los Asistentes IA de Vambe.**

Los asistentes que se crean actualmente son los **Asistentes con Escenarios (V3)**. Los asistentes V2 existentes siguen funcionando con normalidad y no es necesario migrarlos.

[Conocer los Asistentes con Escenarios (V3)](../asistentes-con-escenarios-v3/asistentes-con-escenarios-v3-que-son-y-cuando-usarlos.md)
{% endhint %}

Crear un asistente de Inteligencia Artificial en Vambe es mucho más que escribir un texto largo en un recuadro. Para que tu IA funcione perfectamente, no alucine y realmente venda o atienda a tus clientes, primero debemos entender **cómo piensa.**

Antes de entrar a la configuración técnica, revisemos las 4 reglas de oro que todo creador de asistentes debe conocer.

#### 1. La Analogía del Lego (El Modelo Mental)

Un error común es pensar que la IA es un solo cerebro al que le arrojas toda la información junta. En realidad, construir un asistente en Vambe es como armar una figura de Lego.

Tienes distintas piezas (bloques) y cada una cumple una función específica:

*   **Bloques de Identidad:** Definen la personalidad (quién es).<br>

    <figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FIFmhFAyE65CTCNFnycyx%2Fimage.png?alt=media&#x26;token=df18ec8b-eac0-4dfb-bedc-9e6203ad9dae" alt=""><figcaption></figcaption></figure>
*   **Bloques de Instrucciones:** Definen el comportamiento (qué hace y qué no hace).\
    <br>

    <figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FK2PqEhq3zYW5w0yfDrU2%2Fimage.png?alt=media&#x26;token=ebaf3ae4-6a03-4c69-9d7f-68e0ef8b1215" alt=""><figcaption></figcaption></figure>
*   **Bloques de Información:** Definen su conocimiento (qué sabe, como precios o productos).\
    <br>

    <figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FtlVhn6M3ynNFcslkbvRN%2Fimage.png?alt=media&#x26;token=5f23c578-1eea-40ed-ac46-5dcf9a14c7de" alt=""><figcaption></figcaption></figure>

Si juntas las piezas correctamente, la figura toma forma. Si te falta una (por ejemplo, le dices que venda pero no le das el bloque de precios), la IA se confundirá e inventará respuestas.

#### 2. La Regla de Oro: Divide y Vencerás (Múltiples Asistentes)

Muchos usuarios intentan crear un "Súper Asistente" que salude, califique, venda, agende y además resuelva problemas de soporte técnico. **Esto es un error.**

**¿Por qué no debes hacerlo?**

* Las instrucciones se vuelven kilométricas y confusas.
* Si el cliente cambia de tema, la **IA puede saltarse pasos importantes** y arruinar el flujo.
* Si hay un error, es una pesadilla encontrar dónde falló.

Si flujo se resuelve con muchos asistentes, un ejemplo:

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FjcW9BZW1S5PvOi3OmCUD%2Fimage.png?alt=media&#x26;token=b246fe21-fd45-47c5-8522-97c7d8f7d81d" alt=""><figcaption></figcaption></figure>

La solución: Crea un asistente diferente para cada etapa de tu embudo. Por ejemplo: Un asistente "**Inicial**" para perfilar al cliente, y luego lo derivas a un asistente de "**Ventas**" o a uno de "**Servicio al Cliente**". Así mantienes el orden y la IA siempre tiene un objetivo claro.

{% hint style="info" %}
En los **Asistentes con Escenarios (V3)** esta regla cambia: un mismo asistente puede manejar varias situaciones dentro de una misma conversación mediante Escenarios y Rutas, sin necesidad de encadenar varios asistentes.
{% endhint %}

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FEGMDH6lxMTbZW6foUWJB%2Fimage.png?alt=media&#x26;token=ab4ef937-708b-4075-b409-1bcb8bb0b845" alt=""><figcaption></figcaption></figure>

#### 3. El Mindset "A Prueba de Balas" (Bulletproof)

Cuando pruebes tu asistente por primera vez, probablemente funcione bien. Pero debes diseñar tus instrucciones pensando en que ese asistente **se ejecutará un millón de veces, con un millón de clientes diferentes.**

Para que tu prompt sea "Bulletproof" (a prueba de balas), debes recordar algo vital: **La IA no asume nada.**

* No asumas que la IA saludará por cortesía; dile explícitamente "Saluda y preséntate".
* No dejes vacíos legales. Si no quieres que haga algo, díselo claramente en un bloque de "No hacer". (Ej: "Nunca pidas fotos personales de los clientes").

#### 4. La Cadena de Pensamiento (Secuencialidad)

La IA funciona de maravilla cuando la llevas de la mano paso a paso. En lugar de darle una orden gigante, estructura tus procesos de forma lógica y condicional ("Si pasa X, entonces haz Y").

* **Ejemplo del Nutricionista:** Si tu asistente necesita el peso y la estatura para agendar una cita, y el cliente solo le da la estatura, la IA no debe avanzar. Debe detenerse y decir: "Gracias por tu estatura, ahora indícame tu peso para poder agendarte".

Darle esta secuencialidad evita que la IA se salte reglas o intente adivinar datos faltantes.

Te invito a revisar como se crea cada una de las partes del asistente, importante que **TODAS** son necesarias para crear un asistente de forma completa.

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Bloques de identidad</td><td><a href="parte-2-bloques-de-identidad.md">parte-2-bloques-de-identidad.md</a></td></tr><tr><td>Bloques de instrucciones</td><td><a href="parte-3-bloques-de-instrucciones.md">parte-3-bloques-de-instrucciones.md</a></td></tr><tr><td>Bloques de información y base de conocimiento</td><td><a href="parte-4-bloques-de-informacion-y-base-de-conocimiento.md">parte-4-bloques-de-informacion-y-base-de-conocimiento.md</a></td></tr></tbody></table>
