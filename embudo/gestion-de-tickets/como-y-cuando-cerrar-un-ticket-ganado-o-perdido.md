---
cover: ../.gitbook/assets/Portada 21.png
coverY: 0
---

# Cómo y cuándo cerrar un ticket (ganado o perdido)

Cuando un cliente nos habla y ese contacto entra a nuestro embudo, automáticamente se forma un ticket. Si yo le escribo a un cliente, el ticket se crea en el embudo y etapa que yo escoja.

Una vez entendido qué es un ticket y cómo funciona dentro del embudo, el siguiente paso es comprender **cuándo** y **cómo** se cierran y se marcan como ganados o perdidos. Esta decisión es clave para mantener el embudo ordenado y para definir la lógica de cada proceso.

***

<details>

<summary>¿Cuándo un ticket se marca como ganado o perdido?</summary>

Antes de configurar cualquier cierre automático, es fundamental definir **qué evento determina el éxito o fracaso del ticket**, es decir, cuándo lo marcamos como **ganado** y cuándo como **perdido**.

Ejemplos:

* **Embudo de ventas:**
  * Ganado: cuando el cliente compra.
  * Perdido: cuando finalmente no realiza la compra.
* **Embudo de agendamiento:**
  * Ganado: cuando el cliente agenda.
  * Perdido: cuando no agenda dentro del plazo definido.

Estos hitos pueden activarse:

* Cuando el ticket entra a una etapa.
* Cuando el ticket sale de una etapa.
* Después de un periodo de tiempo sin actividad.

</details>

***

## Cómo cerrar un ticket

Existen cinco formas principales de cerrar un ticket dentro de la plataforma. Todas se configuran desde la misma sección. A continuación se describen y se muestran los pasos para cada una:

{% stepper %}
{% step %}
### Cierre al entrar a una etapa (ejemplo: Finalizado)

Este método se usa cuando el simple hecho de ingresar a una etapa específica **confirma que el ticket fue exitoso**.

Ejemplo: etapa “Finalizado” en un embudo de agendamiento.

Pasos:

1. Ir a la etapa donde quieres configurar esta acción.
2. Hacer clic en **Configuraciones**.
3. Entrar a **Acciones automáticas**.

![](<../.gitbook/assets/image png 4.png>)

4. En el menú izquierdo, seleccionar **Resolución (Ganado/Perdido)**.
5. En “configurar activación”, seleccionar **Cuando un contacto entre a una etapa**.
6. En el panel derecho, elegir si esa etapa debe marcar el ticket como **ganado** o **perdido**.
7. Activar o desactivar el **switch de cierre de ticket**, según si deseas que el ticket se cierre (archive) automáticamente.

![](<../.gitbook/assets/image png 2.png>)

8. Si se cierra, seleccionar:
   * **Embudo** donde se cerrará.
   * **Etapa de retorno**, normalmente la primera etapa.
9. Guardar la acción automática.

Ahora cuando entre alguien a la etapa "Finalizado"...

![](<../.gitbook/assets/ezgif 7b50f3265ea82399 gif.gif>)
{% endstep %}

{% step %}
### Cierre por tiempo de inactividad (sin respuesta)

Se usa cuando un ticket debe considerarse perdido si el cliente no avanza después de cierto plazo.

Ejemplo: etapa inicial “Información de agendamiento”, donde un cliente que no agenda después de X días se considera no interesado.

Pasos:

1. Entrar a la etapa correspondiente.
2. Ir a **Configuraciones → Acciones automáticas**.

![](<../.gitbook/assets/image png 4.png>)

3. En el menú izquierdo, seleccionar **Resolución (Ganado/Perdido)**.
4. Elegir la opción **tiempo**.
5. Definir el tiempo de espera (ejemplo: 2 días).

![](<../.gitbook/assets/image png Nov 18 2025 09 16 06 1309 PM.png>)

6. Seleccionar si el ticket será marcado como **ganado** o **perdido**.
7. Activar el **cierre de ticket** si corresponde.
8. Seleccionar el embudo y la etapa de retorno.
9. Editar y guardar.
{% endstep %}

{% step %}
### Cierre periódico (por horario o día específico)

Permite cerrar tickets de forma automática cada cierto día y hora, sin depender de un evento puntual del cliente.

Ejemplos:

* Todos los lunes a las 09:00
* Todos los martes a las 16:00

Pasos:

1. Entrar a **Configuraciones → Acciones automáticas** desde la etapa correspondiente.

![](<../.gitbook/assets/image png 4.png>)

2. En el menú izquierdo, ir a **Resolución (Ganado/Perdido)**.

![](<../.gitbook/assets/image png Nov 18 2025 09 20 01 9097 PM.png>)

3. Seleccionar **Periódicamente**.
4. Definir el día y la hora.
5. Elegir si marcar como **ganado** o **perdido**.
6. Activar el **cierre de ticket** si deseas que el ticket se archive.
7. Elegir embudo y etapa de retorno.
8. Guardar la acción.
{% endstep %}

{% step %}
### Cierre manual (desde el ticket)

Es la forma más directa y permite decidir caso por caso.

Pasos:

1. Haz click sobre el ticket para abrirlo.
2. En el menú derecho, ingresar a la sección de **Información del ticket**.
3. Seleccionar si se marca como **ganado** o **perdido**.

![](<../.gitbook/assets/image png Nov 18 2025 09 22 44 8535 PM.png>)

4. Si quieres cerrarlo, activar el **switch de cierre de ticket**.

![](<../.gitbook/assets/image png Nov 18 2025 09 25 01 9731 PM.png>)

5. Seleccionar el embudo y la etapa de retorno.

![](<../.gitbook/assets/image png Nov 18 2025 09 25 01 9731 PM.png>)

6. Guardar los cambios.
{% endstep %}

{% step %}
### Etapas Ganadoras o de Leads Perdidos

Este método se utiliza cuando quieres que una etapa específica del embudo determine automáticamente si un ticket debe considerarse **ganado** o **perdido**, sin necesidad de configurar acciones automáticas adicionales. Una vez marcada como “Ganada” o “Perdida”, cualquier ticket que llegue a esa etapa se resolverá de inmediato según el tipo elegido.

Pasos:

1. Ir al embudo donde deseas configurar esta acción.
2. Seleccionar la etapa que quieres convertir en **etapa ganadora** o **etapa de leads perdidos**.
3. Hacer clic en **Configuraciones** dentro de esa etapa.

![](<../.gitbook/assets/image png Nov 24 2025 09 08 35 4533 PM.png>)

4. Desplazarte hacia abajo hasta encontrar la opción **Cambiar tipo de etapa**.
5. Seleccionar si esa etapa será una:
   * **Etapa Ganada**, o
   * **Etapa Perdida**

![](<../.gitbook/assets/image png Nov 24 2025 09 09 40 2030 PM.png>)

6. Guardar.

Resultado: la etapa cambiará de color para indicar su tipo. Desde ese momento, cada vez que un ticket entre en esa etapa será automáticamente marcado como **ganado** o **perdido**.

![](<../.gitbook/assets/image png Nov 24 2025 09 11 01 4797 PM.png>)
{% endstep %}
{% endstepper %}

***

{% include "../.gitbook/includes/untitled.md" %}

***

## Resumen general

* Primero define **qué significa ganar o perder** un ticket en tu proceso.
* Puedes cerrar tickets automáticamente por:
  * entrada a una etapa,
  * tiempo de inactividad,
  * periodicidad programada,
  * o de manera manual.
* Cada cierre requiere decidir si se activa o no el **switch de cierre de ticket**.
* Todas las configuraciones se hacen desde **Configuraciones → Acciones automáticas → Resolución (ganado/perdido)**.
* El cierre archiva el ticket y deja al contacto listo para generar uno nuevo en el futuro.
