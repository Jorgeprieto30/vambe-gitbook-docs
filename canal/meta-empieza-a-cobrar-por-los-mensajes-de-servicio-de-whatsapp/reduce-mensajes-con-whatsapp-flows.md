# Reduce mensajes con WhatsApp Flows

Un Flow es un formulario interactivo que el cliente completa **dentro de WhatsApp**, sin tener que responder una pregunta por mensaje.

En vez de tener esta conversación:

> ¿Cuál es tu nombre?\
> ¿Cuál es tu correo?\
> ¿Qué servicio necesitas?\
> ¿Qué día prefieres?\
> ¿Cuál es tu teléfono?

El cliente completa esos mismos datos en un solo formulario, dentro del propio chat.

{% hint style="info" %}
Esta página explica qué es un Flow y cuándo conviene usarlo. Para el paso a paso de creación dentro de Vambe, revisa **Crea Flows de WhatsApp para capturar información estructurada de tus clientes**.
{% endhint %}

***

### Por qué conviene implementarlos

* Reducen la cantidad de mensajes necesarios para recopilar información.
* Disminuyen el abandono, porque el cliente no tiene que esperar cada pregunta una por una.
* Estructuran las respuestas, evitando datos incompletos o difíciles de interpretar.
* Aceleran la calificación de prospectos.
* Facilitan la automatización, porque las respuestas pueden activar un proceso posterior.
* Mejoran la experiencia del cliente, especialmente en solicitudes repetitivas.
* Reducen el trabajo manual del equipo.
* Pueden ayudar a disminuir el volumen operativo y, según las reglas de cobro vigentes de Meta, el costo asociado a conversaciones con muchos mensajes.

***

### Así se ve un Flow para el cliente

Estos son ejemplos ilustrativos de Meta —no son clientes de Vambe— que muestran el tipo de experiencia que puede armarse con un Flow:

* **Generación de leads con datos de contacto:** el negocio ofrece acceso anticipado a una promoción, el cliente completa nombre, correo y acepta términos en un formulario dentro del chat, y recibe la confirmación en el mismo hilo.

<figure><img src="../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

* **Calificación de interés de compra:** el cliente selecciona categoría, marcas preferidas y uso que le dará al producto; con esas respuestas, el negocio muestra opciones ya filtradas para elegir una y continuar la compra.

<figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

* **Solicitud estructurada en servicios financieros:** el cliente revisa una oferta pre-aprobada, elige monto y plazo, ingresa los datos de pago que corresponda, y confirma en una pantalla de resumen antes de enviar.

<figure><img src="../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

Los tres casos comparten lo mismo: un proceso con **inicio y fin claros**, donde los datos se pueden recoger con campos estructurados —no una conversación abierta que cambia según lo que responde el cliente.

***

### Cuándo conviene usar un Flow

Un buen criterio es usarlo cuando se cumplen estas condiciones:

* La persona debe entregar varios datos.
* Los datos solicitados son prácticamente los mismos en cada caso.
* El proceso tiene un inicio y un fin claros.
* La información puede recogerse con campos estructurados.
* No se necesita una conversación extensa para decidir el siguiente paso.
* El beneficio de reunir los datos de una vez supera el esfuerzo de construir el formulario.

**Buenos casos de uso:** agendamiento (servicio, profesional, fecha y horario), calificación comercial (presupuesto, necesidad, ubicación, plazo), postventa (número de pedido, motivo, evidencia), devoluciones (pedido, motivo, fotografías), encuestas, onboarding y solicitudes internas.

***

### Cuándo NO conviene usar un Flow

No es la mejor herramienta cuando:

* La respuesta siguiente depende mucho de lo que la persona acaba de decir.
* Se necesita negociar o conversar libremente.
* El cliente requiere asesoría personalizada.
* El proceso tiene muchas excepciones.
* La información debe explicarse antes de solicitarla.
* El asistente necesita diagnosticar un problema paso a paso.
* Hay demasiados campos o reglas para mantenerlos en un formulario.

{% hint style="warning" %}
Un Flow debe resolver una tarea concreta y relativamente predecible. No reemplaza una conversación completa con el asistente —y no todos los clientes van a completar el formulario: el asistente siempre debe poder seguir la conversación manualmente si la persona prefiere hablar con alguien, no entiende una pregunta o no puede abrir el Flow.
{% endhint %}

**Casos donde no conviene:** reclamos complejos, soporte técnico que requiere diagnóstico, negociaciones de precio, recomendaciones personalizadas abiertas, conversaciones donde cada cliente necesita preguntas distintas, y procesos con muchas bifurcaciones y excepciones.

***

### En resumen

Un Flow bien acotado reemplaza varios mensajes de ida y vuelta por un solo formulario dentro de WhatsApp, sin sacrificar la calidad del dato que recibes. La clave es usarlo donde el proceso es repetitivo y predecible, y dejar la conversación libre para todo lo demás. Para crear el tuyo, sigue **Crea Flows de WhatsApp para capturar información estructurada de tus clientes**.
