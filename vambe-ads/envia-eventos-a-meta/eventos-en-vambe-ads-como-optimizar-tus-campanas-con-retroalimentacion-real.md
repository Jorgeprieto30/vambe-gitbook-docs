---
cover: ../.gitbook/assets/Portada 20.png
coverY: 0
---

# Eventos en Vambe Ads: cómo optimizar tus campañas con retroalimentación real

## ¿Qué es la funcionalidad de Eventos en Vambe Ads?

La funcionalidad de **Eventos** permite enviar información de retroalimentación directamente a los píxeles de tus plataformas publicitarias, como **Meta Ads** y **TikTok Ads** (Google Ads estará disponible próximamente).

Estos eventos informan a las plataformas cuándo ocurren acciones reales dentro de Vambe, como por ejemplo un **agendamiento**, lo que permite que sus algoritmos aprendan de conversiones reales y no solo de clics o impresiones.

{% hint style="info" %}
Requisito previo: antes de configurar eventos, debes tener tu píxel correctamente conectado.\
Si aún no lo has hecho, revisa: 👉 [Cómo conectar el Meta Pixel en Vambe Ads](https://academy.vambe.ai/docs/c%C3%B3mo-conectar-el-pixel-de-meta-a-vambe)
{% endhint %}

## ¿Para qué sirven los eventos?

Los eventos permiten que tus campañas publicitarias se optimicen automáticamente en base a lo que realmente importa: **acciones reales de tus leads**.

Beneficios principales

* Mejor optimización del algoritmo de las plataformas publicitarias
* Reducción de costos en campañas
* Mejores tasas de conversión
* Leads de mayor calidad

(Video: explicación general — 0:27 a 0:55)

{% embed url="https://www.youtube.com/watch?v=WEYz7obYtQE" %}

## Paso a paso: cómo configurar Eventos en Vambe Ads

{% stepper %}
{% step %}
### Acceder a la sección de Eventos

(Video: 1:07 – 1:14)

* [Ingresa a Vambe Ads](https://academy.vambe.ai/v1/docs/c%C3%B3mo-ingresar-a-vambe-ads):
* En el menú lateral izquierdo, haz clic en **Eventos**

![](../.gitbook/assets/image\(123\).png)

* Si es tu primera vez, verás la vista vacía de eventos

![](../.gitbook/assets/image\(124\).png)
{% endstep %}

{% step %}
### Conectar tu píxel (si no lo has hecho)

(Video: 1:17 – 1:22)

* Haz clic en **Conectar píxel**
* Serás redirigido a la vista de **Workspaces**
* Aquí se encuentran todas las configuraciones de integraciones

(Véase también: https://academy.vambe.ai/v1/docs/c%C3%B3mo-conectar-el-pixel-de-meta-a-vambe)
{% endstep %}

{% step %}
### Configurar la conexión del píxel

(Video: 1:29 – 1:48)

* Puedes conectar:
  * Píxel de **Meta**
  * Píxel de **TikTok**
* El sistema te guiará con un **tutorial paso a paso** y mostrará imágenes con la información necesaria en cada plataforma.
{% endstep %}

{% step %}
### Ingresar las credenciales del píxel

(Video: 1:56 – 2:14)

* Ingresa el **ID del píxel**
* Ingresa la **llave secreta**
* El sistema validará la conexión (toma solo unos segundos)

✅ Una vez validado, el píxel quedará conectado y listo para recibir eventos
{% endstep %}

{% step %}
### Configurar eventos específicos

(Video: 2:18 – 2:41)

* Vuelve a la vista de **Eventos**
* Selecciona el **embudo (pipeline)** donde quieres trabajar

![](../.gitbook/assets/image\(125\).png)

* Define el evento que deseas enviar

![](../.gitbook/assets/image\(126\).png)

Ejemplo práctico:

![](../.gitbook/assets/image\(127\).png)

* Evento: **Cambio de etapa**
* Etapa: _Schedule Leads_
* Resultado: se envía un evento al píxel indicando que ocurrió un **agendamiento**
{% endstep %}

{% step %}
### Guardar y activar el evento

(Video: 2:48 – 2:58)

* Guarda la configuración

A partir de ese momento, cada contacto que entre a la etapa configurada enviará automáticamente el evento a **Meta** y **TikTok**.

![](../.gitbook/assets/image\(128\).png)
{% endstep %}

{% step %}
### Probar la configuración (Test Event)

(Video: 3:18 – 3:37)

* Haz clic en **Test Event**
* Simula un contacto entrando a la etapa configurada
* Podrás ver:
  * El movimiento del contacto en el embudo
  * Que el evento se esté enviando correctamente
{% endstep %}

{% step %}
### Monitoreo y seguimiento de eventos

(Video: 3:41 – 4:09)

* Una vez configurados, los eventos aparecen en el panel principal y se muestran cuando están siendo enviados.
* Esto te permite verificar en tiempo real que todo esté funcionando correctamente.
{% endstep %}
{% endstepper %}

## Tipos de eventos disponibles

(Video: 3:08 – 3:16)

Vambe Ads permite configurar distintos tipos de eventos según tu proceso comercial (por ejemplo, agendamientos, avances de etapa, entre otros). Se recomienda analizar qué tipo de evento se ajusta mejor a la estrategia de tu negocio antes de configurarlos.

## Resultados esperados al usar Eventos

(Video: 3:55 – 4:07)

Una correcta configuración de eventos permite:

* Reducir el costo de las campañas
* Obtener leads con mayor probabilidad de conversión
* Optimizar automáticamente los algoritmos publicitarios
* Mejorar la eficiencia del gasto publicitario

## Notas importantes

* Google Ads estará disponible próximamente
* Configura solo eventos relevantes para tu proceso real
* Usa siempre **Test Event** para validar
* Los eventos se envían automáticamente una vez activos

## Conclusión

La funcionalidad de **Eventos en Vambe Ads** es una herramienta clave para conectar tus campañas publicitarias con lo que realmente ocurre dentro de tu embudo. Al enviar retroalimentación directa a los píxeles, las plataformas publicitarias dejan de optimizar por clics y comienzan a optimizar por **resultados reales**, permitiéndote reducir costos y mejorar la calidad de tus leads.
