---
cover: ../.gitbook/assets/Portada 23.png
coverY: 0
---

# Recuperación de carritos abandonados en Shopify

Potencia tus ventas con la recuperación automática de carritos abandonados en Shopify, una clave del **remarketing** en Vambe. Aprende a configurar esta funcionalidad para enviar mensajes de seguimiento a clientes que no finalizaron su compra, reactivando su interés y aumentando significativamente tu tasa de conversión.

{% hint style="info" %}
Antes de empezar, asegúrate de probar el flujo con un carrito de test antes de usarlo en producción.
{% endhint %}

***

## Requisitos previos

{% stepper %}
{% step %}
#### Plan de Shopify requerido

Es obligatorio contar con el plan Grow de Shopify.

> Sin el plan Grow no es posible continuar con la recuperación de carritos abandonados, ya que se utiliza una funcionalidad que solo está disponible en este plan.
{% endstep %}

{% step %}
#### Número de teléfono del cliente

El mensaje se enviará únicamente a clientes que:

* Hayan abandonado un carrito, y
* Hayan dejado su número de teléfono (ya sea llegando desde Vambe o directamente desde la tienda).

{% hint style="info" %}
No importa si el cliente llegó por Vambe o por la web: el mensaje se enviará en ambos casos siempre que exista un número de teléfono.
{% endhint %}
{% endstep %}

{% step %}
#### Definir el tiempo de envío

El tiempo de espera antes de enviar el mensaje (por ejemplo, 5 horas después del abandono) se configura dentro de Shopify y se ajusta en el flujo de automatización más adelante.
{% endstep %}
{% endstepper %}

***

## ¿Cuándo y a quién se envía el mensaje?

* Cuándo: después del tiempo que determines en el flujo (recomendado: 5 horas).
* A quién: a cualquier persona que deje un carrito abandonado y tenga un número de teléfono registrado.

***

## Configuración paso a paso

{% stepper %}
{% step %}
#### Paso 1: Acceder a la integración de Shopify en Vambe

1. En Vambe, ve al menú inferior izquierdo y haz clic en **Ajustes**.
2. Ingresa a **Integraciones**.
3. Selecciona **Shopify**.

![](<../.gitbook/assets/image png Dec 23 2025 01 12 06 1830 PM.png>)

Dentro del módulo de Shopify encontrarás la sección **Recuperación de carritos abandonados**.

* Haz clic en el ícono de Video.

![](<../.gitbook/assets/image png Dec 23 2025 01 13 03 0159 PM.png>)

* Se abrirá un video explicativo.
* Desplázate hacia abajo hasta encontrar los códigos necesarios (URL, headers y body), ya que los usaremos más adelante.

![](<../.gitbook/assets/Screenshare   2025 12 23 9_52_42 AM (1) gif.gif>)

No cierres esta pestaña, ya que volveremos a copiar esta información.
{% endstep %}

{% step %}
#### Paso 2: Crear la automatización en Shopify

1. Ingresa a tu cuenta de **Shopify**.
2.  Busca en la barra superior "Automatizaciones"\
    <br>

    <figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
3. Luego selecciona **Automatizaciones.**
4.  Haz clic en Crear automatizacion.

    <figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>
5.  Seleccionar Crear **Automatizacion Personalizada**<br>

    <figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>


6.  Seleccionar **Explorar Plantillas**<br>

    <figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>


7. Selecciona la plantilla **Recuperar un pedido abandonado**.

![](<../.gitbook/assets/image png Dec 23 2025 01 31 29 3983 PM.png>)

6.  Instalar la automatización.\
    <br>

    <figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
7.  Aparecera esta vista y entraremos a editarla<br>

    <figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Paso 3: Configurar el tiempo de espera (Wait)

Dentro del flujo de automatización:

1. Identifica el bloque llamado **Wait**.
2. Aquí defines cuánto tiempo pasará desde que el cliente abandona el carrito hasta que se envía el mensaje.

Recomendación: 5 horas.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Este valor puedes ajustarlo según tu estrategia.
{% endstep %}

{% step %}
#### Paso 4: Eliminar el envío de correo por defecto

1. Al final del flujo encontrarás un bloque llamado **Send marketing email**.
2.  Elimínalo, ya que no utilizaremos correo electrónico para este flujo.<br>

    <figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Paso 5: Agregar la acción HTTP Request

1. Haz clic en **Add action en verdadero** (Agregar acción).
2.  Busca y selecciona **HTTP request**.\
    <br>

    <figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

**Configuración del HTTP request**

Usa la información de Vambe que obtuviste en el Paso 1. Copia y pega donde aparece CURL.

<figure><img src="../.gitbook/assets/image (27).png" alt="" width="375"><figcaption></figcaption></figure>

Volver a Shopify y seleccionar **Importar Curl** y pegar el copiado en Vambe<br>

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Luego click en Importar y listo !<br>
{% endstep %}

{% step %}
#### Paso 6: Activar el flujo

1. Guarda la acción.
2. Activa el flujo de trabajo.

![](<../.gitbook/assets/image png Dec 23 2025 01 42 25 7136 PM.png>)

3. Haz clic nuevamente en **Activar**.

![](<../.gitbook/assets/image png Dec 23 2025 01 42 36 9674 PM.png>)

Desde este momento, cada cliente que abandone un carrito recibirá automáticamente el mensaje de seguimiento luego del tiempo configurado.
{% endstep %}

{% step %}
#### Paso 7: Ver ejecuciones del flujo en Shopify

Para revisar las ejecuciones:

1. En Shopify, ve al menú izquierdo.
2. Ingresa a **Aplicaciones**.
3. Selecciona **Flow**.

Aquí podrás ver todas las veces que este flujo se ha ejecutado.
{% endstep %}

{% step %}
#### Paso 8: Ver carritos recuperados en Vambe

Para ver los resultados dentro de Vambe:

1. Ve al menú izquierdo.
2. Haz clic en **E-commerce**.
3. Luego selecciona **Recuperación**.

![](<../.gitbook/assets/image png Dec 23 2025 01 44 33 5849 PM.png>)

En esta sección podrás ver:

* Carritos abandonados.
* Carritos recuperados.
* Flujo completo de seguimiento realizado por Vambe.
{% endstep %}
{% endstepper %}

***

## Resultado final

Con esta configuración:

* Automatizas la recuperación de carritos abandonados.
* Aumentas conversiones sin intervención manual.
* Centralizas la información y resultados directamente en Vambe.
