---
hidden: true
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Cómo configurar confirmaciones y recordatorios en Medilink y Dentalink

En este artículo aprenderás cómo aplicar la URL del webhook de confirmaciones y recordatorios generada en Vambe dentro de MediLink o Dentalink, para que las confirmaciones y recordatorios de citas se envíen automáticamente por WhatsApp.

Este paso es obligatorio para que las notificaciones automáticas funcionen correctamente.

{% hint style="warning" %}
Sin sesión de administrador, no será posible configurar el webhook.
{% endhint %}

***

#### Requisitos previos

* Tener configuradas las [confirmaciones y recordatorios](https://academy.vambe.ai/paso-1-configuraciones-recordatorio) en Vambe.
* Haber copiado la **URL del webhook** generada en la configuración de notificaciones.
* Contar con **acceso administrador** en MediLink o Dentalink.

***

{% stepper %}
{% step %}
### Ingresar a MediLink o Dentalink como administrador

* Accede a tu cuenta de **MediLink o Dentalink**.
* Inicia sesión **con un usuario administrador**.
{% endstep %}

{% step %}
### Acceder a la configuración de Webhooks

* En la parte superior derecha, haz clic en **Administrador**.
* Selecciona la opción **Configuración Webhook**.

![](<../.gitbook/assets/image png Dec 17 2025 04 13 43 2210 PM.png>)
{% endstep %}

{% step %}
### Agregar un nuevo proveedor de webhook

* Dentro de la configuración, haz clic en el botón verde **Agregar proveedor**.

![](<../.gitbook/assets/image png Dec 17 2025 04 14 52 1750 PM.png>)

* Completa los campos de la siguiente forma:

Nombre del proveedor\
`Notificación y confirmación Vambe`

URL del callback

* Pega la **URL del webhook** que copiaste previamente desde Vambe.

![](<../.gitbook/assets/image png Dec 17 2025 04 16 18 0178 PM.png>)
{% endstep %}

{% step %}
### Guardar la configuración

* Haz clic en **Guardar**.

{% hint style="success" %}
Listo. Desde este momento:

* Las confirmaciones de citas
* Y los recordatorios automáticos\
  comenzarán a enviarse desde Vambe según la configuración realizada.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## Qué sucede después de configurarlo

* Cada vez que se cree, confirme o actualice una cita en MediLink o Dentalink, Vambe recibirá el evento automáticamente.
* La plataforma evaluará las reglas configuradas y enviará las plantillas correspondientes por WhatsApp.
* No es necesario volver a configurar este webhook, salvo que cambies de sede o URL.

***

<details>

<summary>Errores comunes a evitar</summary>

* ❌ No usar una cuenta administrador.
* ❌ Pegar una URL incompleta o incorrecta.
* ❌ No haber configurado previamente las notificaciones en Vambe.
* ❌ No guardar los cambios luego de pegar la URL.

</details>
