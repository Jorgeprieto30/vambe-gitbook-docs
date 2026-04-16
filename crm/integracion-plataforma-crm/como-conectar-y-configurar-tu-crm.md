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
Si tienes dudas que puedo conectar con mi CRM, puedes [revisarlo aquí](integracion-de-vambe-con-crms-que-es-posible-que-se-sincroniza-y-que-debes-considerar.md)
{% endhint %}

***

#### 1. Conexión Inicial

1. En el menú lateral izquierdo, ve a la sección **CRM**.
2. Despliega el menú de **Ajustes** y selecciona **Integraciones**.
3. Verás el listado de CRMs disponibles. Haz clic en Conectar en la tarjeta de tu CRM (ej: Pipedrive, HubSpot, etc.).
4. Sigue los pasos de autenticación de tu plataforma externa.
5. Una vez conectado, volverás a Vambe. Si no ves la integración activa inmediatamente, **actualiza la página.**
6. Haz clic en el icono de Lápiz (Editar) para entrar al panel de configuración.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

***

#### 2. Sincronización General

En la primera pestaña **Sincronizar**, encontrarás tres opciones clave que permiten a Vambe "leer" la estructura de tu CRM:

* **Sincronizar Campos**: Detecta automáticamente los campos personalizados de tu CRM para que puedas usarlos en Vambe.
* **Sincronizar Agentes**: Importa los usuarios de tu CRM para asignar dueños a los contactos.
* **Sincronizar Etiquetas**: Trae las etiquetas existentes en tu CRM.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

***

#### 3. Atributos de Contacto (Reglas de Envío)

Esta sección es crítica. Aquí defines los **requisitos mínimos** para que un contacto se envíe al CRM.

* **¿Cómo funciona?** Seleccionas un embudo y defines qué campos son obligatorios (ej: RUT, Email).
* **La Regla:** Si el contacto **NO tiene este dato** (ni la IA ni el humano lo rellenaron), Vambe **NO enviará** el contacto al CRM para evitar ensuciar tu base de datos con leads vacíos.

1. Activa el interruptor del embudo que deseas configurar.
2. Haz clic en el botón **(+)** y selecciona el campo obligatorio (ej: Email).

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

***

#### 4. Configuración de Contacto

Aquí definimos cómo busca, importa y actualiza Vambe la información.

**A. Configuración de Búsqueda**

Define el criterio único para evitar duplicados. Vambe buscará en tu CRM si el contacto ya existe usando estos campos (ej: Email o Teléfono). Si lo encuentra, lo actualiza; si no, lo crea.

<figure><img src="../.gitbook/assets/image (6).png" alt="" width="563"><figcaption></figcaption></figure>

**B. Configuración de Importación**

Define qué datos debe traer **Vambe desde el CRM hacia adentro**. Puedes activar:

* Sincronizar asignación de agentes.
* Sincronizar etiquetas.
* Sincronizar campos de contacto.
* Sincronizar Último Negocio: Importante para traer el contexto de ventas anteriores.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

**C. Webhooks (Bidireccionalidad)**

Activa esta opción para que, cuando algo cambie en tu CRM (ej: cambias una etapa en Pipedrive), se actualice automáticamente en Vambe en tiempo real.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

***

#### 5. Mapeo de Campos

Es momento de conectar los cables. Debes decir qué campo de Vambe corresponde a qué campo de tu CRM.

* **Campos de Contacto:** Asocia datos personales (Nombre, Rut, Email).

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

* **Atributos del Deal (Trato/Ticket):** Asocia datos de la venta (Monto, Producto de interés, Dirección de despacho). Esto es vital para que el negocio se cree con información valiosa en tu CRM.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

***

#### 6. UTMs (Rastreo de Marketing)

Si realizas publicidad digital, puedes mapear los parámetros UTM (Source, Medium, Campaign) para que se envíen al CRM y puedas medir el ROI de tus campañas. Selecciona el valor UTM (ej: `utm_source`) y asócialo al campo correspondiente en tu CRM.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

***

#### 8. Ajustes Finales

En la pestaña Ajustes, podrás ver el estado de la sincronización o **Eliminar** la integración si necesitas desconectar el CRM.

{% hint style="danger" %}
⚠️ **Advertencia**: Si eliminas el CRM, se perderá la configuración de mapeo realizada.
{% endhint %}

