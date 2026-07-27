# Script del botón de WhatsApp: qué hace y cómo validarlo con tu equipo de seguridad

Muchos clientes agregan a su sitio web un botón flotante que dirige directamente a una conversación de WhatsApp. Este artículo documenta en detalle el script que genera ese botón, pensado para que tu equipo de seguridad o TI pueda validar su instalación antes de aprobarla.

{% hint style="info" %}
Si lo que necesitas es el script de atribución de campañas publicitarias (el que se obtiene desde Workspaces para medir de qué anuncio provino cada contacto), revisa los artículos de configuración de Google Ads, Meta Ads o TikTok en esta misma sección. Se trata de un script distinto, con un propósito distinto.
{% endhint %}

***

## Qué es este script

El script agrega un botón flotante de WhatsApp a tu sitio web. Al hacer clic, el visitante es dirigido a una conversación de WhatsApp con el número que configures, pasando por un redirect de Vambe que permite atribuir el origen del contacto.

| Característica | Detalle                                                      |
| -------------- | ------------------------------------------------------------ |
| URL del script | `https://vambeai.com/whatsapp.js`                            |
| Tamaño         | \~10 KB                                                      |
| Tecnología     | JavaScript plano, sin dependencias ni librerías de terceros  |
| Entrega        | HTTPS, alojado en la infraestructura de Vambe                |
| Carga          | Con atributo `defer`, no bloquea el renderizado de la página |

***

## Instalación

{% code title="Instalación del botón" %}
```html
<script src="https://vambeai.com/whatsapp.js" defer></script>
<script>
  document.addEventListener("DOMContentLoaded", function () {
    if (typeof window.createWhatsAppButton === "function") {
      window.createWhatsAppButton({
        phoneNumber: "569XXXXXXXX",
        message: "Hola, quiero más información",
        backgroundColor: "#25D366",
        position: "bottom-right",
        size: 50,
        useWithWebChat: false,
        clientId: "<UUID entregado por Vambe>"
      });
    }
  });
</script>
```
{% endcode %}

El script expone dos funciones: `window.createWhatsAppButton`, para el botón simple, y `window.createWhatsAppChatButton`, para la variante con mini-ventana de chat. Ninguna se ejecuta automáticamente; tu sitio decide cuándo y con qué configuración invocarlas.

***

## Qué hace exactamente

Al invocarse, el script:

1. Inyecta un elemento `<style>` con sus propios estilos (con prefijo `vambe-`, para no interferir con los estilos de tu sitio).
2. Crea el elemento del botón y lo agrega al `<body>`.
3. Renderiza el ícono de WhatsApp como un SVG incluido en el propio script.

La única solicitud de red durante la carga de la página es la descarga del archivo `whatsapp.js`.

{% hint style="info" %}
Este script no realiza llamadas de red adicionales, no carga recursos externos, no crea ni lee cookies, `localStorage` o `sessionStorage`, no lee el contenido de la página ni de sus formularios, y no modifica el DOM existente más allá de agregar sus propios elementos. Tampoco registra listeners de teclado, mouse o navegación distintos al clic sobre su propio botón.
{% endhint %}

***

## Comportamiento al hacer clic

El botón es un enlace estándar (`target="_blank"`, `rel="noopener noreferrer"`). Al hacer clic, el navegador abre:

```
https://api.vambe.ai/api/redirect/website/to-whatsapp?phoneTo=<número>&message=<mensaje>&clientId=<uuid>
```

Ese endpoint registra el clic para atribución y responde con un redirect (HTTP 302) hacia `https://api.whatsapp.com/send`, que abre WhatsApp con el mensaje pre-cargado.

{% hint style="warning" %}
El endpoint tiene un límite de 50 solicitudes por minuto por IP. Si el parámetro `clientId` no está presente, el enlace se genera directo a `api.whatsapp.com`, sin pasar por Vambe y sin atribución.
{% endhint %}

***

## Datos capturados

El script no captura datos en el navegador. La atribución ocurre íntegramente del lado del servidor, en el momento del redirect, y se limita a metadatos estándar de la solicitud HTTP:

| Dato                                                        | Origen                                           |
| ----------------------------------------------------------- | ------------------------------------------------ |
| `clientId` (identificador de tu cuenta Vambe)               | Parámetro del enlace                             |
| Número de WhatsApp destino y mensaje pre-cargado            | Parámetros del enlace                            |
| Parámetros UTM o identificadores de campaña (`utm_*`, etc.) | Solo si están presentes en la URL                |
| User-Agent                                                  | Header HTTP estándar                             |
| Dirección IP                                                | Conexión HTTP                                    |
| URL de origen o referrer                                    | Headers HTTP estándar, si el navegador los envía |

Adicionalmente, el servidor inserta un código de tracking de 8 dígitos en el mensaje pre-cargado, usando caracteres Unicode de ancho cero (invisibles para el usuario), que permite asociar la conversación de WhatsApp resultante con el clic de origen. Este código no contiene información personal.

No se capturan datos personales del visitante, contenido de la página, cookies ni identificadores de dispositivo.

***

## Dominios y Content Security Policy

| Dominio            | Uso                                            | Tipo                                   |
| ------------------ | ---------------------------------------------- | -------------------------------------- |
| `vambeai.com`      | Descarga del script                            | Recurso (`script-src`)                 |
| `api.vambe.ai`     | Redirect de atribución al hacer clic           | Navegación (no requiere `connect-src`) |
| `api.whatsapp.com` | Destino final (WhatsApp / Meta)                | Navegación                             |
| `vambe.ai`         | Enlace "Powered by Vambe" (solo variante chat) | Navegación                             |

Si tu sitio utiliza Content Security Policy:

* `script-src`: agrega `https://vambeai.com`.
* `style-src`: el script inyecta un elemento `<style>`, por lo que requiere `'unsafe-inline'` (o un nonce, si tu sitio lo gestiona).
* No se requieren reglas adicionales de `connect-src`, `img-src`, `font-src` ni `frame-src`, ya que el script no hace llamadas de red ni carga recursos externos.

Otros requisitos: el sitio puede estar servido por HTTP o HTTPS (se recomienda HTTPS), funciona en cualquier navegador moderno, y no requiere frameworks ni configuración adicional del lado del servidor.

***

## Modos de falla

* **Si `vambeai.com` está bloqueado o el script no carga**, el sitio no se ve afectado: el snippet de instalación verifica que `window.createWhatsAppButton` exista antes de invocarlo, por lo que el botón simplemente no se muestra.
* **Si `api.vambe.ai` no responde al hacer clic**, el visitante ve un error de navegación en la pestaña nueva; la página original no se ve afectada.
* El script no tiene mecanismos de auto-actualización ni ejecuta código remoto adicional: lo que está publicado en `vambeai.com/whatsapp.js` es la totalidad del código que se ejecuta.

***

## En resumen

El script del botón de WhatsApp es un componente acotado y de bajo riesgo: no lee datos del sitio, no usa almacenamiento del navegador, y su única función es abrir una conversación de WhatsApp al hacer clic, con la atribución resuelta del lado del servidor. Este artículo puede compartirse directamente con tu equipo de seguridad o TI para agilizar la validación de su instalación.
