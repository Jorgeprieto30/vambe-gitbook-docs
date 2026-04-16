---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo instalar y configurar el Web Chat de Vambe en tu sitio web

El **Web Chat de Vambe** te permite integrar un chat directo en tu página web, conectando automáticamente a los visitantes con un embudo específico dentro de Vambe.

Cada conversación iniciada desde el Web Chat entra directamente a tu embudo, permitiéndote gestionar leads, conversaciones y tickets desde un solo lugar.

Ventajas clave:

* Solicitar datos del cliente antes de iniciar la conversación (correo, teléfono, nombre).
* Conectar el chat a un embudo específico.
* Personalizar completamente la apariencia y comportamiento del chat.
* Facilitar el contacto incluso cuando el cliente aún no escribe manualmente.

{% stepper %}
{% step %}
### Crear el canal de Web Chat

* Ve al menú lateral izquierdo.
* [Ingresa a Canales](https://academy.vambe.ai/v1/docs/c%C3%B3mo-ingresar-a-la-secci%C3%B3n-de-conexi%C3%B3n-de-canales).
* Haz clic en **Web Chat**.

![](../.gitbook/assets/image\(100\).png)

* Crea un nuevo Web Chat asignándole un nombre (por ejemplo: _Página web_).
* Opcionalmente, conéctalo a un canal si lo deseas.
* Haz clic en **Finish**.

Una vez creado, el Web Chat aparecerá en el listado de canales.

![](../.gitbook/assets/image\(101\).png)
{% endstep %}

{% step %}
### Generar el script de instalación

* En el listado de Web Chat, haz clic en los **tres puntos** del Web Chat creado.
* Selecciona **Generate script**.

Este script es el código que deberás insertar en tu página web, en el lugar donde quieras que aparezca el botón del chat.

![](../.gitbook/assets/image\(102\).png)
{% endstep %}

{% step %}
### Configurar el Web Chat

Debajo del script encontrarás todas las opciones de personalización. A continuación, se describen cada una.

![](../.gitbook/assets/image\(103\).png)

#### Información del agente

* **Agent name** — Nombre que verá el cliente como agente del chat.
* **Agent avatar URL** — URL de la imagen del agente que se mostrará en la esquina superior del chat.

{% hint style="warning" %}
La URL del avatar debe ser pública y enlazar directamente a la imagen.
{% endhint %}

#### Solicitud de datos antes de abrir el chat

Puedes pedir información al cliente **antes de que se abra la conversación**:

* **Ask for phone number**
* **Ask for email**
* **Ask for name**

Si activas alguna de estas opciones, el cliente deberá ingresar esos datos antes de iniciar el chat.

#### Apariencia del Web Chat

* **Dark mode** — Activa el tema oscuro.
* **Primary color / Secondary color** — Define los colores del botón y del chat.

En la parte inferior derecha verás una **vista previa en tiempo real** del Web Chat.

#### Idioma y textos

* **Language** — Selecciona el idioma del Web Chat.
* **Chat with us text** — Texto que aparecerá junto al botón para invitar al cliente a iniciar la conversación (ejemplo: _¿Hablamos?_ o _Chatea con nosotros_).

#### Posición del botón

* **Position X**
* **Position Y**

Permite ajustar la ubicación exacta del botón dentro de tu página web.

#### Restricciones por dominio (opcional)

* **Restrict by origin** — Permite definir desde qué URL puede cargarse el Web Chat.
* **Enable URL tracking** — Activa el seguimiento del origen del contacto.

#### Preguntas sugeridas

Las **Suggested questions** permiten mostrar botones con mensajes predefinidos para que el cliente los envíe con un solo clic.\
Ejemplos:

* “Quiero agendar una hora”
* “Necesito información de precios”
* “Hablar con un ejecutivo”
{% endstep %}

{% step %}
### Insertar el script en tu sitio web

1. Copia el **script** que aparece en la parte superior.
2. Pégalo en el código de tu sitio web, idealmente antes del cierre de la etiqueta `<body>` o según lo indique tu CMS.
3. Publica los cambios en tu sitio.
{% endstep %}

{% step %}
### Verificar la conexión con un embudo

Asegúrate de que el Web Chat esté **conectado a un embudo** dentro de Vambe:

* Esto garantiza que cada contacto que inicie conversación cree un ticket automáticamente, ingrese a la etapa correcta del embudo y sea gestionado correctamente por IA o agentes humanos.

Más información: [Verificar la conexión con un embudo](https://academy.vambe.ai/v1/docs/verificar-que-el-n%C3%BAmero-est%C3%A9-asociado-al-embudo-correcto)
{% endstep %}
{% endstepper %}
