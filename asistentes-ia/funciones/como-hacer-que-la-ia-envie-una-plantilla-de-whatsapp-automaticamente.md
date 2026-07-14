# ¿Cómo hacer que la IA envíe una Plantilla de WhatsApp automáticamente?

## ¿Cómo hacer que la IA envíe una Plantilla de WhatsApp automáticamente?

La función **Enviar Plantilla** permite que tu Asistente dispare un mensaje predeterminado (Template) de WhatsApp en el momento exacto de la conversación.

**¿Para qué sirve?** A veces la IA no necesita "inventar" una respuesta, sino entregar información oficial y estructurada que ya tienes preparada, como un PDF adjunto, una lista de precios oficial o una ubicación.

***

**🛑 Requisito Previo: Tener la Plantilla**

Para que la IA pueda enviar una plantilla, esta debe existir previamente en tu plataforma y estar aprobada por Meta.

{% hint style="danger" %}
**¿No tienes plantillas creadas?** La IA no puede crear la plantilla por sí sola. Si aún no tienes ninguna, ve primero a este artículo para configurarlas: 👉 [\[Cómo crear y aprobar Plantillas de WhatsApp\]](https://academy.vambe.ai/canal/plantillas/como-crear-plantillas)
{% endhint %}

***

**Configuración Paso a Paso**

Una vez tengas tu plantilla lista, sigue estos pasos para conectarla a la inteligencia de tu bot:

**Paso 1: Ingresar al Asistente**

1. Ve al menú Asistente y selecciona el bot que editarás.
2. Ubícate en los bloques de **Pasos a Seguir** (si es parte del flujo de ventas) o **Casos Posibles** (si es una respuesta a una pregunta frecuente).

**Paso 2: Escribir la Instrucción (Prompt)**

Debes decirle a la IA qué debe ocurrir en la charla para que ella decida enviar ese formato específico.

* _Fórmula:_ `Si el cliente está interesado en [Opción A], debes ejecutar la función [Nombre de la función]`.

> **Ejemplo Real**: "Si el cliente me dice que está interesado en el Plan Básico, debes ejecutar la función Enviar Plantilla Plan Básico".

**Paso 3: Crear la Función**

Haz clic en + Agregar Función y selecciona Enviar Plantilla.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FRDf7lk0VwgDvVV0nZoGC%2Fimage.png?alt=media&#x26;token=c277e5f2-a42d-4c8d-9e14-dc51a26294db" alt=""><figcaption></figcaption></figure>

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FUCi0IYbesLO3o2pMSmla%2Fimage.png?alt=media&#x26;token=6728cb78-1cd7-4c14-a98d-ac473757f8c9" alt=""><figcaption></figcaption></figure>

Configura los siguientes campos:

1. **Seleccionar Plantilla:** Se desplegará una lista con todas tus plantillas aprobadas. Elige la correcta (Ej: `plan_basico_info`).
2. **Nombre de la función:** Un nombre claro para ti (Ej: "Enviar Info Básico").
3. **Descripción (¡Vital!):** Explícale a la IA cuándo debe usar esta herramienta.
   * _Tip:_ Debe coincidir con la instrucción del paso 2.
   * _Ejemplo:_ "Cuando el cliente quiera información del plan básico".

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FIDAvB73DlwmkPy1DYz6H%2Fimage.png?alt=media&#x26;token=844d3cfb-dd82-4c9b-912f-31165709c29b" alt=""><figcaption></figcaption></figure>

**Paso 4: Confirmación**

Verifica que la tarjeta de la función aparezca debajo de tu texto.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FinqivNROI5yOecCF9EfS%2Fimage.png?alt=media&#x26;token=faed2b7e-1d2e-4953-a2ee-11fc05b5eea2" alt=""><figcaption></figcaption></figure>

***

**💡 Pregunta Frecuente: Costos y Ventana de 24h**

¿Tiene un costo extra enviar esta plantilla? Generalmente NO. Como la IA está respondiendo a una interacción activa del cliente, casi siempre se encontrará dentro de la "ventana de conversación de 24 horas". En este caso, el envío de la plantilla funciona como un mensaje de sesión normal y no genera costos adicionales de apertura de conversación.
