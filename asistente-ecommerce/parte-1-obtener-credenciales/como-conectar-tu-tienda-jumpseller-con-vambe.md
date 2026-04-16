---
description: >-
  Sincroniza tu catálogo. Aprende a conectar Jumpseller para que la IA consulte
  stock, envíe fotos y genere links de compra automáticos.
---

# Cómo conectar tu tienda Jumpseller con Vambe

En este artículo aprenderás cómo conectar tu tienda Jumpseller con Vambe, lo que permitirá a la inteligencia artificial acceder a la información de tu tienda en tiempo real.

¿Qué permite esta integración actualmente?

* **Consultar Stock**: La IA sabrá si tienes productos disponibles.
* **Enviar Fotos**: Mostrará imágenes del producto en el chat.
* **Links de Compra**: La IA generará y enviará automáticamente el enlace directo para que el cliente pague.

{% hint style="success" %}
🚀 **Próximamente**: Estamos trabajando para habilitar la recuperación de carritos abandonados directamente desde Vambe.
{% endhint %}

#### Requisitos previos

* Tener una tienda Jumpseller operativa.
* Tener acceso a la cuenta de "Dueño" o Administrador en Jumpseller para ver las credenciales API.

***

#### 1. Obtener credenciales en Jumpseller

Para conectar ambas plataformas, primero necesitamos obtener tu "Login" y "Auth Token" desde Jumpseller:

1. Ingresa a tu panel de administración en **Jumpseller**.
2. En el menú lateral izquierdo, ve a la sección **Cuenta** y selecciona **Preferencias**.
3. Haz clic sobre **tu cuenta** (debe ser la cuenta con etiqueta de "Dueño" o permisos de administración).

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

4. Al entrar en el detalle de la cuenta, verás un panel al lado derecho titulado API.
5. Allí encontrarás los campos Login y Auth Token.
6. Copia ambos valores, los necesitarás en el siguiente paso.

<figure><img src="../.gitbook/assets/image (12).png" alt="" width="375"><figcaption></figcaption></figure>

***

#### 3. Configurar la conexión

1. Dentro de la tarjeta de Jumpseller, haz clic en el botón azul Conectar.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

2. Se abrirá una ventana emergente solicitando los datos que obtuvimos en el paso 1:
   * Login API: Pega el código de "Login" de Jumpseller.
   * Auth Token: Pega el "Auth Token" de Jumpseller.
   * URL de la tienda: Ingresa la dirección web completa de tu tienda (ej: `https://tutienda.jumpseller.com` o `https://mitienda.com`).
3. Haz clic en Siguiente para finalizar.

<figure><img src="../.gitbook/assets/image (14).png" alt="" width="292"><figcaption></figcaption></figure>

***

#### 4. Verificar la conexión

Para confirmar que todo está funcionando correctamente:

1. Ve al menú lateral izquierdo de Vambe y haz clic en Ecommerce.
2. Si la conexión fue exitosa, verás aparecer automáticamente el listado de tus productos importados desde Jumpseller.
3. ✅ Si ves tus productos con sus fotos y stock, la integración está lista.

