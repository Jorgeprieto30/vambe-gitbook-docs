# Cómo conectar el canal de Email

## Cómo conectar el canal de Email

#### ¿Para qué sirve?

El canal de Email te permite enviar y recibir correos directamente desde Vambe. Según lo que necesites, puedes conectar la casilla real de tu equipo (Gmail o Outlook) para que tu asistente responda conversaciones desde tu propia bandeja, o conectar un dominio para enviar campañas masivas con plantillas personalizadas. También puedes hacer ambas cosas con la misma cuenta.

{% hint style="info" %}
Una vez conectado el canal, aprende a crear plantillas, enviar campañas y automatizar envíos en Cómo usar el canal de Email en Vambe.
{% endhint %}

***

#### Antes de empezar

Ten esto a mano para completar la conexión de una sola vez:

* Permisos para crear canales en tu cuenta de Vambe.
* El embudo de destino, con su asistente ya configurado.
* Si vas a responder conversaciones desde tu propia casilla: acceso a esa cuenta de Gmail u Outlook para autorizar a Vambe.
* Si vas a enviar campañas: la casilla real que recibe los correos (`contacto@`, `ventas@`, `soporte@`) y, si conectarás un dominio propio, acceso a su panel DNS.

***

#### Paso 1: Agrega el canal y elige para qué lo vas a usar

Desde el menú lateral, ve a **Canales** y haz clic en **+ Agregar canal**. En las opciones disponibles, selecciona **Email**.

<figure><img src="../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

Vambe te pregunta primero **¿Para qué vas a usar el correo?**, con tres opciones:

* **Responder y enviar correos** — para atender clientes: los correos que te escriben llegan a la bandeja de Vambe y los contestas ahí mismo, además de poder escribir correos individuales. Conecta tu casilla real (Gmail u Outlook).
* **Solo enviar campañas** — para enviar correos masivos a tus listas de contactos: newsletters, promociones y seguimientos automáticos con plantillas. Usa un dominio verificado, propio o de Vambe.
* **Ambas** — conecta tu casilla para responder mensajes y, además, verifica tu dominio para enviar campañas masivas desde una misma cuenta.

<figure><img src="../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Cómo elegir:** si tu prioridad es que el asistente conteste conversaciones uno a uno desde una casilla real del equipo, parte por **Responder y enviar correos**. Si lo que necesitas es mandar campañas masivas con tu marca, ve directo a **Solo enviar campañas**. **Ambas** te deja las dos cosas configuradas de una vez.
{% endhint %}

***

#### Responder y enviar correos: conecta tu casilla real (Gmail u Outlook)

Esta ruta conecta la cuenta real del equipo —Gmail u Outlook— para que las conversaciones del asistente salgan y entren directamente en esa bandeja: la persona que escribe recibe la respuesta en el mismo hilo, incluido en **Enviados**, y desde la dirección real, no desde un remitente genérico. Al conectar la casilla, Vambe también importa el historial reciente de conversaciones de esa cuenta.

1. Elige tu proveedor de correo: **Gmail** o **Outlook**.
2. Revisa qué autorizas exactamente: Vambe pide permiso para leer los correos que llegan a esa casilla y mostrarlos en Vambe, y para enviar respuestas en tu nombre. No borra ni mueve nada de la cuenta original.

<figure><img src="../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

3. Confirma el inicio de sesión con la cuenta de correo que quieres conectar y acepta los permisos.

<figure><img src="../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

4. Al terminar, la casilla aparece en una nueva sección **Email** dentro de tu lista de canales conectados, con su propio estado e íconos de acción.

<figure><img src="../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Si la casilla queda revocada o alcanza la cuota del proveedor, el envío conversacional **falla de forma visible**: no cae en silencio hacia un envío alternativo desde otra dirección. El estado de la casilla se ve directamente en el canal, así que conviene revisarlo si notas que las respuestas no están saliendo.
{% endhint %}

{% hint style="info" %}
Si ya tenías canales configurados por **reenvío (forwarding)**, siguen funcionando igual: conectar la casilla real no elimina el forwarding existente. Son dos formas de recibir correo que pueden convivir.
{% endhint %}

***

#### Solo enviar campañas: elige tu método de conexión de dominio

Esta ruta aplica si elegiste **Solo enviar campañas** o **Ambas**. Al configurar el canal, puedes elegir entre dos métodos:

* **Dominio Vambe** _(recomendado)_ — Vambe te provee un dominio. Solo necesitas ingresar un subdominio y nosotros nos encargamos del resto.
* **Dominio propio** — Conecta tu propio dominio si no quieres que los correos aparezcan con `@subdominio.vambe-mail.com`.

{% hint style="info" %}
**Cómo elegir:** el criterio no es solo la imagen de marca, sino si administras tus propios DNS. Si tienes acceso al panel de tu dominio y sabes moverte en él, el dominio propio te sirve. Si no, el dominio de Vambe deja el canal andando en la misma sesión y sin depender de nadie.
{% endhint %}

**Opción A: Dominio Vambe (recomendado)**

Con este método, Vambe te ofrece un dominio directamente, eliminando la necesidad de configurar registros DNS manualmente.

1. Selecciona la opción **Dominio Vambe** al configurar el canal.
2. Ingresa el **subdominio** que quieras usar (ej: `tuempresa`).
3. Vambe configurará el resto automáticamente.

Los correos se enviarán y visualizarán con el formato: `@{subdominio}.vambe-mail.com`

{% hint style="info" %}
✅ El canal queda operativo en **menos de 30 segundos**. Con esta ruta puedes saltar directamente al Paso 4.
{% endhint %}

![Paso 1: elegir el dominio de Vambe](https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F4jEVTkJx4NxhcpG46WQU%2Fimage.png?alt=media\&token=cd230903-993f-41df-a7a3-9916ed0036d9)

**Opción B: Dominio propio**

Usa este método si deseas que los correos se envíen desde tu propio dominio y no quieres que aparezca `vambe-mail.com`. El asistente pasa de tres pasos a cuatro al elegir esta ruta.

Completa los siguientes campos:

* **Dominio:** el dominio desde el que enviarás (ej: `tuempresa.com`)
* **Email del remitente:** el prefijo del correo, la parte antes de la arroba (ej: `contacto`, `ventas`)
* **Nombre del remitente:** el nombre que verán tus contactos al recibir el mail

Haz clic en **Continuar**.

{% hint style="info" %}
Si tu asistente va a conversar por este canal, evita un remitente del tipo `noreply` y elige uno que invite a responder. En el **nombre del remitente** usa tu nombre comercial, no el nombre interno del proyecto.
{% endhint %}

![Paso 2: dominio, email del remitente y nombre del remitente](https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FLgYkgxwDLvJewHY9WUpC%2Fimage.png?alt=media\&token=158da9c7-b7c7-4218-b960-98220eb1acf2)

***

#### Agrega los registros DNS

Este paso aplica solo si conectaste con **dominio propio**. Vambe te mostrará los registros que debes agregar en el administrador de tu dominio (GoDaddy, Dynadot, Cloudflare, etc.). Son cuatro: uno confirma que el dominio es tuyo y los otros tres autentican el envío.

| Registro          | Tipo  | Para qué sirve                                            | Ojo con                                         |
| ----------------- | ----- | --------------------------------------------------------- | ----------------------------------------------- |
| `_vambe-verify`   | TXT   | Confirma la propiedad del dominio y evita la suplantación | Es el único TXT. Se pega tal cual, sin comillas |
| `em####`          | CNAME | Autenticación de envío                                    | Proxy desactivado                               |
| `vmb._domainkey`  | CNAME | Firma del dominio                                         | Proxy desactivado                               |
| `vmb2._domainkey` | CNAME | Firma del dominio                                         | Proxy desactivado                               |

Copia cada valor desde Vambe y pégalo en la configuración DNS de tu proveedor. Al terminar, presiona **Verificar DNS**. Si prefieres hacerlo más tarde, **Verificar después** no cancela la conexión: puedes cerrar el diálogo y retomarlo desde la sección **Canales**.

![Paso con los registros DNS y el aviso de propagación](https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FSRXmTRyIIO0DBfWiXqEo%2Fregistros-dns.jpg?alt=media)

{% hint style="danger" %}
⚠️ **El error que más tiempo hace perder:** en los tres CNAME el proxy tiene que quedar desactivado. En Cloudflare el control se llama **Proxy status** y debe mostrar **DNS only**, con la nube gris y no naranja. Si el registro queda proxeado, la verificación nunca pasa y no aparece ningún error que lo explique.
{% endhint %}

![Cloudflare: el registro TXT de verificación](https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FgNDCqhNenwpwwISpEIqj%2Fcloudflare-txt.jpg?alt=media)

![Cloudflare: registro CNAME con Proxy status en DNS only](https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FwgZjWY2i4UTfiLPRhOra%2Fcloudflare-dns-only.jpg?alt=media)

**Entender los contadores**

Verás tres números distintos según dónde estés, y ninguno indica un error:

| Verás                | Cuándo                             | Qué cuenta                             |
| -------------------- | ---------------------------------- | -------------------------------------- |
| **0/4 verificados**  | Mientras cargas los registros      | El TXT de propiedad más los tres CNAME |
| **Verificado (3/3)** | En el canal ya conectado           | Solo los tres CNAME de autenticación   |
| **Verificado (1/1)** | En la recepción por dominio propio | El registro de entrada                 |

{% hint style="warning" %}
⏱️ **Ten en cuenta:** por lo general la verificación toma segundos, pero la propagación DNS puede tardar hasta 48 horas. Si pasan los dos días sin verificar, revisa primero el proxy y luego los registros carácter por carácter.
{% endhint %}

![Un check verde por registro cuando la verificación queda lista](https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2Fk3UTiTZgyWdY4jFCao3X%2Fdns-verificado.jpg?alt=media)

***

#### Verifica que el envío quedó activo

En **Configuración del Canal** la etiqueta **ENVÍO** debe aparecer activa. Ese es el estado correcto al terminar la conexión de dominio por cualquiera de las dos rutas: envío activo y recepción todavía pendiente.

![Configuración del Canal con el envío verificado](https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FLrl4lMMmJoscjyC3Akk1%2Fcanal-envio-activo.jpg?alt=media)

***

#### Activa la recepción de respuestas (canal por dominio)

Si conectaste el canal para campañas y quieres que las respuestas de tus contactos también lleguen a Vambe y se abran como tickets, activa la recepción desde el ícono de bandeja del canal.

{% hint style="info" %}
Sigue el paso a paso en Cómo activar la recepción de correos.
{% endhint %}

***

#### Qué no cambia

El email marketing —tus campañas masivas— se sigue enviando siempre con el dominio autenticado del cliente, sea el dominio de Vambe o uno propio. Conectar tu casilla real para conversaciones no reemplaza ni afecta ese envío.

***

¡Listo! Tu canal de Email quedó conectado. El siguiente paso es definir cómo responde tu asistente en el canal de correo y crear tus plantillas y campañas.
