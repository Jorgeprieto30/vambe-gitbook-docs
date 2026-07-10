# Cómo conectar el canal de Email

## Cómo conectar el canal de Email

#### ¿Para qué sirve?

El canal de Email te permite enviar correos directamente desde Vambe usando tu propio dominio. Una vez conectado, podrás crear campañas masivas con plantillas personalizadas, enviar emails individuales desde la vista de un ticket y automatizar envíos mediante Workflows.

> ⚠️ **Versión actual — Outbound:** Por ahora, el canal de email funciona de forma outbound (envío hacia tus contactos). La integración con el sistema de tickets y la IA está en desarrollo y llegará próximamente.

{% hint style="info" %}
Una vez conectado el canal, aprende a crear plantillas, enviar campañas y automatizar envíos en Cómo usar el canal de Email en Vambe.
{% endhint %}

***

#### Paso 1: Agrega el canal

Desde el menú lateral, ve a **Canales** y haz clic en **+ Asociar canal**. En las opciones disponibles, selecciona **Email**.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FsKBQFZUkHKtPSJjw7XXY%2Fimage.png?alt=media&#x26;token=96040218-06b5-4457-9b39-285d5b1e7720" alt=""><figcaption></figcaption></figure>

***

#### Paso 2: Elige tu método de conexión

Al configurar el canal de Email en Vambe, puedes elegir entre dos métodos de conexión:

* **Dominio Vambe** _(recomendado)_ — Vambe te provee un dominio. Solo necesitas ingresar un subdominio y nosotros nos encargamos del resto.
* **Dominio propio** — Conecta tu propio dominio si no quieres que los correos aparezcan con `@subdominio.vambe-mail.com`.

**Opción A: Dominio Vambe (recomendado)**

Con este método, Vambe te ofrece un dominio directamente, eliminando la necesidad de configurar registros DNS manualmente.

1. Selecciona la opción **Dominio Vambe** al configurar el canal.
2. Ingresa el **subdominio** que quieras usar (ej: `tuempresa`).
3. Vambe configurará el resto automáticamente.

Los correos se enviarán y visualizarán con el formato: `@{subdominio}.vambe-mail.com`

{% hint style="info" %}
✅ El canal queda operativo en **menos de 30 Segundos**
{% endhint %}

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F4jEVTkJx4NxhcpG46WQU%2Fimage.png?alt=media&#x26;token=cd230903-993f-41df-a7a3-9916ed0036d9" alt=""><figcaption></figcaption></figure>

**Opción B: Dominio propio**

Usa este método si deseas que los correos se envíen desde tu propio dominio y no quieres que aparezca `vambe-mail.com`.

Completa los siguientes campos:

* **Dominio:** el dominio desde el que enviarás (ej: `tuempresa.com`)
* **Email del remitente:** el prefijo del correo (ej: `noreply`)
* **Nombre del remitente:** el nombre que verán tus contactos al recibir el mail

Haz clic en **Continuar**.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FLgYkgxwDLvJewHY9WUpC%2Fimage.png?alt=media&#x26;token=158da9c7-b7c7-4218-b960-98220eb1acf2" alt=""><figcaption></figcaption></figure>

***

#### Paso 3: Agrega los registros DNS

Este paso aplica solo si conectaste con **dominio propio**. Vambe te mostrará los registros que debes agregar en el administrador de tu dominio (GoDaddy, Dynadot, Cloudflare, etc.). Los registros son:

* **SPF (Return Path):** un registro CNAME en tu dominio
* **DKIM Selector 1 y 2:** dos registros CNAME adicionales para autenticación

Copia cada valor desde Vambe y pégalo en la configuración DNS de tu proveedor. Si no lo haces de inmediato, puedes hacer clic en **Verificar después** y completarlo más tarde.

{% hint style="warning" %}
⏱️ **Ten en cuenta:** La propagación DNS puede tomar hasta 48 horas. Puedes revisar el estado de verificación en cualquier momento desde la sección **Canales**, donde verás el indicador **Verificar DNS** junto a tu canal de email.
{% endhint %}

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FkUDhW9Z3RtRLYT9HXgb5%2Fimage.png?alt=media&#x26;token=85834731-afbc-45c6-b350-8ed59214bc57" alt=""><figcaption></figcaption></figure>

***

¡Listo! Tu canal de Email quedó conectado. El siguiente paso es crear plantillas y enviar tus campañas.
