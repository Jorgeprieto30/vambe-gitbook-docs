---
description: >-
  Aprende a configurar un Workflow en Vambe que se active automáticamente cuando
  un contacto cambia de etapa en HubSpot, Pipedrive o Salesforce, simplificando
  tu automatización CRM.
---

# Cómo Configurar un Trigger de Workflow por Cambio de Etapa de CRM

El nuevo trigger de Workflow por Cambio de Etapa de CRM permite a Vambe **reaccionar automáticamente** a movimientos importantes en tu sistema CRM. Con este trigger, puedes iniciar Workflows en Vambe tan pronto como un contacto cambia de etapa en **HubSpot, Pipedrive o Salesforce**, sin la necesidad de crear complejas automatizaciones en tu CRM.

Este feature está diseñado para simplificar tu estrategia de automatización, especialmente útil si buscas:
*   **Agilizar la comunicación:** Envía mensajes, notificaciones o asigna tareas en Vambe al instante que un prospecto avanza en tu embudo de ventas CRM.
*   **Reducir costos de licenciamiento:** Permite a usuarios de planes básicos de CRM (como HubSpot Starter) automatizar acciones que antes requerían planes más avanzados y costosos en el propio CRM.
*   **Centralizar la gestión:** Mantén la coherencia entre tu CRM y Vambe, asegurando que las acciones se ejecuten en el momento preciso.

## ¿Cómo funciona el trigger "Cambio de Etapa CRM"?

Una vez configurada la integración con tu CRM, Vambe escucha los cambios de etapa para los contactos. Cuando se detecta un cambio de etapa relevante (según tu configuración), se dispara un Workflow en Vambe.

## Paso a paso: Configurar el Trigger de Workflow

Sigue estos pasos para configurar tu workflow que reacciona a cambios en tu CRM:

### 1. Crea un nuevo Workflow

1.  En el menú lateral izquierdo de Vambe, selecciona **Workflows**.
2.  Haz clic en **Crear Flow**.
3.  Asigna un nombre descriptivo a tu Workflow, por ejemplo: "Bienvenida tras cierre de venta CRM".

### 2. Selecciona el Trigger "Cambio de Etapa CRM"

1.  En la sección "Trigger (Gatillante)", busca y selecciona **"Cambio de Etapa CRM"**.
2.  Haz clic en el nodo para configurarlo.

<figure><img src="../.gitbook/assets/workflow-crm-trigger-1.png" alt="Selector de trigger Cambio de Etapa CRM en Vambe"><figcaption>Selecciona 'Cambio de Etapa CRM' como tu gatillante.</figcaption></figure>

### 3. Configura las Opciones del Trigger

Una vez seleccionado el trigger, verás las siguientes opciones de configuración:

*   **Integración de CRM:** Selecciona la integración CRM específica que deseas monitorear (ej. HubSpot, Pipedrive, Salesforce).
*   **Pipeline de CRM:** Elige el pipeline (embudo de ventas) dentro de tu CRM al que se aplica el cambio.
*   **Etapa de CRM:** Define la etapa específica del CRM que, al ser alcanzada por un contacto, activará este workflow en Vambe.
*   **Buscar contactos en Vambe:** Aquí tienes dos opciones cruciales:
    *   **Buscar solo contactos existentes en Vambe:** El workflow se activará únicamente si el contacto que cambia de etapa en el CRM ya tiene un registro en Vambe.
    *   **Buscar o crear el contacto si no existe:** Si el contacto no está registrado en Vambe, se creará automáticamente un nuevo contacto en Vambe antes de ejecutar el workflow. Esto asegura que todas las automatizaciones puedan proceder incluso con contactos nuevos en tu CRM.

<figure><img src="../.gitbook/assets/workflow-crm-trigger-2.png" alt="Configuración del trigger Cambio de Etapa CRM con opciones de búsqueda"><figcaption>Configura la integración, pipeline, etapa y cómo Vambe debe manejar los contactos.</figcaption></figure>

### 4. Añade Condiciones y Acciones

Una vez configurado el trigger, puedes añadir **Condiciones** (filtros) y **Acciones** para definir qué sucede después de que el contacto cambia de etapa en tu CRM.

**Ejemplo de Workflow:**

*   **Trigger:** Cuando un contacto entra a la etapa "Cotización Aprobada" en HubSpot.
*   **Condición (opcional):** Si el monto del trato es mayor a $500.000.
*   **Acción 1:** Enviar plantilla de WhatsApp al contacto: "¡Felicidades por su compra! Un ejecutivo se contactará en breve para los próximos pasos."
*   **Acción 2:** Cambiar etapa en Vambe a "Cliente Activo".
*   **Acción 3:** Asignar una etiqueta "Cliente VIP" en Vambe.
*   **Acción 4:** Crear una tarea interna para el equipo de Onboarding en Vambe.

## Consideraciones importantes

*   **Permisos del CRM:** Asegúrate de que la integración de Vambe con tu CRM tenga los permisos necesarios para leer los cambios de etapa.
*   **Consistencia de datos:** Para el mapeo y la identificación de contactos, es recomendable que los campos clave (como el correo electrónico) sean consistentes entre Vambe y tu CRM.
*   **Pruebas:** Utiliza el [Modo Test de Workflows](../workflows/README.md#7-modo-test) para simular cambios de etapa y verificar que tu automatización funciona como esperas antes de activarla en producción.

Con este trigger, Vambe te ofrece un control sin precedentes sobre la automatización de tus procesos, permitiéndote reaccionar de forma proactiva a la evolución de tus clientes en el embudo de ventas.
