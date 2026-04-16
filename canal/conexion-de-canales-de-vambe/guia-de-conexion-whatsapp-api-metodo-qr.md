---
description: >-
  Método Oficial. Aprende a conectar tu WhatsApp Business API con el nuevo flujo
  de seguridad: primero registrando el número en Meta y luego vinculándolo
  mediante Código QR en Vambe.
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Guía de Conexión: WhatsApp API (Método QR)

Este método híbrido permite conectar un número de WhatsApp Business utilizando tanto elementos de la conexión oficial por API como la vinculación mediante código QR. Es una alternativa rápida y flexible cuando se requiere conectar un número sin completar el proceso completo de verificación por SMS.

Al finalizar este proceso, tu número quedará activo dentro de Vambe y podrás asociarlo a un embudo para que la inteligencia artificial gestione los mensajes entrantes.

#### Requisitos previos

Antes de iniciar, asegúrate de contar con lo siguiente:

* Un teléfono con la app de **WhatsApp Business** instalado (no es compatible con WhatsApp personal).

![](<../.gitbook/assets/WhatsApp Image 2025 12 12 at 9 58 59 AM jpeg.jpeg>)

* Acceso a un **Business Portfolio** de Meta.
* [Tener el **Business Portfolio** de Meta Verificado](https://academy.vambe.ai/c%C3%B3mo-verificar-tu-negocio-business-manager-en-meta)
* Una **cuenta de Facebook Business** con permisos para crear o administrar cuentas de WhatsApp Business.&#x20;

{% hint style="danger" %}
Al activar WhatsApp Dual, Vambe intentará **conectar automáticamente su línea de crédito** como método de pago para las campañas y el envío de plantillas. (Para consultar los precios, puedes ingresar a _Tarifas de mensajes_ en: [https://business.whatsapp.com/products/platform-pricing?lang=es\_LA](https://business.whatsapp.com/products/platform-pricing?lang=es_LA)).

Vambe, como **Meta Business Partner**, aplica una **comisión del 10%** por la gestión y uso de esta línea de crédito. El cobro total correspondiente al consumo de campañas y plantillas de Meta se realizará a través de Vambe al inicio de cada mes.

**Para consultar el consumo de esta línea de crédito, puedes revisarlo en:** [https://business.facebook.com/billing\_hub/credit\_lines](https://business.facebook.com/billing_hub/credit_lines)<br>

Para **desactivar la línea de crédito**, debe **contactar a soporte** por los canales oficiales
{% endhint %}

#### Parte 1: Configuración inicial en Meta

Antes de entrar a Vambe, debemos dejar el número "pre-registrado" en la plataforma de Meta.

1. Ingresa a tu **Meta Business Suite.**
2. En el menú de la izquierda, ve a Configuración (Settings).
3.  Busca la sección Cuentas de WhatsApp.\
    <br>

    <figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
4.  Haz clic en **Agregar** > Vincula una cuenta de Whatsapp Business.\
    <br>

    <figure><img src="../.gitbook/assets/image (10).png" alt="" width="563"><figcaption></figcaption></figure>


5.  **Verificación**: Ingresa tu número de teléfono. Meta te enviará un código por SMS o Llamada. Ingrésalo para confirmar que el número es tuyo.<br>

    <figure><img src="../.gitbook/assets/image (11).png" alt="" width="563"><figcaption></figcaption></figure>


6. Una vez verificado y creado dentro de **Meta**, haz clic en **Listo**.

{% hint style="warning" %}
Nota: Solo cuando el número exista aquí, podrás pasar a la Parte 2 en Vambe.
{% endhint %}

***

#### Parte 2: Iniciar la conexión desde Vambe

Ahora que el número ya existe en tu portafolio, vamos a conectarlo a la inteligencia artificial.<br>

1. Ingresa a Vambe y ve al menú lateral [Canales](como-ingresar-a-la-seccion-de-conexion-de-canales.md).
2. Haz clic en el botón azul + Agregar canal (abajo a la izquierda).
3.  Selecciona la opción WhatsApp API (Recomendado).<br>

    <figure><img src="../.gitbook/assets/Captura de pantalla 2026-02-17 a la(s) 3.30.31 p.m..png" alt=""><figcaption></figcaption></figure>
4.  Se abrirá una ventana emergente. Haz clic en **Registrar número de teléfono**.

    <figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>


5. **Inicia sesión** con tu cuenta de Facebook/Meta (la misma donde hiciste la Parte 1).
6.  Te preguntará si quieres conectar tu cuenta con "Vambe AI Main". Haz clic en Continuar y luego en Empezar.\
    <br>

    <figure><img src="../.gitbook/assets/image (13).png" alt="" width="338"><figcaption></figcaption></figure>

***

#### Parte 3: Selección de Activos

El sistema te guiará por tres selecciones rápidas para encontrar el número que creaste en la Parte 1:

1. **Portafolio Comercial:** Selecciona la empresa correcta
2.  Cuenta de WhatsApp: Selecciona "**Conecta una app de WhatsApp Business"**.\
    <br>

    <figure><img src="../.gitbook/assets/image (14).png" alt="" width="334"><figcaption></figcaption></figure>
3.  **Número de Teléfono:**

    *   Al llegar a este paso, selecciona Agregar un nuevo número de WhatsApp y debes ingresar el mismo numero que ingresaste antes.

        <figure><img src="../.gitbook/assets/image (15).png" alt="" width="375"><figcaption></figcaption></figure>
    * Una vez hagas click en siguiente verás una lista. Selecciona el número que registraste anteriormente (debería aparecer marcado como "**Registrado**").<br>

    <figure><img src="../.gitbook/assets/image (16).png" alt="" width="375"><figcaption></figcaption></figure>

    \
    Para finalizar click en **siguiente**

***

#### Parte 4: Escanear el código QR y confirmar

<figure><img src="../.gitbook/assets/image (17).png" alt="" width="287"><figcaption></figcaption></figure>



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

#### Parte 5: Finalizar Configuración

De vuelta en el navegador de tu computador:

1. La pantalla se actualizará sola tras el escaneo.
2. Nombre y Zona Horaria: Confirma el nombre de la empresa y selecciona la zona horaria correcta (Ej: GMT-03:00 America/Santiago).
3. Haz clic en Siguiente.
4. Permisos: Meta te mostrará un resumen de lo que se compartirá con Vambe (administrar conversaciones, eventos, etc.). Haz clic en Confirmar.
5. Verás el estado "Conectando a tu cuenta...". Cuando finalice, haz clic en Finalizar.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

***

#### Parte 6: Verificación Final

¡Listo! El número ha quedado conectado oficialmente.

Para asegurarte de que la IA responda, debes hacer un último chequeo: 👉 [\[Verifica aquí que el número esté asociado al embudo correcto\]](verificar-que-el-numero-este-asociado-al-embudo-correcto.md)
