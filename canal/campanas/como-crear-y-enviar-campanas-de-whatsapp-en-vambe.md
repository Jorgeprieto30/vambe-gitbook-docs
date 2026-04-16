---
cover: ../.gitbook/assets/Portada 16.png
coverY: 0
---

# Cómo crear y enviar campañas de WhatsApp en Vambe

Guía completa para preparar tu archivo, configurar tu campaña y enviarla de forma controlada.

Esta guía explica paso a paso cómo crear una campaña de WhatsApp en Vambe, cómo preparar correctamente tu archivo de contactos, cómo cargarlo, validar la información y finalmente enviar la campaña cumpliendo las políticas de Meta.

{% hint style="info" %}
Requisitos previos:

* Tener un número de [WhatsApp Business API](https://academy.vambe.ai/c%C3%B3mo-conectar-whatsapp-api-oficial) o [Dual](https://academy.vambe.ai/c%C3%B3mo-conectar-un-n%C3%BAmero-de-whatsapp-business-a-vambe-mediante-el-m%C3%A9todo-h%C3%ADbrido-api-qr) conectado en Vambe.
* Contar con una [plantilla](../plantillas/como-crear-plantillas.md) de WhatsApp aprobada y disponible para el canal.
* Preparar un archivo Excel o CSV con:
  * `telefono` (formato internacional E.164: +56…, +52…, +57…, etc.)
  * `nombre`
  * Columnas adicionales según las variables de la plantilla (ej.: `var_1`, `var_2`, `var_3`…)

En el paso 2 podrás descargar un archivo de ejemplo con las columnas exactas que requiere tu plantilla.
{% endhint %}

***

#### Paso 1: Crear la Campaña

1. En el menú lateral izquierdo, ve a **Canales** y luego a la pestaña **Campañas**.
2. Haz clic en el botón azul **+ Crear campaña** arriba a la derecha.

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

Se abrirá una ventana de configuración donde debes llenar los datos básicos:

* **Título**: Un nombre interno para identificarla (Ej: "Promo Cyber").
* **Canal**: Elige desde qué número de WhatsApp saldrá el mensaje.
* **Etapa de entrada** (Opcional): Si seleccionas una etapa aquí, todos los clientes que respondan a la campaña se moverán automáticamente a esa columna del embudo.
* **Plantilla**: Selecciona el mensaje que enviarás.
  * _Nota:_ Si tu plantilla no aparece, verifica que esté aprobada y disponible para ese canal específico.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

***

#### Paso 2: Seleccionar a los Destinatarios

Aquí tienes dos caminos: Cargar un Excel externo o usar tus contactos guardados en Vambe.

**Opción A: Usando un archivo Excel**

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

Ideal si tienes una base de datos externa.

1. Selecciona la opción **Excel**.
2.  **Personalizar Columnas**: Verás los campos que requiere tu plantilla (Ej: `{{1}}`, `{{2}}`). Debes asignarles un nombre de columna para tu Excel (Ej: "Nombre", "Descuento").

    * _Tip:_ Puedes agregar campos de "Metadata" fijos si necesitas guardar información extra que no va en el mensaje.

    <figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>


3.  **Descargar Ejemplo:** Haz clic en Descargar y actualizar plantilla. Esto te dará un archivo Excel vacío con las columnas exactas que necesitas llenar.<br>

    | $$521234569$$ | John Doe     | Jorge   | Mark 120  | $$19000$$ |
    | ------------- | ------------ | ------- | --------- | --------- |
    | $$563959094$$ | Ana García   | Beatriz | Delta 289 | $$23000$$ |
    | $$534210456$$ | Carlos Pérez | Ricardo | Gamma 754 | $$53000$$ |
4.  **Cargar Archivo:** Llena ese Excel con tus datos y súbelo en el recuadro de carga.\
    <br>

    <figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

\
**Opción B: Usando Contactos de Vambe (con IA)**

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

Ideal para contactar a gente con la que ya has hablado.

1. Selecciona la opción **Contactos en Vambe.**
2.  **Elegir Vista:** Selecciona la lista o filtro de clientes a los que quieres enviar (Ej: "Todos los clientes", "Etapa Ventas").<br>

    <figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>
3.  Mapeo de Variables con IA:

    * Si tu plantilla tiene variables (ej: "Hola \{{1\}}"), puedes activar el interruptor **"Llenar con IA".**
    * **¿Qué hace esto?** La IA leerá el historial y la información del ticket del cliente para intentar rellenar ese dato automáticamente.
    * _**⚠️ Advertencia:**_ No uses variables para datos externos que la IA no conoce (ej: "Tu código de acceso es \{{2\}}"), ya que la IA no podrá inventarlo.

    <figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>



Haz clic en **Crear** para finalizar la configuración.

***

#### Paso 3: Enviar o Programar

Una vez creada, la campaña aparecerá en tu lista con el estado Pendiente. Aún no se ha enviado nada. Tienes dos opciones:

**1. Enviar Ahora Mismo**

1.  Haz clic en el botón azul **Enviar**<br>

    <figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>


2.  Aparecerá una barra deslizante. Elige la cantidad de mensajes que quieres disparar (puedes enviarlos todos de una vez o por lotes).<br>

    <figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>


3. Haz clic en Enviar X mensajes.

**2. Programar para después**

1.  Haz clic en los tres puntos (⋮) a la derecha del botón Enviar.\
    <br>

    <figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>
2. Selecciona **Programar Campaña**.
3.  Elige la Fecha, la Hora y asegúrate de que la Zona Horaria sea la correcta.\
    <br>

    <figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>
4. Haz clic en **Programar**. El sistema enviará los mensajes automáticamente en ese momento.

***

#### Paso 4: Monitorear Resultados

¿Cómo saber si funcionó? En la lista de campañas, haz clic en los tres puntos (⋮) y selecciona Ver Detalles.

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

Se abrirá un panel de estadísticas donde podrás ver:

* Total de mensajes.
* Enviados exitosamente.
* Errores: (Muy útil para ver si falló algún número).
* Respuestas: Cuánta gente reaccionó a tu campaña.
* Abajo verás el listado nombre por nombre con el estado de cada envío.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

***

## Solución de problemas comunes

| Problema                      | Causa habitual                  | Solución                                                                                                                                                     |
| ----------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Números no reciben el mensaje | Formato telefónico incorrecto   | Asegurar formato +56…                                                                                                                                        |
| Plantilla no aparece          | No está asociada al canal       | Asociar canal en Plantillas → Habilitar                                                                                                                      |
| Error de variables            | Columnas mal nombradas o vacías | Revisar nombres exactos `var_1`, `var_2`…                                                                                                                    |
| Campaña no avanza             | Número WABA sin método de pago  | [Agregar método de pago en Business Manager](../configuracion-en-meta/como-agregar-un-metodo-de-pago-y-configurar-el-perfil-de-tu-numero-de-whatsapp-api.md) |
| Rechazo por Meta              | Contenido no permitido          | Ajustar redacción, categoría y reenviar                                                                                                                      |
