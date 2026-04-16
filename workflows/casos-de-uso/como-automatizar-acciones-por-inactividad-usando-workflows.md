# Cómo automatizar acciones por inactividad usando Workflows

¿Un cliente dejó de responder? ¿Un agente no contestó a tiempo? Ahora puedes detectar esos momentos y actuar automáticamente — todo desde los Workflows, sin necesidad de configurar herramientas separadas.

Los triggers de inactividad te permiten construir flujos que reaccionan al comportamiento real de tus contactos y agentes, haciendo que tus automatizaciones se sientan más naturales y menos robóticas.

***

### ¿Qué son los triggers de inactividad?

Son gatillantes que se activan cuando alguien lleva un tiempo definido sin interactuar en el chat:

| Trigger                      | ¿Cuándo se activa?                                       |
| ---------------------------- | -------------------------------------------------------- |
| **Inactividad del contacto** | Cuando el cliente lleva X tiempo sin enviar un mensaje   |
| **Inactividad del agente**   | Cuando el agente lleva X tiempo sin responder al cliente |

Ambos triggers permiten configurar etapas específicas del embudo, una duración personalizada y Espera Inteligente para respetar horarios hábiles.

***

### Casos de uso típicos

**Con Inactividad del contacto:**

* Reactivar un lead frío que dejó de responder después de 30 minutos.
* Enviar un mensaje de seguimiento si el cliente no contesta tras recibir una cotización.
* Archivar tickets abandonados automáticamente después de 2 días sin actividad.

**Con Inactividad del agente:**

* Reasignar el ticket si el agente no respondió en 4 horas.
* Etiquetar al cliente como "Sin atención" y dejar una nota de alerta.
* Notificar al supervisor cuando un ticket lleva demasiado tiempo sin respuesta.

***

### Cómo configurar un trigger de inactividad

#### Paso 1: Crear el Flow

1. Ve al menú lateral izquierdo → **Workflows** → **Flows**.
2. Haz clic en **Crear Flow**.
3. Haz clic en el nodo de trigger y selecciona el tipo de inactividad que necesitas.

***

#### Paso 2: Configurar el trigger

Al seleccionar **Inactividad del contacto** o **Inactividad del agente**, verás las siguientes opciones:

**Duración:** Define cuánto tiempo debe pasar sin interacción para activar el flujo. Ej: 30 minutos, 4 horas, 1 día.

**Etapas:** Selecciona en qué etapas del embudo se monitorea la inactividad. Solo los contactos que estén en esas etapas activarán el trigger.

**Espera Inteligente:** Actívala si quieres que el tiempo de inactividad solo cuente dentro de tu horario hábil. Define horas activas, días activos y zona horaria.



> 💡 **Ejemplo con Espera Inteligente:** Si un cliente escribe a las 7 PM y configuras inactividad de 30 minutos con horario hábil de 9 AM a 6 PM, el trigger no se activará hasta el día siguiente a las 9 AM — evitando enviar mensajes fuera de horario.

***

#### Paso 3: Agregar acciones

Una vez configurado el trigger, haz clic en **+** para agregar las acciones que se ejecutarán. Puedes usar cualquiera de las acciones disponibles en los Workflows:

* Enviar mensaje con IA
* Enviar plantilla de WhatsApp
* Cambiar de etapa
* Desasignar agente / Asignar nuevo agente
* Crear nota
* Asignar etiqueta
* Ejecutar Webhook
* Y más

***

#### Paso 4: Configurar la cancelación inteligente en las Esperas

Si tu flujo incluye un nodo de **Espera** entre acciones, puedes activar la cancelación automática para que el flujo se detenga si ocurre algo relevante mientras espera:

| Opción                              | Qué hace                                                                                                         |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Cancelar al cambiar de etapa**    | Si el ticket se mueve, la espera se cancela. Evita actuar sobre tickets que ya avanzaron.                        |
| **Cancelar si el contacto escribe** | Si el cliente responde durante la espera, el flujo se detiene. Perfecto para flujos de reactivación.             |
| **Cancelar si un agente escribe**   | Si un agente interviene, el flujo se detiene. Evita que la automatización interfiera con conversaciones activas. |

> 💡 **Buena práctica:** Si usas el trigger de **Inactividad del contacto** y tienes un nodo de espera en el flujo, activa siempre **"Cancelar si el contacto escribe"**. Así el flujo se detiene automáticamente si el cliente responde antes de que se ejecute la siguiente acción.

***

### Ejemplo completo: Reactivar cliente inactivo

**Objetivo:** Si un cliente en la etapa de Calificación no responde en 30 minutos, enviarle un mensaje de reactivación. Si responde antes, cancelar el flujo.

```
Trigger: Inactividad del contacto
  └── Duración: 30 minutos
  └── Etapa: Calificación
  └── Espera Inteligente: Activada (Lun-Vie, 9 AM - 6 PM)

Acción: Espera (5 minutos)
  └── Cancelar si el contacto escribe: ✅

Acción: Enviar mensaje con IA
  └── Prompt: "Reactivar la conversación preguntando amablemente si el cliente sigue interesado."
```

***

### Ejemplo completo: Alerta por agente que no responde

**Objetivo:** Si un agente no contesta en 4 horas, reasignar el ticket y dejar una nota de alerta.

```
Trigger: Inactividad del agente
  └── Duración: 4 horas
  └── Etapa: Pendiente enviar cotización
  └── Espera Inteligente: Activada (Lun-Vie, 9 AM - 7 PM)

Acción: Desasignar agente
Acción: Asignar etiqueta → "Sin atención"
Acción: Asignar agente (balanceado entre el equipo)
Acción: Crear nota → "Cliente sin atención, contactar inmediatamente."
```

***

### Guardar y activar

Una vez armado el flujo, haz clic en **Guardar** (arriba a la derecha). Asegúrate de que el Flow quede en estado **Activo** para que comience a ejecutarse.

***

### Puntos clave a recordar

* Los triggers de inactividad reemplazan completamente a las antiguas Secuencias — toda esa lógica ahora vive en los Workflows.
* La **Espera Inteligente** en el trigger controla cuándo cuenta el tiempo de inactividad. La **cancelación** en el nodo de Espera controla cuándo se detiene el flujo.
* Activa "Cancelar si el contacto escribe" siempre que uses triggers de inactividad del contacto — así la automatización no actúa sobre alguien que ya respondió.
* Si el nuevo agente asignado tampoco responde, el trigger de inactividad del agente se volverá a activar automáticamente — protegiendo al cliente de caer en el olvido.
