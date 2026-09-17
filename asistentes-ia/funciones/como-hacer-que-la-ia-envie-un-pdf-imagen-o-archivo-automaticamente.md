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

1. Ve al menú Asistente.
2. Entra a **Pasos a Seguir** o **Casos Posibles.**

**Paso 2: La Instrucción**

Dile a la IA cuándo debe entregar el material.

* _Fórmula:_ `Cuando [el cliente pida X], debes ejecutar la función [Enviar Documento]`.

> **Ejemplo Real:** "Cuando el cliente me responda las 3 preguntas, debes ejecutar la función enviar PDF de precios".

**Paso 3: Crear la Función y Subir el Archivo**

Haz clic en **+ Agregar Función** y selecciona **Enviar Documento o Imagen.**

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2Fq9u1AqN9PLl3mCfV48gR%2Fimage.png?alt=media&#x26;token=35b4086d-ed5b-44a7-948e-96f0b025141f" alt=""><figcaption></figcaption></figure>

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FKUmhgDftz98uaFt3Cv87%2Fimage.png?alt=media&#x26;token=3fb21e07-2eac-4840-a487-119f829562f9" alt=""><figcaption></figcaption></figure>

Configura los campos:

1. **Nombre**: Ej: "PDF Precios".
2. **Descripción** (**Vital**): Confirma cuándo se activa (Ej: "Cuando pidan precios").
3. **Mensaje del archivo**: Escribe el texto que acompañará a la foto. (Ej: _"Aquí tienes el documento solicitado"_). Recuerda que este texto no cambiará.
4. **Subir Archivo**: Carga tu documento, imagen o video aquí.
   * _Nota:_ Si el archivo es muy pesado (videos largos), podría tardar unos segundos en cargarse y enviarse en el chat.
5. **Orden**: Puedes elegir si enviar primero el texto y luego la imagen, o viceversa.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FvlsbHmtobj6BllJ29Ysy%2Fimage.png?alt=media&#x26;token=d0252813-f0a2-4ea2-a6f4-e5f7443db4d2" alt=""><figcaption></figcaption></figure>

**Paso 4: Verificación Visual**

Asegúrate de ver la tarjeta de la función creada justo debajo de tu texto de instrucción. Si ves la tarjeta con el icono de clip/archivo, ¡está listo!

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FVACX3V8M8geP0tmQoKnZ%2Fimage.png?alt=media&#x26;token=b1093a3d-c7be-4563-9aa1-0097493078b2" alt=""><figcaption></figcaption></figure>

***

## Otra forma de hacerlo: adjuntar el archivo directo en el texto

Si lo que buscas es justamente resolver la limitación anterior (tener un texto dinámico y, al mismo tiempo, un archivo de apoyo), tienes otra opción: adjuntar el archivo directamente dentro de la descripción del asistente, de un escenario o ruta, o de un paso a seguir.

A diferencia de la función **Enviar Documento o Imagen**, aquí el archivo queda incrustado en medio del texto, como una palabra más de la instrucción. Eso significa que la IA puede seguir redactando su respuesta con naturalidad y, en el momento que corresponda, enviar el archivo junto con ese mensaje generado en el momento.

### Cómo adjuntarlo

Estando en el editor de la descripción, un escenario o un paso, tienes cuatro formas de subir el archivo:

* Haciendo clic en el botón **Agregar archivo**, ubicado justo debajo del editor, al lado de **Agregar función**.
* Escribiendo el comando `/image`.
* Arrastrando el archivo directamente dentro del editor.
* Pegando una imagen copiada con `Ctrl+V`.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

Una vez cargado, el nombre del archivo aparece resaltado en azul, en línea con el resto del texto, de la misma forma en que aparecen las funciones. Como no ocupa una fila completa, puedes ubicarlo en medio de una frase (por ejemplo: "Envía la imagen **catalogo-2026.png** y pregunta si tiene dudas"). Al hacer clic sobre el nombre se abre la previsualización del archivo.

Cuando la IA use ese texto para responder, Vambe reconoce automáticamente el archivo adjunto y lo entrega como un archivo real dentro del chat, no como un simple enlace.

{% hint style="info" %}
**Tipos y límites:** puedes adjuntar imágenes, videos, audios y PDF. Las imágenes admiten hasta 5 MB y el resto de los formatos hasta 16 MB. Los archivos SVG no son compatibles.
{% endhint %}

{% hint style="info" %}
Si ya tenías un enlace externo pegado como texto en una instrucción, sigue funcionando exactamente igual. No es necesario que reemplaces nada de lo que ya tenías configurado.
{% endhint %}

***

## En resumen

Vambe te da dos caminos para que tu asistente comparta archivos con tus clientes: la función **Enviar Documento o Imagen**, pensada para entregas puntuales con un mensaje fijo, y la posibilidad de adjuntar el archivo directo dentro del texto de una descripción, escenario o paso, cuando quieres que la IA combine ese archivo con una respuesta redactada en el momento. Elige la que mejor se ajuste a lo que necesitas comunicar en cada caso.
