---
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Cómo obtener las credenciales de Dentalink o Medilink

En esta guía aprenderás cómo obtener las credenciales (token API) desde Dentalink o Medilink y cómo ingresarlas correctamente en Vambe para habilitar la integración.

Estas credenciales permiten que Vambe se comunique con el sistema clínico para consultar información como profesionales, tratamientos, disponibilidad y agendamientos.

#### Requisitos previos

* Tener una cuenta activa en **Dentalink o Medilink**.
* Iniciar sesión con un **usuario administrador**.

{% hint style="warning" %}
Importante: si ingresas con un usuario que no es administrador, no podrás ver ni crear credenciales API.
{% endhint %}

{% stepper %}
{% step %}
### Paso 1: Ingresar a Dentalink o Medilink como administrador

* Accede a tu cuenta de Dentalink o Medilink.
* Inicia sesión utilizando un **usuario con permisos de administrador**.
* Verifica que tienes acceso a las configuraciones avanzadas del sistema.
{% endstep %}

{% step %}
### Paso 2: Acceder a la configuración de API

* Dirígete a la **parte superior derecha**.

![](<../.gitbook/assets/image png Dec 17 2025 02 34 12 9522 PM.png>)

* Haz clic en **Administrador**.
* Selecciona la opción **Configuración API**.

![](<../.gitbook/assets/Captura de pantalla 2025 12 17 a la(s) 11 23 59 a m  png.png>)

Esta sección es donde se gestionan las aplicaciones externas que pueden conectarse al sistema.
{% endstep %}

{% step %}
### Paso 3: Crear un nuevo cliente API

* Dentro de Configuración API, haz clic en **Agregar cliente**.

![](<../.gitbook/assets/image png Dec 17 2025 02 35 30 5601 PM.png>)

* En el campo **Nombre de la aplicación**, escribe: **Vambe**

![](<../.gitbook/assets/image png Dec 17 2025 02 36 10 0963 PM.png>)

* Haz clic en **Crear**.

El sistema registrará a Vambe como una aplicación autorizada.
{% endstep %}

{% step %}
### Paso 4: Obtener el token de acceso

* En el listado de clientes API, busca el cliente llamado **Vambe**.

![](<../.gitbook/assets/image png Dec 17 2025 02 38 17 6603 PM.png>)

* En la misma fila, haz clic en **Ver token**.
* Copia el token que se muestra.

![](<../.gitbook/assets/image png Dec 17 2025 02 39 35 3602 PM.png>)

Este token es la credencial que permitirá a Vambe conectarse con Dentalink o Medilink.
{% endstep %}

{% step %}
### Paso 5: Ingresar el token en Vambe

* Ingresa a Vambe.
* Dirígete a la **parte inferior izquierda** y haz clic en **Ajustes**.
* Accede al submenú **Integraciones**.
* Selecciona **Dentalink** o **Medilink**, según corresponda.

![](<../.gitbook/assets/image png Dec 17 2025 02 41 11 4473 PM.png>)

* Haz clic en **Conectar**.

![](<../.gitbook/assets/image png Dec 17 2025 02 41 35 7553 PM.png>)

* Pega el **token API** que copiaste previamente.

![](<../.gitbook/assets/image png Dec 17 2025 02 42 00 1557 PM.png>)

* Confirma la acción.

Si el token es correcto, Vambe mostrará un mensaje indicando que las credenciales fueron guardadas exitosamente.
{% endstep %}
{% endstepper %}

#### Resultado final

Una vez completados estos pasos:

* Las credenciales quedan correctamente configuradas en Vambe.
* La integración con Dentalink o Medilink queda habilitada.
* Vambe podrá utilizar la información clínica según la configuración del asistente y del embudo.

{% hint style="warning" %}
Errores comunes a evitar:

* Ingresar con un usuario que no es administrador en Dentalink o Medilink.
* Copiar incorrectamente el token (espacios adicionales o incompleto).
* Pegar el token en una integración incorrecta dentro de Vambe.
{% endhint %}

<details>

<summary>¿Te ha sido útil este artículo?</summary>

Sí No

</details>
