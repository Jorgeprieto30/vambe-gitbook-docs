# Cómo activar webhooks de citas y pagos en tiempo real en AgendaPro y Dentalink/Medilink

En este artículo aprenderás a activar los webhooks que le permiten a Vambe recibir las citas y los pagos de AgendaPro, Dentalink o Medilink en tiempo real, apenas se crean o cambian de estado.

Al activarlos, cada vez que se cree, confirme, reagende o cancele una cita, o se registre un pago asociado, Vambe recibe el evento de inmediato. Esto mantiene siempre actualizada la información de tus citas y pagos, y permite que tus workflows en Vambe se activen en el momento exacto en que ocurre el cambio.

{% hint style="info" %}
Esta configuración es distinta de las credenciales de la integración y de los webhooks de confirmaciones y recordatorios por WhatsApp. Aquí le indicas a AgendaPro, Dentalink o Medilink hacia dónde deben avisar cuando cambia una cita o un pago.
{% endhint %}

### Requisitos previos

* Tener la integración con AgendaPro, Dentalink o Medilink ya conectada en Vambe.
* Contar con **acceso administrador** en AgendaPro o en Dentalink/Medilink.

***

## Paso 1: Copiar la URL del webhook desde Vambe

Este primer paso es igual sin importar la plataforma que utilices.

{% stepper %}
{% step %}
#### Ubicar la URL en Ajustes

1. Ingresa a Vambe.
2. En el menú inferior izquierdo, haz clic en **Ajustes**.
3. Entra a **Integraciones** y selecciona la tarjeta de **AgendaPro**, **Dentalink** o **Medilink**, según corresponda.
4. Desplázate hasta la sección **Webhooks**.
5. Copia la URL que corresponde a la cuenta o token que quieres activar.

![](https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2FLo2COIpl0NibRX1Aitul%2Fvambe-webhooks-section.png?alt=media)

{% hint style="warning" %}
Si tienes más de una cuenta o token conectado, cada uno tiene su propia URL. Repite esta configuración una vez por cada uno.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## Paso 2: Pegar la URL en tu plataforma de agendamiento

Con la URL copiada, sigue la guía según la plataforma que utilices.

### En AgendaPro

{% stepper %}
{% step %}
#### Entrar a Configuraciones

* Inicia sesión en tu cuenta de **AgendaPro**.
* En la esquina superior derecha, haz clic en el ícono de ajustes y selecciona **Configuraciones**.

![](https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2Fn5OKhXUy8Wo5YTopLODw%2Fagendapro-configuraciones-menu.png?alt=media)
{% endstep %}

{% step %}
#### Abrir Integraciones

* En el menú lateral izquierdo, dentro de **Opciones avanzadas**, haz clic en **Integraciones**.

![](https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2FfALbMWeVETt0i13C9C1p%2Fagendapro-integraciones-sidebar.png?alt=media)
{% endstep %}

{% step %}
#### Crear el webhook

* Dentro de la sección **API Pública**, desplázate hasta **Webhooks**.
* Haz clic en **Crear Webhook**.
* Pega la URL que copiaste desde Vambe en el campo **URL**.
* Verifica que el interruptor **Activo** esté encendido.
* Haz clic en **Guardar**.

![](https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2FNZl3BooLvfWv51OI3DH4%2Fagendapro-webhook-modal.png?alt=media)
{% endstep %}
{% endstepper %}

### En Dentalink o Medilink

{% stepper %}
{% step %}
#### Entrar a la configuración de Webhooks

* Inicia sesión en tu cuenta de **Dentalink** o **Medilink** con un usuario administrador.
* En la parte superior derecha, haz clic en **Administrador**.
* Selecciona la opción **Configuración Webhook**.

![](https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2F4WCEdeTdZ0OWRRrMlq3i%2Fdentalink-administrador-menu.png?alt=media)
{% endstep %}

{% step %}
#### Agregar un nuevo proveedor

* Haz clic en el botón verde **+ Agregar proveedor**.

![](https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2FDH4kVNLbwzcJfmSWlWFN%2Fdentalink-agregar-proveedor.png?alt=media)
{% endstep %}

{% step %}
#### Completar los datos del proveedor

* En **Ingrese el nombre del proveedor**, escribe, por ejemplo, **Vambe**.
* En **Ingrese la URL del callback**, pega la URL que copiaste desde Vambe.
* Haz clic en **Guardar**.

![](https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2FVrFJ5DrKxDqsDGZ5axFl%2Fdentalink-crear-proveedor-modal.png?alt=media)
{% endstep %}

{% step %}
#### Activar las notificaciones del proveedor

El proveedor queda creado, pero todavía no recibe notificaciones: falta indicarle qué eventos debe avisar.

* En el listado de proveedores, el proveedor que acabas de crear (por ejemplo, **Vambe**) aparece con cuatro acciones disponibles: **Editar**, **Llaves**, **Notificaciones** y **Desactivar** (o **Activar**, si está inactivo). Haz clic en **Notificaciones**.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

* Se abre el modal **Lista de entidades**, con todas las entidades que Dentalink o Medilink puede notificar (Cita, Contrato, Paciente, Pagos, entre otras).
* Baja hasta la sección **Cita** y marca las casillas **Crear** y **Modificar**, tanto en la columna **Producto** como en la columna **API**. Por ahora, estas son las únicas casillas que necesitas activar para que Vambe reciba las citas en tiempo real; el resto de entidades quedan disponibles para configuraciones futuras (por ejemplo, webhooks de pagos).

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

* Haz clic en **Cerrar** para guardar.

{% hint style="warning" %}
Sin este paso, Dentalink o Medilink puede tener el webhook guardado pero no enviará los eventos de citas: la fila del proveedor debe tener también las notificaciones de **Cita** activadas.
{% endhint %}
{% endstep %}
{% endstepper %}

***

## Qué sucede después de activarlo

{% hint style="success" %}
Listo. Desde este momento, cada vez que se cree, actualice o cambie de estado una cita, o se registre un pago, en AgendaPro, Dentalink o Medilink, Vambe recibirá el evento automáticamente y lo reflejará en tiempo real.
{% endhint %}

* No es necesario repetir este paso, salvo que cambies de sede, de cuenta o generes una nueva URL desde Vambe.
* Si conectaste varias cuentas o tokens, recuerda repetir esta configuración por cada uno.

<details>

<summary>Errores comunes a evitar</summary>

* ❌ No usar una cuenta administrador en AgendaPro, Dentalink o Medilink.
* ❌ Pegar una URL incompleta o distinta a la que copiaste desde Vambe.
* ❌ En AgendaPro, dejar el interruptor **Activo** apagado.
* ❌ No hacer clic en **Guardar** después de pegar la URL.
* ❌ En Dentalink o Medilink, crear el proveedor pero olvidar activar las casillas de **Notificaciones** de Cita.
* ❌ Configurar solo una cuenta o token cuando tienes varios conectados.

</details>
