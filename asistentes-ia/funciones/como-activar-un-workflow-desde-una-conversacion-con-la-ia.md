---
description: >-
  Conecta el cerebro de tu IA con tus automatizaciones. Aprende a disparar un
  Flujo de Trabajo (Workflow) complejo directamente desde una conversación.
---

# ¿Cómo activar un Workflow desde una conversación con la IA?

## ¿Cómo activar un Workflow desde una conversación con la IA?

La función Ejecutar Flow es el "botón rojo" que conecta a tu Asistente de Chat con el motor de automatizaciones (Workflows) de Vambe.

**¿Para qué sirve?** Imagina que tienes un proceso complejo diseñado en la sección de Workflows (ej: Calcular una cotización, enviar un correo, esperar 3 días y volver a escribir). En lugar de configurar todo eso dentro del chat, simplemente le dices a la IA: _"Cuando el cliente me dé sus datos, activa ese Workflow"_.

**Diferencia Clave:**

* **Las Funciones normales:** Hacen una cosa puntual (enviar un audio, cambiar etapa).
* **Ejecutar Flow:** Desencadena una cadena de acciones que construiste previamente en el editor de flujos.

***

**⚠️ Requisito Previo: Tener el Workflow Creado**

Para usar esta función, primero debes haber creado la automatización en la sección Workflows y haber seleccionado como "Gatillante" (Trigger) la opción "Flow activado por IA".

{% hint style="info" %}
Si no sabes cómo hacer esto, revisa primero el artículo: 👉 [\[Cómo crear y configurar Workflows\]](https://academy.vambe.ai/workflows)
{% endhint %}

***

**Configuración Paso a Paso**

Sigue estos pasos para conectar la conversación con tu automatización:

**Paso 1: Ingresar al Asistente**

1. Ve al menú Asistente.
2. Entra a **Pasos a Seguir** (si es un proceso lineal, como una cotización) o **Casos Posibles**.

**Paso 2: La Instrucción (El Gatillo)**

Debes decirle a la IA en qué momento exacto debe "presionar el botón" para iniciar el flujo.

* _Fórmula:_ `Cuando [el cliente termine X proceso], debes ejecutar la función [Ejecutar Flow]`.

> Ejemplo Real: "Una vez tengas el nombre, RUT y nivel de ingreso del cliente, activa el flujo de generación de cotización".

**Paso 3: Crear la Función**

Haz clic en **+ Agregar Función** y selecciona **Ejecutar Flow.**

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2F1r4ElKgRJnufgFowkcVi%2Fimage.png?alt=media&#x26;token=29807d2a-bc5e-48d9-b7a9-380ef8d2648e" alt=""><figcaption></figcaption></figure>

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2Fz2InH9z3RiCMfGoAJNiD%2Fimage.png?alt=media&#x26;token=938be2e2-def0-440e-a05c-51d7fe4ed4d5" alt=""><figcaption></figcaption></figure>

Configura los campos:

1. **Seleccionar Flow:** Se desplegará una lista con tus Workflows disponibles. Elige el que corresponde (Ej: "Cotizador Automático").
2. **Nombre**: Un identificador claro (Ej: "Activar Cotización").
3. Descripción (Vital): Confirma cuándo se activa.
   * _Ejemplo:_ "Cuando el cliente entregue todos sus datos financieros".
4. Selecciona los parametros que quieres enviar al WorkFlow, puedes seleccionar entre:
   1. **Algún dato de la conversación:** Para esto escribe en el prompt lo que quieres colocar en ese dato
   2. **Macros:** Datos del contacto como pueden ser por ejemplo: Id del contacto, numero del contacto, etc

![](https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FE3MLIvVZlBwaiHI2gC8e%2Fimage.png?alt=media\&token=894bdc6c-fbc4-4574-98b8-6a0c02584449)<br>

**Paso 4: Verificación**

Asegúrate de ver la tarjeta de la función creada debajo de tu texto.

* Nota: Al activarse esta función, la IA podría "pausar" su comportamiento habitual para dejar que el Workflow tome el control (dependiendo de cómo hayas configurado ese flujo).

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FcyOu8s6JLjhcJWtLtFWa%2Fimage.png?alt=media&#x26;token=d54047d3-fe00-4229-afd7-522d3d85f39a" alt=""><figcaption></figcaption></figure>
