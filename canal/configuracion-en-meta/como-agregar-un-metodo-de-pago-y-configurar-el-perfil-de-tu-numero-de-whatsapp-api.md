---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo agregar un método de pago y configurar el perfil de tu número de WhatsApp API

## Cómo agregar un método de pago y configurar el perfil de tu número de WhatsApp API

{% embed url="https://www.youtube.com/watch?v=HNthqqHjzLg" %}

Para poder enviar **plantillas** (HSM templates) y **campañas** a través de WhatsApp API, es obligatorio asociar un método de pago válido en Meta. Además, configurar correctamente la foto, el nombre para mostrar y la descripción del perfil mejora la experiencia del usuario y aumenta la confianza de tus contactos.

Esta guía explica ambos procesos paso a paso.

***

#### Requisitos previos

Antes de comenzar, debes contar con:

* [Tu **número de WhatsApp API ya conectado** a Vambe.](https://academy.vambe.ai/c%C3%B3mo-conectar-whatsapp-api-oficial)
* Acceso al **Business Portfolio (Centro de Gestión Comercial de Meta)** con permisos para:
  * Ver _Cuentas de WhatsApp_
  * Administrar _Configuración de pago_
* Una **tarjeta de crédito vigente** para asociarla como método de pago.

***

### Parte 1 — Agregar un método de pago a tu cuenta de WhatsApp API

{% stepper %}
{% step %}
### Acceder al Centro de gestión comercial

1. Accede al [**Centro de gestión comercial de Meta (Business Portfolio)**](http://business.facebook.com/).
2. En el menú lateral, ir a **Configuraciones del portafolio.**

![](<../.gitbook/assets/image png Nov 28 2025 03 05 01 1437 PM.png>)
{% endstep %}

{% step %}
### Seleccionar cuentas y cuenta de WhatsApp

3. Seleccionar **Cuentas de WhatsApp**.

![](<../.gitbook/assets/image png Nov 28 2025 03 03 50 4242 PM.png>)

4. Elige la cuenta de WhatsApp correspondiente a tu número (ej.: _“Demo Vambe”_).\
   Aquí verás el estado actual de facturación.\
   Si aparece **“Sin método de pago asignado”**, debes continuar.
{% endstep %}

{% step %}
### Configuración de pago

5. En esa misma vista, ingresar a **Configuración de pago**.

![](<../.gitbook/assets/image png Nov 28 2025 03 05 50 1969 PM.png>)

6. Hacer clic en **Agregar método de pago**.

![](<../.gitbook/assets/undefined 3.png>)

7. Completar el formulario con los datos de la tarjeta de crédito.
8. Guardar la información y dejar la tarjeta como **método de pago predeterminado**.
{% endstep %}
{% endstepper %}

#### Resultado

* Tu número estará habilitado para enviar **plantillas y campañas**, incluso fuera de las 24 horas.
* Cualquier notificación o mensaje tipo “iniciador de conversación” podrá ser enviado sin restricciones de facturación.

***

### Parte 2 — Configurar el perfil del número en WhatsApp Manager

{% stepper %}
{% step %}
### Acceder al Centro de gestión comercial

1. Accede al [**Centro de gestión comercial de Meta (Business Portfolio)**](http://business.facebook.com/).
2. En el menú lateral, ir a **Configuraciones del portafolio.**

![](<../.gitbook/assets/image png Nov 28 2025 03 05 01 1437 PM.png>)
{% endstep %}

{% step %}
### Seleccionar cuentas de WhatsApp y administrador

3. Seleccionar **Cuentas de WhatsApp**.

![](<../.gitbook/assets/image png Nov 28 2025 03 03 50 4242 PM.png>)

4. Seleccionar la cuenta y luego en Administrador de Whatsapp.

![](<../.gitbook/assets/image png Nov 28 2025 03 17 25 4876 PM.png>)
{% endstep %}

{% step %}
### Editar perfil: imagen, nombre y descripción

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

![](<../.gitbook/assets/image png Nov 28 2025 03 19 09 5704 PM.png>)
{% endstep %}
{% endstepper %}

***

### Buenas prácticas recomendadas

* Utiliza **un logo claro y legible** como imagen del canal.
* Mantén un **nombre para mostrar coherente** con tu marca y tus redes oficiales.
* En la descripción, explica brevemente:
  * A qué se dedica tu empresa
  * Qué tipo de mensajes recibirá el usuario (ej.: confirmaciones, recordatorios, avisos, soporte, promociones)
