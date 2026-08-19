---
description: >-
  Antes de conectar Odoo CRM en Vambe necesitas cuatro datos desde tu cuenta de
  Odoo: la URL, el nombre de la base de datos, tu usuario y una Llave de API.
  Aquí te explicamos paso a paso cómo obtener ca
---

# Cómo obtener las credenciales de Odoo CRM

Para conectar Odoo CRM con Vambe necesitas cuatro datos: la **URL** de tu instancia, el **nombre de tu base de datos**, tu **nombre de usuario** y una **Llave de API**. Estos datos se obtienen directamente desde tu cuenta de Odoo, y son distintos entre sí: en particular, la Llave de API **no es la contraseña** con la que inicias sesión en Odoo, aunque son fáciles de confundir.

{% hint style="warning" %}
El error más común al conectar esta integración es ingresar la contraseña del usuario en el campo de la Llave de API. Son credenciales distintas: la contraseña abre tu sesión en Odoo, la Llave de API es la que usa Vambe para conectarse de forma segura sin tocar tu contraseña.
{% endhint %}

***

### Requisitos previos

* Acceso de administrador a tu instancia de Odoo.
* Saber la URL con la que entras a tu cuenta de Odoo (por ejemplo, `https://tuempresa.odoo.com`).

***

### Genera tu Llave de API en Odoo

La Llave de API se genera desde tus preferencias de usuario en Odoo, no desde ningún panel de administración general.

1. En Odoo, haz clic en tu perfil (arriba a la derecha) y selecciona **Preferencias**.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

2. En la ventana **Cambiar mis preferencias**, ve a la pestaña **Seguridad de la cuenta**.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

3. Baja hasta la sección **Claves API** y haz clic en **Nueva clave API**.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

4. Odoo te pedirá tu contraseña para confirmar tu identidad antes de generar la nueva llave.
5. Copia la Llave de API que Odoo genera y guárdala en un lugar seguro. Es el valor que vas a pegar en Vambe.

{% hint style="info" %}
Odoo solo muestra la llave completa una vez, al momento de generarla. Si la pierdes, deberás generar una nueva.
{% endhint %}

***

### Obtén el nombre de tu base de datos

El nombre de tu base de datos solo es visible con el modo desarrollador activo.

1.  En Odoo, ve a **Ajustes → Mi Base de datos**.<br>

    <figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>
2. Baja hasta **Herramientas de desarrollador** y haz clic en **Activar modo de desarrollador**.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

3. Con el modo desarrollador activo, el nombre de tu base de datos aparece justo debajo de tu nombre de usuario, en la esquina superior derecha.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

> También puedes confirmar el nombre de tu base de datos desde **Mis bases de datos** en tu cuenta de Odoo.com.&#x20;

***

### Copia la URL de tu instancia

La URL es la misma dirección que usas para entrar a Odoo desde el navegador, por ejemplo `https://tuempresa.odoo.com`. La encuentras en la barra de direcciones mientras estás dentro de tu cuenta.

***

### Encuentra tu nombre de usuario

Tu nombre de usuario en Odoo corresponde al correo electrónico con el que inicias sesión.

1. Ve a **Ajustes → Usuarios y empresas → Usuarios**.
2. En la columna **Usuario**, verás tu correo electrónico. Ese es el valor que debes usar.

***

### Conecta estas credenciales en Vambe

Con los cuatro datos listos, vuelve a Vambe para completar la conexión.

1. En Vambe, ve a **Ajustes → Integraciones → CRM** y selecciona **Odoo**.
2. Haz clic en **Conectar** y completa el formulario con la **URL**, la **Base de datos**, el **Username** y la **Llave API** que obtuviste.

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

3. Haz clic en **Save** para finalizar la conexión.

***

### En resumen

Conectar Odoo CRM con Vambe depende de reunir cuatro datos desde tu cuenta de Odoo: la URL de tu instancia, el nombre de tu base de datos, tu nombre de usuario y una Llave de API generada específicamente para esta integración. Mantener la Llave de API separada de tu contraseña es lo que evita que la conexión falle y protege el acceso a tu cuenta.
