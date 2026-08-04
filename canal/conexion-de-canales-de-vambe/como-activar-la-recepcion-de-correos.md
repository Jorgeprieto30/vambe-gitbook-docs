# Cómo activar la recepción de correos

## Cómo activar la recepción de correos

#### ¿Para qué sirve?

El canal de Email de Vambe no solo envía: también recibe. Al activar la recepción, las respuestas de tus contactos entran directamente a Vambe, se abren como tickets dentro del embudo que elijas y quedan registradas en el historial del contacto. Tu asistente puede leerlas y responderlas igual que en cualquier otro canal, y tus Ejecutivos pueden retomar la conversación desde la misma vista de Chat.

> Para entrar: en el menú lateral ve a **Canales** y ubica tu canal de email dentro de **Canales conectados**.

Cada canal de email muestra un ícono de bandeja que indica el estado de la recepción. Si aparece en gris, la recepción de respuestas todavía no está habilitada: al pasar el cursor verás el aviso _"La recepción de respuestas no está habilitada. Abre el canal para habilitarla."_ Ese mismo ícono es el punto de partida de la configuración.

\[IMAGEN 1: fila del canal de email en Canales conectados, con el tooltip de recepción no habilitada]

{% hint style="info" %}
¿Aún no tienes el canal de email conectado? Primero sigue la guía de Cómo conectar el canal de Email. La recepción se activa sobre un canal ya creado.
{% endhint %}

***

#### Paso 1: Elige cómo quieres recibir tus correos

Haz clic en el ícono de recepción del canal. Vambe te mostrará dos métodos de configuración, según cómo administres tu correo.

**Opción A: Reenvío desde Gmail (recomendada)**

Pensada para cuentas de Gmail o Google Workspace. Configuras un reenvío automático desde tu bandeja hacia una dirección que Vambe te entrega, y listo.

Necesitas:

* Una cuenta de Gmail o Google Workspace
* Acceso a la configuración de tu correo
* Escribir a tus clientes desde Vambe

**Opción B: Configurar mi dominio propio**

Apunta el registro MX de tu dominio hacia Vambe desde tu proveedor de DNS.

Necesitas:

* Acceso al panel de DNS de tu dominio
* Apoyo de tu equipo técnico, según el proveedor
* Considerar que los cambios pueden tardar entre 24 y 48 horas en propagarse

{% hint style="warning" %}
⚠️ **Por qué recomendamos el reenvío desde Gmail:** al cambiar el registro MX, los correos dejan de llegar a la bandeja de Google y entran únicamente a Vambe. Si quieres seguir viendo tus correos también en Gmail, elige el reenvío.
{% endhint %}

{% hint style="info" %}
Para habilitar la recepción necesitas una cuenta de correo conectada. Conéctala en la primera tarjeta antes de continuar.
{% endhint %}

\[IMAGEN 2: modal "¿Cómo quieres recibir tus correos?" con las dos tarjetas de configuración]

***

#### Paso 2: Configura el reenvío desde Gmail

Al elegir esta opción, Vambe abre un asistente de tres pasos que te acompaña mientras haces los cambios en Gmail. Mantén ambas pestañas abiertas: vas a copiar un dato desde Vambe y pegarlo en Gmail.

**1. Entra a la configuración de reenvío**

En Gmail, haz clic en el ícono de engranaje (arriba a la derecha) y elige **Ver toda la configuración**. Abre la pestaña **Reenvío y correo POP/IMAP**.

\[IMAGEN 3: paso 1 del asistente, con la pestaña de Reenvío y correo POP/IMAP destacada]

**2. Agrega la dirección de reenvío**

En la sección **Reenvío**, haz clic en **Añadir una dirección de reenvío**. Copia la dirección que te muestra Vambe —tiene el formato `fwd-xxxxxxxx@in.vambe-mail.com`— pégala en el campo y confirma con **Siguiente → Continuar → Aceptar**.

\[IMAGEN 4: paso 2 del asistente, con la dirección de reenvío entregada por Vambe]

\[IMAGEN 5: ventana de Gmail "Añadir una dirección de reenvío" con la dirección pegada]

\[IMAGEN 7: ventana de confirmación de Gmail con el botón Proceder]

Google puede pedirte que verifiques tu identidad antes de confirmar el reenvío. Sigue las instrucciones en pantalla: normalmente es una notificación en tu teléfono con un número que debes seleccionar.

\[IMAGEN 6: pantalla de verificación de identidad de Google]

{% hint style="info" %}
Después de confirmar, recarga la página de configuración de Gmail. Recién ahí la dirección queda disponible en el desplegable del paso siguiente.
{% endhint %}

**3. Activa el reenvío y guarda**

De vuelta en **Reenvío y correo POP/IMAP**, selecciona la opción **Reenviar una copia del correo entrante a…** y elige en el desplegable la dirección que acabas de agregar. Baja hasta el final de la página y haz clic en **Guardar cambios**.

\[IMAGEN 10: sección de Reenvío de Gmail con la dirección seleccionada]

Cuando el reenvío queda activo, el asistente de Vambe te lo confirma con el mensaje **¡Reenvío confirmado!** y el ícono de recepción del canal cambia de estado en la lista de canales.

\[IMAGEN 8: paso 3 del asistente con el mensaje ¡Reenvío confirmado!]

***

#### Paso 3: Asocia el canal a un embudo

Para que las respuestas se conviertan en tickets, el canal debe estar asociado a un embudo. En **Canales**, ve al panel **Asocia canales a tus embudos**, busca el embudo donde quieres trabajar los correos y haz clic en **+ Asociar canal**. Vambe confirmará con el mensaje **Canal agregado al pipeline**.

\[IMAGEN 11: panel de asociación de canales a embudos con la confirmación "Canal agregado al pipeline"]

{% hint style="warning" %}
Al asociar un canal de email a un embudo, el asistente ajusta su formato de respuesta al formato de correo y queda preconfigurado para ese canal. Si necesitas afinar el tono, las instrucciones o el contenido de las respuestas, hazlo desde la sección **Asistente**.
{% endhint %}

***

#### Paso 4: Dónde ves las respuestas

Desde ese momento el canal funciona igual que el resto de Vambe. En el menú lateral entra a **Chat** y usa el filtro **Correos** para ver solo las conversaciones de email: cada hilo aparece como un ticket, con su estado de atención y su asignación.

\[IMAGEN 13: vista de Chat con el filtro Correos y la lista de hilos]

Al abrir un ticket verás el hilo completo del correo, la información del contacto a la derecha y el cuadro de respuesta abajo, con las opciones **Responder** y **Responder a todos**. Puedes editar el destinatario, el asunto y el cuerpo antes de enviar, y también agregar notas o tareas asociadas al contacto.

\[IMAGEN 12: ticket de email abierto con el hilo, el panel de contacto y el cuadro de respuesta]

***

#### En resumen

Activar la recepción convierte tu canal de email en una conversación de ida y vuelta: los correos que responden tus contactos llegan a Vambe, se ordenan como tickets dentro del embudo correcto y quedan disponibles para tu asistente y tus Ejecutivos, en el mismo lugar donde ya gestionas WhatsApp, Instagram y el resto de tus canales.
