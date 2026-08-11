# Cómo obtener las credenciales de DentalSoft

En esta guía aprenderás cómo generar las credenciales API desde DentalSoft y cómo ingresarlas en Vambe para habilitar la integración.

Estas credenciales permiten que Vambe se comunique con tu sistema clínico para consultar especialidades, profesionales y disponibilidad, además de crear y gestionar citas directamente desde tu asistente de IA.

#### Requisitos previos

* Tener una cuenta activa en **DentalSoft**.
* Iniciar sesión con un **usuario administrador**.
* Tener habilitada la sección **Configuración API** dentro de tu cuenta de DentalSoft.

{% hint style="warning" %}
La sección **Configuración API** no viene habilitada en todas las cuentas de DentalSoft. Si no la encuentras, escríbenos a tu contacto en Vambe: nosotros nos comunicamos directamente con DentalSoft para solicitar que la habiliten en tu cuenta.
{% endhint %}

{% stepper %}
{% step %}
#### Paso 1: Acceder a la configuración de API en DentalSoft

* Ingresa a DentalSoft con un **usuario con permisos de administrador**.
* En el menú lateral izquierdo, entra a **Administración**.
* Selecciona **Configuración API**.

Esta es la sección donde se generan y administran las credenciales que permiten conectar sistemas externos a tu clínica.
{% endstep %}

{% step %}
#### Paso 2: Crear una nueva credencial

* En la esquina superior derecha de la página, haz clic en **Nuevo**.
* En el campo **Descripción**, escribe: **Vambe**
* Haz clic en **Grabar**.

La descripción es solo una referencia interna para que sepas a qué uso corresponde cada credencial. Al grabar, DentalSoft genera automáticamente un **Client Id** y un **Client Secret** asociados a esa credencial.
{% endstep %}

{% step %}
#### Paso 3: Copiar el Client Id y el Client Secret

* En la tabla **Credenciales API**, dentro de la pestaña **Habilitados**, ubica la credencial que acabas de crear.
* Copia el valor de la columna **Client Id**.
* Copia el valor de la columna **Client Secret**.

{% hint style="info" %}
Si en algún momento necesitas revocar el acceso, puedes deshabilitar la credencial desde esta misma tabla sin afectar el resto de tu cuenta.
{% endhint %}
{% endstep %}

{% step %}
#### Paso 4: Obtener el RUT de la clínica

Además del Client Id y el Client Secret, necesitarás el **RUT de la clínica**. Lo encuentras en la misma página de **Configuración API**, dentro del recuadro de instrucciones que aparece en la parte superior.

Cópialo tal como se indica ahí: **sin puntos, sin guion y sin dígito verificador**. Por ejemplo, para el RUT 76.847.262-K debes ingresar `76847262`.
{% endstep %}

{% step %}
#### Paso 5: Conectar DentalSoft en Vambe

Con las tres credenciales a mano, ya puedes habilitar la integración:

* Ingresa a Vambe.
* Dirígete a la **parte inferior izquierda** y haz clic en **Ajustes**.
* Accede al submenú **Integraciones**.
* En el catálogo, selecciona la tarjeta de **DentalSoft**.
* Haz clic en **Conectar**.
* Completa los tres campos:
  * **Client ID**
  * **Client Secret**
  * **RUT de la Clínica**
* Haz clic en **Siguiente**.

Si las credenciales son correctas, Vambe confirmará que fueron guardadas y la integración quedará activa.
{% endstep %}
{% endstepper %}

#### Resultado final

Una vez completados estos pasos:

* Las credenciales de DentalSoft quedan configuradas en Vambe.
* La integración queda habilitada y disponible para tus asistentes.
* Vambe podrá consultar especialidades, profesionales y disponibilidad, y crear citas según la configuración de tu asistente y de tu embudo.

{% hint style="warning" %}
Errores comunes a evitar:

* Ingresar a DentalSoft con un usuario que no es administrador.
* Copiar el Client Id o el Client Secret de forma incompleta o con espacios adicionales.
* Ingresar el RUT con puntos, guion o dígito verificador.
* Compartir estas credenciales por canales no seguros: con ellas se puede acceder a la información de la clínica.
{% endhint %}

#### Qué información sincroniza Vambe desde DentalSoft

Al conectar la integración, Vambe lee la configuración de tu cuenta de DentalSoft y la replica dentro de Vambe: sucursales, tratamientos, profesionales y la relación entre ellos. Conocer los criterios que se aplican en cada caso te permitirá revisar tu información en DentalSoft antes de conectar y corregir cualquier dato que no se refleje como esperas.

**Sucursales**

Se traen todas las sucursales del listado de la clínica, sin filtros ni condiciones adicionales.

**Tratamientos**

Los tratamientos en Vambe corresponden a las especialidades de DentalSoft. Se sincroniza toda especialidad que se encuentre activa; las inactivas se omiten.

El nombre del tratamiento en Vambe es el nombre de la especialidad, y su descripción corresponde a la abreviación de esa misma especialidad.

La duración no proviene de DentalSoft: se configura directamente en Vambe y se expresa en bloques. El largo del bloque —5 o 15 minutos, según la clínica— se lee desde tu cuenta de DentalSoft al momento de conectar las credenciales.

**Profesionales**

Un profesional queda asociado a una sucursal solo si su usuario en DentalSoft cumple con **todas** las condiciones siguientes:

* Su **tipo de profesional** es **Usuario con agenda**. Ningún otro tipo se sincroniza.
* El **usuario está activo**.
* Tiene un **usuario (login) asignado**. Un profesional sin usuario asociado se descarta.
* Está **asignado a esa sucursal** en su ficha de usuario.

Si un profesional no aparece en Vambe, revisa estos cuatro puntos en su ficha de DentalSoft: basta con que uno no se cumpla para que quede fuera de la sincronización.

**Asociación entre profesionales y tratamientos**

La relación entre profesionales y tratamientos se construye a partir de las especialidades asignadas a cada usuario: el profesional queda disponible bajo cada especialidad que tenga registrada en su ficha.

{% hint style="warning" %}
Un profesional que no tenga **ninguna** especialidad asignada en DentalSoft queda asociado a **todos** los tratamientos de su sucursal. Si observas que un profesional aparece disponible para todos los tratamientos, revisa su ficha de usuario en DentalSoft y asígnale las especialidades que corresponda.
{% endhint %}

<details>

<summary>¿Te ha sido útil este artículo?</summary>

Sí No

</details>
