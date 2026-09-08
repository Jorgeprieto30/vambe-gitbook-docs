---
description: >-
  Cierra la venta sin sacar al cliente de la conversación: conecta tu cuenta de
  cobro, configura la función de link de pago y deja que el asistente cobre por
  ti.
---

# ¿Cómo cobrar dentro del chat con un link de pago?

El momento en que un cliente decide comprar es el más frágil de toda la conversación. La función **Link de pago** permite que tu asistente genere un enlace de cobro y lo envíe dentro del mismo chat, para que el cliente pague sin cambiar de canal ni esperar a que alguien de tu equipo le escriba.

Cuando el pago se acredita, Vambe lo detecta automáticamente: el contacto avanza a la etapa que definiste y se dispara un evento que puedes usar para encadenar tus automatizaciones. En este artículo aprenderás a conectar tu cuenta de cobro, a configurar la función y a entender qué ocurre después del pago.

{% hint style="info" %}
**Para entrar:** en el menú de la izquierda, ve a **Ajustes** y luego a **Integraciones** para conectar tu cuenta de cobro. La función se crea después desde **Asistente**, en la pestaña **Funciones**.
{% endhint %}

***

## 1. Conecta tu cuenta de cobro

Antes de que el asistente pueda cobrar, Vambe necesita saber qué cuenta recibirá el dinero. Esa asociación se hace una sola vez desde el directorio de conectores.

Si vas a cobrar con **Mercado Pago**, sigue los pasos de esta sección. Si vas a cobrar con **Fintoc**, la cuenta bancaria se agrega directamente al crear la función, como verás en el paso 2.

En **Ajustes → Integraciones**, busca la sección **PAGOS** y haz clic en la tarjeta de **Mercado Pago**.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2Fus4utjMIxA0APJqZwNuS%2Fimg-mp-integraciones.png?alt=media" alt="Sección PAGOS del directorio de conectores con la tarjeta de Mercado Pago"><figcaption></figcaption></figure>

Dentro del detalle encontrarás el bloque **Cuentas de Mercado Pago** y el botón **+ Agregar Cuenta**. Al autorizar el acceso, la cuenta queda listada con el estado **Conectado** y ya puede recibir cobros desde cualquier conversación.

Más abajo, el bloque **Características** te muestra qué medios quedan habilitados para tus clientes: **tarjetas de crédito y débito**, **cuotas** y el **saldo de la billetera de Mercado Pago**.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FD4hME7yxCEWbNElpzSA9%2Fimg-mp-cuenta-conectada.png?alt=media" alt="Detalle de la integración de Mercado Pago con una cuenta conectada"><figcaption></figcaption></figure>

{% hint style="info" %}
Puedes asociar más de una cuenta. Es útil cuando trabajas con varias razones sociales o marcas y necesitas que cada cobro llegue al lugar correcto.
{% endhint %}

***

## 2. Crea la función de link de pago

Con la cuenta conectada, el siguiente paso es darle a tu asistente la herramienta para cobrar.

Entra a tu asistente, abre la pestaña **Funciones** y haz clic en **+ Crear función**. En la categoría **Pagos** encontrarás **Link de pago**.

<figure><img src="../.gitbook/assets/img-funcion-catalogo-pagos.png" alt="Panel Crear función con la categoría Pagos, donde se encuentra Link de pago"><figcaption></figcaption></figure>

Se abrirá el panel de configuración con los siguientes campos:

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FjYtTb2QLpkCVfxnNLuUP%2Fimg-funcion-config.png?alt=media" alt="Panel de configuración de la función Link de pago"><figcaption></figcaption></figure>

* **Nombre** — un identificador claro para encontrar la función después (ej: _Cobrar reserva_).
* **Descripción** — le indica a la IA en qué momento debe activarse. Es el campo más importante: descríbelo con la misma lógica que usaste en tus instrucciones (ej: _Cuando el cliente confirme que quiere comprar_).
* **Medio de pago** — elige quién procesa el cobro:
  * **Fintoc**, para transferencia bancaria.
  * **Mercado Pago**, para tarjetas, billetera y cuotas.
* **Cuenta de Mercado Pago** — la cuenta conectada que recibirá el dinero.
* **Etapa tras pago exitoso** — la etapa del embudo a la que se moverá el contacto en cuanto el pago se acredite.
* **Monto fijo (opcional)** — si siempre cobras el mismo valor (una reserva, una suscripción, un abono), escríbelo aquí. Si lo dejas en blanco, el monto se define durante la conversación.

{% hint style="info" %}
Si eliges **Fintoc** y todavía no tienes una cuenta bancaria configurada, Vambe te lo muestra ahí mismo: haz clic en **Agregar una cuenta bancaria** e ingresa el banco, el tipo de cuenta, el número de cuenta y el RUT del titular. Con esos datos la cuenta queda lista para recibir los cobros.
{% endhint %}

<figure><img src="../.gitbook/assets/img-fintoc-config-aviso.png" alt="Configuración de la función Link de pago con Fintoc seleccionado y el aviso de cuenta bancaria pendiente"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/img-agregar-cuenta-bancaria.png" alt="Formulario para agregar una cuenta bancaria: banco, tipo de cuenta, número de cuenta y RUT del titular"><figcaption></figcaption></figure>

***

## 3. Indícale a la IA cuándo cobrar

Una función solo se ejecuta si la IA sabe reconocer el momento. Además de crearla, escribe la instrucción dentro de **Pasos a Seguir** o **Casos Posibles**, según cómo esté construido tu asistente.

* _Fórmula:_ `Cuando [el cliente confirme la compra], debes ejecutar la función [Nombre de la función]`.

> **Ejemplo real:** "Cuando el cliente confirme la hora y el servicio que quiere reservar, ejecuta la función Cobrar reserva y envíale el link de pago".

Procura que la instrucción del texto y la descripción interna de la función digan lo mismo. Cuando ambas coinciden, la IA activa el cobro en el momento exacto y no antes.

***

## 4. Qué ve tu cliente

El asistente envía el enlace dentro de la conversación. Al abrirlo, el cliente llega al checkout de Mercado Pago, donde elige cómo pagar: con su cuenta de Mercado Pago, desde la app, o con tarjeta de crédito, débito o prepaga sin necesidad de tener cuenta.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FZ1hRivBxbBqF68lKOpPk%2Fimg-checkout-mp.png?alt=media" alt="Checkout de Mercado Pago con las opciones de pago disponibles"><figcaption></figcaption></figure>

Una vez completado el pago, ve una confirmación y puede volver al chat. No necesitas avisarle a nadie: el cobro ya quedó registrado.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2F6ZiLljIB7Umhuxx5xeZx%2Fimg-pago-exitoso.png?alt=media" alt="Pantalla de confirmación de pago exitoso"><figcaption></figcaption></figure>

***

## 5. Qué ocurre después del pago

Aquí está el verdadero valor de cobrar desde el chat: el pago no queda como un dato suelto, sino que mueve tu operación.

1. **El contacto cambia de etapa.** Se mueve automáticamente a la etapa que configuraste en el campo **Etapa tras pago exitoso**, sin que nadie tenga que arrastrar la tarjeta a mano.
2. **Se dispara el evento de pago exitoso.** Ese evento puedes usarlo como gatillante en **Workflows** para encadenar lo que venga después: enviar el comprobante, agendar la entrega, avisar a tu equipo interno o iniciar el proceso de postventa. Si cobraste por Fintoc, el evento se llama **Pago Fintoc exitoso**.

<figure><img src="../.gitbook/assets/img-pago-fintoc-exitoso-workflow.png" alt="Evento Pago Fintoc exitoso como activador de un workflow"><figcaption></figcaption></figure>

***

## Consideraciones

{% hint style="warning" %}
**Reembolsos:** si necesitas devolver un pago, se gestiona directamente desde Mercado Pago.
{% endhint %}

* La integración con Mercado Pago está disponible para cuentas chilenas.
* Revisa que la etapa de destino exista en el embudo antes de guardar la función; así evitas que un pago acreditado se quede sin su movimiento correspondiente.

***

## En resumen

Cobrar dentro del chat elimina la fricción justo donde más cuesta: entre el "sí, lo quiero" y el pago efectivo. Conectas tu cuenta una vez, configuras la función indicando quién cobra y a qué etapa avanza el contacto, y desde ahí tu asistente se encarga de generar el enlace, acompañar al cliente hasta el checkout y dejar todo registrado para que tus automatizaciones sigan trabajando solas.
