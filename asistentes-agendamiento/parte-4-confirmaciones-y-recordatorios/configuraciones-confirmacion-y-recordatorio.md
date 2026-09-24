---
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Configuraciones Confirmación y Recordatorio

## Configuraciones Confirmación y Recordatorio

Desde la sección **Citas**, cuentas con un panel de administración donde configuras todo lo relacionado con tus sedes, tu equipo de profesionales, los tratamientos que ofreces y las comunicaciones automáticas hacia tus pacientes. Mantener esta información al día no solo mejora la experiencia del usuario, sino que reduce drásticamente el ausentismo a las citas.

<figure><img src="../.gitbook/assets/Nuevas Vistas.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**Para entrar:** en el menú de la izquierda, haz clic en **Citas**. Ahí encontrarás dos grupos: **Administración** (Sucursales, Profesionales, Tratamientos) y **Ajustes** (Recordatorios, Config. bloques).
{% endhint %}

***

## Sucursales

Desde **Administración > Sucursales** ves, de un vistazo, una tarjeta por cada sede con el estado de sus recordatorios, confirmaciones y reactivaciones. Ahí mismo puedes activarlos o entrar a configurarlos, sin tener que buscar la sucursal en otra pantalla.

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

***

## Profesionales

En **Administración > Profesionales** encuentras una grilla con todo tu equipo. La barra de búsqueda y los filtros por tratamiento y por sucursal te ayudan a ubicar rápidamente a un profesional específico, útil cuando manejas varias sedes o un equipo numeroso.

<figure><img src="../.gitbook/assets/Vista Profesionales (blur).png" alt=""><figcaption></figcaption></figure>

***

## Tratamientos

En **Administración > Tratamientos** revisas, en una sola tabla, todos los tratamientos que ofreces. El buscador te permite encontrar uno por nombre, y una pestaña por sucursal te muestra qué se ofrece en cada sede y a qué precio, para que puedas comparar tu oferta entre sucursales sin salir de la pantalla.

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

***

## Recordatorios

En **Ajustes > Recordatorios** configuras el envío automático de mensajes a tus pacientes, ya sea que utilices **Medilink, Dentalink, Agenda Pro o Reservo**. Esta configuración vive en tres pestañas: **Recordatorios**, **Confirmaciones** y **Reactivaciones**. Cada pestaña muestra una tarjeta por sucursal y, al entrar a una de ellas, un panel de configuración enfocado solo en esa comunicación.

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

### Antes de comenzar: la importancia de las plantillas

Para que el sistema funcione, es fundamental que primero tengas creadas tus plantillas de confirmación y plantillas de recordatorio.

{% hint style="warning" %}
**¿Aún no tienes tus plantillas?** [\[Haz clic aquí para ir a crear la plantilla\]](https://academy.vambe.ai/canal/plantillas/como-crear-plantillas) y vuelve a este artículo cuando estés listo.
{% endhint %}

Al diseñar tus mensajes, asegúrate de incluir variables que Vambe pueda completar automáticamente. Esto permitirá que cada mensaje sea único y contenga la información precisa de la cita.

Variables recomendadas:

* **Nombre del paciente**: Para un trato cercano.
* **Nombre del profesional / doctor**: Para que el paciente sepa quién lo atenderá.
* **Fecha de la cita:** Día exacto del compromiso.
* **Hora de la cita**: El bloque horario agendado.
* **Sede o sucursal:** Fundamental si manejas más de un punto de atención.

<figure><img src="https://1514718626-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FhQjV55x4bDSryBoT4FYC%2Fuploads%2FrGmeHF1SxYPU7tzvacEL%2Fimage.png?alt=media&#x26;token=3aaa7856-04c3-4ac4-b735-83b922aaf87a" alt=""><figcaption></figcaption></figure>

👉 _Puedes revisar el artículo específico de_ [_\[cómo crear plantillas\]_](https://academy.vambe.ai/canal/plantillas/como-crear-plantillas) _para más detalle sobre variables y buenas prácticas._

***

### Pestaña Confirmaciones

Desde la tarjeta de la sucursal, defines:

* **Canal - notificación a cliente:** el medio (por ejemplo, WhatsApp) por el que se envían los mensajes.
* **Selecciona la plantilla:** la que creaste previamente para confirmar citas.
* **Etapa de confirmación:** a qué etapa del CRM llegará el cliente cuando se le envíe este mensaje (ej: "Agendados").
* **Tiempo de envío:** con cuánta anticipación se envía (desde 1 hasta 4 días antes) y a qué hora.
* **Filtro Vambe:** el switch _"Enviar confirmación solo a citas realizadas a través de Vambe"_.
  * **Activado**: solo se envía a citas creadas por la IA.
  * **Desactivado**: se envía a todos los clientes, incluidos los creados manualmente o en otras plataformas.
* **Mensajes de seguimiento:** si el paciente no responde al primer mensaje, defines cuántos mensajes adicionales enviar y el tiempo de espera entre ellos.

### Pestaña Recordatorios

{% hint style="warning" %}
**Nota importante:** el recordatorio solo se envía si el cliente ya está marcado como Confirmado en el sistema.
{% endhint %}

* **Selecciona la plantilla:** usualmente una más breve recordándole que "falta poco" para su cita.
* **Rango horario:** haz clic en **"Agregar rango"** para definir a quiénes notificar según su hora de cita (ej: citas programadas entre las 10:00 y las 23:00).
* **Tipo de aviso:**
  * **Horario fijo:** envía el aviso a todos a una hora específica (ej: el día anterior a las 08:00 AM).
  * **Horario relativo:** envía el aviso X tiempo antes de la cita (ej: 1 hora antes de su hora agendada).

### Pestaña Reactivaciones

Esta pestaña agrupa, por sucursal, la configuración de reactivación para pacientes que se detienen a mitad del agendamiento, complementando a las confirmaciones y recordatorios ya definidos.

### Ajustes finales

En la configuración de recordatorio encontrarás dos opciones adicionales:

* **Enviar recordatorio solo a citas realizadas en Vambe**
* **Eliminar contacto del pipeline cuando la cita es cancelada**: > ⚠️ Recomendación: sugerimos mantener esta opción apagada para no perder el historial del contacto en tu CRM.

Una vez configurado todo, haz clic en Guardar y ¡listo! Tu sistema de seguimiento ya está trabajando por ti.

***

## En resumen

El panel de **Citas** reúne en un mismo lugar la administración de tus sedes, tu equipo de profesionales, tu oferta de tratamientos y las comunicaciones automáticas hacia tus pacientes. Cada vista está pensada para que resuelvas rápido: una tarjeta por sucursal en Sucursales, una grilla filtrable en Profesionales, una tabla comparable en Tratamientos, y pestañas enfocadas por tipo de mensaje en Recordatorios.
