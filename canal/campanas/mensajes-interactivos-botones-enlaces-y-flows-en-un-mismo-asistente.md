# Mensajes Interactivos: botones, enlaces y Flows en un mismo asistente

Los mensajes interactivos permiten que tu asistente envíe experiencias más estructuradas que un mensaje de texto simple: botones, listas o un Flow completo, según lo que necesite la conversación en ese momento.

* **Botones y listas** son más adecuados cuando el cliente debe elegir entre pocas alternativas.
* Un **Flow** es especialmente útil cuando el asistente necesita capturar varios datos de manera ordenada —ver **Crea Flows de WhatsApp para capturar información estructurada de tus clientes**.

{% hint style="info" %}
Un **enlace** no es un componente independiente del mensaje interactivo general: hoy se confirma como parte de una **pantalla de Flow**, no como un tipo de mensaje aparte. Conviene separar los tres conceptos: botones y listas son mensajes interactivos; los enlaces van dentro de una pantalla de Flow; los formularios son WhatsApp Flows.
{% endhint %}

***

### Requisitos confirmados

* La funcionalidad está disponible para **asistentes V3**. No aplica a asistentes V2.
* El asistente debe tener habilitada la herramienta **Send Interactive Message**.
* Cada Flow que el asistente vaya a enviar debe estar **registrado en la configuración del asistente**.
* El Flow debe estar **publicado en el número de WhatsApp** correspondiente —si no lo está, el asistente no podrá enviarlo.
* La **descripción** de cada Flow registrado debe indicar cuándo debe enviarse, no solo qué campos contiene: es lo que el asistente usa para decidir el momento correcto.

***

### Pasos funcionales

1. Abre el asistente V3.
2. Entra a **Configuración del asistente**.
3. Activa **Send Interactive Message**.
4. Agrega el Flow que el asistente podrá enviar.
5. Escribe una descripción clara de **cuándo** utilizarlo.
6. Guarda la configuración.
7. Indica, en la ruta o escenario correspondiente, en qué momento de la conversación debe usarse el mensaje interactivo.
8. Prueba el caso desde WhatsApp.
9. Verifica que el cliente reciba el botón, lista o Flow esperado.
10. Verifica que el asistente continúe la conversación usando las respuestas entregadas.

***

### Qué hay que tener presente

* Activar esta herramienta **cambia el comportamiento del asistente** en conversaciones reales —pruébala antes de dejarla activa para todos los clientes.
* Un Flow correctamente creado **no se enviará** si no está publicado en el número correcto.
* La lista de Flows configurados en el asistente **reemplaza** la configuración anterior; no funciona necesariamente como una lista acumulativa —revisa qué queda registrado después de cada cambio.
* Si eliminas un Flow de esa configuración, puede dejar de estar disponible para el asistente.
* Un Flow no debe usarse para conversaciones que requieren razonamiento abierto o negociación —para eso, deja que el asistente conteste libremente.

***

### En resumen

Un mensaje interactivo bien configurado le da al asistente una herramienta más, junto al texto libre: botones y listas para decisiones rápidas, y Flows para capturar datos estructurados. La clave está en describirle al asistente con claridad **cuándo** usar cada uno, y en probar el caso real antes de dejarlo activo para todos tus clientes.
