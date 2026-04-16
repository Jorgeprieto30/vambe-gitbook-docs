---
description: >-
  Conexión estable y oficial. Aprende el nuevo método paso a paso para conectar
  tu WhatsApp Business API: primero registrando el número en Meta y luego
  vinculándolo en Vambe mediante código QR.
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo conectar WhatsApp API (oficial)

En esta guía paso a paso aprenderás cómo registrar tu número en Meta, configurar tu cuenta de WhatsApp Business y finalmente conectar el canal a tu embudo en Vambe.

Este proceso permite utilizar la integración oficial de WhatsApp Business API, la única que garantiza estabilidad y cumplimiento con las políticas de Meta.

***

#### Requisitos previos

Antes de comenzar, asegúrate de contar con:

* Un número telefónico que pueda recibir **SMS o llamadas**.
* Un número que **no esté vinculado actualmente a ninguna cuenta de WhatsApp**.
* Un **portafolio comercial activo en Meta/Facebook** (el mismo utilizado para administrar anuncios).
* Tener la cuenta de [Meta Verificada](../configuracion-en-meta/como-verificar-tu-negocio-business-manager-en-meta.md)

***

{% stepper %}
{% step %}
### Iniciar la conexión desde Vambe

* Ingresa a la sección de conexión de canales: https://academy.vambe.ai/c%C3%B3mo-ingresar-a-la-secci%C3%B3n-de-conexi%C3%B3n-de-canales
* Seleccionar **WhatsApp API (oficial)**.

![](<../.gitbook/assets/image png Nov 27 2025 02 26 35 6182 PM (2).png>)

* Hacer clic en **Registrar número de teléfono**.

![image.png](<../.gitbook/assets/fb358cb463384708952837e4791263c5ed4e35c26b1c494589e5e8079aca337a (2)>)

Esto abrirá el proceso de conexión directamente con Meta.
{% endstep %}

{% step %}
### Registro del número en Meta

Al hacer clic en “Registrar número de teléfono” dentro de Vambe, se abrirá una nueva pestaña de Meta/Facebook.

![](<../.gitbook/assets/image png Nov 27 2025 03 36 56 3610 PM (2).png>)

* La pantalla mostrará el mensaje **“Conecta tu cuenta fácilmente a Vambe”**.
* Verifica en la esquina superior derecha que estás utilizando la **cuenta correcta de Facebook Business**.

{% hint style="warning" %}
Un error muy común es que los usuarios, sin darse cuenta, están conectados con su cuenta personal, lo que impide acceder al portafolio comercial. Debes asegurarte de estar en la cuenta que administra tu portafolio comercial.
{% endhint %}

* Una vez confirmado, hacer clic en **Continuar**.
{% endstep %}

{% step %}
### Seleccionar el portafolio y crear la cuenta de WhatsApp Business

![](<../.gitbook/assets/image png Nov 27 2025 03 37 48 6118 PM (2).png>)

* Meta mostrará los **portafolios comerciales** asociados a tu cuenta. Selecciona el portafolio correcto.
* Selecciona tu **cuenta de WhatsApp Business** existente.
  * Si no tienes una, selecciona **Crear una cuenta de WhatsApp Business**.
* Haz clic en **Siguiente**.
{% endstep %}

{% step %}
### Ingresar la información comercial (Solo si seleccionaste "Crear una cuenta de WhatsApp Business")

![](<../.gitbook/assets/image png Nov 27 2025 03 39 20 6970 PM (2).png>)

Meta solicitará los datos principales de la empresa asociados al número de WhatsApp API. Debes completar:

* Nombre de la empresa
* Categoría del negocio
* País
* Sitio web
* Zona horaria

Una vez completado, hacer clic en **Siguiente**.
{% endstep %}

{% step %}
### Agregar el número de teléfono

![](<../.gitbook/assets/image png Nov 27 2025 03 39 57 6863 PM (2).png>)

* Hacer clic en **Agregar nuevo número de teléfono**.
* Ingresar el **número que deseas conectar** a WhatsApp API.
{% endstep %}

{% step %}
### Verificación del número

![](<../.gitbook/assets/image png Nov 27 2025 03 40 50 8421 PM (2).png>)

Meta te pedirá seleccionar un método de verificación:

* **Mensaje de texto (SMS)**
* **Llamada telefónica**

Es fundamental tomar nota del código exactamente como llega (formato XXX XXX). Ese mismo código se utilizará **dos veces**: primero en Meta y luego en Vambe.

* Seleccionar el método de verificación.
* Ingresar el código recibido.
* Hacer clic en **Siguiente**.
{% endstep %}

{% step %}
### Finalizar la verificación en Meta

![](<../.gitbook/assets/image png Dec 12 2025 12 37 57 2845 PM (1).png>)

Una vez verificado el número:

* Hacer clic en **Continuar**.
* Meta configurará automáticamente el número dentro del portafolio.
* Cuando el proceso termine, hacer clic en **Finalizar**.

Meta te redirigirá automáticamente a la pestaña de Vambe.
{% endstep %}

{% step %}
### Completar la conexión dentro de Vambe

![](<../.gitbook/assets/Captura de pantalla 2025 12 04 a la(s) 4 46 44 p m  png (2).png>)

Al regresar a Vambe:

* La plataforma solicitará **nuevamente el código de verificación XXX XXX**.
* Ingresa el mismo código que recibiste anteriormente.
* Hacer clic en **Verificar**.
* Seleccionar el **embudo** al que deseas asociar el número.
* Hacer clic en **Finish**.
{% endstep %}

{% step %}
### Verificar que el número esté asociado al embudo correcto

Revisa la guía de verificación [aquí](https://academy.vambe.ai/verificar-que-el-n%C3%BAmero-est%C3%A9-asociado-al-embudo-correcto)
{% endstep %}

{% step %}
### Conexión completada

Después de estos pasos:

* El número queda oficialmente conectado a Vambe.
* El canal aparecerá disponible en la lista de canales.
* El embudo seleccionado comenzará a recibir todos los mensajes entrantes mediante WhatsApp API.
{% endstep %}
{% endstepper %}
