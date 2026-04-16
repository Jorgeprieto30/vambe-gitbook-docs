# ¿Cómo enviar archivos específicos desde una carpeta de Google Drive?

La función **Drive File Transformer** es ideal cuando tienes una carpeta con muchos archivos (por ejemplo: fotos de productos, boletas, fichas técnicas) y necesitas que la IA **elija uno específico** para enviárselo al cliente.

**Diferencia con "Enviar Documento o Imagen":**

* **Enviar Documento:** Envía siempre el _mismo_ archivo fijo.
* **Drive File Transformer:** La IA mira dentro de una carpeta y decide qué archivo enviar según lo que pida el cliente (Ej: "Mándame la foto de la zapatilla roja" -> La IA busca `zapatilla_roja.jpg` y la envía).

***

#### ⚠️ Requisito Obligatorio: Permisos Públicos

Para que esto funcione, la carpeta de Google Drive debe ser accesible.

1. Ve a tu Google Drive y haz clic derecho en la carpeta.
2. Selecciona **Compartir > Acceso general.**
3. Cambia la opción a **"Cualquier persona con el enlace"** (Anyone with the link).

{% hint style="danger" %}
Si la carpeta está privada, la IA no podrá entrar a buscar el archivo.
{% endhint %}

***

#### Configuración Paso a Paso

Sigue estos pasos para conectar tu carpeta con el chat:

**Paso 1: Ingresar al Asistente**

1. Ve al menú [**Asistente**](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md).
2. Entra a **Pasos a Seguir o Casos Posibles.**

**Paso 2: La Instrucción (El Gatillo)**

Debes decirle a la IA qué buscar dentro de la carpeta.

* _Fórmula:_ `Cuando [el cliente pida X], ejecuta la función [Nombre] y envíale el archivo llamado [Nombre del archivo]`.

> **Ejemplo Real:** "Cuando el cliente me entregue su RUT, ejecuta la función drive file y envíale la foto 'cover concepts'".

**Paso 3: Crear la Función**

Haz clic en **+ Agregar Función** y busca **Drive File Transformer.**

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

Configura los campos:

1. **URL de la carpeta:** Pega el enlace de la carpeta de Google Drive (recuerda que debe ser el link de la _carpeta_, no de un archivo suelto).

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
**IMPORTANTE: La ia no sabe que hay en la foto, solo sabe el nombre**
{% endhint %}

**¿Como deberia verse la carpeta de drive?**

-Nombres descriptivos

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

\
**Paso 4: Verificación Visual**

Asegúrate de ver la tarjeta de la función creada debajo de tu texto.

<figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

***

#### 💡 Tips para que funcione perfecto

1. **Nombres Claros:** Asegúrate de que los archivos dentro de tu Drive tengan nombres fáciles de identificar para la IA (Ej: es mejor `precio_plan_basico.pdf` que `IMG_2024_scan.pdf`).
2. **Sin Subcarpetas:** Esta función solo mira los archivos que están "sueltos" en la carpeta principal. Si tienes carpetas dentro de carpetas, la IA no entrará a buscar ahí.
3. **Instrucción Precisa:** Si tienes 10 fotos, dile a la IA explícitamente cuál enviar en el texto del paso (Paso 2). Si no se lo dices, la IA podría adivinar o no enviar nada.
