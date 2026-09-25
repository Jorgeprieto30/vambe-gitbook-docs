# Cómo conectar Philaxmed en Vambe

Philaxmed es una nueva integración de agendamiento disponible en Vambe, pensada para centros médicos y clínicas que administran sus citas, pacientes y tratamientos en esta plataforma.

Al conectar Philaxmed, Vambe puede crear citas, consultar la disponibilidad real de profesionales y especialidades, enviar recordatorios y mantener el estado de las citas sincronizado, todo directamente desde tu asistente de IA.

{% hint style="info" %}
**Para entrar:** en Vambe, ve a **Ajustes** y luego a **Integraciones**, y busca la tarjeta de **Philaxmed**.
{% endhint %}

***

## Solicitar el token a Philaxmed

A diferencia de otras integraciones, el token de acceso no se genera desde Vambe ni desde el propio Philaxmed de forma autónoma: **es Philaxmed quien debe emitirlo** para tu centro médico.

Como Vambe mantiene una buena relación y comunicación con Philaxmed, este proceso suele resolverse rápido. Al solicitar el token, es necesario indicarles también la **URL de la página** del centro médico, ya que Philaxmed la utiliza para configurar correctamente el acceso.

{% hint style="warning" %}
El token es **por sucursal**. Si tu centro médico tiene varias sucursales, Philaxmed debe emitir un token independiente para cada una, y cada uno debe conectarse por separado en Vambe.
{% endhint %}

***

## Conectar el token en Vambe

Una vez que Philaxmed te entregue el token y la URL base del servidor asignado, ingresa a Vambe para completar la conexión:

{% stepper %}
{% step %}
#### Paso 1: Abrir la integración de Philaxmed

En Vambe, dirígete a **Ajustes > Integraciones** y selecciona la tarjeta de **Philaxmed**.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Paso 2: Completar los datos de conexión

En el formulario **Conectar Philaxmed**, completa:

* **Nombre del token**: un nombre que te permita identificar a qué sucursal corresponde (por ejemplo, el nombre de la clínica o de la sede).
* **Token**: el token que Philaxmed emitió para esa sucursal.
* **URL Base**: la URL del servidor que Philaxmed te asignó.

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
#### Paso 3: Guardar

Haz clic en **Guardar**. Si los datos son correctos, la integración quedará habilitada para esa sucursal.
{% endstep %}

{% step %}
#### Paso 4: Repetir por cada sucursal

Si tu centro médico tiene más de una sucursal, repite este proceso con el token y la URL correspondiente a cada una.
{% endstep %}
{% endstepper %}

***

## Cómo funciona la información que trae Vambe

Desde Philaxmed, Vambe se trae las **especialidades** configuradas en el centro médico, no un listado de duraciones por atención: las especialidades **no cuentan con una duración propia**.

Para ofrecer disponibilidad, Vambe simplemente consulta los **slots disponibles** de la especialidad y/o del profesional, tal como están configurados en la agenda de la clínica dentro de Philaxmed.

{% hint style="info" %}
Un mismo profesional puede tener **varias especialidades asociadas**. Vambe respeta esa relación al momento de buscar disponibilidad y agendar.
{% endhint %}

***

## Sincronización, confirmaciones y recordatorios

Philaxmed no cuenta, por ahora, con un sistema de webhooks para recibir cambios en tiempo real. La información se actualiza mediante un **sync nocturno**, por lo que los cambios realizados en Philaxmed durante el día se reflejan en Vambe al día siguiente.

{% hint style="warning" %}
Como la sincronización es nocturna y no en tiempo real, ten esto en cuenta si necesitas que un cambio hecho directamente en Philaxmed (por ejemplo, un bloqueo de agenda) se refleje de inmediato en Vambe.
{% endhint %}

Además de la creación de citas y la consulta de disponibilidad, con Philaxmed también quedaron implementadas las **confirmaciones y los recordatorios** de citas, por lo que tus pacientes pueden recibirlos automáticamente por WhatsApp igual que con el resto de las integraciones de agendamiento.

***

## En resumen

Con Philaxmed conectado, tu centro médico puede ofrecer agendamiento automatizado 24/7: Vambe consulta la disponibilidad real de especialidades y profesionales, crea las citas y se encarga de confirmar y recordar cada una, manteniendo todo sincronizado con tu sistema clínico gracias al sync nocturno.

<details>

<summary>¿Te ha sido útil este artículo?</summary>

Sí No

</details>
