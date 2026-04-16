---
description: >-
  Organiza el trabajo de tu equipo. Aprende a asignar tickets automáticamente a
  tus agentes usando distintas estrategias (al azar, balanceado, en orden) y
  configura alertas para que no se pierda ninguno
---

# Cómo elegir qué agente recibe un ticket y activar notificaciones automáticas

En Vambe puedes asignar agentes de forma automática a las etapas humanas de tu embudo y definir qué notificaciones recibirá cada uno. Esto permite organizar el trabajo del equipo y asegurarse de que siempre haya alguien atendiendo los tickets a tiempo.

> ⚠️ **Nota:** Este proceso solo puede hacerlo un superadministrador o el owner de la cuenta.

***

### Asignación automática de agentes en una etapa

La asignación automática sirve para que, cada vez que un ticket entre a una etapa humana, Vambe decida quién será el agente encargado. Puedes crear lógicas de asignación y reutilizarlas en distintas etapas sin tener que configurarlas desde cero cada vez.

#### ¿Dónde se configura?

1. Ve a tu **Embudo**.
2.  Identifica la etapa donde quieres configurar la asignación (Ej: _Pendiente enviar cotización_, _Atención Humana_).<br>

    <figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>


3. Haz clic en la **tuerca de Configuraciones** de esa etapa.
4.  Entra en **Asignación automática**.\
    <br>

    <figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

Al ingresar, verás un panel con dos opciones:

* **En blanco** — para crear una nueva lógica desde cero.
* **Creaciones anteriores** — para reutilizar una configuración que ya habías guardado.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

***

### Crear una nueva asignación (Paso a Paso)

1. Haz clic en **En blanco**.
2. **Nombre:** Dale un nombre descriptivo a este grupo. Ej: _"Equipo de Ventas Chile"_. Este nombre te servirá para identificar y reutilizar esta asignación en otras etapas.
3. **Estrategia de asignación:** Elige cómo Vambe repartirá los tickets (ver sección siguiente).
4. **Seleccionar ejecutivos:** Busca y marca a los agentes que formarán parte de este grupo.
5. Haz clic en **Crear** (abajo a la derecha).

***

### Estrategias de asignación disponibles

| Estrategia         | Descripción                                                                                      |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| 🔀 **Al azar**     | Asigna tickets de forma completamente aleatoria. Todos los agentes tienen la misma probabilidad. |
| ⚖️ **Balanceado**  | Asigna al agente con menos conversaciones abiertas en ese momento.                               |
| 🔢 **En orden**    | Asigna de forma secuencial: Agente 1 → Agente 2 → Agente 3 → vuelve a empezar.                   |
| 👤 **Directo**     | Asigna el ticket a un único ejecutivo específico. Solo permite seleccionar un agente.            |
| 👤❌ **Desasignar** | Elimina cualquier asignación previa cuando el ticket entra a la etapa.                           |
| 🚫 **Sin acción**  | No realiza ninguna asignación. Útil como resultado de una condición que no debe generar acción.  |

***

### Asignación Condicional (Nuevo)

La estrategia **Condicional** es el modo más avanzado. Permite enrutar contactos a diferentes agentes o equipos según reglas de negocio específicas — sin necesidad de herramientas externas como n8n.

#### ¿Para qué sirve?

* Asignar según **turno horario**: mañana a un equipo, tarde a otro.
* Asignar según el **valor del ticket** o lead score.
* Asignar según **campos personalizados** del contacto o ticket.
* Garantizar que ningún cliente quede sin atención gracias a una **regla de respaldo (Default)**.

#### ¿Cómo funciona?

La asignación condicional evalúa una lista de **reglas en orden, de arriba hacia abajo**. Cuando un ticket entra a la etapa, el sistema revisa cada regla hasta encontrar la primera que se cumpla y ejecuta la asignación correspondiente. Si ninguna regla aplica, se ejecuta la **regla Default**.

#### Configuración paso a paso

**1. Seleccionar el tipo Condicional**

Al crear una nueva asignación, selecciona el tipo **Condicional** en lugar de una estrategia simple.

**2. Crear reglas**

Haz clic en **Agregar regla**. Cada regla tiene tres partes:

* **Nombre:** Un identificador para esa regla. Ej: _"Celular AM"_, _"Leads alto valor"_.
* **Condiciones:** Los filtros que deben cumplirse para activar esta regla.
* **Estrategia + Ejecutivos:** Qué hacer si se cumplen las condiciones.

**3. Configurar las condiciones**

Puedes basar las condiciones en distintos tipos de datos:

| Tipo de condición          | Ejemplos de uso                        |
| -------------------------- | -------------------------------------- |
| **Contexto de asignación** | Hora actual, día de la semana          |
| **Datos del ticket**       | Monto, moneda, puntaje, tipo de ticket |
| **Campo de contacto**      | Cualquier campo asignado al contacto   |
| **Campo personalizado**    | Variables propias de tu cuenta         |

Cada condición permite operadores como _igual a_, _menor que_, _mayor que_, _no es uno de_, entre otros.

Puedes agregar **múltiples condiciones** dentro de una regla y elegir si deben cumplirse todas (**Y**) o al menos una (**O**).

**Ejemplo:**

* Condición 1: Hora actual es menor que 12:00 **Y**
* Condición 2: Campo personalizado "Dispositivo" es igual a "Celular" → Si se cumple → Sin acción (o la estrategia que elijas)

**4. Elegir la estrategia de la regla**

Cada regla tiene su propia estrategia independiente: Al azar, Balanceado, En orden, Directo, Desasignar o Sin acción.

**5. Regla Default (Fallback)**

Siempre existe una regla **Default** al final de la lista. Esta se ejecuta cuando ninguna de las reglas anteriores se cumple. Puedes configurarla como:

* Sin acción (nadie asignado si no hay match).
* Un agente de respaldo específico que siempre reciba los casos no cubiertos.

**6. Ordenar las reglas**

Puedes arrastrar las reglas para cambiar el orden de evaluación. El sistema las revisa de arriba hacia abajo, por lo que el orden importa.

#### Vista resumen de la asignación condicional

Una vez configurada, al entrar a la asignación desde la etapa verás un panel con:

* **Nombre y tipo** de la asignación.
* **Lista de reglas** con su estrategia, número de condiciones y ejecutivos asignados.
* **Etapas compartidas** — cuántas etapas usan esta misma configuración.
* Botones para **editar**, **cambiar asignación** o **quitar de esta etapa**.

***

### ¿Cómo reutilizar una asignación en otra etapa?

Si quieres que el mismo grupo o la misma lógica condicional aplique en otra columna del embudo:

1. Ve a **Configuraciones** de la nueva etapa → **Asignación automática**.
2. En **Creaciones anteriores**, busca la tarjeta con el nombre que guardaste.
3. Haz clic en ella y presiona **Agregar a la etapa**.

> 💡 Si usas una asignación condicional que evalúa campos del ticket, asegúrate de que esos campos existan y se llenen en todas las etapas donde la reutilices.

***

#### Configurar notificaciones para agentes <a href="#configurar-notificaciones-para-agentes" id="configurar-notificaciones-para-agentes"></a>

Una vez configurada la asignación automática, puedes decidir quién será notificado y en qué situaciones.

**¿Dónde se configura?**

1. En la misma etapa, vuelve a **Configuraciones**.
2. Entra a **Notificaciones**.

<figure><img src="https://academy.vambe.ai/~gitbook/image?url=https%3A%2F%2F1206003950-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FPJ99HMo8PHzRCg7pW0PH%252Fuploads%252FJFpt90Iav3p5hNmrPZtG%252Fimage.png%3Falt%3Dmedia%26token%3D88f2ad93-2c4e-4a34-ae86-5328fd3cb595&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=20a7f596&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Aquí puedes elegir:

¿Quién recibe la **notificación**?

* El agente asignado anteriormente
* El owner de la cuenta
* Ambos

<figure><img src="https://academy.vambe.ai/~gitbook/image?url=https%3A%2F%2F1206003950-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FPJ99HMo8PHzRCg7pW0PH%252Fuploads%252FByrEx7QQ17VeX0IC00li%252Fimage.png%3Falt%3Dmedia%26token%3D9a5d4ffd-f345-492b-858f-a73c7a015ff2&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=78eb2fe7&#x26;sv=2" alt=""><figcaption></figcaption></figure>

**¿Dónde recibirán la notificación?**

* Correo electrónico
* **Notificación** dentro de Vambe _(Puedes activar uno o ambos)._

<figure><img src="https://academy.vambe.ai/~gitbook/image?url=https%3A%2F%2F1206003950-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FPJ99HMo8PHzRCg7pW0PH%252Fuploads%252F5gkxwrcO5Vl1KkeveClo%252Fimage.png%3Falt%3Dmedia%26token%3D595e8041-892f-4a67-86ec-91e923b5fe5a&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=9138e4e0&#x26;sv=2" alt=""><figcaption></figcaption></figure>

**¿Qué tipo de notificaciones se pueden activar?**

* **Notificar al entrar a una etapa:** Cuando un ticket llega a esta etapa, se envía una notificación automática. Útil para etapas donde el cliente requiere atención inmediata.
* **Notificar nuevos mensajes:** Envía una notificación cuando un ticket asignado recibe un mensaje nuevo. Ideal para que ningún mensaje quede sin responder.

<figure><img src="https://academy.vambe.ai/~gitbook/image?url=https%3A%2F%2F1206003950-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FPJ99HMo8PHzRCg7pW0PH%252Fuploads%252FUxm3PZF8pOgHGjIeSO1i%252Fimage.png%3Falt%3Dmedia%26token%3D49a1ff87-a82d-41d5-b6b3-592f325ed8fd&#x26;width=768&#x26;dpr=3&#x26;quality=100&#x26;sign=5ad1b54e&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Una vez elegido qué notificaciones activar, presiona **Guardar**.

***

### Resumen final

| Función                    | Descripción                                                                                              |
| -------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Asignación automática**  | Distribuye tickets usando lógicas al azar, balanceadas, en orden, directa, condicional o desasignando.   |
| **Asignación condicional** | Enruta tickets a diferentes agentes según reglas basadas en horario, monto, campos personalizados y más. |
| **Reutilización**          | Guarda grupos y lógicas para aplicarlas en múltiples etapas sin reconfigurar.                            |
| **Notificaciones**         | Alerta cuando un ticket entra a una etapa o recibe un mensaje nuevo.                                     |
| **Permisos**               | Solo superadministrador u owner puede configurar esto.                                                   |

💡 **Buena práctica:** Los agentes deben revisar y cerrar sus tickets asignados cuando terminen para que la asignación balanceada funcione correctamente. En la asignación condicional, asegúrate de que los campos usados en las condiciones estén siempre completos para evitar que todos los tickets caigan en el Default.
