---
description: >-
  Aprende a identificar si tu canal usa WhatsApp API oficial o API Dual, qué
  revisar antes de reconectarlo y cómo resolver los problemas más comunes
  durante el proceso.
---

# Guía de reconexión: WhatsApp API y WhatsApp API Dual

Si tu canal de WhatsApp aparece desconectado, inactivo o dejó de recibir mensajes, primero debes identificar qué tipo de conexión utiliza. El proceso **no es igual** para WhatsApp API oficial y WhatsApp API Dual.

{% hint style="danger" %}
**No elimines el canal ni crees uno nuevo para probar.** En la mayoría de los casos, el problema se resuelve reconectando el canal existente —crear uno nuevo puede duplicar el número, perder el historial y desconectar el embudo que ya tenías configurado.
{% endhint %}

***

### Decisión rápida: ¿qué tipo de canal tengo?

* **¿Usas WhatsApp en el teléfono para responder?**
  * Sí → probablemente tienes **API Dual** o **QR tradicional**.
  * No → probablemente tienes **WhatsApp API oficial**.
* **¿La conexión original se hizo escaneando un código QR?**
  * Sí → revisa si era API Dual o QR tradicional (sección siguiente).
  * No → probablemente era WhatsApp API oficial.

Si no estás seguro, no reconectes al azar: revisa primero el tipo de canal que muestra Vambe, en la sección [Cómo ingresar a la sección de conexión de canales](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/como-ingresar-a-la-seccion-de-conexion-de-canales).

***

## 1. Diferencias entre WhatsApp API, API Dual y QR

| Tipo de conexión            | ¿Se usa la app de WhatsApp en el teléfono? | ¿Cómo se conecta?                           | Características principales                                      |
| --------------------------- | ------------------------------------------ | ------------------------------------------- | ---------------------------------------------------------------- |
| **WhatsApp API oficial**    | No                                         | Mediante Meta y la configuración del número | El canal funciona desde la plataforma de WhatsApp Business API   |
| **WhatsApp API Dual**       | Sí, junto con Vambe                        | Mediante código QR y Meta                   | Permite usar la app de WhatsApp Business y Vambe al mismo tiempo |
| **WhatsApp QR tradicional** | Sí                                         | Mediante vinculación similar a WhatsApp Web | No es una conexión API oficial ni una conexión Dual              |

**WhatsApp API oficial** es la conexión directa con la infraestructura oficial de Meta:

* No se utiliza la aplicación de WhatsApp en el teléfono para responder.
* El número se registra dentro de una cuenta de WhatsApp Business de Meta.
* El número debe poder recibir un código por SMS o llamada durante el registro o la validación.
* Requiere acceso al Business Portfolio o cuenta empresarial correspondiente.
* Permite usar funciones oficiales como plantillas, campañas y automatizaciones, sujetas a las políticas de Meta.

**WhatsApp API Dual o Dual Coexistence** (también llamada WhatsApp Coexistence):

* Permite utilizar la app de WhatsApp Business en el teléfono y Vambe simultáneamente.
* La conexión inicial o la reconexión se realiza mediante un código QR.
* Requiere una cuenta de WhatsApp Business, no una cuenta personal.
* El Business Portfolio de Meta debe estar verificado.
* Puede requerir un método de pago configurado en Meta para campañas y mensajes con plantillas.
* Los mensajes enviados desde el teléfono y desde Vambe tienen reglas diferentes.

**WhatsApp QR tradicional** —importante no confundirlo con API Dual:

* Se realiza como una vinculación parecida a WhatsApp Web.
* No corresponde a WhatsApp API oficial.
* No ofrece las mismas capacidades de plantillas, campañas y automatizaciones oficiales.
* Puede depender de la sesión del teléfono conectado.

{% hint style="warning" %}
**API Dual y QR tradicional no son lo mismo**, aunque ambos puedan usar un código QR. API Dual utiliza la conexión oficial de WhatsApp Business y permite trabajar con Vambe y la app de WhatsApp Business simultáneamente; el QR tradicional no.
{% endhint %}

***

## 2. Cómo identificar el tipo de canal

1. Ingresa a Vambe.
2. Abre la sección **Canales**.
3. Busca el canal de WhatsApp que presenta problemas.
4. Revisa el nombre, el número y el tipo de conexión mostrado.

<figure><img src="../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

5. Confirma cómo se conectó originalmente:

* Si se configuró desde Meta y no se utiliza la app de WhatsApp en el teléfono, probablemente es **WhatsApp API oficial**.
* Si se escaneó un código QR desde la app de WhatsApp Business y el teléfono todavía se usa para responder, probablemente es **API Dual**.
* Si se vinculó como WhatsApp Web y no se configuró como API, probablemente es un canal **QR tradicional**.

**Señales rápidas para reconocerlos**

Es probablemente **WhatsApp API oficial** si:

* El número no está activo en la app de WhatsApp del teléfono.
* Se configuró un Business Portfolio en Meta.
* El número se validó mediante SMS o llamada.
* Se utilizan plantillas de WhatsApp desde Vambe.
* La conexión aparece como WhatsApp API oficial.

Es probablemente **API Dual** si:

* El número sigue funcionando en la app WhatsApp Business.
* El teléfono se utiliza para responder conversaciones.
* La conexión se realizó escaneando un código QR.
* El canal aparece como Dual, Coexistence o una denominación similar.
* Se puede responder desde el teléfono y desde Vambe.

Es probablemente **QR tradicional** si:

* Se conecta de forma similar a WhatsApp Web.
* No existe una configuración de WhatsApp Business API en Meta.
* El canal no tiene funciones oficiales de API.
* La conexión depende de una sesión activa en el teléfono.

***

## 3. Qué revisar antes de reconectar

**Accesos necesarios**

* Acceso a la cuenta de Vambe.
* Permisos suficientes para administrar canales.
* Acceso de administrador o administrador técnico al Business Portfolio de Meta.
* Acceso a la cuenta de WhatsApp Business correspondiente.
* Acceso al teléfono que utiliza el número, si se trata de API Dual.

**Información del canal** — ten a mano:

* El nombre interno del canal en Vambe.
* El número completo con código de país.
* Los últimos dígitos del número, para evitar confundirlo con otro.
* El tipo de conexión.
* El Business Portfolio de Meta asociado.
* La cuenta de WhatsApp Business correspondiente.

**Condiciones técnicas** — comprueba que:

* El teléfono tenga conexión estable a internet.
* El navegador esté actualizado.
* Las ventanas emergentes no estén bloqueadas.
* El teléfono tenga batería suficiente.
* La app WhatsApp Business esté actualizada, si utilizas API Dual.
* El usuario tenga permisos para escanear códigos QR o administrar dispositivos vinculados.
* El número pueda recibir SMS o llamadas, si Meta solicita una verificación.
* No haya otra persona intentando registrar o reconectar el mismo número al mismo tiempo.

{% hint style="danger" %}
- No compartas códigos de verificación, contraseñas ni códigos QR.
- No elimines el número de Meta antes de confirmar qué tipo de conexión necesita.
- No crees un canal nuevo para reemplazar uno desconectado sin revisar el canal original.
- No abras varios procesos de conexión en distintas pestañas.
- Si el asistente, el embudo o las conversaciones son importantes para la operación, confirma que el canal original siga asociado al embudo correcto antes de tocar nada.
{% endhint %}

***

## 4. Cómo reconectar WhatsApp API oficial

Utiliza este procedimiento cuando el canal sea una conexión oficial de WhatsApp API y no uses la aplicación de WhatsApp en el teléfono.

{% stepper %}
{% step %}
**Abrir la sección de canales**

1. Ingresa a Vambe.
2. Abre **Canales**.
3. Ubica el canal de WhatsApp que aparece desconectado o con problemas.

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

5. Revisa si Vambe muestra una opción como **Reconectar**, **Conectar nuevamente** o una acción equivalente.

Si el canal original aparece disponible para reconexión, usa ese canal. Evita crear uno nuevo.
{% endstep %}

{% step %}
**Confirmar la cuenta de Meta**

Cuando se abra el proceso de Meta:

* Confirma que estás utilizando el **Business Portfolio correcto**.
* Verifica que la cuenta tenga permisos de administrador.
* Selecciona la cuenta de WhatsApp Business que corresponde al número.
* Confirma que estás trabajando con el número correcto.

<figure><img src="../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Uno de los errores más comunes es iniciar sesión con una cuenta personal o con un Business Portfolio distinto al que originalmente administraba el canal.
{% endhint %}
{% endstep %}

{% step %}
**Confirmar o registrar el número**

Según el estado del canal, Meta puede mostrar una opción para confirmar un número existente, volver a autorizar la conexión, agregar un número de teléfono o registrarlo nuevamente.

{% hint style="danger" %}
Si Meta muestra un número que no reconoces, **detén el proceso** y revisa la cuenta antes de continuar.
{% endhint %}

Si aparece la opción para registrar un número:

1. Selecciona **Agregar nuevo número de teléfono**.
2. Ingresa el número con su código de país.
3. Selecciona el método de verificación: SMS o llamada telefónica.
4. Ingresa el código recibido.
5. Completa el proceso en Meta.
6. Regresa a Vambe y continúa con la verificación si la plataforma la solicita.

En algunos flujos, el código recibido debe usarse primero en Meta y luego nuevamente en Vambe. Sigue exactamente las instrucciones que aparecen en pantalla.
{% endstep %}

{% step %}
**Finalizar la conexión**

1. Confirma que Meta haya terminado la configuración.
2. Regresa a Vambe.
3. Verifica que el canal cambie a un estado conectado o activo.
4. Confirma que el número y el nombre del canal sean correctos.
5. Revisa que el canal continúe asociado al embudo correspondiente.
{% endstep %}

{% step %}
**Hacer una prueba**

1. Envía un mensaje al número desde otro teléfono.
2. Envía una respuesta desde Vambe, respetando las reglas de WhatsApp para conversaciones abiertas y plantillas.

{% hint style="info" %}
Si el mensaje llega al canal pero el asistente no responde, el problema podría no ser la conexión. Revisa que el canal esté asociado a un embudo y que exista un asistente activo en la primera etapa correspondiente.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## 5. Cómo reconectar WhatsApp API Dual

Utiliza este procedimiento cuando el número siga funcionando en la app WhatsApp Business y también deba usarse desde Vambe.

{% stepper %}
{% step %}
**Preparar el teléfono**

* Abre la app WhatsApp Business.
* Confirma que estás utilizando la cuenta correcta.
* Verifica que el número corresponda al canal de Vambe.
* Comprueba que el teléfono tenga conexión a internet.
* Mantén abierta la app durante el proceso.
* Asegúrate de que la app esté actualizada.

{% hint style="warning" %}
La función Dual no corresponde a una cuenta personal de WhatsApp. Debe utilizarse con WhatsApp Business.
{% endhint %}
{% endstep %}

{% step %}
**Confirmar los requisitos de Meta**

Antes de escanear el código QR, verifica que:

* El Business Portfolio esté verificado.
* Tienes permisos para administrar la cuenta.
* La cuenta de WhatsApp Business corresponde al número correcto.
* Existe un método de pago configurado en Meta, si se usarán plantillas o campañas.
* No hay otro proceso de vinculación abierto.
{% endstep %}

{% step %}
**Iniciar la reconexión desde Vambe**

1. Ingresa a **Canales**.
2. Ubica el canal Dual desconectado.
3. Selecciona la opción de reconexión que muestre Vambe.
4. Espera a que aparezca el código QR.

<figure><img src="../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
No uses una captura de pantalla antigua. El código QR puede cambiar y debe escanearse directamente desde la pantalla activa de Vambe.
{% endhint %}
{% endstep %}

{% step %}
**Escanear el código QR**

Desde la app WhatsApp Business:

1. Abre **Configuración** o el menú de opciones.
2. Ingresa a **Dispositivos vinculados**.
3. Selecciona **Vincular un dispositivo**.
4. Autoriza la acción si la app lo solicita.
5. Escanea el código QR que aparece en Vambe.

Si el código expiró, genera uno nuevo y vuelve a escanearlo.
{% endstep %}

{% step %}
**Confirmar la vinculación**

1. Espera a que Vambe confirme la conexión.
2. Verifica que el canal aparezca activo.
3. Comprueba que el teléfono continúe mostrando la vinculación correspondiente.
4. Confirma que el canal siga conectado al embudo correcto.
{% endstep %}

{% step %}
**Hacer pruebas desde ambos lugares**

* Envía un mensaje desde el teléfono.
* Responde desde Vambe.
* Envía un mensaje desde otro número hacia el canal.
* Confirma que la conversación aparezca en Vambe.

{% hint style="info" %}
En una conexión Dual, desde el teléfono se puede responder usando la app, pero desde Vambe aplican las reglas de WhatsApp API, incluida la ventana de atención de 24 horas. Cuando esa ventana está cerrada, puede ser necesario usar una plantilla aprobada para iniciar o retomar la conversación desde Vambe.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## 6. Qué hacer si la reconexión no funciona

**El código QR no aparece**

Revisa que: estés reconectando un canal Dual y no un canal API oficial; el navegador no esté bloqueando la pantalla de conexión; no haya otro proceso abierto en una pestaña diferente; el canal siga existiendo en Vambe; la sesión anterior no esté a medio completar. Si la pantalla queda en blanco, actualiza la página una sola vez y vuelve a ingresar al canal —no abras muchos procesos simultáneos.

**El código QR expiró**

Los códigos QR son temporales. Cierra el código anterior, solicita o genera uno nuevo, abre WhatsApp Business en el teléfono, ingresa a **Dispositivos vinculados** y escanea el código nuevo directamente desde la pantalla. No intentes escanear una captura de pantalla antigua.

**WhatsApp no permite escanear el código**

Comprueba que: estés usando WhatsApp Business y no WhatsApp personal; la app esté actualizada; la cámara tenga permisos; el brillo de la pantalla sea suficiente; el teléfono tenga conexión a internet; el código no haya expirado; no se haya alcanzado el límite de dispositivos vinculados.

**Meta indica que el número ya está conectado**

Este mensaje puede aparecer porque el número ya está asociado a otra cuenta de WhatsApp Business, sigue vinculado a una conexión anterior, se inició un proceso nuevo en vez de reconectar el canal existente, se eligió un Business Portfolio equivocado, o el número está activo en una app incompatible con el tipo de conexión elegido.

{% hint style="danger" %}
No elimines la cuenta ni desvincules el número sin confirmar primero cuál es la conexión correcta. Si el número ya pertenece a un canal funcional, intenta reconectar ese canal en lugar de registrarlo nuevamente.
{% endhint %}

**No llega el código por SMS**

Verifica el código de país, la cobertura del teléfono, que el número pueda recibir SMS, que no tenga bloqueadas llamadas o mensajes internacionales, y que no se hayan solicitado demasiados códigos seguidos. Si está disponible, prueba la opción de llamada telefónica. No compartas el código con otra persona ni lo ingreses en una página que no sea Meta o Vambe.

**Meta muestra el Business Portfolio equivocado**

Cancela el proceso, cierra la sesión de Meta si es necesario, vuelve a iniciar sesión con el usuario administrador correcto, confirma el Business Portfolio asociado al canal y repite la reconexión desde el canal existente. Si no tienes acceso al Business Portfolio correcto, necesitarás que un administrador de Meta realice la reconexión.

**La cuenta de Meta no está verificada**

La conexión Dual requiere un Business Portfolio verificado. Si Meta solicita verificar la empresa, revisa el estado de verificación en Meta Business, completa la verificación solicitada, confirma que la cuenta figure como verificada y vuelve a iniciar el proceso de reconexión. No intentes solucionar una falta de verificación creando otro canal.

**El canal aparece conectado, pero no recibe mensajes**

Revisa en este orden: que el número utilizado por el cliente sea el correcto; que el canal esté activo en Vambe; que el canal siga conectado a un embudo; que el embudo tenga una primera etapa válida; que exista un asistente asignado a esa etapa; que el mensaje de prueba no se esté enviando desde el mismo teléfono administrador; que no existan restricciones o bloqueos en Meta.

**El canal recibe mensajes, pero el asistente no responde**

La reconexión podría estar correcta. Revisa si el canal está asociado a un embudo, si el asistente está activo, si el contacto fue enviado a la etapa correcta, si existe una configuración para no responder, si el mensaje está dentro de las reglas de atención de WhatsApp, o si se requiere una plantilla porque la ventana de 24 horas está cerrada.

**Se creó un canal duplicado**

No continúes probando sobre ambos canales. Primero identifica cuál es el canal original, cuál tiene el historial y la configuración correcta, cuál está conectado al embudo, y cuál utiliza el número correcto. Después, solicita ayuda antes de eliminar cualquiera de los canales —eliminar el canal equivocado puede afectar la operación y las asociaciones existentes.

***

## 7. Lista de verificación final

La reconexión puede considerarse completa cuando se cumplen todos estos puntos:

* El canal aparece como conectado o activo.
* El número es el correcto.
* El tipo de conexión coincide con la configuración original.
* El Business Portfolio seleccionado es el correcto.
* En API Dual, el teléfono aparece vinculado correctamente.
* El canal está conectado al embudo correspondiente.
* Se recibe un mensaje de prueba.
* Se puede responder desde Vambe.
* En API Dual, se puede responder desde el teléfono.
* El mensaje llega al contacto correcto.
* No existe un segundo canal duplicado para el mismo número.
* El equipo sabe desde dónde debe responder y qué reglas aplican.

***

## 8. Cuándo solicitar ayuda

Solicita soporte si:

* No sabes si el canal es API, Dual o QR.
* Meta muestra una cuenta o número que no reconoces.
* El número aparece conectado a otra cuenta y no sabes cuál.
* El Business Portfolio correcto no aparece.
* No tienes permisos de administrador.
* La reconexión termina, pero el canal sigue desconectado.
* El canal está conectado, pero los mensajes no llegan después de realizar las pruebas.
* Hay dos canales con el mismo número.
* El proceso solicita eliminar o desvincular información y no estás seguro de las consecuencias.

**Información que debes entregar a soporte**

* Nombre interno del canal.
* Últimos dígitos del número.
* Tipo de conexión, si lo conoces.
* Mensaje exacto del error.
* Captura de pantalla del error.
* Paso en el que se detuvo la reconexión.
* Si el número funciona en la app WhatsApp Business.
* Si el Business Portfolio está verificado.
* Si el canal aparece conectado a un embudo.

{% hint style="danger" %}
**Nunca envíes:** contraseñas, códigos de verificación, tokens, códigos QR, ni datos de acceso a Meta.
{% endhint %}

***

### Preguntas frecuentes

**¿WhatsApp API y API Dual son lo mismo?** No. Ambas son conexiones oficiales relacionadas con Meta, pero funcionan distinto. WhatsApp API oficial se usa desde la plataforma y no requiere la app de WhatsApp en el teléfono. API Dual permite usar la app WhatsApp Business y Vambe al mismo tiempo.

**¿Puedo reconectar API Dual sin el teléfono?** No. Para API Dual necesitas acceder al teléfono que tiene instalada la cuenta WhatsApp Business, porque debes escanear el código QR desde la sección de dispositivos vinculados.

**¿Puedo conectar un número personal como API Dual?** No. API Dual requiere una cuenta de WhatsApp Business.

**¿Puedo usar el mismo número en WhatsApp API oficial y API Dual?** No debes iniciar dos conexiones distintas con el mismo número sin confirmar primero la configuración compatible. Hacerlo puede producir conflictos, duplicados o errores de registro.

**¿La reconexión elimina las conversaciones?** No se debe asumir que las conversaciones se eliminarán ni que se conservarán automáticamente. Por eso es importante no borrar el canal ni registrar nuevamente el número sin confirmar el procedimiento correcto.

**¿Por qué puedo responder desde el teléfono, pero no desde Vambe?** En API Dual, el teléfono y Vambe tienen reglas diferentes. Si la conversación está fuera de la ventana de atención de 24 horas, desde Vambe puede ser necesario usar una plantilla aprobada.

**¿Por qué el canal aparece conectado, pero el asistente no responde?** La conexión del canal es solo una parte de la configuración. También debes revisar que el canal esté asociado a un embudo y que exista un asistente activo en la etapa correspondiente.

**¿El nombre del canal lo ven los clientes?** No. Es un nombre interno para identificarlo dentro de Vambe. Los clientes reciben los mensajes desde el número asociado.

***

### En resumen

Si después de seguir estos pasos el canal continúa desconectado, no elimines la conexión ni registres nuevamente el número. Guarda el mensaje de error y solicita ayuda indicando el nombre del canal, los últimos dígitos del número y el paso exacto en que falló la reconexión.
