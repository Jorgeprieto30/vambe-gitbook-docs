# Gestión de etiquetas y asignación automática (V2)

{% hint style="warning" %}
**La configuración del bloque de Etiquetas descrita en este artículo corresponde al Asistente con Bloques (V2), la versión anterior de los Asistentes IA de Vambe.**

La creación de etiquetas en el CRM es transversal y aplica a cualquier asistente. En los **Asistentes con Escenarios (V3)**, las Etiquetas se configuran desde los bloques de identidad del asistente.

[Conocer los Asistentes con Escenarios (V3)](../asistentes-con-escenarios-v3/asistentes-con-escenarios-v3-que-son-y-cuando-usarlos.md)
{% endhint %}

## Gestión de etiquetas y asignación automática

En este artículo aprenderás qué son las etiquetas, cómo crearlas, cómo asignarlas manualmente y cómo configurarlas para que se asignen de forma automática durante una conversación.

Las etiquetas te permiten **clasificar contactos o tickets**, facilitando el seguimiento, la segmentación y la organización del trabajo del equipo.

***

**¿Qué son las etiquetas y para qué sirven?**

Las etiquetas son marcadores que se pueden asignar para identificar características relevantes de:

* **Un contacto** (por ejemplo: tipo de cliente).
* **Un ticket** (por ejemplo: nivel de interés o tamaño de oportunidad).

👉 Es muy importante definir desde el inicio **si una etiqueta pertenece al contacto o al ticket**, ya que esto determina dónde se verá y cómo se utilizará.

![Ejemplo de etiquetas](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/G0UZX3fGV8BjRqmhOJNF/image%20png%20Dec%2019%202025%2001%2004%2002%203752%20PM.png)

***

**Crear una etiqueta**

{% stepper %}
{% step %}
**Paso: Acceder a la sección de Etiquetas**

* Ve al menú lateral izquierdo.
* Ingresa a **CRM**.
* Haz clic en **Etiquetas**.
{% endstep %}

{% step %}
**Paso: Crear nueva etiqueta**

* Haz clic en **Crear etiqueta**.
{% endstep %}

{% step %}
**Paso: Definir parámetros de la etiqueta**

Al crearla, deberás definir:

* **Tipo de etiqueta**
  * Contacto → se guarda a nivel del cliente.
  * Ticket → se guarda a nivel de la conversación/proceso.
* **Nombre de la etiqueta** (claro y descriptivo).
* **Color**, para identificarla visualmente.

![Crear etiqueta](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/VAkuo8yngxsYISG5KjZO/image%20png%20Dec%2019%202025%2001%2009%2025%201794%20PM.png)
{% endstep %}

{% step %}
**Paso: Finalizar creación**

Cuando esté todo listo, haz clic en **Crear**.

La etiqueta quedará disponible para ser usada.

![Etiqueta creada](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/P3ftY8ivSlYZwM17Z76k/image%20png%20Dec%2019%202025%2001%2011%2027%208765%20PM.png)
{% endstep %}
{% endstepper %}

***

{% hint style="info" %}
A tener en cuenta: define claramente si una etiqueta pertenece al contacto o al ticket, porque eso determina dónde se verá y cómo se utilizará.
{% endhint %}

***

**Asignar etiquetas de forma manual**

Puedes asignar etiquetas manualmente de dos maneras, según su tipo:

{% stepper %}
{% step %}
**Etiquetas de tipo ticket**

* Abre el ticket del contacto.
* Ve a la parte superior derecha (información del ticket).
* Busca la sección **Etiquetas**.
* Haz clic en **Agregar** y selecciona la etiqueta.

![Etiquetas en ticket](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/8sKijykYBixuOUse8HNV/image%20png%20Dec%2019%202025%2001%2015%2000%202974%20PM.png)
{% endstep %}

{% step %}
**Etiquetas de tipo contacto**

* Abre el ticket.
* Ve a la información del **Contacto**.
* En la sección de etiquetas del contacto, haz clic en **Agregar**.
* Selecciona la etiqueta correspondiente.

![Etiquetas en contacto](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/hyTd8N0l0yqXz9ugSOmA/image%20png%20Dec%2019%202025%2001%2018%2005%207399%20PM.png)

📌 Las etiquetas de contacto se mantienen incluso si el ticket se cierra.
{% endstep %}
{% endstepper %}

***

**Asignación automática de etiquetas**

Además de asignarlas manualmente, las etiquetas pueden **asignarse automáticamente durante una conversación**, según criterios definidos. Para esto, es necesario configurarlo dentro de un asistente de IA.

***

**Configurar etiquetas automáticas en un asistente**

{% stepper %}
{% step %}
**Paso: Acceder al asistente**

1. [Ingresa al Asistente donde quieres que ocurra la asignación.](como-ingresar-al-asistente-de-inteligencia-artificial.md)
{% endstep %}

{% step %}
**Paso: Agregar bloque de Etiquetas**

* En el menú lateral del asistente, haz clic en **Agregar otro bloque**.

![Agregar bloque](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/FW5Tmk1ZM0nwb1gD4t0r/image%20png%20Dec%2019%202025%2001%2020%2039%209509%20PM.png)

* Selecciona el bloque **Etiquetas**.
  * Si no existe, haz clic en **Crear bloque**.

![Crear bloque etiquetas](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/7EfgaXoVL2VzVwjmk8am/image%20png%20Dec%2019%202025%2001%2021%2053%201714%20PM.png)
{% endstep %}

{% step %}
**Paso: Configurar el bloque**

Dentro del bloque:

* **Lado izquierdo:** selecciona la etiqueta que se asignará.
* **Lado derecho:** escribe la instrucción que explica _cuándo_ debe asignarse esa etiqueta.

![Configurar bloque etiquetas](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/SRzVE1BCh0Yil54C3NK8/image%20png%20Dec%2019%202025%2001%2022%2055%207532%20PM.png)
{% endstep %}

{% step %}
**Paso: Guardar y activar**

1. Haz clic en **Guardar**.
2. Verifica que el bloque de etiquetas aparezca activo en el asistente.
{% endstep %}
{% endstepper %}

***

**Ejemplo práctico (expandible)**

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

**¿Qué ocurre después?**

Una vez configurado:

* El asistente comenzará a **asignar etiquetas automáticamente**.
* No es necesario indicar explícitamente que se guarden.
* Las etiquetas aparecerán en el ticket o en el contacto según el tipo definido.

Esto permite clasificar clientes y oportunidades sin intervención manual, manteniendo orden y consistencia.

***

**Resumen rápido**

* Las etiquetas sirven para clasificar **contactos o tickets**.
* Primero debes **crear la etiqueta** y definir su tipo.
* Se pueden asignar:
  * Manualmente desde el ticket o el contacto.
  * Automáticamente mediante un bloque de etiquetas en un asistente.
* La descripción del bloque define **cuándo** se asigna cada etiqueta.
* Una vez activo, el etiquetado ocurre de forma automática durante las conversaciones.
