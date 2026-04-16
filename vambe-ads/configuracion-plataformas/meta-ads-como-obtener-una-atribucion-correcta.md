---
cover: ../.gitbook/assets/Portada 20.png
coverY: 0
---

# Meta Ads: cómo obtener una atribución correcta

La atribución correcta en **Meta Ads** es clave para entender **desde dónde provienen realmente tus clientes** y qué campañas están generando conversaciones y conversiones reales en Vambe.

En este artículo aprenderás **cuándo la atribución es automática** y **cuándo necesitas una configuración adicional** para que Vambe pueda identificar correctamente el origen del contacto.

## ¿Para qué sirve la atribución?

La atribución permite:

* Saber si un cliente llegó desde una **publicidad** o desde tu **sitio web**.
* Identificar **qué campaña, conjunto o anuncio** generó la conversación.
* Medir correctamente el costo por lead y el rendimiento real de tus anuncios.

## Escenario 1: Click directo a WhatsApp desde el anuncio (sin configuración)

Si tus anuncios de Meta usan el objetivo **Click a WhatsApp** (o “Enviar mensaje”):

✅ **No necesitas realizar ninguna configuración adicional.**

En este caso:

* Meta envía automáticamente la información del anuncio.
* Vambe identifica de forma directa desde qué anuncio proviene el cliente.
* La atribución es inmediata y precisa.

Este es el escenario más simple y recomendado si tu estrategia lo permite.

## Escenario 2: Click del anuncio hacia tu sitio web (requiere configuración)

Si el anuncio dirige primero a una **página web** y luego el usuario inicia la conversación (por ejemplo, haciendo clic en “Hablar por WhatsApp”), **sí es necesaria una configuración adicional**.

### Requisitos para que la atribución funcione

* El usuario debe **ingresar su número de teléfono** en algún punto del flujo.
* O bien, debe existir una acción clara de contacto (formulario, botón, etc.).

{% hint style="info" %}
Recomendación: utilizar un formulario que solicite el número de teléfono **antes de redirigir a WhatsApp**, para asegurar una atribución precisa.
{% endhint %}

## Paso a paso: Insertar el script de seguimiento web

{% stepper %}
{% step %}
### Accede a Vambe Ads

Ingresa a **Vambe Ads** y dirígete a **Workspaces**.
{% endstep %}

{% step %}
### Obtén el script

En la parte inferior derecha encontrarás la sección **Seguimiento de tráfico web**. Haz clic en **Obtener script de seguimiento**.

![](../.gitbook/assets/image\(81\).png)

Este script contiene un **Tracking ID único** que permite a Vambe identificar visitas desde anuncios y relacionar esas visitas con conversaciones posteriores.
{% endstep %}

{% step %}
### Inserta el script en tu sitio

* Copia el script de seguimiento.
* Pégalo **dentro de la etiqueta** `<head>` de tu sitio web.
* Si usas un CMS (WordPress, Webflow, Shopify, etc.), busca la opción para agregar código personalizado en el **head** del sitio.
* Publica los cambios y asegúrate de que el código esté activo en la página de destino del anuncio.
{% endstep %}
{% endstepper %}

## Verificación del tracking

{% stepper %}
{% step %}
1. Ingresa a tu sitio web desde un anuncio activo.
{% endstep %}

{% step %}
2. Inicia una conversación (WhatsApp o formulario).
{% endstep %}

{% step %}
3. Verifica en Vambe que el contacto tenga información de atribución asociada.
{% endstep %}
{% endstepper %}

Si el script está correctamente instalado, Vambe podrá identificar **desde qué anuncio, campaña o plataforma provino ese cliente**.
