# Cómo crear una automatización para clientes problemáticos en Vambe

Gestionar clientes insatisfechos o de alta complejidad puede ser un desafío que consume tiempo y recursos. En Vambe, puedes automatizar la identificación y atención de estos casos, asegurando una respuesta rápida y coordinada para desescalar situaciones y proteger la reputación de tu marca.

Este artículo te guiará para configurar un Workflow que identifica, alerta y ofrece soluciones proactivas a clientes clasificados como 'problemáticos'.

## Beneficios de automatizar la gestión de clientes problemáticos

*   **Respuesta inmediata:** Atiende situaciones delicadas antes de que escalen.
*   **Asignación inteligente:** Dirige estos casos directamente al equipo o agente más capacitado.
*   **Consistencia:** Asegura que todos los clientes problemáticos reciban un protocolo de atención estandarizado.
*   **Registro centralizado:** Mantén un historial claro para análisis y mejora de procesos.

## Estrategias para identificar un cliente problemático en Vambe

Antes de automatizar, es crucial definir qué hace a un cliente "problemático". Puedes usar:

1.  **Etiquetado manual:** Los agentes aplican una etiqueta como "Problemático" o "Reclamación" a los contactos.
2.  **Puntuación negativa (Lead Score):** Si un contacto alcanza un Lead Score muy bajo debido a interacciones negativas.
3.  **Encuestas (NPS/CSAT):** Un NPS bajo o CSAT negativo puede disparar la identificación.
4.  **Palabras clave en mensajes:** Aunque más avanzado, se puede usar la IA para detectar sentimientos negativos o palabras específicas.
5.  **Historial de interacciones:** Un alto volumen de tickets abiertos en poco tiempo.

## Configura tu Workflow para clientes problemáticos

A continuación, se detalla un ejemplo de cómo configurar un Workflow para gestionar automáticamente a los clientes etiquetados como "Problemáticos".

### Paso 1: Definir el Trigger (Gatillante)

El evento que inicia la automatización. Para este caso, la forma más sencilla es usar la asignación de una etiqueta.

*   **Trigger:** **Etiqueta asignada**
*   **Configuración:** Selecciona la etiqueta que usarás para identificar a estos clientes (ej: "Cliente Problemático", "Reclamación Urgente").

<figure><img src=".gitbook/assets/image-placeholder-trigger.png" alt="Configuración de trigger de etiqueta asignada"></figure>

### Paso 2: (Opcional) Agrega Condiciones (Filtros)

Puedes refinar cuándo se ejecuta el Workflow. Por ejemplo, si quieres que la automatización solo se active para ciertos canales o si el ticket está en una etapa específica.

*   **Condición:** **Condición de Canal**
*   **Configuración:** Si el canal es "WhatsApp" o "Instagram", puedes adaptar el mensaje o el flujo.
*   **Condición:** **Condición de Metadatos**
*   **Configuración:** Para clientes con un histórico de compras elevado (clientes VIP problemáticos) o cualquier otro dato relevante.

<figure><img src=".gitbook/assets/image-placeholder-condition.png" alt="Configuración de condición en Workflow"></figure>

### Paso 3: Definir las Acciones

Aquí es donde Vambe interviene para gestionar el caso. Puedes encadenar varias acciones para una respuesta integral.

1.  **Asignar ejecutivo:**
    *   **Acción:** **Asignar ejecutivo**
    *   **Configuración:** Selecciona al equipo o agente especializado en resolver conflictos (ej: "Soporte Senior", "Gerencia de Experiencia"). Esto asegura que el caso sea atendido por el personal adecuado de inmediato.

2.  **Crear nota interna:**
    *   **Acción:** **Crear nota**
    *   **Configuración:** _"Cliente identificado como 'Problemático'. Revisar historial y priorizar contacto. Objetivo: desescalar y ofrecer solución proactiva."_
    *   Esta nota es visible solo para los agentes y sirve como una alerta interna y guía para la acción.

3.  **Enviar mensaje con IA (Respuesta proactiva):**
    *   **Acción:** **Enviar mensaje con IA**
    *   **Configuración:** Define un prompt que genere un mensaje de disculpa, empatía y propuesta de solución.
        *   _Prompt de ejemplo:_ "Genera un mensaje empático para un cliente insatisfecho que acaba de ser etiquetado como 'Problemático'. Ofrece una disculpa sincera, reconoce su frustración y dile que nuestro equipo especializado ya está revisando su caso para ofrecerle una solución personalizada a la brevedad."
    *   Este mensaje puede desescalar la situación mientras el agente especializado se prepara para intervenir.

4.  **Agregar a una hoja de cálculo para seguimiento:**
    *   **Acción:** **Agregar fila a Google Sheet**
    *   **Configuración:** Conecta a tu hoja de cálculo de Google Drive y mapea los datos del cliente (nombre, ID de ticket, fecha, agente asignado, descripción del problema) para un registro exhaustivo y análisis posterior.

5.  **(Opcional) Notificación externa:**
    *   **Acción:** **Enviar webhook**
    *   **Configuración:** Envía una señal a tu CRM o sistema de gestión de proyectos para crear una alerta o tarea de seguimiento en otras plataformas.

<figure><img src=".gitbook/assets/image-placeholder-actions.png" alt="Configuración de acciones en Workflow"></figure>

## Ejemplo de flujo completo

**Escenario:** Un cliente interactúa de forma negativa y un agente lo etiqueta manualmente como "Problemático".

*   **Trigger:** **Etiqueta asignada** (Etiqueta: "Problemático")
*   **Acción 1:** **Asignar ejecutivo** (al equipo "Soporte VIP")
*   **Acción 2:** **Crear nota** ("Alerta: Cliente 'Problemático' asignado a Soporte VIP para resolución.")
*   **Acción 3:** **Enviar mensaje con IA** (Desescalada inicial y aviso de atención especializada)
*   **Acción 4:** **Agregar fila a Google Sheet** (Registro para monitoreo y reportes)

## Consejos adicionales

*   **Monitorea los resultados:** Revisa regularmente la efectividad de tu Workflow y los tiempos de resolución para clientes problemáticos.
*   **Capacita a tus agentes:** Asegúrate de que los agentes sepan cuándo y cómo etiquetar correctamente a un cliente para activar estas automatizaciones.
*   **Itera y mejora:** Ajusta tu flujo de trabajo basándote en el feedback y los resultados para optimizar la experiencia del cliente y la eficiencia operativa.

Con esta automatización, transformas un desafío potencial en una oportunidad para demostrar la capacidad de respuesta y el compromiso de tu marca con la satisfacción del cliente en Vambe.
