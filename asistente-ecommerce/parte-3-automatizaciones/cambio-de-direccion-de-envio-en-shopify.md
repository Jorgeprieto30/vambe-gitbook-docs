# Cambio de dirección de envío en Shopify

Cuando un cliente se equivoca en la dirección de su pedido, normalmente tiene que escribirle a soporte y alguien del equipo entra a Shopify a corregirla a mano. Con esta función, el cliente le escribe directamente al asistente —por ejemplo, "me equivoqué en la dirección de mi pedido"— y Vambe cambia la dirección de envío por él, sin que nadie de soporte tenga que intervenir.

> Para crearla: en el menú de la izquierda, entra a **Asistente** y luego a **Funciones**. Haz clic en **Crear función** y selecciona **Cambiar Dirección de Envío**, dentro de la categoría **Acciones principales**.

***

## Cómo protege al cliente antes de cambiar algo

Antes de tocar cualquier dato, el asistente valida que el número de teléfono desde el que escribe el cliente sea el mismo que quedó registrado en la orden. Si no coincide, no realiza ningún cambio y deriva la conversación a soporte.

***

## Cuándo no permite el cambio

Esta función está diseñada para ser poco permisiva a propósito: prefiere no cambiar la dirección antes que cambiarla mal. No permite modificarla cuando:

* el pedido ya está en preparación o despachado
* el pedido está cancelado o cerrado
* la nueva dirección tiene un costo de envío mayor
* el cambio implica enviar a otro país
* el número de pedido es ambiguo (en ese caso, pregunta cuál es en vez de adivinar)

{% hint style="info" %}
En cualquiera de estos casos, el asistente responde con un mensaje claro explicando por qué no puede hacer el cambio y deriva la conversación.
{% endhint %}

***

## Requisito: actualizar el permiso en Shopify

Para poder cotizar el costo de envío de la nueva dirección antes de aplicarla, Vambe necesita un permiso adicional en Shopify (`read_draft_orders`). Si tu tienda todavía no lo tiene, al configurar la función aparece un aviso con el botón **Actualizar app en Shopify**. Con hacer clic ahí y confirmar los permisos, la función queda lista para usarse — no hace falta ninguna configuración adicional.

\[IMAGEN 1: Modal de configuración de la función mostrando el aviso "Esta tienda necesita actualizar la app de Vambe" con el botón para actualizarla]

***

## Disponibilidad

Esta función está disponible solo para tiendas conectadas por **Shopify**.

***

## En resumen

Cambiar la dirección de envío deja de ser una tarea manual para soporte: el cliente la resuelve directamente por chat, y el asistente solo actúa cuando está seguro de que es seguro hacerlo. Cuando hay cualquier duda —de identidad, de estado del pedido o de costo— prefiere derivar antes que arriesgarse a un error.
