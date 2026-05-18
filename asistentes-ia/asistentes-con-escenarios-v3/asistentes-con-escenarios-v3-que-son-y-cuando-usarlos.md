# Asistentes con Escenarios (V3): ¿Qué son y cuándo usarlos?

Vambe ahora ofrece dos tipos de asistentes. Antes de crear uno, es importante entender cuál se adapta mejor a lo que necesita.

***

### Los dos tipos de asistentes

Al hacer clic en **Crear asistente**, verá dos opciones:

<figure><img src="../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

|                                      | Asistente con Bloques (V2)                         | Asistente con Escenarios (V3)                                                                                                                              |
| ------------------------------------ | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **¿Cómo funciona?**                  | Sigue un flujo rígido definido por pasos y bloques | La IA descubre el camino óptimo según el contexto de cada conversación                                                                                     |
| **Límite de contexto**               | Sí                                                 | No                                                                                                                                                         |
| **Reutilizable en múltiples etapas** | Parcial                                            | Sí                                                                                                                                                         |
| **Bloques disponibles**              | Todos (incluyendo Pasos a seguir y Casos posibles) | Solo identidad: Personificación, Objetivo, No Hacer, Etiquetas, Formato de Respuesta, Productos, Agendamiento                                              |
| **Flujo de conversación**            | Definido por Pasos a seguir y Casos posibles       | Definido por Escenarios y Rutas                                                                                                                            |
| **Integraciones externas**           | No                                                 | **Sí (Slack, Notion, Linear y más, para ejecutar acciones directamente desde la conversación)**                                                            |
| **Ideal para**                       | Flujos lineales y predecibles                      | Conversaciones complejas, naturales y multi-propósito, y para automatizar tareas en herramientas externas.                                               |

> 💡 Ambas versiones coexisten. No es necesario migrar los asistentes V2 existentes. Puede seguir usándolos y crear asistentes V3 para nuevos casos de uso.

***

### ¿Cuándo usar cada uno?

**Use Asistente con Bloques (V2) si:**

*   Su flujo es simple y lineal (ej: calificar un lead con 3 preguntas fijas).
*   Ya tiene asistentes configurados y funcionando bien.
*   No necesita que el asistente navegue entre múltiples temas.

**Use Asistente con Escenarios (V3) si:**

*   Su asistente necesita manejar múltiples situaciones en una misma conversación (ventas + soporte + agendamiento).
*   Quiere reutilizar el mismo asistente en varias etapas del embudo.
*   Busca conversaciones más naturales donde la IA decida el camino según el contexto.
*   Tiene flujos complejos que antes requerían varios asistentes encadenados.
*   **Necesita que la IA ejecute acciones en herramientas externas (Slack, Notion, Linear, etc.) directamente desde la conversación, como enviar mensajes o crear tickets.**
*   Requiere un control adicional sobre las respuestas mediante el **Juez personalizado**, accesible directamente desde la interfaz del asistente con escenarios.

***

### Cómo crear un Asistente con Escenarios

1.  Vaya al menú lateral → **Asistentes** → haga clic en **+ Crear**.
2.  Seleccione **Asistente con escenarios**.
3.  Asigne un nombre y seleccione el modelo de IA.
4.  Haga clic en **Crear asistente**.

Al entrar al asistente recién creado, verá el panel de **Resumen** con varias pestañas principales:

*   **Escenarios:** Aquí define el comportamiento y los flujos de conversación.
*   **Bloques:** Configura la personalidad base (identidad) del asistente.
*   **Funciones:** Las acciones que el asistente puede ejecutar (cambio de etapa, enviar plantilla, integraciones externas, etc.).
*   **Juez:** Configure aquí el Juez personalizado para establecer políticas de revisión y corrección de respuestas de la IA.
*   **Base de conocimiento, Retroalimentación, Probar asistente:** Configuraciones secundarias.
