---
cover: ../.gitbook/assets/Portada 20.png
coverY: 0
---

# Google Ads: Cómo obtener la atribución correcta

En este artículo aprenderás cómo configurar **Google Ads** para lograr una **atribución correcta** dentro de **Vambe**, permitiéndote identificar exactamente **desde qué campaña, anuncio o formato publicitario provienen tus clientes**.

La atribución correcta es clave para:

* Entender qué campañas generan conversaciones reales.
* Medir el costo real por lead o cliente.
* Optimizar presupuesto hacia lo que realmente convierte.

***

## ¿Qué permite esta configuración?

Con la atribución bien configurada, Vambe podrá:

* Asociar cada conversación con su anuncio de origen.
* Diferenciar clientes que llegan desde publicidad versus otros canales.
* Mostrar métricas reales por campaña, tipo de anuncio y plataforma.

***

## Campañas compatibles en Google Ads

Esta configuración aplica para los siguientes tipos de campañas:

* Search
* Performance Max (PMax)
* Shopping
* Demand Gen
* Display
* App
* Video

***

## Paso 1: Ingresar a la configuración de la campaña

{% stepper %}
{% step %}
### Ingresar a Google Ads y seleccionar campaña

* Ingresa a **Google Ads**.
* Ve al menú **Campañas**.
* Selecciona la campaña que deseas configurar.
* Haz clic en **Configuración** a nivel campaña.

![Configuración de campaña](../.gitbook/assets/image\(82\).png)
{% endstep %}
{% endstepper %}

***

## Paso 2: Configurar “Campaign URL options”

{% stepper %}
{% step %}
### Localizar Campaign URL options

Dentro de la configuración de la campaña, busca la sección **Campaign URL options**.

![Campaign URL options](../.gitbook/assets/image\(83\).png)
{% endstep %}

{% step %}
### Agregar Tracking template

En el campo **Tracking template**, agrega el siguiente valor:

{% code title="Tracking template" %}
```plaintext
{lpurl}?ad_id={creative}
```
{% endcode %}

¿Qué hace este tracking?

* `{lpurl}` mantiene la URL original del anuncio.
* `ad_id={creative}` permite que Vambe identifique exactamente **qué anuncio generó la visita**.

Esta información será utilizada posteriormente por Vambe para hacer el match con la conversación.
{% endstep %}
{% endstepper %}

***

## Caso especial: Google Smart Campaigns

En **Google Smart Campaigns**, la configuración se realiza a nivel de anuncio.

{% stepper %}
{% step %}
### Pasos para Smart Campaigns

* Ingresa a la configuración del anuncio.
* En la sección **Landing page**, agrega el parámetro directamente a la URL:

{% code title="Ejemplo URL (Smart Campaigns)" %}
```plaintext
https://ejemplo.com/?ad_id={creative}
```
{% endcode %}

Esto cumple la misma función que el tracking template en campañas estándar.

![Smart Campaigns landing page](../.gitbook/assets/image\(84\).png)
{% endstep %}
{% endstepper %}

***

## Paso 3: Insertar el script universal de Vambe

Para que la atribución funcione correctamente, **es obligatorio instalar el script universal de Vambe** en la página de destino del anuncio.

### ¿Dónde encontrar el script?

1. Ingresa a **Vambe Ads**.
2. Ve a **Workspaces**.
3. En la parte inferior derecha encontrarás la sección **Seguimiento de tráfico web**.
4. Haz clic en **Obtener script de seguimiento**.

![Obtener script de seguimiento](<../.gitbook/assets/image(81) (1).png>)

Este script contiene un **Tracking ID único** que permite a Vambe:

* Identificar visitas desde anuncios.
* Relacionar esas visitas con conversaciones posteriores.

### Instalación del script

* El script debe pegarse **dentro del** `<head>` de la página web de destino.
* Si usas un CMS (WordPress, Webflow, Shopify, etc.), busca la sección para insertar código personalizado en el head.
* Publica los cambios una vez instalado.

***

## Consideraciones importantes para la atribución

{% hint style="warning" %}
El script solo hará match si ocurre una de estas acciones en la página (cualquiera de las dos basta):

* El usuario hace clic en un botón para hablar por WhatsApp.
* El usuario ingresa su **número de teléfono** en la página.
{% endhint %}

{% hint style="info" %}
Recomendación clave:

* Utiliza un **formulario que solicite el número de teléfono** y luego redirige al usuario a WhatsApp.\
  Esto aumenta significativamente la tasa de coincidencia entre anuncio y conversación.
{% endhint %}

***

## Validación de la configuración

{% stepper %}
{% step %}
### Publica y prueba

1. Publica la campaña.
2. Genera una interacción real (clic + conversación).
3. Verifica en Vambe Ads que el contacto aparezca con su **origen de Google Ads** y el **ad\_id** correspondiente.
{% endstep %}
{% endstepper %}
