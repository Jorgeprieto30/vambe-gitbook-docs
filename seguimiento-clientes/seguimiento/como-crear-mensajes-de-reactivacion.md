---
cover: ../.gitbook/assets/portada 18.png
coverY: 0
---

# ¿Cómo crear mensajes de reactivación?

En este artículo aprenderás cómo enviar mensajes de seguimiento automáticos a tus clientes cuando dejan de responder, permitiéndote retomar la conversación de forma oportuna y sin esfuerzo manual.

Este tipo de seguimiento es ideal para:

* Reactivar clientes que dejaron de responder.
* Aumentar la tasa de cierre o agendamiento.
* Mantener conversaciones activas sin depender del seguimiento manual del equipo.

***

## 🧠 ¿Cómo funciona el seguimiento automático?

Vambe permite enviar un **mensaje automático** después de que transcurre una cierta cantidad de tiempo sin respuesta del cliente.

* Puedes definir el tiempo de espera (por ejemplo: 5 minutos, 10 minutos, 1 hora, hasta un máximo de **24 horas**).
* Si necesitas enviar el mensaje **después de 24 horas**, el envío debe hacerse **mediante una plantilla aprobada**.
* El mensaje puede ser generado dinámicamente por IA o enviado como plantilla fija.

***

## ⚠️ Recomendaciones antes de comenzar

{% hint style="info" %}
Antes de configurar un seguimiento automático, considera lo siguiente:

* La etapa debe tener Inteligencia Artificial activa: es altamente recomendable que el seguimiento se configure en etapas con IA, ya que permite personalizar el mensaje y aplicar condiciones inteligentes.
* Evita múltiples seguimientos en la misma etapa: no se recomienda tener más de un mensaje de seguimiento por etapa, ya que un exceso de mensajes puede provocar reportes por parte de los clientes en WhatsApp o redes sociales.
{% endhint %}

***

## ⚙️ Paso a paso: cómo crear un mensaje de seguimiento

{% stepper %}
{% step %}
### Selecciona la etapa correcta

* Ve al **embudo**.
* Identifica la etapa donde deseas que se envíe el seguimiento cuando el cliente deje de responder.
{% endstep %}

{% step %}
### Ingresa a la configuración de la etapa

* Haz clic en la **tuerca de configuración** ubicada en la parte superior derecha de la etapa.
* Selecciona **Acciones automáticas**.

![](../.gitbook/assets/image\(76\).png)
{% endstep %}

{% step %}
### Configura la acción de envío de mensaje

* En el menú izquierdo, selecciona **Enviar mensaje**.
* En el panel central, elige la opción **Con tiempo**.
* Define **cuánto tiempo debe pasar** desde la última respuesta del cliente antes de enviar el mensaje (ejemplo: 30 minutos, 1 hora, etc.).

![](../.gitbook/assets/image\(77\).png)
{% endstep %}

{% step %}
### Define el tipo de mensaje

En el panel derecho puedes elegir entre dos opciones:

*   Mensaje con IA\
    Aquí debes escribir una **instrucción**, no el texto literal.

    Ejemplo de instrucción:

    > “Reactivar el interés del cliente con una pregunta amable relacionada con su consulta anterior.”

    ![](../.gitbook/assets/image\(78\).png)
*   Plantilla\
    Útil si el mensaje se enviará después de 24 horas o si necesitas un texto fijo aprobado previamente.

    Si no tienes una plantilla debes crearla: https://academy.vambe.ai/v1/docs/como-crear-plantillas
{% endstep %}
{% endstepper %}

***

## 🧠 (Opcional) Agregar una condición con IA

Puedes agregar una **condición inteligente** para decidir si el mensaje debe enviarse o no.

Ejemplos de condiciones:

* No enviar el mensaje si el cliente ya se despidió.
* Enviar el mensaje solo si el cliente preguntó por un producto específico.
* No enviar seguimiento si el ticket ya fue cerrado.

La IA evaluará esta condición antes de ejecutar el envío.

![](../.gitbook/assets/image\(79\).png)

***

## ✅ Guardar y activar

* Revisa la configuración.
* Haz clic en **Crear**.
* El mensaje de seguimiento quedará activo automáticamente.

![](../.gitbook/assets/image\(80\).png)

A partir de ahora, cuando un cliente deje de responder en esa etapa y se cumpla el tiempo definido, Vambe enviará el mensaje de seguimiento de forma automática.
