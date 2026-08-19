---
description: >-
  Centraliza tu gestión. Aprende a conectar HubSpot, Pipedrive, Salesforce y
  otros CRMs para sincronizar contactos, tratos y automatizar el envío de leads
  desde Vambe.
---

# Cómo conectar y configurar tu CRM

Vambe permite integrarse nativamente con los CRMs más importantes del mercado para mantener tu base de datos y tu equipo de ventas alineados.

**Integraciones disponibles:**

* HubSpot (Deals y Tickets)
* Pipedrive
* Salesforce
* Zoho (CRM y Desk)
* ActiveCampaign
* Odoo CRM

A continuación, te explicamos paso a paso cómo realizar la conexión y la configuración avanzada de sincronización.

{% hint style="info" %}
Si tienes dudas que puedo conectar con mi CRM, puedes revisarlo aquí
{% endhint %}

***

#### 1. Conexión Inicial

1. En el menú lateral izquierdo, ve a la sección **CRM**.
2. Despliega el menú de **Ajustes** y selecciona **Integraciones**.
3. Verás el listado de CRMs disponibles. Haz clic en Conectar en la tarjeta de tu CRM (ej: Pipedrive, HubSpot, etc.).

{% hint style="info" %}
¿Vas a conectar **Odoo CRM**? A diferencia de otros CRMs, Odoo requiere que generes una Llave de API manualmente antes de este paso. Revisa primero [cómo obtener las credenciales de Odoo CRM](como-obtener-las-credenciales-de-odoo-crm.md).
{% endhint %}

4. Sigue los pasos de autenticación de tu plataforma externa.
5. Una vez conectado, volverás a Vambe. Si no ves la integración activa inmediatamente, **actualiza la página.**
6. Haz clic en el icono de Lápiz (Editar) para entrar al panel de configuración.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FMa2WOFQGyb9aHllO5vDX%2Fimage.png?alt=media&#x26;token=0b5c9518-690d-47d0-9ba9-d7cf2a2e2efc" alt=""><figcaption></figcaption></figure>

***

#### 2. Sincronización General

En la primera pestaña **Sincronizar**, encontrarás tres opciones clave que permiten a Vambe "leer" la estructura de tu CRM:

* **Sincronizar Campos**: Detecta automáticamente los campos personalizados de tu CRM para que puedas usarlos en Vambe.
* **Sincronizar Agentes**: Importa los usuarios de tu CRM para asignar dueños a los contactos.
* **Sincronizar Etiquetas**: Trae las etiquetas existentes en tu CRM.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FJKpqXHiNc3Mb8SQU7hkz%2Fimage.png?alt=media&#x26;token=1c7dabc5-1eb2-4b10-8358-f8dc386dbefd" alt=""><figcaption></figcaption></figure>

***

#### 3. Atributos de Contacto (Reglas de Envío)

Esta sección es crítica. Aquí defines los **requisitos mínimos** para que un contacto se envíe al CRM.

* **¿Cómo funciona?** Seleccionas un embudo y defines qué campos son obligatorios (ej: RUT, Email).
* **La Regla:** Si el contacto **NO tiene este dato** (ni la IA ni el humano lo rellenaron), Vambe **NO enviará** el contacto al CRM para evitar ensuciar tu base de datos con leads vacíos.

1. Activa el interruptor del embudo que deseas configurar.
2. Haz clic en el botón **(+)** y selecciona el campo obligatorio (ej: Email).

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FGbQcXq5SJDeAcx5zkt9M%2Fimage.png?alt=media&#x26;token=cc7a00ad-e981-481c-8e3e-ca97ce309057" alt="" width="563"><figcaption></figcaption></figure>

***

#### 4. Configuración de Contacto

Aquí definimos cómo busca, importa y actualiza Vambe la información.

**A. Configuración de Búsqueda**

Define el criterio único para evitar duplicados. Vambe buscará en tu CRM si el contacto ya existe usando estos campos (ej: Email o Teléfono). Si lo encuentra, lo actualiza; si no, lo crea.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FFzy2JSzvHOiqVTIeR4c7%2Fimage.png?alt=media&#x26;token=ce72b940-3a38-4208-b174-84639f54d91c" alt="" width="563"><figcaption></figcaption></figure>

**B. Configuración de Importación**

Define qué datos debe traer **Vambe desde el CRM hacia adentro**. Puedes activar:

* Sincronizar asignación de agentes.
* Sincronizar etiquetas.
* Sincronizar campos de contacto.
* Sincronizar Último Negocio: Importante para traer el contexto de ventas anteriores.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FfONGSvtV3AFtttKYbo5u%2Fimage.png?alt=media&#x26;token=5e7ad941-48aa-4e88-87b5-57516096516d" alt=""><figcaption></figcaption></figure>

**C. Webhooks (Bidireccionalidad)**

Activa esta opción para que, cuando algo cambie en tu CRM (ej: cambias una etapa en Pipedrive), se actualice automáticamente en Vambe en tiempo real.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FzZa1xwC8zUoLvaICA0wJ%2Fimage.png?alt=media&#x26;token=b2b4ee12-67fd-4756-ae8b-77f28d224ad8" alt=""><figcaption></figcaption></figure>

***

#### 5. Mapeo de Campos

Es momento de conectar los cables. Debes decir qué campo de Vambe corresponde a qué campo de tu CRM.

* **Campos de Contacto:** Asocia datos personales (Nombre, Rut, Email).

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2Fgi5xHrI6UBNOllJIjvR8%2Fimage.png?alt=media&#x26;token=d4935004-df4a-4e95-bd4d-07f722d631f3" alt=""><figcaption></figcaption></figure>

* **Atributos del Deal (Trato/Ticket):** Asocia datos de la venta (Monto, Producto de interés, Dirección de despacho). Esto es vital para que el negocio se cree con información valiosa en tu CRM.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2F66FS8JoXwJVAyNvPye1T%2Fimage.png?alt=media&#x26;token=e5c2dbe4-e2f9-41e7-bf56-3658e7889afe" alt=""><figcaption></figcaption></figure>

***

#### 6. UTMs (Rastreo de Marketing)

Si realizas publicidad digital, puedes mapear los parámetros UTM (Source, Medium, Campaign) para que se envíen al CRM y puedas medir el ROI de tus campañas. Selecciona el valor UTM (ej: `utm_source`) y asócialo al campo correspondiente en tu CRM.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FR6Dv7YjDtLZcT9TBeeSd%2Fimage.png?alt=media&#x26;token=e2e2fa5e-5861-4755-bb55-1fe4c0522890" alt=""><figcaption></figcaption></figure>

***

#### 7. Etapas (El disparador)

Esta es la configuración más importante para la automatización. Aquí decides **cuándo y dónde** se envía el lead.

Debes configurar la siguiente lógica:

1. **Etapa Vambe**: Selecciona la etapa de tu embudo en Vambe que servirá de "gatillo" (ej: Cuando entre a "Cotización Enviada").
2. **Pipeline CRM**: Selecciona a qué embudo de tu CRM irá.
3. **Etapa CRM**: Selecciona en qué etapa exacta caerá en tu CRM.
4. **Crear Trato (Switch):**
   * **Activado**: Crea el Contacto + el Negocio (Deal/Oportunidad).
   * **Desactivado**: Solo crea o actualiza el Contacto (sin crear oportunidad de venta).

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2F8VyZcnqKugkufRw3imtt%2Fimage.png?alt=media&#x26;token=60b74a80-c72d-4c43-9915-4e40b211ed71" alt=""><figcaption></figcaption></figure>

***

#### 8. Automatización Inversa: Trigger de Workflow por Cambio de Etapa CRM

Además de enviar información desde Vambe a tu CRM, ahora puedes configurar **Workflows en Vambe** que se activen automáticamente cuando un contacto **cambia de etapa directamente en tu CRM**. Esta funcionalidad simplifica significativamente la automatización y te permite reaccionar a eventos clave sin la necesidad de complejos flujos en tu sistema CRM.

**Beneficios clave:**

* **Automatización Directa:** Ejecuta acciones en Vambe (ej. enviar mensajes, asignar ejecutivos) tan pronto como una etapa cambia en HubSpot, Pipedrive o Salesforce.
* **Optimización de Costos:** Permite a usuarios de planes básicos de CRM (como HubSpot Starter) automatizar acciones que antes requerían planes más avanzados y costosos.
* **Flexibilidad:** El trigger ofrece dos opciones para gestionar los contactos:
  * **Buscar solo contactos existentes en Vambe:** Activa el workflow solo si el contacto ya está registrado en Vambe.
  * **Buscar o crear el contacto si no existe:** Si el contacto no está en Vambe, se creará automáticamente para poder ejecutar el workflow.

Para configurar este trigger, dirígete a la sección de Workflows en Vambe y selecciona la opción **"Cambio de Etapa CRM"** como gatillante.

***

#### 9. Ajustes Finales

En la pestaña Ajustes, podrás ver el estado de la sincronización o **Eliminar** la integración si necesitas desconectar el CRM.

{% hint style="danger" %}
⚠️ **Advertencia**: Si eliminas el CRM, se perderá la configuración de mapeo realizada.
{% endhint %}
