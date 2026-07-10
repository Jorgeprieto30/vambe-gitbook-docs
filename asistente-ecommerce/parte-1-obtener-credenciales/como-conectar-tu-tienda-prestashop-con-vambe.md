# Cómo conectar tu tienda PrestaShop con Vambe

## Cómo conectar tu tienda PrestaShop con Vambe

En este artículo aprenderás cómo conectar tu tienda **PrestaShop** con **Vambe**, lo que permitirá a la inteligencia artificial acceder a la información de tu catálogo y gestionar conversaciones relacionadas con productos, precios y stock.

{% hint style="info" %}
Requisitos previos

* Acceso de **superadmin** a PrestaShop.
* Acceso a **Vambe**.
* El **plugin de integración Vambe** (archivo `.zip`). Solícitalo al equipo de integraciones.
{% endhint %}

El proceso tiene 3 partes: (1) crear la API Key en PrestaShop, (2) conectar desde Vambe usando esa clave, y (3) instalar el plugin en PrestaShop.

{% stepper %}
{% step %}
**Crear la API Key en PrestaShop**

1. Inicia sesión en el panel de administración de PrestaShop.
2. Ve a **Parámetros Avanzados → Webservice**.
3. Verifica que los dos switches estén activados (en verde):
   * **Activar el servicio Web**
   * **Activar modo CGI para PHP**

{% hint style="warning" %}
Si alguno de los dos switches está apagado, actívalo y guarda antes de continuar.
{% endhint %}

4. Haz clic en el botón **Añadir una nueva clave webservice** (esquina superior derecha).
5. Completa los campos:
   * **Descripción de la clave** → escribe "Integración Vambe".
   * **Clave** → presiona el botón **Generar** (esto crea la clave automáticamente). Cópiala y guárdala, la necesitarás en el Paso 2.
   * **Habilitar clave de servicio** → activado (switch en verde).
6. En la sección **Permisos**, activa los recursos necesarios para que Vambe pueda leer tu catálogo (productos, categorías, combinaciones, stock, precios).
7. Haz clic en **Guardar**.

{% hint style="info" %}
La clave generada es la que irá en el campo **Access Key** del formulario de Vambe. Guárdala en un lugar seguro antes de cerrar la pantalla.
{% endhint %}
{% endstep %}

{% step %}
**Conectar desde Vambe**

1. En Vambe, ve a **Integraciones → PrestaShop** y haz clic en **Conectar**.
2. En el formulario que se abre, completa los campos:
   * **Nombre** → nombre identificador de la API Key (ej: "Prestashop HDpro").
   * **Access Key** → pega la clave que copiaste en el Paso 1.
   * **Link de la Tienda** → URL completa de tu tienda incluyendo la barra al final (ej: `https://hdpro.cl/`).
   * **Use Category** → actívalo si quieres que Vambe traiga las categorías de producto.
   * **Use Combinations** → actívalo si el catálogo tiene variantes (tallas, colores, etc.).
3. Haz clic en **Conectar**.
{% endstep %}

{% step %}
**Instalar el plugin en PrestaShop**

Este paso es obligatorio para que la integración funcione correctamente. El plugin lo provee el equipo de integraciones de Vambe.

1. Solicita el archivo `.zip` del plugin al equipo de integraciones.
2. En PrestaShop, ve a **Módulos → Gestor de módulos**.
3. Haz clic en **Subir un módulo** (esquina superior).
4. Selecciona el archivo `.zip` recibido y espera a que se instale.

{% hint style="info" %}
Una vez instalado el plugin, la integración queda activa y Vambe comenzará a sincronizar el catálogo.
{% endhint %}
{% endstep %}

{% step %}
**Verificar la conexión**

1. En Vambe, dirígete al **catálogo de productos**.
2. Verifica que los productos de PrestaShop estén apareciendo correctamente con precios, stock y categorías.

✅ Si el catálogo aparece sincronizado, tu tienda PrestaShop ya está correctamente conectada a Vambe.

Si algo no aparece, revisa que los permisos del Paso 1 estén correctamente guardados y que el plugin esté activo.
{% endstep %}
{% endstepper %}

### ¿Qué sigue?

Una vez conectada tu tienda PrestaShop, podrás:

* Utilizar la inteligencia artificial para responder consultas sobre productos, precios y stock.
* Gestionar conversaciones relacionadas con tu catálogo.
* Automatizar flujos de atención y venta.
