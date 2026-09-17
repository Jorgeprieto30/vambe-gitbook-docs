# Crea Flows de WhatsApp para capturar información estructurada de tus clientes

{% hint style="info" %}
¿No tienes claro si un Flow es lo que necesitas? Revisa primero **Reduce mensajes con WhatsApp Flows** para ver cuándo conviene usarlo.
{% endhint %}

***

### Requisitos de compatibilidad

Los WhatsApp Flows no funcionan con cualquier conexión. Requieren un número conectado mediante la plataforma oficial de WhatsApp Business de Meta.

| Tipo de conexión                        | ¿Compatible con Flows?                                                                                                          |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| WhatsApp API oficial                    | Sí                                                                                                                              |
| WhatsApp Dual o híbrido                 | Puede serlo, si el número está respaldado por la conexión oficial de Meta y aparece en Vambe como un número WhatsApp habilitado |
| WhatsApp QR / Web WhatsApp              | No                                                                                                                              |
| Instagram, Messenger, Web Chat o TikTok | No usan WhatsApp Flows                                                                                                          |

***

### Dónde se administran

Los Flows se crean y administran desde **Canales → WhatsApp Flows**. Ahí verás dos pestañas —**Flows** y **Plantillas asociadas**—, el listado de tus flujos existentes ("Tus Flujos") y el botón **+ Crear** para empezar uno nuevo.

<figure><img src="../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Crear el Flow no significa que se enviará automáticamente a los clientes. Una vez publicado, debe abrirse mediante un mensaje interactivo del asistente, una plantilla de WhatsApp o una automatización —ver **Mensajes Interactivos: botones, enlaces y Flows en un mismo asistente**.
{% endhint %}

***

### El editor de creación

Al hacer clic en **+ Crear** se abre el editor **Crear flujo de WhatsApp**, dividido en un panel de configuración a la izquierda y una vista previa en vivo dentro de un teléfono a la derecha.

<figure><img src="../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

**Sección Principal**

* **Nombre del flujo** — el nombre interno con el que identificarás este Flow (por ejemplo, «Encuesta satisfacción»).
* **Categorías** — se agregan con **Agregar categoría**.
* **Números de WhatsApp** — se agregan con **Agregar número**; define en qué número(s) va a estar disponible este Flow.

**Sección Pantallas**

Cada pantalla ("Pantalla 1", "Pantalla 2"...) tiene:

* **Título** — lo que ve el cliente como encabezado de la pantalla.
* **ID de pantalla** — un identificador interno en mayúsculas (por ejemplo, `START`, `CONFIRM`) que se usa para enrutar entre pantallas.
* **Pantalla terminal** — un interruptor que marca esa pantalla como el cierre del Flow. Al activarlo aparece un segundo interruptor, **Pantalla de éxito**, para marcarla específicamente como la confirmación final.

Dentro de **Construcción**, cada pantalla se arma agregando bloques con el botón **Agregar**:

| Bloque                  | Campos que configura                                                                                                                                                                                                                                                                                                              |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Encabezado de texto** | Texto                                                                                                                                                                                                                                                                                                                             |
| **Cuerpo de texto**     | Texto                                                                                                                                                                                                                                                                                                                             |
| **Entrada de texto**    | Interruptor **Requerido**, **Etiqueta** (lo que ve el cliente), **Tipo de entrada** (Texto, Email, teléfono, número, etc.), **Texto de ayuda** opcional. El **nombre del campo** se genera automáticamente a partir de la etiqueta (por ejemplo, "Full name" → `full_name`) —es el identificador con el que llega el dato a Vambe |
| **Lista desplegable**   | Interruptor **Requerido**, **Etiqueta**, pares **Valor** (no visible para el usuario) / **Opción** (visible para el usuario), que se van sumando con **Agregar elemento**                                                                                                                                                         |
| **Pie de página**       | **Tipo de pie de página** (por ejemplo, Simple), **Etiqueta** del botón, y **Pantalla de destino** —a qué pantalla salta el cliente al tocar ese botón                                                                                                                                                                            |

Al terminar una pantalla, **Agregar pantalla** (al pie del editor) suma la siguiente. El botón **Crear**, arriba a la derecha, publica el Flow.

{% hint style="info" %}
El **pie de página** de cada pantalla es lo que define el flujo de navegación: su campo **Pantalla de destino** apunta al **ID de pantalla** que sigue. Así armas Flows de varias pantallas sin lógica adicional.
{% endhint %}

***

### Límites de estructura

| Límite                            | Valor                |
| --------------------------------- | -------------------- |
| Pantallas por Flow                | Máximo 8             |
| Campos de entrada por pantalla    | Máximo 5             |
| Botones por pantalla              | 1 (el pie de página) |
| Opciones en un campo de selección | Entre 2 y 20         |

Para cargas de archivos (foto o documento), Meta impone además: máximo un campo de foto o documento por pantalla, hasta 30 archivos en los campos de carga, ≈ 25 MB por archivo, y un límite total de ≈ 100 MB por Flow.

**Tipos de campo disponibles:** texto, texto largo, correo, teléfono, número, selección única, lista desplegable, selección múltiple, fecha, aceptación de términos, fotos y documentos.

***

### Buenas prácticas

1. **Un Flow por objetivo.** Mejor tener un Flow de agendamiento, otro de cotización y otro de devolución, que uno gigante para todo.
2. **Pide solo lo necesario.** Cada campo adicional aumenta la posibilidad de abandono; no preguntes algo que el asistente pueda obtener después o que ya tenga disponible.
3. **Separa por etapas.** Por ejemplo: pantalla 1 datos de contacto, pantalla 2 necesidad o servicio, pantalla 3 fecha o detalle adicional, pantalla 4 confirmación. Con seis o más campos, agrúpalos en pantallas de tres a cinco.
4. **Incluye una pantalla final de confirmación**, para que el cliente pueda revisar lo que está enviando antes de terminar.
5. **Usa nombres claros** en las etiquetas ("¿Qué servicio necesitas?", no "Campo 1" o "Dato adicional").
6. **Mantén las opciones cortas** —fáciles de seleccionar desde un teléfono. Si hay muchas alternativas, agrúpalas o sepáralas en otra pantalla.
7. **Define qué pasará después**: crear o actualizar un ticket, mover de etapa, avisar a un ejecutivo, enviar una cotización, activar un workflow, agendar una reunión.
8. **Ten siempre una alternativa conversacional.** No todos los clientes completarán el formulario; el asistente debe poder continuar manualmente si la persona dice «prefiero hablar con alguien», no entiende una pregunta o no puede abrir el Flow.

***

### Publicación

{% hint style="danger" %}
Un Flow publicado **no se puede devolver a estado borrador**. Revisa bien nombres, campos y navegación entre pantallas antes de crear el Flow definitivo, y pruébalo con casos reales antes de usarlo ampliamente.
{% endhint %}

Si vas a enviar el Flow mediante una plantilla de WhatsApp, esa plantilla debe cumplir también con las reglas y aprobaciones de Meta.

***

### Casos avanzados

Algunos escenarios —lógica condicional compleja entre pantallas, o conectar el Flow a un sistema externo para traer datos dinámicos— pueden requerir configuración adicional más allá de este editor. Si tu caso lo necesita, conviérsalo con tu equipo de implementación de Vambe.

***

### En resumen

Un Flow se arma con pantallas, y cada pantalla con bloques —encabezado, cuerpo, campos de entrada y un pie de página que decide a dónde salta el cliente—, todo visible en tiempo real en la vista previa del teléfono. Una vez creado, no se envía solo: falta indicarle al asistente cuándo debe abrirlo. Eso se configura en **Mensajes Interactivos: botones, enlaces y Flows en un mismo asistente**.
