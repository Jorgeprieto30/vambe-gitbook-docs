---
cover: ../.gitbook/assets/Portada 20.png
coverY: 0
---

# Cómo conectar el Meta Pixel (CAPI) en Vambe Ads

## ¿Para qué sirve conectar el Meta Pixel en Vambe Ads?

Conectar el **Meta Pixel mediante la API de Conversión (CAPI)** permite que Vambe envíe **eventos reales de tus clientes directamente a Meta**, como conversaciones, interés, agendamientos o compras.

Esto es clave porque:

* Meta deja de optimizar solo por clics o vistas.
* Tus campañas comienzan a aprender desde **acciones reales dentro de Vambe**.
* Puedes identificar qué anuncios atraen a los clientes más calificados.
* Mejoras la segmentación, el retargeting y la optimización automática de campañas.
* Alimentas al algoritmo de Meta con señales de mayor calidad, aumentando el rendimiento publicitario.

En resumen, el Pixel conecta lo que ocurre **después del anuncio** con la optimización de tus campañas.

{% stepper %}
{% step %}
### Paso 1: Ingresar a Vambe Ads y a la configuración del Pixel

* Ingresa a Vambe Ads desde tu cuenta de Vambe: https://academy.vambe.ai/v1/docs/c%C3%B3mo-ingresar-a-vambe-ads
* En el menú izquierdo, haz clic en **Workspaces**.
* Dentro del workspace, ve a la sección **Meta Ads**.
* Busca el bloque **Interacción de Meta Pixel**.
* Haz clic en **Conectar**.

![](../.gitbook/assets/image\(85\).png)

En esta sección, Vambe te mostrará las instrucciones y los campos que necesitarás completar más adelante.
{% endstep %}

{% step %}
### Paso 2: Acceder al Administrador de Eventos de Meta

1. Ingresa a tu cuenta de Meta Business Manager.
2. Ve al **Administrador de Eventos**: [https://eventsmanager.facebook.com/events\_manager2](https://eventsmanager.facebook.com/events_manager2)
3. En el menú lateral, entra a **Conjunto de datos**.

Aquí verás los píxeles y conjuntos de datos disponibles en tu cuenta.

Si aún no tienes un conjunto de datos creado:

* Ve a **Configuración del negocio en** [**https://business.facebook.com/**](https://business.facebook.com/).
* Selecciona **Obtener datos** → **Conjuntos de datos**.
* Haz clic en **Agregar** y crea un nuevo conjunto de datos (Pixel).

![](../.gitbook/assets/image\(86\).png)
{% endstep %}

{% step %}
### Paso 3: Obtener el ID del conjunto de datos (Pixel)

* Dentro del **Administrador de Eventos (**[**https://eventsmanager.facebook.com/events\_manager2**](https://eventsmanager.facebook.com/events_manager2)**)**, selecciona el conjunto de datos creado.
* Entra a la pestaña **Configuración**.
* Copia el **Identificador del conjunto de datos**.
* Guarda este ID, ya que lo usarás más adelante en Vambe Ads.

![](../.gitbook/assets/image\(87\).png)
{% endstep %}

{% step %}
### Paso 4: Configurar la API de Conversión (CAPI) en Meta

1. Dentro del conjunto de datos, ve a la pestaña **Resumen**.
2. Busca la sección **Enviar eventos desde un servidor**.
3. Haz clic en **Configurar API de Conversión**.

![](../.gitbook/assets/image\(88\).png)

4. Selecciona **Ver otras formas de configurar**.
5. Elige **Configurar manualmente**.
6. Haz clic en **Siguiente**.

![](../.gitbook/assets/image\(89\).png)

7. Selecciona **API de Conversión y Pixel de Meta**.

![](../.gitbook/assets/image\(90\).png)

8. Haz clic en **Iniciar configuración de CAPI** y luego en **Finalizar**.

![](../.gitbook/assets/image\(91\).png)
{% endstep %}

{% step %}
### Paso 5: Seleccionar eventos y parámetros correctos

![](../.gitbook/assets/image\(93\).png)

1. En la configuración de CAPI, haz clic en **Continuar**.
2. Selecciona los eventos que deseas enviar desde Vambe hacia Meta.
   * Recomendado: marcar **Todos**.

![](../.gitbook/assets/image\(94\).png)

3. Haz clic en **Continuar**.
4. En la sección **Seleccionar detalles del evento**, marca **Identificador del evento**.
   * ⚠️ Este paso es obligatorio para evitar duplicaciones y errores de atribución.

![](../.gitbook/assets/image\(95\).png)

5. Continúa revisando la configuración hasta finalizar el proceso.
{% endstep %}

{% step %}
### Paso 6: Generar el token de acceso de CAPI

1. En la sección **Primeros pasos – API de Conversión**, haz clic en **Empezar**.

![](../.gitbook/assets/image\(96\).png)

2. Selecciona **Generar token de acceso**.

![](../.gitbook/assets/image\(97\).png)

3. Elige el conjunto de datos correspondiente.

![](../.gitbook/assets/image\(98\).png)

4. Haz clic en **Generar token de acceso**.
5. Copia el token generado y guárdalo.
{% endstep %}

{% step %}
### Paso 7: Conectar el Pixel en Vambe Ads

1. Regresa a **Vambe Ads**.
2. En la sección de conexión de Meta Pixel:
   * Pega el **ID del conjunto de datos**.
   * Pega el **Token de acceso** generado.
3. Guarda la configuración.

![](../.gitbook/assets/image\(99\).png)

✅ Con esto, el Meta Pixel queda correctamente conectado a Vambe Ads.
{% endstep %}
{% endstepper %}

## Resultado final

Desde este momento:

* Vambe enviará eventos reales a Meta mediante CAPI.
* Tus campañas podrán optimizarse con datos de alta calidad.
* Podrás crear audiencias basadas en comportamiento real (agendados, interesados, compradores).
* Mejorará la atribución y el rendimiento general de tus anuncios.
