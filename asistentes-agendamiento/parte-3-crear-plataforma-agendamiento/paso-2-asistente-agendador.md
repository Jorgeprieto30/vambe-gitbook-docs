---
cover: ../.gitbook/assets/Portada 13.png
coverY: 0
---

# Paso 2: Asistente Agendador

En este artículo aprenderás a crear y configurar el **asistente de agendamiento**, que es el encargado de **buscar disponibilidad, confirmar datos del paciente y agendar una cita** de forma automática.

Este asistente se asigna a la etapa **Agendamiento** del embudo y trabaja en conjunto con el asistente de “Información y dudas generales” creado en la Parte 1.

{% hint style="warning" %}
Antes de comenzar, asegúrate de que:

* Las etapas del embudo ya estén creadas.
* Ya exista el asistente de la etapa inicial (Parte 1).
* Tengas configurada e integrada tu plataforma de agenda (Dentalink, AgendaPro, Reservo, etc.).
{% endhint %}

{% stepper %}
{% step %}
### Crear el asistente

1. Ve al menú lateral izquierdo y entra en **Asistentes**.
2. Haz clic en **Crear asistente** (arriba a la derecha).

![](<../.gitbook/assets/image (7).png>)

3. Asigna un **nombre claro** (por ejemplo: _Info y dudas generales_).
4. Selecciona el modelo de inteligencia artificial recomendado según tu plan.
5. Haz clic en **Crear asistente**.

Una vez creado, comenzaremos a configurar sus bloques.\
Si ya tienes tu asistente creado, accede a:\
https://academy.vambe.ai/c%C3%B3mo-ingresar-al-asistente-de-inteligencia-artificial?hsLang=es

Para agregar bloques ve al menú de la izquierda y haz click en "agregar bloque".

![](../.gitbook/assets/image\(1\).png)
{% endstep %}

{% step %}
### Configurar los bloques de identidad (bloques compartidos)

En este asistente reutilizaremos varios bloques del asistente anterior para mantener coherencia y ahorrar tiempo.

{% hint style="info" %}
Al reutilizar un bloque existente, este pasa a ser **compartido**. Cualquier cambio que hagas en ese bloque se reflejará automáticamente en todos los asistentes que lo usen.
{% endhint %}

#### Bloque de Personificación (compartido)

* Dentro del asistente, haz clic en **Agregar otro bloque**.
* Selecciona **Personificación**.
* Elige el mismo bloque de personificación usado en el asistente de la Parte 1.
* Click en "Usar bloque compartido".

#### Bloque de Objetivo (nuevo para agendamiento)

Objetivo recomendado para el asistente de agendamiento:

* Verificar disponibilidad de horarios.
* Confirmar los datos del paciente (nombre, fecha, hora, ubicación y correo).
* Agendar citas correctamente en la plataforma de reserva.
* Entregar indicaciones básicas posteriores al agendamiento.

![](<../.gitbook/assets/image png Dec 22 2025 01 42 57 4193 PM.png>)

#### Bloque de Formato de respuesta (compartido)

* Agrega el bloque **Formato de respuesta**.
* Selecciona el mismo bloque utilizado en el asistente anterior.

Con esto finalizamos los **bloques de identidad**.
{% endstep %}

{% step %}
### Configurar los bloques de instrucción

Aquí definimos **cómo actúa el asistente** y en qué orden.

#### Bloque: Pasos a seguir

Este bloque es el flujo principal del asistente de agendamiento. Incluye llamadas a funciones clave como:

* Buscar información del paciente.
* Buscar disponibilidad.
* Crear una reserva.

⚠️ Importante: en este bloque **no se agregan directamente las funciones**. Estas se configuran más adelante en el bloque **Aplicaciones de reserva**.

Tip: en el subpaso 2.1 puedes definir qué datos pedir al cliente (RUT, correo, teléfono, etc.) y ajustar esto según tu operación.

Se recomienda agregar una imagen de ejemplo con la estructura completa de los pasos.



<figure><img src="../.gitbook/assets/image png Dec 22 2025 01 44 20 7010 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image png Dec 22 2025 01 44 59 4038 PM.png" alt=""><figcaption></figcaption></figure>

<br>

Importante: una vez agendado, debes ejecutar la función "Cambio de etapa a agendados" para que el cliente pase al siguiente asistente una vez agendado.

#### Bloque: Caso posible “Paso a Agendados” (compartido)

* Usa el mismo bloque compartido creado en la Parte 1.
* Detecta clientes que:
  * Ya tienen una cita.
  * Quieren reagendar o cancelar.
  * Preguntan por su hora.\
    Acción: Ejecutar la función **Cambiar de etapa a Agendados**.

#### Bloque: Caso posible “Todos” (compartido)

* Reutilízalo también. Detecta:
  * Dudas complejas.
  * Solicitud de hablar con una persona.
  * Casos urgentes.\
    Acción: Ejecutar la función **Cambiar de etapa a Ayuda humana**.

Si tienes dudas sobre estos bloques, referencia el artículo de la **Parte 1**.

#### Bloque: No hacer (compartido)

Reutiliza el mismo bloque de límites del asistente inicial, por ejemplo:

* No confirmar citas sin datos completos.
* No inventar disponibilidad.
* No prometer resultados.
* No entregar diagnósticos.
{% endstep %}

{% step %}
### Bloques de información (compartidos)

En este asistente también se utilizan los mismos bloques de información:

* Tratamientos.
* Especialistas.
* Propuesta de valor.
* Ubicación, horarios, etc.

Si necesitas ayuda para crear estos bloques, referencia el artículo de la **Parte 1**.
{% endstep %}

{% step %}
### Bloque nuevo – Aplicaciones de reserva

Este es el **único bloque nuevo** de este asistente.

#### Configuración del bloque

1. Agrega el bloque **Aplicaciones de reserva**.

![](<../.gitbook/assets/image png Dec 22 2025 01 47 40 0962 PM.png>)

2.  **Pestaña Configuración**<br>

    <figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

    * Selecciona el **token** de la clínica.
    * Selecciona la **Sucursal**.
    * Define la **Zona Horaria**.
    * Define el estado en que quedará el cliente tras agendar.<br>

    **Pestaña Servicios**<br>

    <figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

    * Aquí verás todos los tratamientos y profesionales cargados desde tu plataforma de agenda.
    * Usa la barra de búsqueda para encontrar rápidamente un tratamiento o profesional específico.

    ### Sincronización

    Una vez completada la configuración, haz clic en **Sincronizar**.<br>

    Para clínicas con muchos tratamientos y servicios, la sincronización puede tomar varios minutos. Por eso puedes ingresar tu **correo electrónico** antes de sincronizar: recibirás una notificación cuando el proceso termine y podrás seguir trabajando en segundo plano sin quedarte esperando en la pantalla.

    Una vez finalizada la sincronización, haz clic en **Importar datos** para cargar la información sincronizada en el bloque.

    > ⚠️ **Dentalink es la excepción:** su sincronización ocurre de forma directa en el bloque y toma solo unos segundos. Verás un aviso indicando que no debes abandonar la vista hasta que termine.

    Al sincronizar se cargarán:

    * Tratamientos
    * Profesionales
    * Disponibilidad

#### Configuración de ejecución de funciones

En la parte inferior del bloque deberás definir:

* **Cuándo obtener información del cliente** → Cuando el cliente entrega su RUT u otro identificador.
* **Cuándo obtener disponibilidad** → Cuando el cliente indica que quiere buscar una hora.
* **Cuándo crear una reserva** → Cuando el cliente ya eligió fecha y horario.

Se recomienda incluir una imagen de referencia con esta configuración.

![](<../.gitbook/assets/image png Dec 22 2025 01 59 20 4468 PM.png>)
{% endstep %}

{% step %}
### Guardar y asignar el asistente a la etapa

Tu asistente Agendador ya está creado. Debería verse así:

![](<../.gitbook/assets/image png Dec 22 2025 02 01 45 2630 PM.png>)

Pasos para asignarlo:

1. Haz clic en **Guardar** dentro del asistente.
2. Ve al **Embudo**.
3. En la etapa **Agendamiento**, haz clic en la tuerca.
4. Selecciona **Editar etapa**.
5. Desactiva el switch **Etapa humana**.
6. Selecciona el asistente de agendamiento.
7. Guarda los cambios.

Si tienes dudas de cómo asignar el asistente a una etapa, puedes ir leer este artículo dando click [aquí](https://academy.vambe.ai/c%C3%B3mo-asignar-un-asistente-de-inteligencia-artificial-a-una-etapa-del-embudo)
{% endstep %}
{% endstepper %}
