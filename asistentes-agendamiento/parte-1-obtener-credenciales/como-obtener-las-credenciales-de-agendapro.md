---
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Cómo obtener las credenciales de AgendaPro

En esta guía aprenderás cómo obtener las credenciales de AgendaPro y utilizarlas para conectar tu cuenta con Vambe, permitiendo la integración correcta entre ambas plataformas.

### Requisitos previos

Antes de comenzar, asegúrate de:

* Tener acceso a una cuenta activa de **AgendaPro**
* Contar con plan **Pro**

{% stepper %}
{% step %}
### Ingresar a AgendaPro

* Inicia sesión en tu cuenta de **AgendaPro**.
* En la esquina superior derecha, haz clic en **Configuraciones**.
* Dentro del menú, vuelve a hacer clic en **Configuraciones**.

![](<../.gitbook/assets/image png Dec 17 2025 03 03 44 6474 PM.png>)
{% endstep %}

{% step %}
### Acceder a las opciones avanzadas

1. En el menú lateral izquierdo, selecciona **Opciones avanzadas**.

![](<../.gitbook/assets/image png Dec 17 2025 03 05 08 3059 PM.png>)

2. Dentro de esta sección, haz clic en **Integraciones/API Pública**.

![](<../.gitbook/assets/Captura de pantalla 2025 12 17 a la(s) 11 53 25 a m  png 1.png>)

3. Desplázate hacia abajo hasta encontrar los campos:
   * **API Pública User**
   * **API Pública Password**

![](<../.gitbook/assets/image png Dec 17 2025 03 07 19 3080 PM.png>)

Estos datos corresponden a las credenciales que necesitarás para la integración.

{% hint style="warning" %}
Si no ves esta sección, verifica que estés usando una cuenta con permisos de administrador y que tienes el plan Pro.
{% endhint %}
{% endstep %}

{% step %}
### Conectar AgendaPro en Vambe

1. Ingresa a **Vambe**.
2. En el menú inferior izquierdo, haz clic en **Ajustes**.
3. Accede a la sección **Integraciones**.
4. Selecciona **AgendaPro**.

![](<../.gitbook/assets/image png Dec 17 2025 03 08 37 1583 PM.png>)

5. Haz clic en **Conectar**.

![](<../.gitbook/assets/image png Dec 17 2025 03 09 10 5602 PM.png>)

6. Ingresa:
   * El **User** obtenido desde AgendaPro.
   * El **Password** obtenido desde AgendaPro.

![](<../.gitbook/assets/image png Dec 17 2025 03 09 31 0896 PM.png>)

7. Haz clic en **Siguiente**.
{% endstep %}

{% step %}
### Integración completada

Una vez ingresadas correctamente las credenciales:

* Vambe confirmará que las credenciales fueron guardadas.
* La integración con AgendaPro quedará activa.
* A partir de este momento, Vambe podrá interactuar con AgendaPro según la configuración del embudo y los flujos definidos.
{% endstep %}
{% endstepper %}
