# ¿Qué es la Base de Conocimiento y cómo configurarla en Vambe?

La **Base de Conocimiento** es un espacio central dentro de Vambe donde puedes almacenar, organizar y conectar información clave para que los asistentes de inteligencia artificial la utilicen al responder a los clientes.

Gracias a la base de conocimiento, los asistentes pueden entregar respuestas más precisas, coherentes y alineadas con la información real de tu negocio.

***

## ¿Para qué sirve la Base de Conocimiento?

La Base de Conocimiento permite que los asistentes de Vambe puedan:

* Responder preguntas frecuentes con información real del negocio.
* Explicar servicios, tratamientos, precios o procesos.
* Acceder a documentos internos o externos sin inventar respuestas.
* Mantener coherencia entre distintos asistentes.
* Escalar la atención sin perder calidad.

***

## ¿Qué tipo de información puedes cargar?

### Información interna (dentro de Vambe)

* Texto escrito directamente en documentos internos.
* Información estructurada por carpetas y documentos.

### Información externa (conectada)

Puedes conectar carpetas desde plataformas como:

* Google Drive
* Notion
* Dropbox
* HubSpot
* Intercom
* Salesforce

Una vez conectadas, los asistentes podrán usar esa información para responder.

***

## Cómo acceder a la Base de Conocimiento

{% stepper %}
{% step %}
### Acceder a la sección de Conocimiento

* En el menú lateral izquierdo, ingresa a **Asistentes**.
* En el submenú, haz clic en **Conocimiento**.

![Resumen de carpetas](../.gitbook/assets/image\(28\).png)

{% hint style="info" %}
Las carpetas que muestran el logo de una plataforma externa indican que están conectadas desde una fuente externa.\
Las carpetas sin logo son carpetas internas de Vambe.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## Cómo crear una carpeta interna

Las carpetas internas almacenan información directamente dentro de Vambe.

{% stepper %}
{% step %}
### Crear nueva carpeta

* Dentro de **Conocimiento**, haz clic en **Crear nueva carpeta**.

![Crear carpeta](../.gitbook/assets/image\(29\).png)
{% endstep %}

{% step %}
### Asignar nombre

* Asigna un nombre claro a la carpeta (por ejemplo: “Tratamientos”, “Preguntas frecuentes”, “Políticas”).
* Confirma la creación.

La carpeta se creará vacía y lista para recibir documentos.

![Carpeta creada](../.gitbook/assets/image\(30\).png)
{% endstep %}
{% endstepper %}

***

## Cómo crear documentos internos

{% stepper %}
{% step %}
### Añadir documento

* Ingresa a la carpeta que creaste.
* Haz clic en **Añadir documento**.

![Añadir documento](../.gitbook/assets/image\(31\).png)
{% endstep %}

{% step %}
### Escribir o pegar contenido

* Escribe o pega el contenido que deseas que los asistentes utilicen.

![Editor de documento](../.gitbook/assets/image\(32\).png)
{% endstep %}

{% step %}
### Guardar

* Guarda el documento.\
  Este contenido quedará disponible para la inteligencia artificial.
{% endstep %}
{% endstepper %}

***

## Cómo conectar documentos externos (Google Drive, Notion, etc.)

### Paso 1: Ir a documentos externos

{% stepper %}
{% step %}
### Ir a Documentos externos

* Dentro de **Conocimiento**, haz clic en **Documentos externos**.
* En la parte superior derecha, selecciona **Crear nueva conexión**.

![Crear conexión](../.gitbook/assets/image\(33\).png)
{% endstep %}
{% endstepper %}

***

### Paso 2: Elegir la plataforma

Selecciona la plataforma desde la cual deseas conectar información (por ejemplo, **Google Drive**).

{% hint style="info" %}
Recomendación importante: cuando conectas una fuente externa, **siempre debes seleccionar una carpeta**, no un archivo individual.
{% endhint %}

***

### Paso 3: Autorizar y seleccionar carpeta

{% stepper %}
{% step %}
### Autorizar la plataforma

1. Inicia sesión en la plataforma seleccionada.
2. Acepta los permisos solicitados.
{% endstep %}

{% step %}
### Seleccionar carpeta

* Cuando aparezca la opción de selección, elige **la carpeta** que contiene los archivos que deseas sincronizar.

![Seleccionar carpeta](../.gitbook/assets/image\(34\).png)
{% endstep %}

{% step %}
### Conectar datos

* Haz clic en **Seleccionar**.
* Luego presiona **Connect data**.

![Conectar datos](../.gitbook/assets/image\(36\).png)

{% hint style="warning" %}
Error común: buscar un archivo específico en lugar de la carpeta. Todo lo que esté dentro de la carpeta seleccionada será agregado a la Base de Conocimiento.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## Sincronización y verificación

* Una vez conectada la carpeta, Vambe comenzará a sincronizar la información.
* Después de unos minutos, la fuente aparecerá como conectada.
* Eso confirma que los documentos ya forman parte de la Base de Conocimiento.

![Conectado](../.gitbook/assets/image\(37\).png)

***

## Pregunta frecuente

<details>

<summary>¿Puedo subir un archivo externo directamente a Vambe?</summary>

No. Actualmente no es posible subir archivos externos directamente.

Opciones correctas:

* Copiar y pegar el contenido en un documento interno.
* Subir el archivo (PDF, DOC, etc.) a una carpeta de Google Drive y conectar esa carpeta.

</details>

***

## Siguiente paso recomendado

* Conecta la base de conocimiento a uno o más asistentes.
* Indica en los bloques de instrucciones cuándo y cómo deben usar esa información.
* Prueba el asistente para validar que esté respondiendo correctamente.
