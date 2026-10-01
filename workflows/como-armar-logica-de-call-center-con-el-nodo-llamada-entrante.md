# Cómo armar lógica de Call Center con el nodo Llamada entrante

Hasta ahora, Workflows podía reaccionar a una llamada una vez que esta **terminaba** (con el trigger **Llamada finalizada**), pero no había forma de tomar acciones **mientras el teléfono aún está sonando**, antes de que la llamada se conecte con alguien. El nuevo trigger **Llamada entrante**, junto con los nodos **Rechazar llamada** y **Enrutar llamada**, resuelve esto y permite armar lógica de call center nativa dentro de Vambe.

***

### El trigger: Llamada entrante

Este trigger se activa en cuanto entra una llamada a uno de los **teléfonos de voz** que selecciones —antes de que esa llamada se conecte con un ejecutivo o con la IA. A partir de ahí puedes armar la lógica que necesites: evaluar condiciones, cambiar la etapa del ticket, asignar un ejecutivo, o decidir directamente qué pasa con la llamada.

Al configurarlo, tienes un interruptor clave:

* **Decidir el enrutamiento en este flujo** — si lo activas, los nodos que agregues **antes** del enrutamiento se ejecutan mientras el teléfono suena, y pueden cambiar la etapa, asignar al ejecutivo o rechazar la llamada; los nodos que agregues **después** se ejecutan recién una vez que la llamada ya se conectó.

{% hint style="info" %}
Si dejas este interruptor apagado, la llamada se enruta de forma automática como ocurre hoy —sin que tu flujo decida ese paso—, y el nodo Llamada entrante funciona solo como gatillante para el resto de tu lógica.
{% endhint %}

***

### Los dos nodos nuevos

* **Rechazar llamada** — corta la llamada entrante.
* **Enrutar llamada** — conecta la llamada con un ejecutivo o con IA. Este nodo **solo aparece** si activaste "Decidir el enrutamiento en este flujo" en el trigger Llamada entrante, y existe justamente para asegurar que tus acciones previas (cambiar etapa, asignar ejecutivo, etc.) se ejecuten **antes** de que la llamada se conecte.

***

### Ejemplo: enrutar a IA si el ticket está en etapa humana

Un caso típico de call center: quieres que, apenas entra una llamada, si el ticket todavía está en una etapa atendida por un humano, se mueva automáticamente a una etapa con IA para que la atienda una AI Call; y si no cumple esa condición, se rechace la llamada.

1. **Trigger:** Llamada entrante, con "Decidir el enrutamiento en este flujo" activado.
2. **Condición:** ¿La etapa actual del ticket es una etapa humana?
3. **Si se cumple:** Cambiar etapa (a una etapa con IA) → Enrutar llamada.
4. **Si no se cumple:** Rechazar llamada.

{% hint style="info" %}
La captura de referencia usa nombres de etapa genéricos ("Ganado", "Nuevo") solo para mostrar el nodo en funcionamiento —reemplázalos por las etapas reales de tu embudo.
{% endhint %}

***

### En resumen

El trigger **Llamada entrante** te da una ventana de acción mientras el teléfono aún está sonando: puedes evaluar condiciones, mover el ticket de etapa o asignar un ejecutivo antes de decidir, con **Enrutar llamada**, a quién se conecta —o cortarla directamente con **Rechazar llamada**. Esto desbloquea lógicas de call center —enrutamiento condicional, desborde a IA, rechazo de llamadas fuera de criterio— de forma nativa en Workflows, sin depender de un sistema externo.
