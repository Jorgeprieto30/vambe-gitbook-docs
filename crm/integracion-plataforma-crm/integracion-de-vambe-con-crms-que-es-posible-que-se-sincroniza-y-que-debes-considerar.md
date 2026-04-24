# Integración de Vambe con CRMs: qué es posible, qué se sincroniza y qué debes considerar

Antes de configurar una integración, es clave entender qué es un CRM, qué rol cumple dentro de tu operación, y qué puede (y qué no puede) hacer Vambe con cada uno.

Este artículo entrega el marco completo para que sepas exactamente qué esperar antes de avanzar a la configuración paso a paso.

## ¿Qué es un CRM?

Un **CRM (Customer Relationship Management)** es un sistema diseñado para centralizar y organizar **todas las interacciones de una empresa con sus clientes y prospectos**.

Su principal objetivo es convertirse en una **fuente única de verdad** (system of record), donde quedan registrados:

*   Quién es el cliente
*   Cuándo y por qué canales interactuó
*   Quién es el responsable comercial
*   Qué negocios (tratos/deals) existen
*   Qué tareas, actividades y estados tiene cada relación

Un CRM no es solo un embudo: es la **base histórica y operativa del negocio**.

## ¿Cómo se mueve un contacto dentro de un CRM?

La mayoría de los CRMs comparten un flujo evolutivo similar, conocido como Lifecycle:

{% stepper %}
{% step %}
### Lead

Es el primer registro. Existe información básica, pero aún no hay una intención de compra validada.
{% endstep %}

{% step %}
### Contacto (MQL – Marketing Qualified Lead)

El contacto muestra interés real: responde, pregunta, interactúa. Ya forma parte activa de la base.
{% endstep %}

{% step %}
### Deal / Trato / Oportunidad

Representa un negocio concreto.

Un mismo contacto puede tener **múltiples tratos** (por ejemplo: distintas compras, servicios o cuentas).

**Importante:** el contacto es permanente, los tratos son transaccionales.
{% endstep %}
{% endstepper %}

## ¿Qué rol cumple Vambe junto a un CRM?

Vambe **no reemplaza al CRM**, sino que lo **alimenta y se integra con él**.

Vambe se encarga de:

*   Gestionar conversaciones multicanal con IA
*   Calificar, enrutar y estructurar información
*   Crear y mover contactos, tratos y tickets
*   Enviar contexto limpio y estructurado al CRM

### Automatización Inteligente: Vambe reacciona a cambios en tu CRM

Más allá de enviar datos a tu CRM, Vambe ahora puede **reaccionar a los cambios que ocurren en él**. Con el nuevo trigger de Workflow por Cambio de Etapa CRM, puedes configurar Vambe para que inicie automatizaciones complejas (como enviar mensajes, cambiar etapas en Vambe o asignar agentes) de forma automática cuando un contacto avanza o se mueve entre etapas en HubSpot, Pipedrive o Salesforce.

Esto amplía las capacidades de automatización bidireccional, permitiéndote:
*   **Simplificar flujos:** No necesitas crear complejas automatizaciones en tu CRM solo para disparar acciones en Vambe.
*   **Optimizar costos:** Acceder a funcionalidades de automatización avanzadas en Vambe, incluso si utilizas planes básicos de tu CRM (ej. HubSpot Starter).

Para una configuración detallada, consulta la documentación sobre [Workflows en Vambe](../workflows/README.md).

El CRM recibe esa información y la usa para:

*   Reportes financieros
*   Automatizaciones comerciales
*   Gestión de equipos
*   Seguimiento histórico

## ¿Con qué CRMs se integra Vambe?

Actualmente, Vambe se integra con los siguientes CRMs:

*   Zoho
*   Odoo
*   HubSpot (Deals y Tickets)
*   Pipedrive
*   ActiveCampaign
*   Salesforce

Cada uno tiene **capacidades y limitaciones propias**, y por eso la integración **no es idéntica en todos los casos**.

## ¿Qué se puede sincronizar con cada CRM?

La siguiente tabla resume **qué objetos se pueden crear o sincronizar desde Vambe hacia cada CRM**:

| CRM                     | Leads | Contactos | Tratos / Deals |               Tags | Agentes |
| :---------------------- | ----: | --------: | -------------: | -----------------: | ------: |
| Zoho                    |     ❌ |         ✅ |              ✅ |                  ✅ |       ✅ |
| Odoo                    |  🟡\* |         ✅ |              ✅ |                  ✅ |       ✅ |
| HubSpot (Deals/Tickets) |     ❌ |         ✅ |              ✅ |                  ❌ |       ✅ |
| Pipedrive               |     ❌ |         ✅ |              ✅ | ✅ (solo en tratos) |       ✅ |
| ActiveCampaign          |     ❌ |         ✅ |              ✅ |                  ✅ |      🟡 |
| Salesforce              |  🟡\* |         ✅ |              ✅ |                  ✅ |       ✅ |

🟡 _En Odoo y Salesforce, el concepto de “Lead” se maneja como un Trato, no como un objeto independiente._

🟡 **ActiveCampaign** no maneja “agentes” como un objeto estándar; la asignación de responsables depende de usuarios, campos o automatizaciones. Por eso, la sincronización de agentes desde Vambe puede variar según la configuración de cada cuenta.

## Explicación por tipo de objeto

### Leads

*   Actualmente, Vambe **no trabaja con el objeto Lead puro** en la mayoría de los CRMs.
*   Esto es intencional: muchos CRMs manejan leads de forma inconsistente o directamente no los utilizan.
*   En Odoo y Salesforce, el lead se asimila a un trato, por eso aparecen como compatibilidad parcial.

👉 **Vambe trabaja principalmente con Contactos y Tratos.**

### Contactos

*   Vambe **crea y actualiza contactos en todos los CRMs**.
*   El contacto es **permanente**: una vez creado, se reutiliza en futuras conversaciones.
*   El correo electrónico suele ser la **llave primaria recomendada** para evitar duplicados.

### Tratos / Deals / Tickets

*   Vambe puede **crear tratos automáticamente** cuando un contacto entra a una etapa definida.
*   Los tratos se mueven según el avance del contacto en el embudo.
*   Un mismo contacto puede tener múltiples tratos a lo largo del tiempo.

### Tags

Existen diferencias importantes entre CRMs:

*   Algunos permiten tags en **contactos y tratos**.
*   Otros solo en **tratos**.
*   Otros **no soportan tags nativamente**.

Ejemplos:

*   Pipedrive → tags solo en tratos
*   HubSpot → no soporta tags como objeto nativo

👉 Si un CRM no soporta tags, Vambe **no puede forzar su creación**.

### Agentes

*   Vambe puede sincronizar agentes en todos los CRMs.
*   Para evitar errores de permisos, **se recomienda conectar el CRM con un usuario administrador u owner**.

## Consideraciones y limitaciones importantes

Antes de configurar tu integración, ten en cuenta:

*   No todos los CRMs soportan los mismos tipos de campos.
*   Campos tipo selector pueden fallar si los valores no coinciden exactamente.
*   Los tokens de conexión pueden expirar y requerir reconexión.
*   Automatizaciones existentes en el CRM pueden activarse al recibir datos desde Vambe.
*   **Workflows en Vambe:** Al configurar el trigger "Cambio de Etapa CRM", considera que los workflows en Vambe se activarán en función de los cambios en tu CRM. Revisa la lógica de tus automatizaciones en Vambe para asegurar el comportamiento deseado.

{% hint style="warning" %}
Siempre revisa las automatizaciones activas en tu CRM antes de mapear etapas o campos.
{% endhint %}

## Qué deberías tener claro antes de configurar

Antes de pasar a los artículos técnicos, deberías poder responder:

*   ¿Qué CRM uso y qué objetos necesito sincronizar?
*   ¿Qué campos son obligatorios en mi CRM?
*   ¿Qué etapas del embudo quiero reflejar en el CRM?
*   ¿Qué información debe quedar permanente (contacto) y cuál transaccional (trato)?
*   ¿Qué automatizaciones quiero disparar en Vambe cuando un contacto cambie de etapa en mi CRM?

Si tienes estas respuestas claras, la configuración será mucho más simple y estable.

## Próximos pasos

En los siguientes artículos aprenderás:

*   Cómo conectar cada CRM paso a paso
*   Cómo mapear etapas correctamente
*   Cómo evitar duplicados
*   Cómo sincronizar campos, agentes y etiquetas
*   Cómo usar el nuevo trigger de Workflow para que Vambe reaccione a cambios en tu CRM.

Este artículo es el **marco conceptual** para que todas esas configuraciones tengan sentido.
