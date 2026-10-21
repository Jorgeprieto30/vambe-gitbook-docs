---
description: >-
  Reconoce en Workflows a los contactos que escriben por WhatsApp desde un
  anuncio Click to WhatsApp: responde distinto, etiqueta y ramifica según la
  campaña.
---

# Reacciona en Workflows cuando un contacto llega desde un anuncio de WhatsApp (CTWA)

Los workflows pueden saber cuándo un contacto escribió por WhatsApp desde un anuncio **Click to WhatsApp (CTWA)**. Esa es justamente la conversación en la que Meta abre la ventana de entrada por anuncio (_free entry point_) si respondes dentro de 24 horas, y el evento **Conversación iniciada desde anuncio de WhatsApp (CTWA)** te permite reconocerla y actuar en consecuencia.

Puedes usarlo como disparador de un flujo o como condición dentro de uno: para responder distinto a quien llega desde un anuncio, etiquetarlo como lead de pauta o ramificar el flujo según la campaña de la que vino.

{% hint style="info" %}
**Para entrar:** en el menú de la izquierda, ve a **Workflows** y crea o abre un Flow. Como disparador, el evento se elige en el trigger **Evento capturado**; como condición, en la **condición por evento**.
{% endhint %}

***

## Cómo usar el evento

### Como disparador

El flujo corre apenas el contacto escribe desde el anuncio. Para configurarlo, elige el trigger **Evento capturado** y, en la lista de eventos, **Conversación iniciada desde anuncio de WhatsApp (CTWA)**.

El evento se dispara con cualquier tipo de mensaje con el que el contacto inicie la conversación: texto, imagen, video o audio.

### Como condición

Dentro de un flujo, la **condición por evento** te deja preguntar _¿tuvo este evento en los últimos 7 días?_ Sirve para saber si la conversación sigue en el periodo de entrada por anuncio de Meta y decidir qué hacer según la respuesta.

***

## Casos de uso

### Responder distinto a quien llega desde un anuncio

Cuando el evento dispara el flujo, puedes enviar un mensaje de bienvenida o una plantilla específica de la campaña, asignar el contacto a un equipo de ventas y etiquetarlo como lead de pauta.

### Aprovechar la entrada por anuncio

Si el contacto vino de un anuncio en los últimos 7 días, la condición por evento permite que el flujo le envíe el seguimiento o la plantilla aprovechando ese periodo específico de la conversación.

### Segmentar por anuncio

El evento trae el ID del anuncio, la campaña, el conjunto de anuncios, el título y el texto del anuncio. Con esos datos puedes ramificar el flujo según la campaña de la que vino el contacto y darle a cada una su propio tratamiento.

***

## Detalles que conviene conocer

* Funciona con **WhatsApp API oficial** y **Apollo**.
* Se dispara **una sola vez por conversación**: si Meta reenvía el mensaje, no se duplica, y las importaciones de historial no lo disparan.
* El evento queda **asociado al ticket** de esa conversación.
* Solo aplica a **WhatsApp**: Messenger e Instagram no tienen el periodo de entrada por anuncio de Meta.

***

## En resumen

El evento **Conversación iniciada desde anuncio de WhatsApp (CTWA)** le da a tus workflows la capacidad de distinguir a quien llegó desde un anuncio de quien escribió por su cuenta. Con él puedes dar una bienvenida a medida, etiquetar y asignar al contacto, aprovechar el periodo de 7 días de entrada por anuncio de Meta para enviar plantillas y ramificar el flujo según la campaña, todo desde el momento en que el contacto escribe.
