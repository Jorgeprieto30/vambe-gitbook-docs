# Gestión de etiquetas y asignación automática

En este artículo aprenderás qué son las etiquetas, cómo crearlas, cómo asignarlas manualmente y cómo configurarlas para que se asignen de forma automática durante una conversación.

Las etiquetas te permiten **clasificar contactos o tickets**, facilitando el seguimiento, la segmentación y la organización del trabajo del equipo.

***

#### ¿Qué son las etiquetas y para qué sirven?

Las etiquetas son marcadores que se pueden asignar para identificar características relevantes de:

* **Un contacto** (por ejemplo: tipo de cliente).
* **Un ticket** (por ejemplo: nivel de interés o tamaño de oportunidad).

👉 Es muy importante definir desde el inicio **si una etiqueta pertenece al contacto o al ticket**, ya que esto determina dónde se verá y cómo se utilizará.

![Ejemplo de etiquetas](<../.gitbook/assets/image png Dec 19 2025 01 04 02 3752 PM.png>)

***

#### Crear una etiqueta

{% stepper %}
{% step %}
### Paso: Acceder a la sección de Etiquetas

* Ve al menú lateral izquierdo.
* Ingresa a **CRM**.
* Haz clic en **Etiquetas**.
{% endstep %}

{% step %}
### Paso: Crear nueva etiqueta

* Haz clic en **Crear etiqueta**.
{% endstep %}

{% step %}
### Paso: Definir parámetros de la etiqueta

Al crearla, deberás definir:

* **Tipo de etiqueta**
  * Contacto → se guarda a nivel del cliente.
  * Ticket → se guarda a nivel de la conversación/proceso.
* **Nombre de la etiqueta** (claro y descriptivo).
* **Color**, para identificarla visualmente.

![Crear etiqueta](<../.gitbook/assets/image png Dec 19 2025 01 09 25 1794 PM.png>)
{% endstep %}

{% step %}
### Paso: Finalizar creación

Cuando esté todo listo, haz clic en **Crear**.

La etiqueta quedará disponible para ser usada.

![Etiqueta creada](<../.gitbook/assets/image png Dec 19 2025 01 11 27 8765 PM.png>)
{% endstep %}
{% endstepper %}

***

{% hint style="info" %}
A tener en cuenta: define claramente si una etiqueta pertenece al contacto o al ticket, porque eso determina dónde se verá y cómo se utilizará.
{% endhint %}

***

#### Asignar etiquetas de forma manual

Puedes asignar etiquetas manualmente de dos maneras, según su tipo:

{% stepper %}
{% step %}
### Etiquetas de tipo ticket

* Abre el ticket del contacto.
* Ve a la parte superior derecha (información del ticket).
* Busca la sección **Etiquetas**.
* Haz clic en **Agregar** y selecciona la etiqueta.

![Etiquetas en ticket](<../.gitbook/assets/image png Dec 19 2025 01 15 00 2974 PM.png>)
{% endstep %}

{% step %}
### Etiquetas de tipo contacto

* Abre el ticket.
* Ve a la información del **Contacto**.
* En la sección de etiquetas del contacto, haz clic en **Agregar**.
* Selecciona la etiqueta correspondiente.

![Etiquetas en contacto](<../.gitbook/assets/image png Dec 19 2025 01 18 05 7399 PM.png>)

📌 Las etiquetas de contacto se mantienen incluso si el ticket se cierra.
{% endstep %}
{% endstepper %}

***

#### Asignación automática de etiquetas

Además de asignarlas manualmente, las etiquetas pueden **asignarse automáticamente durante una conversación**, según criterios definidos. Para esto, es necesario configurarlo dentro de un asistente de IA.

***

#### Configurar etiquetas automáticas en un asistente

{% stepper %}
{% step %}
### Paso: Acceder al asistente

1. [Ingresa al Asistente donde quieres que ocurra la asignación.](https://academy.vambe.ai/v1/docs/asistentes-ia-1)
{% endstep %}

{% step %}
### Paso: Agregar bloque de Etiquetas

* En el menú lateral del asistente, haz clic en **Agregar otro bloque**.

![Agregar bloque](<../.gitbook/assets/image png Dec 19 2025 01 20 39 9509 PM.png>)

* Selecciona el bloque **Etiquetas**.
  * Si no existe, haz clic en **Crear bloque**.

![Crear bloque etiquetas](<../.gitbook/assets/image png Dec 19 2025 01 21 53 1714 PM.png>)
{% endstep %}

{% step %}
### Paso: Configurar el bloque

Dentro del bloque:

* **Lado izquierdo:** selecciona la etiqueta que se asignará.
* **Lado derecho:** escribe la instrucción que explica _cuándo_ debe asignarse esa etiqueta.

![Configurar bloque etiquetas](<../.gitbook/assets/image png Dec 19 2025 01 22 55 7532 PM.png>)
{% endstep %}

{% step %}
### Paso: Guardar y activar

1. Haz clic en **Guardar**.
2. Verifica que el bloque de etiquetas aparezca activo en el asistente.
{% endstep %}
{% endstepper %}

***

#### Ejemplo práctico (expandible)

<details>

<summary>Ver ejemplo práctico</summary>

Supongamos que tienes las etiquetas:

* Pequeño
* Mediano
* Grande

La instrucción podría ser:

* Si el cliente indica una cantidad entre 1 y 5 → asignar **Pequeño**.
* Si indica entre 6 y 10 → asignar **Mediano**.
* Si indica más de 10 → asignar **Grande**.

La IA evaluará la conversación y asignará la etiqueta correcta según lo que el cliente diga.

</details>

***

#### ¿Qué ocurre después?

Una vez configurado:

* El asistente comenzará a **asignar etiquetas automáticamente**.
* No es necesario indicar explícitamente que se guarden.
* Las etiquetas aparecerán en el ticket o en el contacto según el tipo definido.

Esto permite clasificar clientes y oportunidades sin intervención manual, manteniendo orden y consistencia.

***

#### Resumen rápido

* Las etiquetas sirven para clasificar **contactos o tickets**.
* Primero debes **crear la etiqueta** y definir su tipo.
* Se pueden asignar:
  * Manualmente desde el ticket o el contacto.
  * Automáticamente mediante un bloque de etiquetas en un asistente.
* La descripción del bloque define **cuándo** se asigna cada etiqueta.
* Una vez activo, el etiquetado ocurre de forma automática durante las conversaciones.
