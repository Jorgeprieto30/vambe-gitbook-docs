---
description: >-
  Entrega información visual. Configura a tu Asistente IA para que envíe
  catálogos, listas de precios (PDF), imágenes o videos promocionales dentro del
  chat.
---

# ¿Cómo hacer que la IA envíe un PDF, imagen o archivo automáticamente?

La función **Enviar Documento o Imagen** permite que tu asistente adjunte un archivo específico (PDF, JPG, PNG, Video, etc.) en el momento que la conversación lo requiera.

**¿Para qué sirve?** Es ideal para entregar material de apoyo que no puede explicarse solo con texto, como:

* Un Brochure corporativo (PDF).
* Una lista de precios o menú.
* Una foto de un producto específico.
* Un video promocional.

***

#### ⚠️ Limitación Importante: El Texto Fijo

Antes de configurarla, debes saber algo crucial que explicó nuestro experto Jorge Prieto:

Esta función **NO permite que la IA redacte un mensaje dinámico acompañando al archivo.**

* **El problema:** Si usas esta función, el archivo se enviará acompañado de un texto fijo que tú escribes al configurarla.
* **La consecuencia:** Si el cliente hace una pregunta específica justo en ese momento (ej: "¿Tienen talla M?"), la IA podría ignorar la pregunta y solo responder con el archivo y tu texto pre-grabado (ej: "Aquí tienes el catálogo").

> **Recomendación**: Usa esta función para entregas de información muy concretas donde no se espera mucha interacción conversacional en ese preciso instante.

***

#### Configuración Paso a Paso

Sigue estos pasos para adjuntar tus archivos:

**Paso 1: Ingresar al Asistente**

1. [Ve al menú Asistente.](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md)
2. Entra a **Pasos a Seguir** o **Casos Posibles.**

**Paso 2: La Instrucción**

Dile a la IA cuándo debe entregar el material.

* _Fórmula:_ `Cuando [el cliente pida X], debes ejecutar la función [Enviar Documento]`.

> **Ejemplo Real:** "Cuando el cliente me responda las 3 preguntas, debes ejecutar la función enviar PDF de precios".

**Paso 3: Crear la Función y Subir el Archivo**

Haz clic en **+ Agregar Función** y selecciona **Enviar Documento o Imagen.**

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

Configura los campos:

1. **Nombre**: Ej: "PDF Precios".
2. **Descripción** (**Vital**): Confirma cuándo se activa (Ej: "Cuando pidan precios").
3. **Mensaje del archivo**: Escribe el texto que acompañará a la foto. (Ej: _"Aquí tienes el documento solicitado"_). Recuerda que este texto no cambiará.
4. **Subir Archivo**: Carga tu documento, imagen o video aquí.
   * _Nota:_ Si el archivo es muy pesado (videos largos), podría tardar unos segundos en cargarse y enviarse en el chat.
5. **Orden**: Puedes elegir si enviar primero el texto y luego la imagen, o viceversa.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

**Paso 4: Verificación Visual**

Asegúrate de ver la tarjeta de la función creada justo debajo de tu texto de instrucción. Si ves la tarjeta con el icono de clip/archivo, ¡está listo!

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>
