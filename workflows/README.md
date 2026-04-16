# Workflows: Automatización Avanzada

Los **Workflows** son el motor de automatización de Vambe. Similar a herramientas como Zapier, esta funcionalidad te permite crear cadenas de "Causa y Efecto" dentro de la plataforma.

**¿Para qué sirven?** Desde enviar un mensaje de "Fuera de Horario" los fines de semana, hasta encuestar a un cliente 4 días después de una compra en Shopify. Si ocurre "X", Vambe hará "Y".

***

#### 1. Estructura de un Workflow

Para crear uno, dirígete al menú lateral izquierdo Workflows y haz clic en Crear Flow.

Un flujo se compone de tres piezas clave:

1. **Trigger (Gatillante)**: El evento que inicia todo (Ej: "Se asignó una etiqueta").
2. **Condición (Filtro)**: Reglas opcionales para decidir si avanzar o no (Ej: "¿Es fin de semana?").
3. **Acción**: Lo que el sistema hará (Ej: "Enviar mensaje").

<figure><img src=".gitbook/assets/Captura de pantalla 2026-02-06 a la(s) 1.20.34 p.m..png" alt=""><figcaption></figcaption></figure>

***

#### 2. Selecciona tu Trigger (Gatillante)

Lo primero es definir qué debe pasar para que el flujo se active. Vambe ofrece una gran variedad de gatillantes nativos:

**Datos de Contacto/Ticket:**

* **Etiqueta asignada:** Ej: Si etiquetan a alguien como "VIP".
* **Campos actualizados:** Ej: Si cambia el estado de un pedido.
* **Agente asignado:** Cuando se asigna un agente al ticket.
* **Lead score asignado:** Cuando cambia el puntaje del lead.
* **Monto del ticket actualizado:** Cuando se modifica el monto.
* **Estado del ticket cambiado:** Cuando el ticket pasa a ganado, perdido, etc.

**Eventos de Embudo:**

* **Ingreso a etapa / Salida de etapa:** Se activa cuando un ticket entra o sale de una etapa específica.

**E-commerce y Agendamiento (Evento Capturado):** Fundamental para Shopify/WooCommerce. Se activa cuando se crea una orden (Order Created), se recupera un carrito, o se agenda una cita.

**Conversacional:**

* **Mensaje recibido en etapa humana:** Ideal para auto-respuestas cuando el agente no está.
* **Mensaje enviado por un humano:** Se activa cuando un agente envía un mensaje.
* **NPS/CSAT respondido:** Para tomar acciones según la calificación del cliente.
* **Llamada finalizada:** Cuando termina una llamada con el contacto.
* **Reacción a mensaje:** Cuando el contacto reacciona a un mensaje.
* **Inactividad del contacto (Nuevo):** Se activa cuando el contacto lleva un tiempo definido sin enviar un mensaje. Permite configurar etapas específicas, duración y Espera Inteligente para respetar horarios hábiles.
* **Inactividad del agente (Nuevo):** Se activa cuando el agente lleva un tiempo definido sin responder al contacto.

**Externos y Técnicos:**

* **Webhook:** Para recibir señales de tu propio sistema.
* **Trigger Recurrente:** Para ejecutar tareas periódicas. Ej: Cada lunes a las 9 AM.
* **Typeform respondido:** Se dispara automáticamente cuando un cliente completa un formulario de Typeform.
* **Flow activado por IA:** Se activa cuando una función de un asistente lo ejecuta.
* **Evento de error:** Se activa cuando ocurre un error en el flujo.

<figure><img src=".gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

***

#### 3. Agrega Condiciones (Filtros)

Una vez activado el trigger, puedes poner "puertas" lógicas. Si la condición se cumple (Sí), el flujo sigue un camino; si no (No), puede seguir otro o detenerse.

Tipos de condiciones disponibles:

* **Condición de Horario:** "¿Es sábado o domingo?", "¿Son pasadas las 18:00?".
* **Condición de Metadatos:** "¿El precio del producto es mayor a $1.000.000?".
* **Condición de Canal:** "¿El cliente habla por Instagram o WhatsApp?".
* **Evaluar con IA:** Usar inteligencia artificial para decidir si el cliente cumple un requisito complejo.
* **Condición Aleatoria:** Dividir el tráfico 50/50 (A/B Testing).

<figure><img src=".gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

***

#### 4. Ejecuta Acciones

Finalmente, define qué hará Vambe. Puedes encadenar múltiples acciones una tras otra.

#### Contacto / Ticket

* **Asignar etiqueta** / **Desasignar etiqueta**
* **Cambiar etapa**
* **Actualizar campos**
* **Asignar ejecutivo** / **Desasignar ejecutivos**
* **Marcar como ganado o perdido**
* **Cerrar ticket** / **Abrir ticket**
* **Obtener o crear contacto**
* **Actualizar monto del ticket**

#### Conversacional

* **Enviar mensaje con IA:** Genera un mensaje usando inteligencia artificial según el prompt que definas.
* **Enviar plantilla:** Envía un mensaje pre-aprobado de WhatsApp. Ideal cuando han pasado más de 24 horas desde el último mensaje del cliente.
* **Enviar archivo**
* **Enviar mensaje de voz**
* **Crear nota:** Deja una nota interna visible solo para los agentes.
* **Enviar encuesta de feedback:** Envía una encuesta NPS o CSAT directamente al contacto.
* **Enviar mensaje:** Mensaje de texto simple sin IA.
* **Enviar mensaje programado**
* **Activar llamada IA**

#### CRM

* **Obtener ID de deal CRM**
* **Obtener ID de contacto CRM**
* **Asignar ID de entidad CRM**
* **Asignar ID de contacto CRM**

#### General

* **Enviar webhook:** Envía una señal a un sistema externo.
* **Ejecutar función de IA:** Activa una función configurada en un asistente.
* **Crear tarea**
* **Agregar fila a Google Sheet:** Ideal para reportes y registros externos.
* **Ejecutar código:** Para automatizaciones de alta complejidad en Python o Javascript. Los resultados están disponibles en nodos posteriores mediante `data`, `logs` y `errors`.
* **Espera:** Pausa el flujo durante un tiempo definido antes de continuar con la siguiente acción.
* **Cancelar flujo programado:** Cancela un flujo que está en espera antes de que se ejecute.
* **Detener flujo:** Finaliza el flujo en ese punto.

**Cancelación inteligente en el nodo Espera**

El nodo de Espera cuenta con opciones de cancelación automática. Puedes activar una o varias para que la espera se detenga si ocurre algo mientras el flujo está en pausa:

| Opción de cancelación               | Cuándo usarla                                                                                                                        |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| **Cancelar al cambiar de etapa**    | Si el ticket se mueve a otra etapa, la espera se detiene. Evita ejecutar acciones sobre tickets que ya avanzaron.                    |
| **Cancelar si el contacto escribe** | Si el cliente responde durante la espera, se cancela. Ideal para flujos de reactivación.                                             |
| **Cancelar si un agente escribe**   | Si un agente interviene manualmente, el flujo se detiene. Evita que la automatización interfiera con conversaciones humanas activas. |

<figure><img src=".gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

***

#### Ejemplos de uso ("Recetas")

#### 🔔 1. Reactivar cliente inactivo sin interrumpir si ya respondió

**Trigger:** Inactividad del contacto (30 min, etapa: Calificación) **Espera:** 5 minutos → Cancelar si el contacto escribe ✅ **Acción:** Enviar mensaje con IA → _"Reactivar la conversación preguntando si el cliente sigue interesado."_

***

#### 🚨 2. Agente que no responde → Reasignación automática

**Trigger:** Inactividad del agente (4 horas, etapa: Pendiente enviar cotización) **Acción 1:** Desasignar ejecutivos **Acción 2:** Asignar etiqueta → _"Sin atención"_ **Acción 3:** Asignar ejecutivo (balanceado) **Acción 4:** Crear nota → _"Cliente sin atención, contactar inmediatamente."_

***

#### 🛍️ 3. Post-venta inteligente: encuesta + oferta de recompra

**Trigger:** Evento capturado (Order Created) **Espera:** 4 días → Cancelar al cambiar de etapa ✅ **Acción 1:** Enviar encuesta de feedback (NPS) **Trigger 2:** NPS/CSAT respondido **Condición:** ¿Puntaje mayor a 8? **Acción 2 (Si):** Enviar plantilla con oferta de recompra

***

#### 🔥 4. Lead scoring automático con alerta al mejor agente

**Trigger:** Monto del ticket actualizado **Condición:** Monto mayor a $1.000.000 **Acción 1:** Cambiar etapa → _"Prioritario"_ **Acción 2:** Asignar ejecutivo → _agente senior específico_ **Acción 3:** Crear tarea → _"Llamar cliente en menos de 1 hora"_ **Acción 4:** Agregar fila a Google Sheet → registro de leads de alto valor

***

#### 📋 5. Cierre automático de tickets abandonados + registro

**Trigger:** Inactividad del contacto (2 días, etapa: Inicial) **Acción 1:** Marcar como perdido **Acción 2:** Asignar etiqueta → _"Abandonado"_ **Acción 3:** Agregar fila a Google Sheet → Nombre, teléfono, etapa, fecha **Acción 4:** Cerrar ticket

***

#### 5. Modo Test

Antes de lanzar tu workflow al público, utiliza el Modo Test. Esta herramienta te permite simular una conversación y ver paso a paso cómo se activan los triggers y si las condiciones se cumplen o fallan, asegurando que tu lógica sea perfecta antes de afectar a clientes reales.
