---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo agregar un método de pago y configurar el perfil de tu número de WhatsApp API

## Cómo agregar un método de pago y configurar el perfil de tu número de WhatsApp API

### Cómo agregar un método de pago y configurar el perfil de tu número de WhatsApp API

#### Cómo agregar un método de pago y configurar el perfil de tu número de WhatsApp API

{% embed url="https://www.youtube.com/watch?v=HNthqqHjzLg" %}

Para poder enviar **plantillas** (HSM templates) y **campañas** a través de WhatsApp API, es obligatorio asociar un método de pago válido. Además, configurar correctamente la foto, el nombre para mostrar y la descripción del perfil mejora la experiencia del usuario y aumenta la confianza de tus contactos.

Esta guía explica ambos procesos paso a paso.

***

**Requisitos previos**

Antes de comenzar, debes contar con:

* [Tu **número de WhatsApp API ya conectado** a Vambe.](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/como-conectar-whatsapp-api-oficial)
* Acceso al **Business Portfolio (Centro de Gestión Comercial de Meta)** con permisos para:
  * Ver _Cuentas de WhatsApp_
  * Administrar _Configuración de pago_
* Una **tarjeta de crédito vigente** para asociarla como método de pago.

***

**Parte 1 — Agregar un método de pago a tu cuenta de WhatsApp API**

{% hint style="success" %}
**Opción recomendada: usa el método de pago de Vambe.** No necesitas asociar una tarjeta en Meta: puedes cargar el envío de plantillas al método de pago de Vambe, y estas se facturan junto con tu suscripción, en un solo cobro. Si prefieres esta opción, escríbele a tu contacto en Vambe para activarla. Si en cambio quieres facturar directamente con Meta, sigue los pasos de más abajo.
{% endhint %}

{% stepper %}
{% step %}
**Acceder al Centro de gestión comercial**

1. Accede al [**Centro de gestión comercial de Meta (Business Portfolio)**](http://business.facebook.com/).
2. En el menú lateral, ir a **Configuraciones del portafolio.**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/DA6aSkCJbn0kfKuqDDUU/image%20png%20Nov%2028%202025%2003%2005%2001%201437%20PM.png)
{% endstep %}

{% step %}
**Seleccionar cuentas y cuenta de WhatsApp**

3. Seleccionar **Cuentas de WhatsApp**.

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/kIMfLxtmlWDtwHlmJIlF/image%20png%20Nov%2028%202025%2003%2003%2050%204242%20PM.png)

4. Elige la cuenta de WhatsApp correspondiente a tu número (ej.: _“Demo Vambe”_).\
   Aquí verás el estado actual de facturación.\
   Si aparece **“Sin método de pago asignado”**, debes continuar.
{% endstep %}

{% step %}
**Configuración de pago**

5. En esa misma vista, ingresar a **Configuración de pago**.

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/37Xx62C8rzFrNAMzvGvQ/image%20png%20Nov%2028%202025%2003%2005%2050%201969%20PM.png)

6. Hacer clic en **Agregar método de pago**.

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/h9a8cxg23jKpnO72YZva/undefined%203.png)

7. Completar el formulario con los datos de la tarjeta de crédito.
8. Guardar la información y dejar la tarjeta como **método de pago predeterminado**.
{% endstep %}
{% endstepper %}

**Resultado**

* Tu número estará habilitado para enviar **plantillas y campañas**, incluso fuera de las 24 horas.
* Cualquier notificación o mensaje tipo “iniciador de conversación” podrá ser enviado sin restricciones de facturación.

***

**Parte 2 — Configurar el perfil del número en WhatsApp Manager**

{% stepper %}
{% step %}
**Acceder al Centro de gestión comercial**

1. Accede al [**Centro de gestión comercial de Meta (Business Portfolio)**](http://business.facebook.com/).
2. En el menú lateral, ir a **Configuraciones del portafolio.**

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/DA6aSkCJbn0kfKuqDDUU/image%20png%20Nov%2028%202025%2003%2005%2001%201437%20PM.png)
{% endstep %}

{% step %}
**Seleccionar cuentas de WhatsApp y administrador**

3. Seleccionar **Cuentas de WhatsApp**.

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/kIMfLxtmlWDtwHlmJIlF/image%20png%20Nov%2028%202025%2003%2003%2050%204242%20PM.png)

4. Seleccionar la cuenta y luego en Administrador de Whatsapp.

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/VSlTHMwU5pNJzd5JAMmS/image%20png%20Nov%2028%202025%2003%2017%2025%204876%20PM.png)
{% endstep %}

{% step %}
**Editar perfil: imagen, nombre y descripción**

Aquí podrás editar:

Imagen de perfil

* Subir la foto que representará tu canal (idealmente el logo de tu empresa).
* Asegúrate de que sea clara, centrada y fácilmente reconocible.

Nombre para mostrar (Display Name)

* Edita el nombre si deseas que tus clientes vean una etiqueta más clara o comercial.
* **Importante:** Meta debe aprobar este nombre.
* Los cambios no se reflejan de inmediato.

Descripción del negocio

* Escribe un texto breve (1–2 líneas) que explique:
  * Quién es la empresa
  * Qué tipo de mensajes envía
  * Qué servicios ofrece

Esto ayuda a mejorar la confianza del usuario y evita bloqueos o reportes.

![](https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/7AJ3hDSECw8eaW1mzUwD/image%20png%20Nov%2028%202025%2003%2019%2009%205704%20PM.png)
{% endstep %}
{% endstepper %}

***

**Buenas prácticas recomendadas**

* Utiliza **un logo claro y legible** como imagen del canal.
* Mantén un **nombre para mostrar coherente** con tu marca y tus redes oficiales.
* En la descripción, explica brevemente:
  * A qué se dedica tu empresa
  * Qué tipo de mensajes recibirá el usuario (ej.: confirmaciones, recordatorios, avisos, soporte, promociones)
