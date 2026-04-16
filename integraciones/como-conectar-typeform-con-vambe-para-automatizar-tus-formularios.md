---
description: >-
  Esta guía te enseñará a conectar Typeform con Vambe para automatizar la
  captura de datos y la gestión de tus clientes de forma profesional.
---

# ¿Cómo conectar Typeform con Vambe para automatizar tus formularios?

**Typeform** es una de las plataformas más potentes para crear formularios web personalizados y dinámicos. Gracias a su integración con **Vambe**, puedes transformar cada respuesta de un cliente en una acción automática dentro de tu ecosistema de atención, permitiéndote capturar información clave o datos sensibles y disparar flujos de trabajo al instante.

#### ⚠️ Requisitos previos

> **💡 Habilitación de cuenta:** Para comenzar, asegúrate de tener una cuenta activa en ambas plataformas. La integración se activa a nivel de Business Manager en Vambe.

***

#### Configuración Paso a Paso

**Paso 1: Conectar las cuentas**

1. Dirígete al menú de **Ajustes** y selecciona la pestaña **Integraciones**.
2.  En la sección de **Productividad**, localiza la tarjeta de **Typeform**.<br>

    <figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>


3. Haz clic en **Agregar cuenta**. Se abrirá una ventana emergente donde deberás autorizar los permisos para que Vambe pueda leer tus formularios y respuestas.

**Paso 2: Crear el Workflow (Trigger)**

Una vez conectado, puedes crear un flujo automatizado que reaccione a las respuestas:

1.  Ve a Workflows > Flows y haz clic en Crear Flow.<br>

    <figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>


2.  Como Trigger (activador), selecciona la opción **Typeform respondido**.<br>

    <figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>


3.  Selecciona tu cuenta vinculada y el formulario específico que deseas utilizar (ej: "Form de prueba"). Vambe cargará automáticamente las preguntas de dicho formulario.\
    <br>

    <figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

***

Aunque el flujo final depende de lo que cada cliente necesite, te recomendamos este ejemplo base para automatizar el ingreso de leads:

**Acción 1: Obtener o crear contacto**

1.  Haz clic en el icono (+) del workflow y selecciona Acción.<br>

    <figure><img src="../.gitbook/assets/image (28).png" alt="" width="258"><figcaption></figcaption></figure>


2.  En "Seleccionar una acción", elige Obtener o crear contacto.<br>

    <figure><img src="../.gitbook/assets/image (29).png" alt="" width="375"><figcaption></figcaption></figure>


3.  Cambia la condición de búsqueda de **ID** a **Phone**.\
    <br>

    <figure><img src="../.gitbook/assets/image (30).png" alt="" width="274"><figcaption></figcaption></figure>


4.  Haz clic en **Agregar variable**, entra en **answers** y selecciona la pregunta donde el usuario ingresó su número (ej: "¿Cuál es tu número de teléfono?"). <br>

    <figure><img src="../.gitbook/assets/image (32).png" alt="" width="375"><figcaption></figcaption></figure>


5.  Selecciona el valor **value** para capturar el dato exacto.<br>

    <figure><img src="../.gitbook/assets/image (33).png" alt="" width="375"><figcaption></figcaption></figure>


6.  Define el **Canal de teléfono** (WhatsApp), selecciona el número de tu empresa y, opcionalmente, **mapea otra variable para el Nombre del contacto**.<br>

    <figure><img src="../.gitbook/assets/image (34).png" alt="" width="250"><figcaption></figcaption></figure>

\
**Acción 2: Enviar mensaje de bienvenida**

1.  Haz clic nuevamente en el icono (+) y selecciona otra Acción.<br>

    <figure><img src="../.gitbook/assets/image (35).png" alt="" width="224"><figcaption></figcaption></figure>


2.  Elige **Enviar plantilla** y selecciona la plantilla que deseas enviar (ej: "feedback\_nps" o un saludo inicial).<br>

    <figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>
3. Si tu plantilla requiere variables, asígnalas utilizando los datos capturados en el paso anterior.
4. Recueda siempre **activar** tu WorkFlow

***

#### 💡 Resumen del Workflow

Una vez configurado este flujo recomendado, el proceso funcionará de la siguiente manera:

1. Respuesta: El usuario completa el formulario en Typeform.
2. Sincronización: Vambe detecta la respuesta y crea automáticamente el contacto en tu base de datos (o lo actualiza si ya existe).
3. Interacción: El sistema envía de forma inmediata una plantilla de WhatsApp al cliente, asegurando una respuesta rápida y profesional.

***

#### 💡 Tips y Buenas Prácticas

* 💡 Datos Sensibles: Usa Typeform para preguntar información que Meta suele restringir en plantillas directas (como datos de salud o financieros) y guárdalos automáticamente en Vambe.
* 💡 Variables Dinámicas: Asegúrate de mapear siempre el campo de Teléfono correctamente; si este valor está vacío o es erróneo, las acciones posteriores como enviar mensajes fallarán.
* 🛑 Tickets vs Contactos: Recuerda que crear un contacto no abre automáticamente una conversación. Es fundamental añadir el paso de Abrir ticket si deseas que tu equipo de agentes pueda responderle al cliente.
