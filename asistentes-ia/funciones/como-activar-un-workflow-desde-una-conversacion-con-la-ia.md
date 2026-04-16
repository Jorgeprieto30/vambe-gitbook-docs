---
description: >-
  Conecta el cerebro de tu IA con tus automatizaciones. Aprende a disparar un
  Flujo de Trabajo (Workflow) complejo directamente desde una conversación.
---

# ¿Cómo activar un Workflow desde una conversación con la IA?

La función Ejecutar Flow es el "botón rojo" que conecta a tu Asistente de Chat con el motor de automatizaciones (Workflows) de Vambe.

**¿Para qué sirve?** Imagina que tienes un proceso complejo diseñado en la sección de Workflows (ej: Calcular una cotización, enviar un correo, esperar 3 días y volver a escribir). En lugar de configurar todo eso dentro del chat, simplemente le dices a la IA: _"Cuando el cliente me dé sus datos, activa ese Workflow"_.

**Diferencia Clave:**

* **Las Funciones normales:** Hacen una cosa puntual (enviar un audio, cambiar etapa).
* **Ejecutar Flow:** Desencadena una cadena de acciones que construiste previamente en el editor de flujos.

***

#### ⚠️ Requisito Previo: Tener el Workflow Creado

Para usar esta función, primero debes haber creado la automatización en la sección Workflows y haber seleccionado como "Gatillante" (Trigger) la opción "Flow activado por IA".

{% hint style="info" %}
Si no sabes cómo hacer esto, revisa primero el artículo: 👉 [\[Cómo crear y configurar Workflows\]](https://app.gitbook.com/s/0xCLgfGby0xiCWJaqr57/)
{% endhint %}

***

#### Configuración Paso a Paso

Sigue estos pasos para conectar la conversación con tu automatización:

**Paso 1: Ingresar al Asistente**

1. [Ve al menú Asistente.](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md)
2. Entra a **Pasos a Seguir** (si es un proceso lineal, como una cotización) o **Casos Posibles**.

**Paso 2: La Instrucción (El Gatillo)**

Debes decirle a la IA en qué momento exacto debe "presionar el botón" para iniciar el flujo.

* _Fórmula:_ `Cuando [el cliente termine X proceso], debes ejecutar la función [Ejecutar Flow]`.

> Ejemplo Real: "Una vez tengas el nombre, RUT y nivel de ingreso del cliente, activa el flujo de generación de cotización".

**Paso 3: Crear la Función**

Haz clic en **+ Agregar Función** y selecciona **Ejecutar Flow.**

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

Configura los campos:

1. **Seleccionar Flow:** Se desplegará una lista con tus Workflows disponibles. Elige el que corresponde (Ej: "Cotizador Automático").
2. **Nombre**: Un identificador claro (Ej: "Activar Cotización").
3. Descripción (Vital): Confirma cuándo se activa.
   * _Ejemplo:_ "Cuando el cliente entregue todos sus datos financieros".
4. Selecciona los parametros que quieres enviar al WorkFlow, puedes seleccionar entre:
   1. **Algún dato de la conversación:** Para esto escribe en el prompt lo que quieres colocar en ese dato
   2. **Macros:** Datos del contacto como pueden ser por ejemplo: Id del contacto, numero del contacto, etc

![](<../.gitbook/assets/image (17).png>)<br>



**Paso 4: Verificación**

Asegúrate de ver la tarjeta de la función creada debajo de tu texto.

* Nota: Al activarse esta función, la IA podría "pausar" su comportamiento habitual para dejar que el Workflow tome el control (dependiendo de cómo hayas configurado ese flujo).

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>
