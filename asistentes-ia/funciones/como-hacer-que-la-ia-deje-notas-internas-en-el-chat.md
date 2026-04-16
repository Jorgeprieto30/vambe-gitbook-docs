---
description: >-
  Mejora la comunicación interna. Configura a tu Asistente IA para que deje
  notas privadas y resúmenes en el ticket, evitando que tu equipo humano tenga
  que leer conversaciones eternas.
---

# ¿Cómo hacer que la IA deje notas internas en el chat?

La función **Crear Nota** permite que tu Inteligencia Artificial actúe como una secretaria eficiente, dejando "Post-its" o apuntes internos dentro de la conversación.

**¿Para qué sirve?** Imagina que un cliente habla durante 30 minutos con la IA, hace preguntas, cambia de opinión y finalmente pide una devolución.

* **Sin la función**: Tu vendedor humano entra al chat y tiene que leer 50 mensajes para entender qué pasó.
* **Con la función:** La IA deja una nota amarilla que dice: _"El cliente compró el producto X pero quiere cambiarlo por color azul"_.

***

#### Configuración Paso a Paso

Sigue estos pasos para que tu bot empiece a tomar apuntes:

**Paso 1: Ingresar al Asistente**

1. [Ve al menú Asistente](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md).
2. Entra a Pasos a Seguir (si es un resumen al final de un flujo) o Casos Posibles (si es para anotar una incidencia específica, como un reclamo).

**Paso 2: La Instrucción (El Pedido)**

Debes decirle a la IA **cuándo** anotar y **qué** anotar.

* _Fórmula:_ `Cuando [ocurra X], debes ejecutar la función [Crear Nota] con [La información a guardar]`.

> **Ejemplo de Resumen:** "Cuando el cliente termine de dar sus datos, ejecuta la función crear nota con un resumen de la conversación y lo que pidió".

**Paso 3: Crear la Función**

Haz clic en **+** Agregar Función y selecciona **Crear Nota.**

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

Configura los campos:

1. **Nombre**: Ej: "Nota Resumen".
2. **Descripción (Vital)**: Confirma cuándo se activa (Ej: "Cuando el cliente termine de dar sus datos").
3. **Contenido de la nota**: Aquí le dices a la IA qué escribir. Puedes poner instrucciones como: _"Resumen de lo solicitado por el cliente"_ o _"Datos de facturación del cliente"_.

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>



**Paso 4: Verificación Visual**

Asegúrate de ver la tarjeta de la función "**📝 Crear Nota**" justo debajo de tu texto de instrucción.

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

***

#### 🕵️ ¿Dónde veo las notas creadas?

Esta es una duda frecuente. Si la conversación con el cliente sigue y sigue, la nota visual (el recuadro amarillo en el chat) puede quedar muy arriba y perderse en el historial.

Para encontrar todas las notas rápidamente: No hagas _scroll_ infinito hacia arriba. Mira a la derecha de tu pantalla, en el panel de detalles del ticket.

1. Busca la sección Documentos y Multimedia.
2. Ahí encontrarás una pestaña o listado con todas las Notas que se han creado en ese ticket, ordenadas y fácil de leer.

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>
