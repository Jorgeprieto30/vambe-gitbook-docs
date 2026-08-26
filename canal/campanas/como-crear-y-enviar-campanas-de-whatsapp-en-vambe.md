---
description: >-
  Guía de las campañas de WhatsApp creadas desde la Vista antigua: prepara tu
  archivo, configura la campaña, envíala y revisa sus resultados.
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo crear y enviar campañas de WhatsApp desde la Vista antigua

## Cómo crear y enviar campañas de WhatsApp en Vambe

Guía completa para preparar tu archivo, configurar tu campaña y enviarla de forma controlada.

Esta guía explica paso a paso cómo crear una campaña de WhatsApp en Vambe, cómo preparar correctamente tu archivo de contactos, cómo cargarlo, validar la información y finalmente enviar la campaña cumpliendo las políticas de Meta.

{% hint style="info" %}
Requisitos previos:

* Tener un número de [WhatsApp Business API](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/como-conectar-whatsapp-api-oficial) o [Dual](https://academy.vambe.ai/canal/conexion-de-canales-de-vambe/guia-de-conexion-whatsapp-api-metodo-qr) conectado en Vambe.
* Contar con una plantilla de WhatsApp aprobada y disponible para el canal.
* Preparar un archivo Excel o CSV con:
  * `telefono` (formato internacional E.164: +56…, +52…, +57…, etc.)
  * `nombre`
  * Columnas adicionales según las variables de la plantilla (ej.: `var_1`, `var_2`, `var_3`…)

En el paso 2 podrás descargar un archivo de ejemplo con las columnas exactas que requiere tu plantilla.
{% endhint %}

***

**Paso 1: Crear la Campaña**

1. En el menú lateral izquierdo, ve a **Canales** y luego a la pestaña **Campañas**.
2. Haz clic en el botón azul **+ Crear campaña** arriba a la derecha.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FEbf0yHfpHZlmdOheXPQv%2Fimage.png?alt=media&#x26;token=2384c95e-b369-4093-a67a-38e59d0f65f1" alt=""><figcaption></figcaption></figure>

Se abrirá una ventana de configuración donde debes llenar los datos básicos:

* **Título**: Un nombre interno para identificarla (Ej: "Promo Cyber").
* **Canal**: Elige desde qué número de WhatsApp saldrá el mensaje.
* **Etapa de entrada** (Opcional): Si seleccionas una etapa aquí, todos los clientes que respondan a la campaña se moverán automáticamente a esa columna del embudo.
* **Plantilla**: Selecciona el mensaje que enviarás.
  * _Nota:_ Si tu plantilla no aparece, verifica que esté aprobada y disponible para ese canal específico.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FjivujRA9xXdycQbJl8Rk%2Fimage.png?alt=media&#x26;token=78671677-3494-4841-9a03-5e37a0695bdc" alt=""><figcaption></figcaption></figure>

***

**Paso 2: Seleccionar a los Destinatarios**

Aquí tienes dos caminos: Cargar un Excel externo o usar tus contactos guardados en Vambe.

**Opción A: Usando un archivo Excel**

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2F3vJZeULxrPcMecWen9wz%2Fimage.png?alt=media&#x26;token=e9969c25-7f9d-44ab-b3aa-c34540b512f3" alt=""><figcaption></figcaption></figure>

Ideal si tienes una base de datos externa.

1. Selecciona la opción **Excel**.
2.  **Personalizar Columnas**: Verás los campos que requiere tu plantilla (Ej: `{{1}}`, `{{2}}`). Debes asignarles un nombre de columna para tu Excel (Ej: "Nombre", "Descuento").

    * _Tip:_ Puedes agregar campos de "Metadata" fijos si necesitas guardar información extra que no va en el mensaje.

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FJTYdEq5uzXnrIbulurxr%2Fimage.png?alt=media&#x26;token=a7934443-dcf9-4f52-a98b-b71d89b82324" alt=""><figcaption></figcaption></figure>
3.  **Descargar Ejemplo:** Haz clic en Descargar y actualizar plantilla. Esto te dará un archivo Excel vacío con las columnas exactas que necesitas llenar.<br>

    | $$521234569$$ | John Doe     | Jorge   | Mark 120  | $$19000$$ |
    | ------------- | ------------ | ------- | --------- | --------- |
    | $$563959094$$ | Ana García   | Beatriz | Delta 289 | $$23000$$ |
    | $$534210456$$ | Carlos Pérez | Ricardo | Gamma 754 | $$53000$$ |
4.  **Cargar Archivo:** Llena ese Excel con tus datos y súbelo en el recuadro de carga.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FWSIXKYDz18zW9qEoZThv%2Fimage.png?alt=media&#x26;token=b255bb36-3628-45d7-80bd-5352b1267707" alt=""><figcaption></figcaption></figure>

\
**Opción B: Usando Contactos de Vambe (con IA)**

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2Fej7kQxLzJnvcBPUaWRrr%2Fimage.png?alt=media&#x26;token=cc7ff051-3041-4588-a2eb-735d31e9831c" alt=""><figcaption></figcaption></figure>

Ideal para contactar a gente con la que ya has hablado.

1. Selecciona la opción **Contactos en Vambe.**
2.  **Elegir Vista:** Selecciona la lista o filtro de clientes a los que quieres enviar (Ej: "Todos los clientes", "Etapa Ventas").<br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FK7KbJEoteqpfJKYvr7Pv%2Fimage.png?alt=media&#x26;token=21f92ee0-f894-4943-af01-9bc4dde981e3" alt=""><figcaption></figcaption></figure>
3.  Mapeo de Variables con IA:

    * Si tu plantilla tiene variables (ej: "Hola \{{1\}}"), puedes activar el interruptor **"Llenar con IA".**
    * **¿Qué hace esto?** La IA leerá el historial y la información del ticket del cliente para intentar rellenar ese dato automáticamente.
    * _**⚠️ Advertencia:**_ No uses variables para datos externos que la IA no conoce (ej: "Tu código de acceso es \{{2\}}"), ya que la IA no podrá inventarlo.

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FUsVNrzTHOik6RcSa7YDm%2Fimage.png?alt=media&#x26;token=e27a1eff-6033-4ee1-8b7e-f9a9a92742c1" alt=""><figcaption></figcaption></figure>

Haz clic en **Crear** para finalizar la configuración.

***

**Paso 3: Enviar o Programar**

Una vez creada, la campaña aparecerá en tu lista con el estado Pendiente. Aún no se ha enviado nada. Tienes dos opciones:

**1. Enviar Ahora Mismo**

1.  Haz clic en el botón azul **Enviar**<br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FjJjT41l7MRguFF4Eminb%2Fimage.png?alt=media&#x26;token=46075d33-df20-4777-991b-d5deeae5fc25" alt=""><figcaption></figcaption></figure>
2.  Aparecerá una barra deslizante. Elige la cantidad de mensajes que quieres disparar (puedes enviarlos todos de una vez o por lotes).<br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2Flh1zCaQesXsIEhndwWL4%2Fimage.png?alt=media&#x26;token=1c18ee16-7165-4cf4-acd3-bf3a7e24c1ce" alt=""><figcaption></figcaption></figure>
3. Haz clic en Enviar X mensajes.

**2. Programar para después**

1.  Haz clic en los tres puntos (⋮) a la derecha del botón Enviar.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FwDp1DVLtXSvrliK9dQNR%2Fimage.png?alt=media&#x26;token=c7e8345f-0309-4623-a2ec-6a9f9be6e6a5" alt=""><figcaption></figcaption></figure>
2. Selecciona **Programar Campaña**.
3.  Elige la Fecha, la Hora y asegúrate de que la Zona Horaria sea la correcta.\
    <br>

    <figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FwHuRrS1SaVcUjmBujit1%2Fimage.png?alt=media&#x26;token=4c072453-85a2-4616-9aca-4a00e5473f29" alt=""><figcaption></figcaption></figure>
4. Haz clic en **Programar**. El sistema enviará los mensajes automáticamente en ese momento.

***

**Paso 4: Monitorear Resultados**

¿Cómo saber si funcionó? En la lista de campañas, haz clic en los tres puntos (⋮) y selecciona Ver Detalles.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FwDp1DVLtXSvrliK9dQNR%2Fimage.png?alt=media&#x26;token=c7e8345f-0309-4623-a2ec-6a9f9be6e6a5" alt=""><figcaption></figcaption></figure>

Se abrirá un panel de estadísticas donde podrás ver:

* Total de mensajes.
* Enviados exitosamente.
* Errores: (Muy útil para ver si falló algún número).
* Respuestas: Cuánta gente reaccionó a tu campaña.
* Abajo verás el listado nombre por nombre con el estado de cada envío.

<figure><img src="https://502444442-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FCFdmz6HrosBiYP1q1BJ6%2Fuploads%2FO38gdtO4DjZWQh5eCLII%2Fimage.png?alt=media&#x26;token=ec88d44d-2cfd-452f-af09-eb4b31412d29" alt=""><figcaption></figcaption></figure>

***

### Solución de problemas comunes

| Problema                      | Causa habitual                  | Solución                                   |
| ----------------------------- | ------------------------------- | ------------------------------------------ |
| Números no reciben el mensaje | Formato telefónico incorrecto   | Asegurar formato +56…                      |
| Plantilla no aparece          | No está asociada al canal       | Asociar canal en Plantillas → Habilitar    |
| Error de variables            | Columnas mal nombradas o vacías | Revisar nombres exactos `var_1`, `var_2`…  |
| Campaña no avanza             | Número WABA sin método de pago  | Agregar método de pago en Business Manager |
| Rechazo por Meta              | Contenido no permitido          | Ajustar redacción, categoría y reenviar    |
