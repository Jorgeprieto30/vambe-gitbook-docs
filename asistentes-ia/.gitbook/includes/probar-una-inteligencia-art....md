---
title: Probar una inteligencia art...
---

{% stepper %}
{% step %}
## Probar una inteligencia artificial individual

Esta opción sirve cuando quieres evaluar solo un asistente en particular, aislado del resto del embudo.

### ¿Cómo hacerlo?

[Debes ingresar al asistente](https://academy.vambe.ai/c%C3%B3mo-ingresar-al-asistente-de-inteligencia-artificial)

### Probar el asistente

Una vez dentro del asistente, verás arriba a la derecha un botón llamado **Probar**.

![](<../assets/image png Dec 03 2025 03 59 21 0818 PM.png>)

Al hacer clic:

* Podrás enviar mensajes de prueba directamente a ese asistente.
* Simularás conversaciones como si ese asistente estuviera atendiendo un cliente real, pero solo dentro de esa etapa.

### Consideraciones importantes

* Esta prueba sirve únicamente para asistentes aislados.
* Si tu embudo usa varias inteligencias artificiales, esta prueba NO muestra cómo fluyen los clientes entre etapas.
* Es ideal para revisar errores puntuales, lógica interna o bloques específicos.
{% endstep %}

{% step %}
## Probar todo el embudo completo (Playground)

Esta es la prueba más representativa del mundo real. Simula a un cliente entrando por primera vez a tu embudo y avanzando etapa por etapa.

### Cómo acceder

{% stepper %}
{% step %}
En el menú izquierdo, entra a **Asistentes**.
{% endstep %}

{% step %}
Selecciona la opción **Playground**.
{% endstep %}

{% step %}
Escribe un mensaje para comenzar la prueba.
{% endstep %}
{% endstepper %}

![](<../assets/image png Dec 03 2025 04 02 15 8775 PM.png>)

### ¿Qué puedes probar aquí?

* El flujo completo del cliente.
* Cómo interactúan todas las inteligencias artificiales entre sí.
* Si las funciones (cambio de etapa, agendamientos, búsquedas, etiquetas, etc.) están operando correctamente.
* Qué ocurre cuando el cliente cumple ciertas condiciones dentro del proceso.

Es la prueba ideal cuando:

* Estás revisando un embudo nuevo.
* Hiciste cambios recientes en pasos a seguir o casos posibles.
* Necesitas validar la experiencia completa del usuario.
{% endstep %}

{% step %}
## Probar con IA (simulación automatizada)

Esta opción permite generar pruebas automáticas, donde múltiples perfiles simulados interactúan con tu embudo al mismo tiempo. Es una forma avanzada de testeo que ayuda a identificar errores que podrían pasarse por alto en pruebas manuales.

### Cómo acceder

{% stepper %}
{% step %}
En el menú izquierdo, entra a **Asistentes**.
{% endstep %}

{% step %}
Haz clic en **Probar con IA**.
{% endstep %}
{% endstepper %}

![](<../assets/image png Dec 04 2025 02 22 50 5392 PM.png>)

### Cómo ejecutar un test

{% stepper %}
{% step %}
Haz clic en **Crear nuevo test**.

![](<../assets/image png Dec 04 2025 02 23 28 6603 PM.png>)
{% endstep %}

{% step %}
Selecciona el embudo que quieres probar.

![](<../assets/image png Dec 04 2025 02 23 58 1378 PM.png>)
{% endstep %}

{% step %}
Elige los **perfiles simulados**.

* Vambe genera algunos perfiles automáticamente.
* Puedes editar perfiles o crear otros completamente nuevos.

![](<../assets/image png Dec 04 2025 02 25 56 1586 PM.png>)
{% endstep %}

{% step %}
Haz clic en **Siguiente** para iniciar las simulaciones.
{% endstep %}
{% endstepper %}

### ¿Qué hace este sistema?

* Simula varias personas hablándole a tu embudo.
* Prueba diferentes rutas, casos posibles y variaciones.
* Recorre todo el flujo buscando inconsistencias.

![](<../assets/image png Dec 04 2025 02 28 46 4196 PM.png>)

### Resultados

Una vez finalizado el test, recibirás:

* Respuestas generadas por los asistentes ante cada situación.
* Alertas de comportamiento inesperado.
* Sugerencias de mejoras en pasos a seguir, casos posibles o información faltante.

![](<../assets/image png Dec 04 2025 02 32 36 8652 PM.png>)
{% endstep %}
{% endstepper %}
