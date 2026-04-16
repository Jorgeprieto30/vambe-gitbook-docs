---
cover: ../.gitbook/assets/Portada 20.png
coverY: 0
---

# ¿Por qué algunos eventos configurados en Vambe Ads no se envían a Meta, Google o TikTok?

![](<../.gitbook/assets/image png Dec 02 2025 12 30 55 1051 PM.png>)

En algunos casos, los usuarios configuran correctamente sus eventos dentro de **Vambe Ads**, pero aun así ciertos eventos no se envían a las plataformas publicitarias.

Esto **no ocurre por un error o un problema técnico**: es un comportamiento **intencional**, diseñado para **proteger la calidad de los datos** y evitar señales inválidas que podrían perjudicar el rendimiento de tus campañas.

Vambe Ads solo envía eventos que cumplen con los **requisitos mínimos que Meta, Google y TikTok** necesitan para atribuir y optimizar correctamente.

{% stepper %}
{% step %}
### No enviamos eventos si el correo no existe en nuestras bases internas

Para que Meta, Google o TikTok puedan atribuir un evento, necesitan un identificador confiable del usuario.

El más importante es **el correo electrónico**.

Si el contacto no tiene correo, o el correo no está presente en nuestras bases, Vambe Ads **bloquea el evento automáticamente**.

¿Por qué?

Enviar un evento sin correo haría que la plataforma no pueda relacionarlo con ningún usuario real, generando **ruido**, reduciendo la calidad de la señal y disminuyendo la capacidad de optimización.
{% endstep %}

{% step %}
### No enviamos eventos sin un clic previo registrado

Para Google Ads, el evento **solo se enviará si existe un Google Click ID** previo registrado. Sin ese identificador, el evento no se envía. Para Meta y TikTok, también se considera el click ID como señal de atribución, pero pueden existir mecanismos alternativos de matching."

Estas plataformas funcionan con atribución basada en clics.

Sin ese registro previo, el evento sería descartado por la plataforma de todos modos.

En lugar de enviar señales que no serán utilizadas, Vambe Ads evita enviarlas para **proteger la reputación y estabilidad de tu cuenta publicitaria**.
{% endstep %}

{% step %}
### Si la información del evento está incompleta, el envío también se bloquea

Cada evento requiere ciertos parámetros mínimos (dependiendo de la plataforma y el tipo de evento).

Si la información recibida está incompleta, inconsistente o no cumple con los requisitos exigidos, Vambe Ads detiene el envío automáticamente.

Esto se hace para evitar:

* Errores de atribución
* Penalizaciones por mala calidad de datos
* Ineficiencias en el aprendizaje de los algoritmos de Meta, Google o TikTok
{% endstep %}
{% endstepper %}

{% hint style="info" %}
En resumen, Vambe Ads **no enviará un evento** si:

* ❌ El correo del contacto no está en nuestras bases
* ❌ Para Google Ads: no existe un Google Click ID previo asociado
* ❌ La información del evento está incompleta o no cumple los requisitos mínimos

Este comportamiento es **automático** y no requiere acción adicional. La prioridad es: **Enviar menos eventos, pero enviarlos con muy alta calidad**, para garantizar señales reales, completas y útiles para la optimización de campañas.
{% endhint %}
