---
cover: ../.gitbook/assets/Portada 23.png
coverY: 0
---

# Recuperación de carritos abandonados en Shopify

En este artículo aprenderás cómo activar y configurar la recuperación automática de carritos abandonados en Shopify, utilizando Vambe para enviar mensajes de seguimiento a clientes que no finalizaron su compra. Este flujo permite contactar automáticamente a los clientes y aumentar la tasa de conversión de ventas perdidas.

{% hint style="info" %}
Antes de empezar, asegúrate de probar el flujo con un carrito de test antes de usarlo en producción.
{% endhint %}

***

## Requisitos previos

{% stepper %}
{% step %}
### Plan de Shopify requerido

Es obligatorio contar con el plan Grow de Shopify.

> Sin el plan Grow no es posible continuar con la recuperación de carritos abandonados, ya que se utiliza una funcionalidad que solo está disponible en este plan.
{% endstep %}

{% step %}
### Número de teléfono del cliente

El mensaje se enviará únicamente a clientes que:

* Hayan abandonado un carrito, y
* Hayan dejado su número de teléfono (ya sea llegando desde Vambe o directamente desde la tienda).

{% hint style="info" %}
No importa si el cliente llegó por Vambe o por la web: el mensaje se enviará en ambos casos siempre que exista un número de teléfono.
{% endhint %}
{% endstep %}

{% step %}
### Definir el tiempo de envío

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
### Paso 1: Acceder a la integración de Shopify en Vambe

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
### Paso 2: Crear la automatización en Shopify

1. Ingresa a tu cuenta de **Shopify**.
2. En el menú lateral izquierdo, haz clic en **Marketing**.
3. Luego selecciona **Automatizaciones.**

![](<../.gitbook/assets/image png Dec 23 2025 01 17 52 5042 PM.png>)

4. Haz clic en **Ver plantillas**.
5. Selecciona la plantilla **Recuperar un pedido abandonado**.

![](<../.gitbook/assets/image png Dec 23 2025 01 31 29 3983 PM.png>)

6. Activa la automatización.

![](<../.gitbook/assets/image png Dec 23 2025 01 32 49 2696 PM.png>)

7. Haz clic en **Editar** y luego en **Continuar**.

![](<../.gitbook/assets/image png Dec 23 2025 01 32 59 4711 PM.png>)
{% endstep %}

{% step %}
### Paso 3: Configurar el tiempo de espera (Wait)

Dentro del flujo de automatización:

1. Identifica el bloque llamado **Wait**.
2. Aquí defines cuánto tiempo pasará desde que el cliente abandona el carrito hasta que se envía el mensaje.

Recomendación: 5 horas.

![](<../.gitbook/assets/image png Dec 23 2025 01 34 00 6736 PM.png>)

Este valor puedes ajustarlo según tu estrategia.
{% endstep %}

{% step %}
### Paso 4: Eliminar el envío de correo por defecto

1. Al final del flujo encontrarás un bloque llamado **Send marketing email**.
2. Elimínalo, ya que no utilizaremos correo electrónico para este flujo.

![](<../.gitbook/assets/image png Dec 23 2025 01 34 49 4748 PM.png>)
{% endstep %}

{% step %}
### Paso 5: Agregar la acción HTTP Request

1. Haz clic en **Add action** (Agregar acción).
2. Busca y selecciona **HTTP request**.

![](<../.gitbook/assets/image png Dec 23 2025 01 35 26 1266 PM.png>)

#### Configuración del HTTP request

Usa la información de Vambe que obtuviste en el Paso 1. Copia y pega exactamente lo que aparece en Vambe dentro de los campos de Shopify.

![](<../.gitbook/assets/Screenshare   2025 12 23 9_52_42 AM (1) gif 1.gif>)

* Método: cambia **HTTP method** a **POST**.

![](<../.gitbook/assets/image png Dec 23 2025 01 36 03 2593 PM.png>)

* URL: copia la **URL** desde Vambe y pégala en el campo **URL** de Shopify.

![](<../.gitbook/assets/image png Dec 23 2025 01 37 24 9133 PM.png>)

* Headers: agrega los siguientes headers:
  * Content-Type: `application/json`
  * X-API-KEY: valor único por cuenta (cópialo desde Vambe)

{% hint style="warning" %}
Content-Type siempre es `application/json`. X-API-KEY cambia según cada cuenta.
{% endhint %}

* Body: copia todo el body desde Vambe y pégalo en el campo **Body** en Shopify.

Ejemplo visual de cómo debería quedar:

![](<../.gitbook/assets/image png Dec 23 2025 01 40 54 6584 PM.png>)
{% endstep %}

{% step %}
### Paso 6: Activar el flujo

1. Guarda la acción.
2. Activa el flujo de trabajo.

![](<../.gitbook/assets/image png Dec 23 2025 01 42 25 7136 PM.png>)

3. Haz clic nuevamente en **Activar**.

![](<../.gitbook/assets/image png Dec 23 2025 01 42 36 9674 PM.png>)

Desde este momento, cada cliente que abandone un carrito recibirá automáticamente el mensaje de seguimiento luego del tiempo configurado.
{% endstep %}

{% step %}
### Paso 7: Ver ejecuciones del flujo en Shopify

Para revisar las ejecuciones:

1. En Shopify, ve al menú izquierdo.
2. Ingresa a **Aplicaciones**.
3. Selecciona **Flow**.

Aquí podrás ver todas las veces que este flujo se ha ejecutado.
{% endstep %}

{% step %}
### Paso 8: Ver carritos recuperados en Vambe

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
