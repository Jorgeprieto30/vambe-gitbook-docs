---
description: >-
  Asegura la calidad de tus datos. Configura "candados" para que la IA (o tu
  equipo) no pueda ingresar a un cliente en una etapa específica sin tener los
  datos obligatorios completos, incluyendo ahora campos de contacto.
---

# Campos Requeridos: Datos obligatorios por etapa

La funcionalidad de **Campos Requeridos** actúa como un filtro de calidad en tu embudo de ventas. Te permite definir qué información es **obligatoria para entrar** a una etapa específica, incluyendo ahora **campos de contacto**. Esto permite una personalización más profunda en la recolección de datos por fase del proceso.

**La Regla de Oro**: Los campos son requeridos para **ENTRAR** a la etapa.

* Si la IA intenta mover a un cliente a "Cotización", primero verificará si tiene los datos que exige "Cotización".
* Si tú mueves manualmente un ticket a "Cotización", el sistema te pedirá rellenar esos datos manualmente.

{% hint style="danger" %}
**Requisito Previo**: El Campo (Dato), ya sea personalizado o de contacto, debe existir previamente en Vambe y estar asociado al Ticket. _Si aún no los has creado:_ 👉 [\\[Cómo crear campos personalizados y asignarlos al Ticket\\]](https://academy.vambe.ai/crm/gestion-de-campos-y-datos-a-recopilar)
{% endhint %}

***

#### 1. ¿Cómo funciona la lógica de la IA?

Cuando tu Asistente IA decide que es momento de avanzar a un cliente (ej: el cliente pide cotizar), el sistema ejecuta una validación de seguridad sobre la etapa de destino:

1. **Intento de Cambio**: La IA ejecuta la función `change_stage` para mover al cliente a la etapa objetivo (ej: "Pendiente Enviar Cotización").
2. **Verificación de Destino**: El sistema revisa: _"¿Esta etapa de destino exige algún dato obligatorio?"_.
3. **Extracción Inteligente** (Gemini Flash):
   * Si el dato falta (ej: RUT), la IA analiza toda la conversación histórica y las herramientas usadas previamente para ver si el cliente ya lo mencionó.
   * Si lo encuentra, lo guarda automáticamente y autoriza la entrada a la etapa.
4. **Solicitud Activa**:
   * Si el dato no existe en el chat, el sistema bloquea el cambio de etapa.
   * La IA, en lugar de mover al cliente, le responde solicitando el dato faltante.

> Ejemplo:
>
> * Meta: Entrar a la etapa "Pendiente Cotización" (Requiere: RUT).
> * Acción: La IA detecta que falta el RUT.
> * Respuesta al cliente: _"Para generarte la cotización formal y avanzar, necesito que me ayudes con tu RUT por favor."_

***

#### 2. Configuración Paso a Paso

Para activar estos requisitos de entrada, sigue estos pasos:

1.  Ingresa a tu Embudo y haz clic en el icono de Lápiz (Editar Embudo) arriba a la derecha.\
    <br>

    <figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>


2.  Selecciona la pestaña Tickets.<br>

    <figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>


3. Ubica la columna de la Etapa de Destino (la etapa a la cual quieres ponerle requisitos de entrada).
4. Activa el interruptor "Campos requeridos".
5. Selecciona en la lista los datos (incluyendo campos de contacto) que deben estar llenos para permitir la entrada.

<figure><img src="../.gitbook/assets/image (13).png" alt="" width="563"><figcaption></figcaption></figure>

6. Haz clic en Guardar cambios.<br>

<figure><img src="../.gitbook/assets/Captura de pantalla 2026-02-03 a la(s) 11.55.06 a.m..png" alt=""><figcaption></figcaption></figure>

***

#### 3. Movimientos Manuales vs. IA

Es importante entender cómo afecta esto a tu operación diaria:

*   🤖 Movimiento por IA: Es 100% automático. La IA busca el dato en el chat. Si no está, se lo pide al cliente de forma natural en la conversación.\
    <br>

    <figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>



* 👤 Movimiento Manual (Agente): Si tú arrastras un ticket manualmente hacia una etapa con requisitos, el sistema detectará que falta el dato y abrirá una ventana emergente obligándote a rellenarlo manualmente en ese momento. No podrás soltar el ticket en esa etapa hasta completar la información.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

***

#### 4. Visualización en Logs (Field Extraction)

Puedes monitorear cómo la IA busca esta información revisando los logs de conversación o el Playground. Verás un evento llamado FIELD\_EXTRACTION.

* Required fields: Muestra qué pedía la etapa de destino.
* Missing fields: Muestra qué no encontró.
* Message sent to user: Muestra la pregunta que generó para pedir el dato.
