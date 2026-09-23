# Crea Flows de WhatsApp para capturar información estructurada de tus clientes

Cuando necesitas pedirle datos a un cliente —su nombre, su correo, qué servicio busca— hacerlo con mensajes de texto sueltos funciona, pero es lento y da pie a errores de tipeo o respuestas incompletas. Los Flows de WhatsApp resuelven esto: son formularios nativos que se abren dentro del mismo chat, con campos, botones y pantallas que guian al cliente paso a paso. Puedes pedirle a **PandAI** que los arme por ti o crearlos a mano.

{% hint style="info" %}
**Para entrar:** en el menú lateral, ve a **Canales → WhatsApp Flows**.
{% endhint %}

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FF53xiBbfCbDurNV7Yvnj%2Fimage.png?alt=media&#x26;token=9860a816-fe22-49b4-9040-3ff2e29cb50c" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
¿No tienes claro si un Flow es lo que necesitas? Revisa primero [**Reduce mensajes con WhatsApp Flows**](https://academy.vambe.ai/canal/meta-empieza-a-cobrar-por-los-mensajes-de-servicio-de-whatsapp/reduce-mensajes-con-whatsapp-flows) para ver cuándo conviene usarlo.
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

{% hint style="warning" %}
Crear el Flow no significa que se enviará automáticamente a los clientes. Una vez publicado, debe abrirse mediante un mensaje interactivo del asistente, una plantilla de WhatsApp o una automatización —más abajo, en **Cómo conectar un WhatsApp Flow a un asistente**.
{% endhint %}

***

### Creación con PandAI: que lo arme por ti

Si prefieres no construir el Flow bloque por bloque, PandAI ofrece dos caminos, disponibles al darle contexto sobre **Asistentes**:

* **Crear un WhatsApp Flow** — le describes qué información necesitas capturar y PandAI arma el Flow completo de forma automática, aplicando el mismo proceso que harías a mano pero sin que tengas que tocar cada pantalla tú mismo. Igual que en la creación manual, este Flow queda como una pieza suelta: si lo quieres dentro de un asistente, hay que ir a asociarlo a mano en **Mensajes Interactivos**.
* **Condensar una ruta en un WhatsApp Flow** — PandAI lee los escenarios y rutas de tu asistente y te recomienda qué rutas conversacionales conviene transformar en un Flow, para reducir la cantidad de mensajes que el asistente tiene que enviar para recolectar la misma información. A diferencia de la opción anterior, aquí no necesitas asociar nada tú mismo: PandAI conecta el Flow resultante directo a la función de **Mensajes Interactivos** del asistente.

***

### Creación manual: paso a paso

Si prefieres armar el Flow tú mismo —o quieres entender qué hay detrás de lo que PandAI genera—, desde **Canales → WhatsApp Flows** haz clic en **+ Crear** para abrir el constructor, dividido en un panel de configuración a la izquierda y una vista previa en vivo dentro de un teléfono a la derecha. Ahí defines tres cosas antes de tocar el contenido del formulario:

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FiRAYBymAA4PEyBZvTFta%2Fimage.png?alt=media&#x26;token=264d42f4-94e1-4da1-9343-1051f3086164" alt=""><figcaption></figcaption></figure>

* **Nombre del flujo** — el nombre interno con el que identificarás este Flow (por ejemplo, «Encuesta satisfacción»).
* **Categorías** — se agregan con **Agregar categoría**.
* **Números de WhatsApp** — se agregan con **Agregar número**; define en qué número(s) va a estar disponible este Flow.

Con eso listo, arma el contenido del formulario en **Pantallas**. Cada pantalla ("Pantalla 1", "Pantalla 2"...) tiene:

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

### Cómo conectar un WhatsApp Flow a un asistente

Un Flow creado y publicado no se envía solo: hay que indicarle al asistente cuándo debe abrirlo. Si lo generaste con la opción **Condensar una ruta** de PandAI, esta conexión ya quedó hecha; si lo creaste a mano o con **Crear un WhatsApp Flow**, sigue estos pasos.

**1. Verifica que el asistente sea V3**

Los WhatsApp Flows solo funcionan con asistentes **V3**. Los asistentes V2 no tienen la función de mensajes interactivos.

**2. Publica el Flow en un número de WhatsApp**

El Flow debe estar disponible en el **mismo número** desde el cual responde el asistente:

1. Ve a la sección de Flows.
2. Abre el Flow que quieres usar.
3. Revisa o completa sus pantallas y campos.
4. Publicálo en el número de WhatsApp correspondiente.
5. Guarda los cambios.

{% hint style="warning" %}
Un Flow publicado solamente en un canal web, Instagram u otro canal **no podrá enviarse** como WhatsApp Flow.
{% endhint %}

**3. Abre el asistente V3**

1. Ve a **Asistentes**.
2. Abre el asistente V3.
3. Entra a su configuración o automatizaciones.
4. Busca **Enviar mensaje interactivo**.

**4. Activa los mensajes interactivos**

Activa la función **Enviar mensaje interactivo**. Esta función permite que el asistente envíe botones, listas o WhatsApp Flows.

**5. Agrega el Flow al asistente**

Dentro de la configuración de mensajes interactivos:

1. Selecciona **Agregar Flow**.
2. Elige el Flow correspondiente.
3. Escribe una **descripción clara de cuándo debe utilizarlo** —por ejemplo, «Cuando el cliente quiere seleccionar una sesión de cine y elegir un asiento», no solo una lista de los campos del formulario.

{% hint style="info" %}
La descripción debe indicar **cuándo** debe enviarse el Flow, no solamente qué campos contiene. El asistente decide el momento correcto en base a esa descripción.
{% endhint %}

**6. Guarda la configuración**

{% hint style="warning" %}
Si ya había otros Flows configurados, asegúrate de conservarlos: la lista de Flows **reemplaza la configuración anterior completa**, no se acumula sola.
{% endhint %}

**7. Indica al asistente que use la función en la ruta correspondiente**

Conectar el Flow al asistente no hace que se envíe automáticamente. La ruta o escenario donde se recopilan esos datos debe indicarle al asistente que utilice la función de mensajes interactivos, con una referencia de función con un formato similar a:

```
{{function:Send Interactive Message(...)}}
```

{% hint style="danger" %}
No escribas manualmente el nombre del Flow dentro de la ruta. El Flow que se va a utilizar se determina mediante la descripción configurada en los mensajes interactivos, no por lo que escribas en la ruta.
{% endhint %}

La ruta también debe indicar qué hacer después de que el cliente complete el formulario, porque las respuestas regresan como datos estructurados.

**8. Verifica la conexión del asistente**

Confirma que:

* El asistente sea V3.
* El asistente esté asignado a una etapa activa.
* La etapa pertenezca a un embudo conectado al número de WhatsApp.
* El Flow esté publicado en ese mismo número.
* La ruta incluya la referencia de **Enviar mensaje interactivo**.
* La descripción del Flow explique claramente cuándo debe utilizarse.

**Errores comunes**

* **El Flow existe, pero no se envía:** probablemente no está publicado en el número de WhatsApp.
* **El asistente no encuentra el Flow:** no fue agregado a la lista de mensajes interactivos.
* **El Flow está conectado, pero el asistente sigue preguntando campo por campo:** falta la referencia de función dentro de la ruta.
* **El Flow no funciona en Instagram o Web Chat:** los WhatsApp Flows funcionan solo para WhatsApp.
* **El asistente es V2:** esta función solo está disponible en asistentes V3.

{% hint style="info" %}
Para la explicación conceptual de cómo conviven botones, listas y Flows dentro de un mismo asistente, revisa [Mensajes Interactivos: botones, enlaces y Flows en un mismo asistente](https://academy.vambe.ai/canal/whatsapp-flows/mensajes-interactivos-botones-enlaces-y-flows-en-un-mismo-asistente).
{% endhint %}

***

### Casos avanzados

Algunos escenarios —lógica condicional compleja entre pantallas, o conectar el Flow a un sistema externo para traer datos dinámicos— pueden requerir configuración adicional más allá de este editor. Si tu caso lo necesita, conviérsalo con tu equipo de implementación de Vambe.

***

### En resumen

Un Flow se arma con pantallas, y cada pantalla con bloques —encabezado, cuerpo, campos de entrada y un pie de página que decide a dónde salta el cliente. Puedes armarlo tú mismo en el editor, pedírselo a PandAI ya listo, o pedirle a PandAI que directamente convierta una ruta conversacional existente en un Flow y la conecte sola. Sea cual sea el camino, una vez publicado en el número correcto falta un último paso —salvo que uses «Condensar una ruta»—: conectarlo a tu asistente V3 siguiendo esta guía para que sepa cuándo enviarlo.
