---
description: >-
  Combina mensajería, correo y llamadas IA en un solo flujo de contacto que se
  detiene apenas tu cliente responde o convierte, y mide cada paso.
---

# Campañas: contacta a tus clientes con un flujo omnicanal

Una campaña en Vambe es una secuencia coordinada de intentos de contacto hacia un grupo de clientes. En lugar de enviar una sola plantilla y esperar, defines un flujo de pasos —mensajería, correo y llamadas IA— con tiempos de espera entre uno y otro, y Vambe deja de insistir apenas la persona responde o cumple el objetivo que definiste.

Esto cambia la pregunta que puedes responder sobre tus envíos: en vez de cuántos mensajes salieron, pasas a saber qué combinación de canales te trae más respuestas y más conversiones. En esta guía verás cómo armar el flujo, cargar tu audiencia, programar el envío y leer los resultados.

> Para entrar: en el menú de la izquierda, ve a **Canales** y luego a **Campañas**. Para crear una, haz clic en **+ Crear campaña**.

***

## Cómo funciona una campaña

Cada campaña es un flujo de engagement: intenta contactar a la persona por los canales que definas, en el orden que definas, y se detiene en cuanto logra su propósito.

Hay dos momentos que conviene tener claros desde el principio:

* **Cuando el contacto responde, se crea el ticket.** No antes. El ticket nace por el canal en que la persona contestó y entra a la etapa que definiste para ese paso, así que desde ahí la conversación queda en manos de tu equipo o de tu asistente de Vambe.
* **Cuando se cumple el objetivo, se detienen los envíos pendientes.** Si la persona ya compró o ya te escribió, no recibe los mensajes siguientes del flujo.

La campaña trabaja a nivel de cliente, no de contacto suelto: una misma persona puede tener un número de WhatsApp, un correo y un teléfono, y el flujo elige el dato correcto según el canal de cada paso.

***

## Paso 1: arma el flujo

El primer paso del asistente de creación define el nombre de la campaña, su objetivo y los pasos de contacto.

### Nombre y objetivo

El **nombre** es interno y te sirve para identificar la campaña (por ejemplo, «Descuentos cyber»). El **objetivo** es la definición más importante de toda la campaña, porque cumple dos funciones: marca el hito que detiene el flujo y es la base con la que después se mide la conversión.

Puedes elegir entre estos objetivos:

* **Cambio de etapa**, cuando el éxito es que el cliente avance en tu embudo.
* **Orden creada**, para campañas de ecommerce en las que quieres medir compras.
* **Cita reservada** o **Cita confirmada**, para campañas de agendamiento.
* **Eventos personalizados** que tenga configurados tu organización.
* **Sin objetivo**, cuando lo que buscas es simplemente que la persona te responda.

<figure><img src="../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Elige el objetivo pensando en qué te gustaría poder afirmar al final de la campaña. Si tu objetivo es una orden creada, el panel de resultados te mostrará cuántas personas compraron y por qué monto; si es «Sin objetivo», te mostrará cuántas respondieron.
{% endhint %}

### Los pasos de contacto

Debajo eliges **Nuevo flujo** —o uno que hayas guardado antes— y vas agregando pasos. Los pasos se ejecutan en orden, de arriba hacia abajo, y tienes tres tipos disponibles:

* **Plantilla mensajería**, para enviar una plantilla por WhatsApp u otro canal de mensajería.
* **Correo**, para enviar una plantilla de email.
* **Llamada IA**, para que un asistente de voz llame al contacto.

Al seleccionar un paso, se configura en el panel de la derecha. En los pasos de mensajería y de llamada defines el **canal** por el que sale el contacto y la **etapa al responder**, es decir, el embudo y la columna donde caerá el ticket si la persona contesta por ahí. Después eliges la plantilla —o la guía de llamada, en el caso de la llamada IA— y nombras las variables que la plantilla necesita.

<figure><img src="../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Cuando tu flujo tiene varios pasos por distintos canales, lo más simple es apuntar todos a la misma etapa: así, responda por donde responda, el cliente entra al mismo lugar de tu embudo.
{% endhint %}

Entre un paso y el siguiente defines cuánto esperar antes de volver a intentarlo: **si no responde en X días**, sale el paso siguiente. Un flujo típico parte con una plantilla de WhatsApp, espera un día, envía un correo y, si tampoco hay respuesta, hace un último intento con una llamada IA dos días después.

Los pasos de correo y de llamada IA están disponibles según los canales que tengas habilitados en tu cuenta.

### Guarda el flujo y confirma

Antes de continuar, ponle un **nombre al flujo**. Los flujos quedan guardados como workflows, así que un flujo que te funcionó lo puedes reutilizar en la próxima campaña sin volver a armarlo paso a paso.

Al pasar a la audiencia, Vambe te confirma tres cosas: el flujo queda fijo y para cambiarlo tendrás que crear otra campaña, la audiencia se validará contra esos pasos, y todavía no se envía nada.

***

## Paso 2: carga la audiencia

Aquí eliges de dónde salen los destinatarios. Tienes dos caminos.

### Segmentos

Un segmento es un grupo de clientes que cumple con las reglas que tú defines —etiquetas que comparten, hace cuánto compraron, y otros criterios— y que Vambe recalcula constantemente, así que siempre sabes cuántas personas califican. Es la forma recomendada de armar una audiencia, porque el mismo segmento te sirve campaña tras campaña.

Selecciona el segmento, decide cómo se completan las variables de tus plantillas —puedes rellenarlas tú con un valor fijo, como un saludo— y haz clic en **Cargar audiencia**.

### Planilla Excel

Si tu base está fuera de Vambe, sube una planilla. Vambe te arma la plantilla exacta que necesitas: una fila por contacto con las columnas obligatorias **telefono**, **email** y **nombre**, más una columna por cada variable de cada paso del flujo. En lugar de completar las variables plantilla por plantilla, las llenas todas centralizadas en el mismo archivo.

También puedes agregar columnas opcionales: campos de metadata que quieras guardar en el contacto cuando se cree, y un **ejecutivo** asociado.

Descarga la planilla de ejemplo, complétala con tus datos y súbela en el recuadro de carga.

Al confirmar, Vambe registra a todos los contactos que aún no existían y te muestra un resumen de la carga: cuántos contactos se crearon, cuántos ya existían y cuántas filas se omitieron.

{% hint style="warning" %}
Una vez confirmada, la audiencia queda fija: no se puede modificar. Revisa bien tu segmento o tu planilla antes de confirmar.
{% endhint %}

***

## Paso 3: define cómo sale el envío

El último paso decide el ritmo de la campaña. Puedes enviar a toda la audiencia o solo a una parte, lo que es ideal para hacer una prueba con un grupo pequeño antes de soltar el resto.

Tienes tres modalidades:

* **Enviar ahora**: la campaña sale de inmediato.
* **Programar envío**: eliges el día y la hora en que quieres que salga.
* **Enviar en grupos**: defines cuántas personas entran en cada grupo y cuánta pausa hay entre uno y otro —por ejemplo, 100 personas cada una hora—, y decides si el primer grupo sale ahora o queda programado.

<figure><img src="../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Enviar en grupos distribuye la carga en el tiempo y ayuda a cuidar la reputación de tu número de WhatsApp y de tu dominio de correo cuando la audiencia es grande.
{% endhint %}

Antes de confirmar, Vambe te muestra un resumen del costo estimado del envío desglosado por canal, para que puedas comparar qué tan rentable resulta cada estrategia.

***

## Sigue los resultados

En el listado de campañas ves de un vistazo el estado de cada una: los pasos que la componen, cómo se construyó la audiencia, el proceso del envío —cuántos quedan pendientes, encolados, en curso y finalizados—, cuándo ocurrirá el próximo envío y el costo aproximado acumulado, que se actualiza todas las noches.

Al entrar a una campaña enviada encuentras tres pestañas.

### Resumen

Muestra el desempeño general contra el objetivo que definiste, dentro de una **ventana** de tiempo que tú controlas. La ventana define hasta cuándo cuentas una respuesta o una conversión como atribuible a la campaña: si consideras que convertir a los siete días ya no es mérito del envío, la bajas a dos y las cifras se recalculan.

Ahí encuentras cuántas personas convirtieron y cuánto demoraron en hacerlo, cuántas respondieron, y el alcance del envío separado entre alcanzados, parciales —a quienes se pudo contactar por algunos medios pero no por otros— y no alcanzados.

<figure><img src="../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

Más abajo, el bloque **Qué pasó entre un envío y el siguiente** es el que te dice si cada paso vale la pena: te muestra qué porcentaje respondió después del primer paso, cuánto sumó el segundo sobre lo que quedaba, y así sucesivamente.

<figure><img src="../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

### Progreso por paso

Entrega el detalle de cada nodo del flujo: la vista previa del mensaje, el canal por el que salió y la distribución por estado: enviado, omitido, falló, en curso y pendiente.

Es normal que el primer paso tenga muchos más envíos que el segundo, y aquí entiendes exactamente por qué. Vambe desglosa **por qué fallaron los envíos** (números no registrados, restricciones de entrega) y **por qué se omitieron**: la mayoría suele ser gente que ya respondió o convirtió entre un paso y otro, y por lo tanto no hacía falta volver a contactar, más quienes se dieron de baja de los mensajes de marketing.

### Destinatarios

El listado persona por persona, con su estado, el grupo en que salió, la fecha de envío y el resultado. Puedes buscar por nombre, teléfono o email, filtrar, descargar la tabla y abrir la conversación de cualquier destinatario para ver caso a caso qué ocurrió.

***

## Campañas creadas anteriormente

Si tu organización ya tenía campañas creadas, encontrarás una **Vista antigua** en la sección de Campañas. Está ahí para que puedas consultarlas, revisar sus resultados y terminar de enviar las que hayan quedado a medias. Las campañas que crees de aquí en adelante se arman con el flujo omnicanal descrito en esta guía.

***

## En resumen

Una campaña bien armada no es un mensaje masivo: es una conversación que insiste con inteligencia y se detiene a tiempo. Al definir un objetivo claro, encadenar dos o tres intentos por canales distintos y revisar el aporte de cada paso, dejas de gastar envíos en gente que ya te contestó y empiezas a saber cuál de tus estrategias de contacto realmente convierte.
