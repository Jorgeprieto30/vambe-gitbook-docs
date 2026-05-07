# Cómo conectar herramientas externas a tu asistente V3 con Funciones

### ¿Para qué sirve?

Las funciones de integraciones externas permiten que tu asistente v3 interactúe con otras herramientas directamente dentro de una conversación. Por ejemplo, puede enviar un mensaje a un canal de Slack, crear una página en Notion o abrir un ticket en Linear, todo de forma automática cuando se cumpla una condición que tú definas.

***

### ¿Qué integraciones están disponibles?

Al crear una función de integración externa, encontrarás las siguientes opciones ya disponibles:

* **Slack** — Envía mensajes a canales o usuarios de tu workspace
* **Notion** — Crea, busca y lee páginas en tu workspace
* **Linear** — Crea tickets en el Linear de tu equipo
* **Agregar Fila a Hoja** — Conecta Google Sheets y agrega una fila cuando se cumpla la condición
* **Buscar Fila en Hoja** — Busca una fila específica en Google Sheets según la condición
* **Link Fintoc** — Genera un link de pago con Fintoc para realizar un pago o acción financiera
* **Checkout Vambe** — Crea un link de checkout con productos Vambe y sus cantidades

{% hint style="info" %}
💡 **¿No encuentras la integración que necesitas?** Usa el botón **Solicitar una integración** dentro del catálogo. Trabajamos con un catálogo de cientos de apps (Gmail, Google Calendar, HubSpot, Outlook, Google Drive, Airtable, GitHub, Supabase, entre muchas otras) y solemos habilitarlas en aproximadamente una semana.
{% endhint %}

***

### Paso a paso: crear una función de integración externa

#### 1. Accede a las funciones de tu asistente

Desde el menú lateral, ve a **Asistente** y abre el asistente v3 al que quieres agregar la integración. Haz clic en la pestaña **Funciones**.

#### 2. Crea una nueva función

Haz clic en **+ Crear función**. Se abrirá un panel con las categorías disponibles:

* Acciones principales
* Búsqueda de información
* Agendamiento
* Cálculos
* **Integraciones externas** ← selecciona esta

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

#### 3. Elige la integración

Dentro de **Integraciones externas**, verás las opciones disponibles. Las que aún no están conectadas mostrarán la etiqueta **SIN CONECTAR**. Selecciona la que necesitas.

#### 4. Conecta tu cuenta (si es la primera vez)

Si la integración no está conectada, haz clic en **Conectar**. Dependiendo de la herramienta:

* Algunas te pedirán autorizar el acceso desde la plataforma externa (ej: Notion te redirige para seleccionar el workspace y dar permisos)
* Otras requieren ingresar credenciales directamente en Vambe

Una vez autorizada, Vambe mostrará las funciones disponibles para esa integración.

#### 5. Configura los parámetros de la función

Al crear la función, el asistente te pedirá definir:

* **Cuándo usarla** — la condición o momento en que el asistente debe ejecutarla
* **Parámetros requeridos** — algunos son opcionales y puedes dejar el valor por defecto, pero otros son obligatorios. Por ejemplo, en Slack tendrás que especificar el canal al que se enviará el mensaje (por ID o nombre)

#### 6. Guarda y asocia la función

Una vez configurada, la función quedará asociada al asistente y se ejecutará automáticamente cada vez que se cumpla la condición definida. También puedes reutilizar funciones ya creadas desde la librería de **Funciones** en el menú lateral.

***

### Tipos de funciones por categoría

Además de las integraciones externas, al crear una función tienes acceso a otras categorías útiles:

**Acciones principales** Cambio de Etapa, Quitar contacto del embudo, Enviar Plantilla, Enviar Audio, Llamada Webhook, Crear Nota, Enviar Documento o Imagen, Ejecutar Flow.

**Búsqueda de información** Permite al asistente consultar fuentes externas para responder con datos actualizados.

**Agendamiento** Agendamiento de Citas, Google Calendar, Outlook — para crear o gestionar eventos automáticamente según condiciones.

**Cálculos** Resolver Problema Matemático — el asistente resuelve operaciones matemáticas cuando lo necesita.

***

### ¿Tienes ideas de nuevas integraciones?

Si tus clientes necesitan conectar otras herramientas como ClickUp, Discord, Google Drive u otras, puedes solicitarlas directamente desde el botón **Solicitar una integración** dentro del catálogo. El equipo de Vambe las habilita en aproximadamente una semana.
