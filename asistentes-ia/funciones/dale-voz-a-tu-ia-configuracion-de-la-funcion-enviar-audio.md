---
description: >-
  Humaniza la experiencia de tus clientes. Configura tu IA para que envíe notas
  de voz generadas dinámicamente, haciendo que la conversación se sienta mucho
  más cercana y natural.
---

# Dale voz a tu IA: Configuración de la función Enviar Audio

Una de las herramientas más sorprendentes para aumentar la tasa de respuesta y humanizar a tu bot es la función **Enviar Audio**.

A diferencia de lo que muchos piensan, esta función **NO envía un archivo MP3 pregrabado**. Lo que hace es tomar la respuesta que generó la Inteligencia Artificial (texto) y convertirla en una nota de voz fluida y natural en tiempo real.

**¿Por qué usarla?**

* Genera cercanía: El cliente siente que habla con una persona real.
* Explica mejor: Ideal para respuestas largas o complejas (como trayectorias de empresa o explicaciones técnicas) que por texto serían aburridas.

***

#### Voces Disponibles

Actualmente, puedes elegir entre distintas personalidades de voz para que coincidan con la identidad de tu marca. Las opciones disponibles son:

* **Fernanda**
* **Tony**
* **Valeria**
* **Pablo**
* **Sofía**

***

#### Configuración Paso a Paso

Sigue estos pasos para que tu asistente empiece a hablar:

**Paso 1: Ingresar al Asistente**

1. [Ve al menú Asistente](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md) y selecciona el bot.
2. Ubícate en Pasos a Seguir o Casos Posibles.

**Paso 2: Instrucción de Contenido (El Guion)**

Aquí es donde ocurre la magia. Debes decirle a la IA qué debe decir en ese audio. La IA buscará la información en tu Base de Conocimiento y la transformará en voz.

* _Fórmula:_ `Cuando [ocurra X], debes ejecutar la función [Enviar Audio] describiendo [Tema a hablar]`.

> Ejemplo Real: "Cuando el cliente escoja el plan que quiere, descríbele el plan usando la función Enviar Audio".

**Paso 3: Crear la Función**

Haz clic en + Agregar Función y selecciona Enviar Audio.

<p align="center"><br><img src="../.gitbook/assets/image (27).png" alt=""></p>

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Configura los campos:

1. Voz: Selecciona una de las voces disponibles (Ej: Fernanda).
2. Nombre: Un identificador (Ej: "Enviar nota de voz").
3. Descripción (Vital): Confirma cuándo se activa.
   * _Ejemplo:_ "Cuando el cliente escoja el plan que quiere".

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

**Paso 4: Verificación Visual (¿Cómo debe verse?)**

Es fundamental confirmar que la función quedó realmente vinculada al paso.

Revisa la estructura: Debes ver el recuadro con tu instrucción escrita y, justo debajo, la tarjeta pequeña que dice "🎙️ Enviar nota de voz". Si ves el texto pero no ves la tarjeta del micrófono abajo, la IA no enviará el audio.

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

***

#### 💡 Preguntas Frecuentes

¿Puedo subir mis propios audios pregrabados? No con esta función. Esta herramienta es generativa: crea el audio al instante basándose en lo que la IA decide responder. Si quieres enviar un archivo de audio fijo (MP3), debes usar la función _\[Enviar Documento o Imagen]_&#x20;

¿Funciona en otros idiomas? ¡Sí! Si la instrucción es "Responde en inglés" o si el cliente habla en otro idioma, la IA generará el audio en ese idioma con una fluidez sorprendente.

¿De dónde saca la información para hablar? La IA lee tu Base de Conocimiento (Bloques de información). Si le pides que explique la "Oferta del Mes" por audio, asegúrate de que esa oferta esté escrita en la información de tu bot.
