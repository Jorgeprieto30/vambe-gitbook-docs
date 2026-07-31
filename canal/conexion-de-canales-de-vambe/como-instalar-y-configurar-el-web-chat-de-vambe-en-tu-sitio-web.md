---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo instalar y configurar el Web Chat de Vambe en tu sitio web

El Web Chat de Vambe te permite integrar un chat flotante directamente en tu página web, conectando automáticamente a los visitantes con un embudo específico dentro de Vambe.

Cada conversación iniciada desde el Web Chat entra directamente a tu embudo, permitiéndote gestionar leads, conversaciones y tickets desde un solo lugar. Además, ahora cuentas con un editor completo que incluye un panel de previsualización en vivo, donde verás reflejado cada cambio mientras configuras el chat.

**Ventajas clave:**

* Solicitar datos del cliente antes de iniciar la conversación (correo, teléfono, nombre).
* Conectar el chat a un embudo específico.
* Personalizar completamente la apariencia, las secciones y el comportamiento del chat.
* Agregar pestañas (tabs) adicionales con enlaces, recursos y accesos directos.
* Autenticar usuarios de forma segura mediante JWT.

**Crear el canal de Web Chat**

1. Ve al menú lateral izquierdo y entra a la sección de **Canales**.
2. Haz clic en **Agregar canal**.
3.  Selecciona **Web Chat** y luego haz clic en **Conectar**.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FYtuGnztUQmnDtKjRl8qy%2Fimage.png?alt=media&#x26;token=ee02d6c9-ef2e-48b1-af52-f44a2cfff4e3" alt=""><figcaption></figcaption></figure>

Se abrirá la vista de configuración (**Configurando Webchat**), donde podrás personalizar todo el comportamiento y la apariencia del chat. A la derecha verás siempre el panel **Previsualiza los cambios**, que refleja en vivo cada ajuste que realices.

**Configuración principal**

**Nombre del canal y embudo**

* **Nombre del canal** — El nombre interno con el que identificarás este Web Chat (por ejemplo: Vambe web).
* **Embudo** — Selecciona el embudo donde llegarán todos los tickets generados por este canal. Cada contacto que inicie una conversación creará un ticket automáticamente e ingresará a la etapa correspondiente del embudo.

**Información del asistente**

* **Nombre asistente IA** — Nombre que verá el cliente en la parte superior del Web Chat.
* **Idioma** — Selecciona el idioma del Web Chat.
* **URL del icono** — URL pública de la imagen que se mostrará como avatar del asistente. Debe enlazar directamente a la imagen.

**Solicitud de datos antes de abrir el chat**

Puedes pedir información al cliente antes de que se abra la conversación:

* **Solicitar Email**
* **Solicitar teléfono**
* **Solicitar nombre**

Si activas una o más de estas opciones, el cliente deberá completar esos datos antes de poder abrir el Web Chat e iniciar la conversación.

**Apariencia**

* **Colores** — Define el color primario y secundario del botón y del chat.
* **Tema** — Elige cómo se verá el chat entre **Modo claro** y **Modo oscuro**.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FlCLXC7QjHdiR18PRTLGj%2Fimage.png?alt=media&#x26;token=b2fb7e48-eb9e-41d2-a4e4-d6a22e1c481f" alt=""><figcaption></figcaption></figure>

**Opciones avanzadas**

Despliega la sección **Avanzado** para acceder a configuraciones adicionales de posición, fuente, restricciones y autenticación.

**Posición del botón**

* **Posición X del botón** — Distancia en px del botón al borde lateral.
* **Posición Y del botón** — Distancia en px del botón al borde inferior.

**Fuente**

* **Fuente** — Font-family CSS del webchat. Si lo dejas vacío usa la fuente de tu sitio. Útil cuando tu sitio no define una fuente y se filtra la del navegador (Times).

**Restricciones y seguimiento**

* **Restringir por origen** — El webchat solo funcionará en el dominio que ingreses. Al activarlo, aparecerá el campo **Dominio permitido**.
* **URL de seguimiento** — Registra la URL de la página donde está embebido el webchat.
* **Mostrar último ticket cerrado** — Al abrir el webchat, muestra el último ticket cerrado del contacto cuando no tiene uno activo.
* **Mostrar tiempo de respuesta** — Muestra al visitante el tiempo estimado de primera respuesta según tu SLA.

<details>

<summary><strong>Autenticar usuarios con JWT (configuración técnica)</strong></summary>

{% hint style="info" %}
**Nota:** Esta sección es más técnica y está pensada para clientes con un equipo de desarrollo. Si no necesitas validar la identidad de tus usuarios, puedes omitirla.
{% endhint %}

Por defecto, el Web Chat puede identificar a un usuario mediante un `externalUserId` enviado en el script. Sin embargo, exponer ese ID directamente en el script puede representar un riesgo de seguridad, ya que cualquiera podría manipularlo.

Para resolver esto, la opción **Autenticar usuarios con JWT** permite que, en lugar de enviar el `externalUserId` en texto plano, tu sitio envíe un **token firmado**. Vambe valida ese token con un secret compartido y confirma que la identidad del usuario es legítima.

**Cómo funciona:**

1. Activa la opción **Autenticar usuarios con JWT**.
2. **JWT Secret** — Configura aquí un secret (una clave). Este mismo secret debe usarse en tu sitio para firmar el token de autenticación.
3. Tu sitio firma el token con ese secret y lo envía a Vambe en lugar del `externalUserId`.
4. Cuando el token llega a Vambe, validamos que la firma corresponda al secret configurado. Si la firma es válida, el usuario se autentica y se carga el Web Chat. Si el token está firmado con un secret distinto, la validación falla y la sesión no se carga.

**Campo del ID de usuario en el token**

Define el nombre del campo dentro del token firmado donde se encuentra el ID de usuario. Esto es configurable porque depende de cómo esté estructurada la información en el token desde tu sitio (podría venir como `sub`, `userId`, etc.).

Por ejemplo, si tu token tiene esta estructura, deberías ingresar `sub`:

json

```json
{
  "sub": "user-123",
  "name": "Ada Lovelace",
  "iat": 1716239022
}
```

En este caso, el ID de usuario (`user-123`) viene en el campo `sub`.

</details>

**Secciones del Web Chat**

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2Fy8iBaF2GJVBlf1PMw6nX%2Fimage.png?alt=media&#x26;token=3735a25f-4b3b-461a-aec0-38a556f1ff5a" alt=""><figcaption></figcaption></figure>

Las **Secciones** son las pestañas (tabs) que verá el cliente en la parte inferior del Web Chat. Puedes agregar **hasta cuatro tabs**. La pestaña de **Chat** viene por defecto; si dejas solo esa, el webchat se muestra directamente con la vista de conversación.

Además de Chat, puedes crear tabs personalizadas para mostrar distintos recursos, enlaces y accesos según lo que necesites (por ejemplo, una de conocimiento, una de soporte, etc.). Las tabs y los bloques se pueden reordenar arrastrándolos.

Por cada sección puedes configurar:

* **Etiqueta** — Nombre de la pestaña.
* **Ícono** — Ícono que la representa.
* **Título** y **Subtítulo** — Textos de encabezado de la sección.
* **Bloques** — Los elementos que aparecen en el cuerpo de la sección.

**Tipos de bloques**

Dentro de cada sección puedes agregar distintos bloques para armar el contenido:

* **Texto** — Un bloque de texto simple (por ejemplo, un título de grupo como "Recursos").
* **Link** — Un enlace a una URL externa, con su propio ícono.
* **Acceso rápido** — Un acceso directo que lleva a otra tab del Web Chat.
* **Chat CTA** — Un acceso directo a la vista de chat.
* **Buscador de artículos** — Un buscador que permite encontrar artículos.
* **Artículos sugeridos** — Muestra artículos sugeridos. Hoy funcionan como enlaces (se configuran con una URL); a futuro podrán visualizarse dentro del mismo Web Chat sin redirigir a una página externa.

Cada bloque permite elegir su ícono, ocupar el ancho completo y ajustar su orden. El panel de previsualización refleja en vivo cómo se verá cada bloque.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FK36kFHgwuakAnRTBdhap%2Fimage.png?alt=media&#x26;token=406d8507-ff2d-4df1-abef-0e14ca9d9c4d" alt=""><figcaption></figcaption></figure>

**Generar e insertar el script en tu sitio web**

Una vez configurado el Web Chat, ve a la vista de **Conectar** para obtener el script de instalación.

1. Copia el script que aparece en esa vista.
2. Pégalo en el código de tu sitio web, idealmente antes del cierre de la etiqueta `<body>` o según lo indique tu CMS.
3. Publica los cambios en tu sitio.

Con el nuevo formato, el script solo necesita el **Client ID** y el **Channel ID**; el resto de la configuración (colores, secciones, textos, etc.) se trae automáticamente desde Vambe.

> **Importante:** Cualquier valor que escribas manualmente en el script sobrescribirá la configuración guardada en Vambe. Por ejemplo, si defines colores en el script, esos colores tendrán prioridad sobre los configurados en el editor.

**Verificar la conexión con el embudo**

Antes de terminar, asegúrate de que el Web Chat esté conectado al embudo correcto dentro de Vambe. Esto garantiza que cada contacto que inicie una conversación:

* Cree un ticket automáticamente.
* Ingrese a la etapa correcta del embudo.
* Sea gestionado correctamente por IA o por Ejecutivos.

Una vez verificado, haz clic en **Crear** para dejar el canal activo.

Más información: [Verificar la conexión con un embudo](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/verificar-que-el-numero-este-asociado-al-embudo-correcto)
