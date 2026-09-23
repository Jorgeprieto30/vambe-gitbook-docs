# Conecta un botón de WhatsApp flotante a tu sitio web

Además del Web Chat completo, Vambe te permite agregar un botón flotante de WhatsApp a tu sitio: un ícono que aparece en una esquina de la página y que, al hacer clic, lleva al visitante directo a una conversación de WhatsApp con tu negocio. Es una alternativa más liviana al Web Chat, pensada para negocios que quieren dar acceso rápido a WhatsApp sin instalar un chat completo en la página.

{% hint style="info" %}
El botón flotante no es lo mismo que el **Web Chat**: el botón redirige a una conversación de WhatsApp, mientras que el Web Chat abre el chat dentro de tu propio sitio. Si lo que necesitas es eso, revisa [Cómo instalar y configurar el Web Chat de Vambe en tu sitio web](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/como-instalar-y-configurar-el-web-chat-de-vambe-en-tu-sitio-web).
{% endhint %}

***

### Cómo generar el script

1. Ve al menú lateral y entra a **Canales**.
2. En tu canal de WhatsApp, haz clic en los tres puntos a la derecha.
3. Selecciona **Generar script**.

Ahí se abre el selector con dos tipos de botón: **Botón directo** y **Chat emergente**.

<figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

***

### La diferencia entre los dos tipos

Ambos aparecen como el mismo ícono flotante en tu sitio, pero cambia lo que pasa al hacer clic:

* **Botón directo:** redirige de inmediato a WhatsApp. El visitante hace clic y se abre WhatsApp (web o la app, según el dispositivo) con una conversación ya iniciada hacia tu número, con un mensaje predefinido cargado. No hay ningún paso intermedio dentro de tu página.
* **Chat emergente:** al hacer clic, se despliega una pequeña ventana de chat dentro de la misma página —donde el visitante puede escribir su mensaje— y recién al enviarlo se lo redirige a WhatsApp con ese mensaje ya escrito. Agrega un paso de fricción menor, pero le da al visitante la oportunidad de personalizar lo que va a preguntar antes de salir de tu sitio.

{% hint style="info" %}
**En la práctica:** si quieres el camino más corto a la conversación, usa **Botón directo**. Si prefieres que el visitante piense y escriba su consulta antes de saltar a WhatsApp —por ejemplo, para que llegue con más contexto—, usa **Chat emergente**.
{% endhint %}

***

### Personaliza el botón antes de copiar el script

Desde la misma vista donde se genera el código puedes ajustar el mensaje inicial, el color de fondo del botón, el tamaño del ícono y su posición en la pantalla, con un preview en vivo que refleja los cambios. Vambe genera el script ya con tu número de teléfono y tu identificador de cliente cargados —solo tienes que copiarlo.

Si ya tienes el **Web Chat** de Vambe instalado en la misma página, activa la opción **Usar con webchat**: esto ubica el botón de WhatsApp sobre el Web Chat, abajo a la derecha, para que no se superpongan.

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>

***

### Dónde pegar el script

El script va en el `<head>` de tu página, o justo debajo de donde abre esa etiqueta.

**Instalarlo en Shopify**

1. Desde tu panel de Shopify, ve a **Tienda online → Ver código** (junto al tema activo).

<figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

2. Dentro del explorador de archivos, abre **Layout → theme.liquid**.
3. Pega el script justo debajo de la etiqueta `<head>` —normalmente se encuentra alrededor de la línea 40 del archivo, aunque puede variar según el tema.

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

4. Guarda los cambios.

Como `theme.liquid` es el layout que usan todas las páginas de tu tienda, el botón queda instalado en todo el sitio con este único paso.

***

### Sigue explorando

[Cómo instalar y configurar el Web Chat de Vambe en tu sitio web](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/como-instalar-y-configurar-el-web-chat-de-vambe-en-tu-sitio-web).

***

### En resumen

El botón flotante de WhatsApp es una forma liviana de conectar tu sitio a una conversación de WhatsApp, con dos variantes: **Botón directo**, que lleva de inmediato a WhatsApp, y **Chat emergente**, que abre primero una ventana dentro de tu página para que el visitante escriba su mensaje antes de saltar. Se genera desde **Canales → tu canal de WhatsApp → los tres puntos → Generar script**, y se instala pegando el código en el `<head>` de tu sitio —en Shopify, dentro de **Tienda online → Ver código → theme.liquid**.
