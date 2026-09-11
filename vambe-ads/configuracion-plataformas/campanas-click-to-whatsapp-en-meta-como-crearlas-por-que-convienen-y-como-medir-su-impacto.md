# Campañas Click to WhatsApp en Meta: cómo crearlas, por qué convienen y cómo medir su impacto

Un anuncio Click to WhatsApp (Meta lo llama CTWA; Google usa el nombre click to chat) es técnicamente una campaña normal de Meta Ads, con una sola diferencia: su destino de conversión no es una página web, sino una conversación de WhatsApp. La persona toca **Enviar mensaje** en el anuncio y aparece directo en tu chat, sin landing que cargue, sin formulario que llenar y sin redirect al navegador.

Este artículo repasa qué es este formato y por qué conviene, cómo crear la campaña paso a paso, qué revisar antes de publicarla, y cómo medir su impacto real conectando el anuncio con lo que pasa después en tu embudo.

{% hint style="info" %}
La campaña se crea y publica desde el Administrador de Anuncios o Meta Business Suite, fuera de Vambe. Donde sí entra Vambe es en la medición: **Vambe Ads** conecta cada campaña con lo que realmente ocurre en tu embudo después del clic.
{% endhint %}

***

## Por qué conviene este formato

### La ventana de 72 horas

Cuando alguien te escribe desde un anuncio Click to WhatsApp o desde el botón de tu página de Facebook, Meta lo trata como un punto de entrada gratuito (_free entry point_). Si respondes dentro de las primeras 24 horas, se abre una ventana de 72 horas en la que los mensajes de esa conversación no tienen costo de entrega.

El beneficio aplica cuando la persona entra desde el anuncio o desde el botón de la página, en Android o iOS — escritorio y web no están soportados —, y requiere que el negocio responda dentro de esas primeras 24 horas. Es política de Meta y puede cambiar.

### Cuatro razones para usar campañas CTWA

Este formato reduce la fricción de entrada: no hay landing que cargue, formulario que llenar ni redirect al navegador, así que la persona pasa del feed al chat en un toque. También trae una intención más alta, porque abrir una conversación es un paso más grande que llenar un campo — quien lo da llega con una pregunta concreta.

Además, el lead se califica hablando: en el chat puedes preguntar presupuesto, urgencia, comuna o tipo de servicio sin que la persona sienta que está siendo encuestada. Y esa conversación genera una mejor señal para el algoritmo, porque los datos de intención que produce se devuelven a Meta como eventos de conversión, y el algoritmo aprende a buscar leads parecidos a los que sí cierran.

***

## Requisitos antes de crear la campaña

Revisar esta lista antes de tocar el Administrador de Anuncios evita la mayoría de los retrabajos:

| Requisito                        | Detalle                                                                      | Quién lo resuelve |
| -------------------------------- | ---------------------------------------------------------------------------- | ----------------- |
| Página de Facebook               | Activa y dentro del portafolio de Meta del cliente                           | Cliente           |
| Número de WhatsApp conectado     | Vinculado al portafolio y visible como destino del anuncio                   | Cliente + Vambe   |
| Número operando por API o Apollo | Indispensable para automatizar la respuesta y para la atribución del anuncio | Vambe             |
| Cuenta publicitaria con pago     | Método de pago validado y sin restricciones activas                          | Cliente           |
| Asistente publicado              | Con embudo y etapas listas, para que el lead entre calificándose             | Vambe             |

***

## Cómo crear la campaña, paso a paso

Hay dos rutas. La primera da control completo y es la recomendada para campañas que van a escalar; la segunda sirve para promocionar rápido una publicación que ya está rindiendo.

### Ruta A — Administrador de Anuncios de Meta (recomendada)

{% stepper %}
{% step %}
#### Crear la campaña y elegir objetivo

Elige **Interacción**, **Tráfico** o **Ventas**: son los tres objetivos que permiten WhatsApp como destino. **Interacción** es el punto de partida habitual cuando lo que buscas son conversaciones.

Si el anuncio toca crédito, empleo, vivienda, política o temas sociales, declara la categoría especial correspondiente.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Elegir WhatsApp como destino de conversión

En el conjunto de anuncios, dentro de **Conversión**, selecciona **Apps de mensajería** y luego **Clic para enviar mensaje**. Elige **WhatsApp** como canal y confirma la página y el número que van a recibir los chats.
{% endstep %}

{% step %}
#### Configurar audiencia y creativo

Define audiencia, presupuesto, calendario y ubicaciones en Facebook e Instagram. Carga el creativo —imagen, video o carrusel— y redacta el mensaje de apertura pre-llenado con el que se abrirá la conversación.
{% endstep %}

{% step %}
#### Revisar y publicar

Revisa la vista previa del anuncio tal como se verá en Facebook e Instagram, y publica.
{% endstep %}
{% endstepper %}

### Ruta B — Promocionar desde Meta Business Suite (rápida)

{% stepper %}
{% step %}
#### Elegir el objetivo

En **Crear nuevo anuncio**, elige el objetivo **Conseguir mensajes**.
{% endstep %}

{% step %}
#### Cargar el contenido

Usa una publicación existente que ya esté rindiendo, o sube texto y contenido multimedia nuevos.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Configurar el destino del mensaje

En **Destino del mensaje**, apaga **Destino automático** y marca solo **WhatsApp**, eligiendo el número correcto en el desplegable.

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Definir audiencia y presupuesto

Define la audiencia y el presupuesto diario, y revisa el resumen antes de confirmar: el monto final que se cobra puede incluir impuestos estimados, así que el total que ve el cliente en su factura no es el presupuesto base que se configuró.

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Publicar y verificar

Publica y envía un mensaje de prueba para confirmar que llega al número de WhatsApp esperado.
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
El error más frecuente ocurre en el paso de **Destino del mensaje**: **Destino automático** viene activado por defecto y envía a la persona a la app de mensajería donde más interactúa, que puede ser Messenger o Instagram en vez de WhatsApp. Cuando eso pasa, la conversación no abre la ventana de 72 horas y no queda atribuida en el embudo. Si el objetivo es WhatsApp, ese interruptor va apagado.
{% endhint %}

***

## Los primeros minutos definen el resultado

El anuncio abre la puerta; lo que pasa después del clic decide si hay venta. Cuatro reglas prácticas ayudan a aprovecharlo:

El **mensaje de apertura debe calzar con el creativo** — si el anuncio ofrece una evaluación gratis, el mensaje pre-llenado tiene que hablar de esa evaluación, no un genérico "Hola, quiero información". Hay que **responder en segundos, no en horas**: además de mejorar la conversión, hacerlo dentro de las primeras 24 horas es justamente la condición que deja activa la ventana de 72 horas.

También conviene **calificar en el chat**: dos o tres preguntas bien puestas separan al curioso del comprador, y esa señal es la que después alimenta las campañas. Y es mejor dar **respuestas completas en vez de muchas cortas** — consolidar la respuesta en un mensaje bien armado mejora la experiencia y ordena la operación.

***

## Cómo medir el impacto

El Administrador de Anuncios muestra impresiones, clics, conversaciones iniciadas y costo por conversación. Es información útil, pero se detiene en el clic: no dice si esa conversación se convirtió en un lead calificado, en una hora agendada o en una venta. Ese tramo lo cubre **Vambe Ads**, que conecta cada campaña con lo que realmente pasó en el embudo.

| Métrica                                             | Dónde se mide | Qué decisión habilita                                   |
| --------------------------------------------------- | ------------- | ------------------------------------------------------- |
| Impresiones y clics                                 | Meta Ads      | Si el creativo y la audiencia funcionan                 |
| Conversaciones iniciadas y costo por conversación   | Meta Ads      | Si el anuncio consigue abrir el chat                    |
| Campaña, conjunto y anuncio que originó cada lead   | Vambe Ads     | Qué anuncio traer de vuelta y cuál apagar               |
| Etapa del embudo de cada contacto                   | Vambe Ads     | Dónde se están cayendo los leads del anuncio            |
| Costo por lead calificado, por agendado y por venta | Vambe Ads     | Cómo repartir el presupuesto de verdad                  |
| Eventos de conversión devueltos a Meta              | Vambe Ads     | Que el algoritmo optimice hacia cierres, no hacia chats |
| Comparación entre Meta, Google y TikTok             | Vambe Ads     | Dónde poner el próximo peso invertido                   |

{% hint style="info" %}
Meta marca los resultados diarios estimados del Administrador de Anuncios como proyecciones según puja, presupuesto y audiencia — las cifras reales pueden ser mayores o menores. Sirven para dimensionar la campaña, no para reportar su resultado final.
{% endhint %}

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Con Vambe Ads, el ciclo se cierra de punta a punta: la **atribución real** sigue el camino del anuncio al cierre, viendo en qué etapa está cada contacto que llegó por campaña. Los **eventos de comportamiento** —cliente interesado, que agenda, que compra, que abandona el carrito— se envían a las plataformas como señales de alta calidad. Las **audiencias dinámicas** se arman directamente desde el embudo (compraron, agendaron, mostraron interés sin cerrar) para retargeting, exclusiones y lookalikes, sin exportar archivos.

Las campañas de Meta y Google también se pueden **crear y editar desde Vambe**, con asistente conversacional o de forma manual, y los **reportes de atribución** se exportan a Excel o Google Sheets para las reuniones con el cliente.

***

## Errores que más cuestan

Además de dejar **Destino automático** encendido, hay otros errores que le cuestan caro a la campaña. **Publicar sin asistente activo** hace que el anuncio genere chats a cualquier hora; si nadie responde rápido, el lead se enfría y la ventana de 72 horas no se aprovecha. Un **creativo que no anticipa el canal** también resta: conviene decir explícito "escríbenos por WhatsApp", porque eso reduce clics accidentales y sube la calidad del chat.

Otro error frecuente es **leer "conversaciones iniciadas" como si fueran ventas** —es una métrica de apertura, no de resultado—, y **no devolver eventos de conversión**: sin esa señal, Meta optimiza a ciegas hacia quien abre chats, no hacia quien compra. Por último, **cambiar el número de destino sin avisar** rompe la continuidad de la atribución y deja campañas activas apuntando a un canal que ya no se atiende.

***

## Checklist de publicación

1. Página, número y cuenta publicitaria verificados en el portafolio de Meta.
2. Objetivo **Interacción**, **Tráfico** o **Ventas**, con conversión en **Apps de mensajería**.
3. WhatsApp como único destino; **Destino automático** apagado.
4. Número de destino confirmado con una prueba real de mensaje.
5. Creativo que anticipa que se abre WhatsApp.
6. Mensaje de apertura alineado con la promesa del anuncio.
7. Asistente publicado y respondiendo en segundos.
8. Embudo y etapas listas para calificar el lead que entra.
9. Eventos de conversión configurados en Vambe Ads.
10. Reporte de atribución revisado a los 7 y a los 30 días.

***

## En resumen

El anuncio abre la puerta; la velocidad de respuesta define el resultado. Una campaña Click to WhatsApp bien configurada elimina la fricción entre el anuncio y la conversación, y aprovecha la ventana de 72 horas para calificar al lead mientras aún está caliente. Lo que separa una buena campaña de una que solo genera chats sin cerrar es lo que pasa después del clic — y esa parte del ciclo, del anuncio al cierre, es la que Vambe Ads te permite ver completa.
