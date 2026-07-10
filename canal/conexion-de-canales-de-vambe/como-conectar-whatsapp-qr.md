---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo conectar WhatsApp QR

## Cómo conectar WhatsApp QR

{% stepper %}
{% step %}
**Ingresa a la sección de conexión de canales**

Accede a la sección de conexión de canales [aquí](https://academy.vambe.ai/c%C3%B3mo-ingresar-a-la-secci%C3%B3n-de-conexi%C3%B3n-de-canales?hsLang=es)
{% endstep %}

{% step %}
**Selecciona WhatsApp**

Selecciona WhatsApp como tipo de canal a conectar.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FRn68wTNsc1DXjYZ4sJTW%2Fimage.png?alt=media&#x26;token=5fc89fcd-ee2a-4373-860d-203383970f71" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Completa Nombre del canal y Número de teléfono**

Coloca el Nombre del canal en Vambe y el Número de teléfono.

_El Nombre del canal es un nombre interno; los clientes NO verán este nombre._

{% hint style="warning" %}
IMPORTANTE: El número debe estar con el código de país.
{% endhint %}

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F0ia0gNYYse5LuGGUNlI0%2Fimage.png?alt=media&#x26;token=61061f56-f51a-4f23-8a52-c8ea76949450" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**Escanea el código QR**

Escanea el código QR que aparece en pantalla utilizando la cámara de tu teléfono, siguiendo el mismo proceso que usarías para WhatsApp Web. (El código dinámico cambia cada 15 segundos).

Pasos en el teléfono:

* Abre WhatsApp.
* Toca los tres puntos (⋮) o Configuración.
* Selecciona "Dispositivos vinculados".
* Toca "Vincular un dispositivo".
* Apunta la cámara al código QR mostrado en Vambe.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FQwcfrLILeuKnlcPupCw0%2Fimage.png?alt=media&#x26;token=1ab50f6b-5a87-4b2f-bbe9-71a71f3f788d" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
**¿WhatsApp te pide una clave de acceso? Conéctate importando tu sesión**

WhatsApp cambió cómo se vinculan los dispositivos: para algunas cuentas ahora pide una **clave de acceso (passkey)** adicional al escanear el QR. Ese paso solo se puede completar en el navegador del propio usuario, con su teléfono al lado, así que el código QR de siempre no alcanza para conectar esos números.

Para esos casos existe una segunda forma de conectar, dentro de la misma pantalla. Si el QR no funciona, haz clic en la opción **¿WhatsApp te pide una clave de acceso? Conéctate importando tu sesión**.

<figure><img src="../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Este método aparece solo cuando hace falta. Si conectas con el QR de siempre, no cambia nada para ti.
{% endhint %}

**1. Instala el extractor (una sola vez)**

Arrastra el botón **Extract WhatsApp Session** hacia tu barra de marcadores. Si no ves la barra de marcadores, actívala desde el menú del navegador (en Brave o Chrome: menú → Marcadores → Mostrar barra de marcadores).

<figure><img src="../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

**2. Extrae tu sesión**

Abre [web.whatsapp.com](https://web.whatsapp.com) e inicia sesión de forma normal. Aquí sí puedes aprobar la clave de acceso, porque tienes tu teléfono a mano. Espera a que carguen todos tus chats.

Con los chats ya cargados, haz clic en el marcador **Extract WhatsApp Session**. Acepta los avisos que muestre la página y se descargará automáticamente un archivo llamado `wa-extract.json`.

{% hint style="danger" %}
El archivo `wa-extract.json` contiene las credenciales completas de tu cuenta. No lo compartas y bórralo después de conectar.
{% endhint %}

**3. Sube tu sesión en Vambe**

Vuelve a Vambe y haz clic en **Continuar**. Arrastra el archivo `wa-extract.json` a la zona de carga o haz clic para buscarlo.

<figure><img src="../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

La conexión puede tardar unos minutos. Si demora demasiado, puedes volver a subir el archivo para reintentar. Una vez conectado, tu WhatsApp queda vinculado igual que con el QR.
{% endstep %}

{% step %}
**Espera la confirmación de conexión**

Espera a que el sistema confirme la conexión exitosa.
{% endstep %}

{% step %}
**Selecciona el Embudo**

En el menú que se desplegará, selecciona el embudo específico al que deseas vincular este número de WhatsApp.
{% endstep %}

{% step %}
**Finaliza la configuración**

Haz clic en "Finish" o "Finalizar" para terminar la configuración.
{% endstep %}

{% step %}
**Verifica que los mensajes entren al embudo**

Para que los mensajes entren al embudo debemos asegurar que el canal esté vinculado a este; una vez vinculado la IA comenzará a tomar las conversaciones que entran.

Dirígete a la sección de conexión de canales y verifica que el número esté conectado al embudo [aquí](https://academy.vambe.ai/c%C3%B3mo-ingresar-a-la-secci%C3%B3n-de-conexi%C3%B3n-de-canales?hsLang=es)

También puedes verificar específicamente que este [asignado al embudo correcto](https://academy.vambe.ai/verificar-que-el-n%C3%BAmero-est%C3%A9-asociado-al-embudo-correcto)
{% endstep %}
{% endstepper %}

¡Listo! Tu embudo ahora recibirá automáticamente todos los mensajes enviados a ese número a través de WhatsApp.
