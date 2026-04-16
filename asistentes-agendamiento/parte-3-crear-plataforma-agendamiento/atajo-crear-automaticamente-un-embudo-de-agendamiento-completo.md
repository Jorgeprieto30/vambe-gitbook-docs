---
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Atajo: Crear automáticamente un embudo de agendamiento completo

Este artículo presenta un **atajo** que te permite crear, en pocos pasos, un embudo de agendamiento completamente funcional, sin necesidad de construir manualmente cada una de sus partes.

![Imagen principal](<../.gitbook/assets/image png Dec 26 2025 01 37 33 8120 PM.png>)

Al usar este atajo, Vambe creará automáticamente lo que normalmente se configura en:

* Paso 0: Crear las etapas
* Paso 1: Crear tu primer asistente de agendamiento
* Paso 2: Asistente Agendador
* Paso 3: Asistente Agendados

👉 Más adelante podrás profundizar y personalizar cada uno de esos pasos por separado. Este atajo está pensado para **partir rápido** y dejar el sistema listo para conectar.

***

#### ¿Qué hace este atajo?

Al activar esta opción, Vambe crea automáticamente:

* Un embudo de tipo **Agendamiento**
* Las etapas:
  * Información inicial
  * Agendamiento
  * Agendados
  * Ayuda humana
* Los asistentes de inteligencia artificial correspondientes a cada etapa
* La estructura base para integrarse con tu plataforma de agendamiento

Es ideal si quieres **ahorrarte la configuración manual inicial** y luego ajustar detalles con calma.

***

{% hint style="warning" %}
Requisitos antes de comenzar

Antes de usar este atajo, debes cumplir **sí o sí** con lo siguiente:

* Tener las [**credenciales de tu plataforma de agendamiento**](https://academy.vambe.ai/asistentes-agendamiento#parte-1-obtener-credenciales) listas

(AgendaPro, Dentalink, Medilink o Reservo)

Sin credenciales, la plantilla no podrá activarse.
{% endhint %}

***

{% stepper %}
{% step %}
### Crear un nuevo embudo usando el atajo

* Ingresa a **Embudo**.
* En la esquina superior derecha, haz clic en los **tres puntos**.
* Selecciona **Nuevo embudo**.

![Crear nuevo embudo](<../.gitbook/assets/image png Dec 26 2025 01 41 58 2188 PM.png>)
{% endstep %}

{% step %}
### Configurar los datos base del embudo

Completa la información inicial:

* **Nombre del embudo**\
  Ejemplo: _Agendamiento Vambe_
* **Tipo de embudo**\
  Selecciona: **Agendamiento**

![Configurar datos base](<../.gitbook/assets/image png Dec 26 2025 01 47 18 5144 PM.png>)

* **Plataforma de agendamiento**\
  Selecciona la que utilizas:
  * AgendaPro
  * Dentalink
  * Medilink
  * Reservo

{% hint style="warning" %}
Importante: aquí se activará la plantilla automática, por eso es clave tener las credenciales listas.
{% endhint %}

![Seleccionar plataforma](<../.gitbook/assets/image png Dec 26 2025 01 47 53 8024 PM.png>)
{% endstep %}

{% step %}
### Conectar credenciales y sitio web

* Ingresa las **credenciales** de la plataforma seleccionada.

![Credenciales](<../.gitbook/assets/image png Dec 26 2025 01 48 29 5795 PM.png>)

* Ingresa la **URL de tu sitio web**.

![URL sitio web](<../.gitbook/assets/image png Dec 26 2025 01 48 58 0098 PM.png>)
{% endstep %}

{% step %}
### Confirmar información del negocio

Vambe detectará automáticamente:

* Nombre del asistente
* Nombre de la empresa
* Rubro del negocio
* Propuesta de valor

Puedes editar cualquiera de estos datos, o continuar sin cambios.

Haz clic en **Continuar**.

![Confirmar negocio](<../.gitbook/assets/image png Dec 26 2025 01 51 33 6180 PM.png>)
{% endstep %}

{% step %}
### Seleccionar zona horaria

* Elige tu **zona horaria**.
* Haz clic en **Completar**.

Esto es clave para:

* Agendamientos
* Recordatorios
* Confirmaciones automáticas

Una vez completado este paso debes hacer click en siguiente.

![Zona horaria](<../.gitbook/assets/image png Dec 26 2025 01 52 09 6578 PM.png>)

![Siguiente](<../.gitbook/assets/image png Dec 26 2025 01 53 50 8902 PM.png>)
{% endstep %}

{% step %}
### Revisar asistentes y etapas creadas

Verás un **preview** con:

* Las etapas del embudo
* Los asistentes asignados a cada etapa

👉 Recomendación: **No modificar nada en este punto.** Más adelante podrás cambiar nombres, instrucciones o asistentes con mayor control.

Haz clic en **Siguiente**.

![Revisión asistentes y etapas](<../.gitbook/assets/image png Dec 26 2025 01 54 27 5130 PM.png>)
{% endstep %}

{% step %}
### Seleccionar o crear el tipo de ticket

Aquí defines el tipo de ticket que usará el embudo:

* Si ya tienes uno, selecciónalo.
  *   Haz click en **Agregar Campos**.

      ![Agregar campos](<../.gitbook/assets/image png Dec 26 2025 01 56 50 7834 PM.png>)
  * Selecciona los campos a recolectar.
* Si no tienes ninguno:
  *   Haz clic en **Crear tipo de ticket**.

      ![Crear tipo de ticket](<../.gitbook/assets/image png Dec 26 2025 01 57 48 6493 PM.png>)
  * Asigna un nombre.
  * Decide si usarás **monto** o no.
  * Selecciona los **campos del ticket**.

📌 Importante: estos campos son los **datos que la inteligencia artificial recopilará** durante la conversación.

Si necesitas crear un campo nuevo, revisa:\
👉 [_Cómo crear campos de datos en Vambe_](https://academy.vambe.ai/c%C3%B3mo-crear-un-campo-en-vambe)

_Una vez completada debes hacer click en siguiente_
{% endstep %}

{% step %}
### Acciones automáticas (recomendado dejar por defecto)

Vambe configurará acciones automáticas como:

* Seguimiento por inactividad
* Mensajes cuando el cliente deja de responder
* Movimientos automáticos entre etapas

👉 Recomendación: Déjalas **tal como vienen**. Están pensadas para cubrir los casos más comunes.

Haz clic en **Siguiente**.

![Acciones automáticas](<../.gitbook/assets/image png Dec 26 2025 01 59 00 2872 PM.png>)
{% endstep %}

{% step %}
### Revisión final y creación del embudo

En el resumen final podrás revisar:

* Tipo de negocio
* Tipo de ticket
* Etapas creadas
* Asistentes asignados
* Acciones automáticas

Si todo está correcto, haz clic en **Crear**.

![Resumen final](<../.gitbook/assets/image png Dec 26 2025 01 59 26 3738 PM.png>)
{% endstep %}
{% endstepper %}

***

## Resultado final

![Resultado final](<../.gitbook/assets/image png Dec 26 2025 01 37 33 8120 PM.png>)

✅ Tu embudo de agendamiento queda creado automáticamente con:

* Etapas listas
* Asistentes funcionando
* Integración preparada
* Estructura lista para conectar canales

A partir de aquí puedes:

* Personalizar los asistentes
* Ajustar instrucciones
* Revisar en detalle los pasos 0, 1, 2 y 3
* [Configurar notificaciones y recordatorios](https://academy.vambe.ai/paso-1-configuraciones-recordatorio)
* [Crear tus agentes y notificaciones](https://academy.vambe.ai/c%C3%B3mo-crear-usuarios-en-vambe)

{% hint style="info" %}
Importante: Para que comiences a recibir mensajes, debes [conectar tus canales](https://academy.vambe.ai/canales#main-content)
{% endhint %}
