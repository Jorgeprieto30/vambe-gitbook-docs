# Asistentes con Escenarios (V3): ¿Qué son y cuándo usarlos?

Vambe ahora ofrece dos tipos de asistentes. Antes de crear uno, es importante entender cuál se adapta mejor a lo que necesitas.

***

### Los dos tipos de asistentes

Al hacer clic en **Crear asistente**, verás dos opciones:

<figure><img src="../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

|                                      | Asistente con Bloques (V2)                         | Asistente con Escenarios (V3)                                                                                 |
| ------------------------------------ | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **¿Cómo funciona?**                  | Sigue un flujo rígido definido por pasos y bloques | La IA descubre el camino óptimo según el contexto de cada conversación                                        |
| **Límite de contexto**               | Sí                                                 | No                                                                                                            |
| **Reutilizable en múltiples etapas** | Parcial                                            | Sí                                                                                                            |
| **Bloques disponibles**              | Todos (incluyendo Pasos a seguir y Casos posibles) | Solo identidad: Personificación, Objetivo, No Hacer, Etiquetas, Formato de Respuesta, Productos, Agendamiento |
| **Flujo de conversación**            | Definido por Pasos a seguir y Casos posibles       | Definido por Escenarios y Rutas                                                                               |
| **Ideal para**                       | Flujos lineales y predecibles                      | Conversaciones complejas, naturales y multi-propósito                                                         |

> 💡 Ambas versiones coexisten. No es necesario migrar los asistentes V2 existentes. Puedes seguir usándolos y crear asistentes V3 para nuevos casos de uso.

***

### ¿Cuándo usar cada uno?

**Usa Asistente con Bloques (V2) si:**

* Tu flujo es simple y lineal (ej: calificar un lead con 3 preguntas fijas).
* Ya tienes asistentes configurados y funcionando bien.
* No necesitas que el asistente navegue entre múltiples temas.

**Usa Asistente con Escenarios (V3) si:**

* Tu asistente necesita manejar múltiples situaciones en una misma conversación (ventas + soporte + agendamiento).
* Quieres reutilizar el mismo asistente en varias etapas del embudo.
* Buscas conversaciones más naturales donde la IA decida el camino según el contexto.
* Tienes flujos complejos que antes requerían varios asistentes encadenados.

***

### Cómo crear un Asistente con Escenarios

1. Ve al menú lateral → **Asistente** → haz clic en **+ Crear**.
2. Selecciona **Asistente con escenarios**.
3. Asigna un nombre y selecciona el modelo de IA.
4. Haz clic en **Crear asistente**.

Al entrar al asistente recién creado, verás el panel de **Resumen** con cuatro pestañas principales:

* **Escenarios:** Aquí defines el comportamiento y los flujos de conversación.
* **Bloques:** Configura la personalidad base (identidad) del asistente.
* **Funciones:** Las acciones que el asistente puede ejecutar (cambio de etapa, enviar plantilla, etc.).
* **Base de conocimiento, Retroalimentación, Probar asistente:** Configuraciones secundarias.
