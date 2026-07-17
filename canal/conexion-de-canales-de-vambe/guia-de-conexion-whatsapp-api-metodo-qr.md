---
description: >-
  Método Oficial. Aprende a conectar tu WhatsApp Business API con el nuevo flujo
  de seguridad: primero registrando el número en Meta y luego vinculándolo
  mediante Código QR en Vambe.
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Guía de Conexión: WhatsApp API (Método QR - Dual Coexistence)

## Guía de Conexión: WhatsApp API (Método QR - Dual Coexistence)

Este método híbrido permite conectar un número de WhatsApp Business utilizando tanto elementos de la conexión oficial por API como la vinculación mediante código QR. Es una alternativa rápida y flexible cuando se requiere conectar un número sin completar el proceso completo de verificación por SMS.

Al finalizar este proceso, tu número quedará activo dentro de Vambe y podrás asociarlo a un embudo para que la inteligencia artificial gestione los mensajes entrantes.

**Requisitos previos**

Antes de iniciar, asegúrate de contar con lo siguiente:

* Un teléfono con la app de **WhatsApp Business** instalado (no es compatible con WhatsApp personal).

<img src="https://content.gitbook.com/content/CFdmz6HrosBiYP1q1BJ6/blobs/QuVHU0Oz1pxLh80m9eLj/WhatsApp%20Image%202025%2012%2012%20at%209%2058%2059%20AM%20jpeg.jpeg" alt="" width="375">

* Acceso a un **Business Portfolio** de Meta.
* [Tener el **Business Portfolio** de Meta Verificado](https://academy.vambe.ai/canal/configuracion-en-meta/como-verificar-tu-negocio-business-manager-en-meta)
* Una **cuenta de Facebook Business** con permisos para crear o administrar cuentas de WhatsApp Business.

{% hint style="danger" %}
Al activar WhatsApp Dual, Vambe intentará **conectar automáticamente su línea de crédito** como método de pago para las campañas y el envío de plantillas. (Para consultar los precios, puedes ingresar a _Tarifas de mensajes_ en: [https://business.whatsapp.com/products/platform-pricing?lang=es\_LA](https://business.whatsapp.com/products/platform-pricing?lang=es_LA)).

Vambe, como **Meta Business Partner**, aplica una **comisión del 10%** por la gestión y uso de esta línea de crédito. El cobro total correspondiente al consumo de campañas y plantillas de Meta se realizará a través de Vambe al inicio de cada mes.

**Para consultar el consumo de esta línea de crédito, puedes revisarlo en:** [https://business.facebook.com/billing\_hub/credit\_lines](https://business.facebook.com/billing_hub/credit_lines)<br>

Para **desactivar la línea de crédito**, debe **contactar a soporte** por los canales oficiales
{% endhint %}

**Parte 1: Configuración inicial en Meta**

Antes de entrar a Vambe, debemos dejar el número "pre-registrado" en la plataforma de Meta.

1. Ingresa a tu **Meta Business Suite.**
2. En el menú de la izquierda, ve a Configuración (Settings).
3.  Busca la sección Cuentas de WhatsApp.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FkwSkjLk8kpwqITy4pl1p%2Fimage.png?alt=media&#x26;token=9755e71c-e11d-418e-9431-1f3234ebdef5" alt=""><figcaption></figcaption></figure>
4.  Haz clic en **Agregar** > Vincula una cuenta de Whatsapp Business.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F4o3vy2zJOtaDYTFHp8yJ%2Fimage.png?alt=media&#x26;token=fa0e0213-0de0-4e2d-82fa-7428a9f1f348" alt="" width="563"><figcaption></figcaption></figure>
5.  **Verificación**: Ingresa tu número de teléfono. Meta te enviará un código por SMS o Llamada. Ingrésalo para confirmar que el número es tuyo.<br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FUveOLZaIzkGjN72pIUQA%2Fimage.png?alt=media&#x26;token=b7841364-cbbf-497d-aa62-505f63e89a8b" alt="" width="563"><figcaption></figcaption></figure>
6. Una vez verificado y creado dentro de **Meta**, haz clic en **Listo**.

{% hint style="warning" %}
Nota: Solo cuando el número exista aquí, podrás pasar a la Parte 2 en Vambe.
{% endhint %}

***

**Parte 2: Iniciar la conexión desde Vambe**

Ahora que el número ya existe en tu portafolio, vamos a conectarlo a la inteligencia artificial.<br>

1. Ingresa a Vambe y ve al menú lateral Canales.
2. Haz clic en el botón azul + Agregar canal (abajo a la izquierda).
3.  Selecciona la opción WhatsApp API (Recomendado).<br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FjwvmYtjdQtQHGQC2Fejj%2FCaptura%20de%20pantalla%202026-02-17%20a%20la(s)%203.30.31%E2%80%AFp.m..png?alt=media&#x26;token=f3317ba0-0476-46de-803d-205d09ed1040" alt=""><figcaption></figcaption></figure>
4.  Elegir si queremos conectar un **Whatsapp Business existente** o tienes un **chip nuevo**\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F3OSypZDLdORgJJHiAqlT%2Fimage.png?alt=media&#x26;token=f658ae9f-994e-4dc4-bd67-6d970a70f37a" alt=""><figcaption></figcaption></figure>
5. **Inicia sesión** con tu cuenta de Facebook/Meta (la misma donde hiciste la Parte 1).
6.  Te preguntará si quieres conectar tu cuenta con "Vambe AI Main". Haz clic en Continuar y luego en Empezar.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FQ8vzT35AKkLwJru9ZbEf%2Fimage.png?alt=media&#x26;token=351a6d7a-c7c7-49d8-8e6e-fcd427bfbc3c" alt="" width="338"><figcaption></figcaption></figure>

***

**Parte 3: Selección de Activos**

El sistema te guiará por tres selecciones rápidas para encontrar el número que creaste en la Parte 1:

1. **Portafolio Comercial:** Selecciona la empresa correcta
2.  Cuenta de WhatsApp: Selecciona "**Conecta una app de WhatsApp Business"**.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FZB3Dk4lMMK13w6Xdtsm2%2Fimage.png?alt=media&#x26;token=3a2bf215-18f6-474b-907a-2fb4fac40d99" alt="" width="334"><figcaption></figcaption></figure>
3.  **Número de Teléfono:**

    *   Al llegar a este paso, selecciona Agregar un nuevo número de WhatsApp y debes ingresar el mismo numero que ingresaste antes.

        <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F3Kn2ae6OHuaHLexd63rq%2Fimage.png?alt=media&#x26;token=66b33149-d0b8-4872-93cc-2e3241fdd44f" alt="" width="375"><figcaption></figcaption></figure>
    * Una vez hagas click en siguiente verás una lista. Selecciona el número que registraste anteriormente (debería aparecer marcado como "**Registrado**").<br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FQ7hTpPd0JfboWVajflDo%2Fimage.png?alt=media&#x26;token=55edba17-5ecf-4a34-8fa4-c04aa5be8cb9" alt="" width="375"><figcaption></figcaption></figure>

    \
    Para finalizar click en **siguiente**

***

**Parte 4: Escanear el código QR y confirmar**

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F5qZV5k3SNbyZn0jGNt94%2Fimage.png?alt=media&#x26;token=7da6859d-b59c-4484-a7c4-90366d1ff66e" alt="" width="287"><figcaption></figcaption></figure>

Meta mostrará un código QR en pantalla. En este punto, la conexión se valida físicamente con tu celular.

Pasos en el teléfono: En tu teléfono, abre WhatsApp Business y sigue exactamente esta ruta:

1. Ve a Configuración (o Menú en Android).
2. Selecciona Dispositivos vinculados.
3. Toca en Vincular un dispositivo.
4. Escanea el código QR que aparece en la pantalla de tu computador.

{% hint style="danger" %}
_**Error muy común:** No escanear el QR con la cámara principal de la App. Siempre debe hacerse desde el menú "Dispositivos Vinculados" de WhatsApp Business._
{% endhint %}

El proceso de conexión puede tardar unos segundos. Verás en el teléfono que se ha vinculado una sesión (generalmente con el nombre de la empresa o Meta).

***

**Parte 5: Finalizar Configuración**

De vuelta en el navegador de tu computador:

1. La pantalla se actualizará sola tras el escaneo.
2. Nombre y Zona Horaria: Confirma el nombre de la empresa y selecciona la zona horaria correcta (Ej: GMT-03:00 America/Santiago).
3. Haz clic en Siguiente.
4. Permisos: Meta te mostrará un resumen de lo que se compartirá con Vambe (administrar conversaciones, eventos, etc.). Haz clic en Confirmar.
5. Verás el estado "Conectando a tu cuenta...". Cuando finalice, haz clic en Finalizar.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FUCK5mQDzrgShZXWxt0a7%2Fimage.png?alt=media&#x26;token=86de1337-6c81-4f59-a97d-ea0358987c65" alt=""><figcaption></figcaption></figure>

***

**Parte 6: Verificación Final**

¡Listo! El número ha quedado conectado oficialmente.

Para asegurarte de que la IA responda, debes hacer un último chequeo: 👉 \[Verifica aquí que el número esté asociado al embudo correcto]
