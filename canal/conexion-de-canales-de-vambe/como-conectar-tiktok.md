# Cómo conectar TikTok

En este artículo aprenderás cómo conectar tu cuenta de TikTok a Vambe para que las conversaciones que lleguen por ahí sean atendidas por tu asistente, igual que con WhatsApp, Instagram o Messenger.

{% hint style="info" %}
Conectar TikTok tiene **dos partes distintas**: primero vinculas la cuenta de TikTok con Vambe, y después conectas ese canal a un embudo para que los contactos entren a una etapa y el asistente pueda responder. Tener la cuenta conectada **no es suficiente** por sí solo —si no está asociada a un embudo, los mensajes no se procesan.
{% endhint %}

***

**Requisitos previos**

Antes de comenzar, asegúrate de que:

* Tienes acceso administrativo a la cuenta de TikTok que quieres conectar.
* La cuenta es una **cuenta de TikTok Business** (no una cuenta personal).
* Tienes creado un embudo en Vambe al que conectar el canal.
* Ese embudo tiene un **asistente asignado a su primera etapa**.
* Tienes permisos suficientes en Vambe para administrar canales y embudos.

***

{% stepper %}
{% step %}
**Ingresar a la sección de conexión de canales**

[Accede a la sección de conexión de canales](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/como-ingresar-a-la-seccion-de-conexion-de-canales), o entra directo desde el menú lateral a **Canales**.

<figure><img src="../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Agregar o revisar el canal de TikTok**

1. Haz clic en **Agregar canal** (o revisa el canal de TikTok si ya existe uno sin conectar).
2. Elige **TikTok**.

<figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

3. Autoriza la cuenta de TikTok cuando la plataforma lo solicite.
4. Confirma que el canal quede listado como **activo**.
{% endstep %}

{% step %}
**Conectar TikTok a un embudo**

1. Ve a la configuración del embudo donde quieres recibir las conversaciones de TikTok.
2. Busca la sección de canales conectados.
3. Selecciona la cuenta de TikTok.
4. Confirma la conexión.

Un mismo embudo puede tener varios canales conectados a la vez —por ejemplo, WhatsApp, Instagram y Messenger junto con TikTok.
{% endstep %}

{% step %}
**Revisar la primera etapa del embudo**

Cuando llega un contacto nuevo desde TikTok, entra a la **primera etapa** del embudo conectado, y el asistente configurado en esa etapa es el que debe atenderlo.

{% hint style="warning" %}
Si la primera etapa no tiene un asistente asignado, la conversación no va a tener la automatización esperada —va a entrar al embudo, pero nadie (ni la IA) la va a responder automáticamente.
{% endhint %}
{% endstep %}

{% step %}
**Probar el flujo completo**

Después de conectar el canal:

1. Envía un mensaje de prueba desde TikTok.
2. Confirma que se cree el contacto o la conversación en Vambe.
3. Verifica que ingrese a la primera etapa del embudo.
4. Revisa que responda el asistente correcto.
5. Confirma que las funciones configuradas —cambio de etapa, notas, etiquetas, workflows— actúen según corresponda.
{% endstep %}
{% endstepper %}

***

**Qué cambia al conectarlo**

* Las nuevas conversaciones de TikTok pueden ingresar al embudo.
* El asistente de la primera etapa puede responder automáticamente.
* Las conversaciones quedan disponibles para seguimiento desde Vambe.
* Aplican las mismas reglas comerciales del embudo: etapas, asignaciones, etiquetas y derivación a ejecutivos.
* Si el canal **no** está conectado a un embudo, los mensajes de ese canal no son procesados por el asistente.

***

{% hint style="danger" %}
**Importante:** conectar TikTok no significa automáticamente que la IA va a empezar a responder. También deben estar correctamente configurados el embudo, la primera etapa, el asistente asignado, sus instrucciones, y las funciones o automatizaciones que quieras usar.
{% endhint %}

***

**Resultado final**

* Los mensajes de TikTok ingresarán automáticamente a Vambe.
* Los tickets se crearán dentro del embudo configurado.
* Si el ticket entra a una etapa con asistente, responderá la IA.
* Si entra a una etapa humana, deberá responder un ejecutivo.

Referencia: [Verificar que el número esté asociado al embudo correcto](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/verificar-que-el-numero-este-asociado-al-embudo-correcto)
