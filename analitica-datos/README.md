# Service Level Agreement (SLA): Gestión y Cumplimiento de Tiempos de Respuesta

Evita que tus clientes queden esperando sin respuesta. Con el SLA (Service Level Agreement) en Vambe puedes establecer compromisos internos de tiempo de respuesta para tu equipo, visualizar el estado de cada ticket en tiempo real y analizar el cumplimiento de tu operación con datos concretos.

El SLA no es solo una métrica: es una herramienta de gestión que te permite pasar de una atención reactiva a una operación proactiva, donde cada segundo cuenta para la satisfacción del cliente.

***

### Parte 1: Configuración del SLA

#### Paso 1 — Acceder a la configuración de tickets

El SLA se configura dentro de cada tipo de ticket. Para llegar ahí:

1. Ve al menú lateral izquierdo y selecciona **CRM**.
2. Dentro de CRM, entra a **Configurar Tickets**.
3. Ubica el ticket al que quieres aplicar el SLA y haz clic en **Ir a editar**.

> 💡 Si aún no tienes tickets creados, puedes crear uno nuevo desde esta misma vista con el botón **Crear nuevo ticket**.

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

#### Paso 2 — Abrir el módulo de SLA

Dentro del editor del ticket, verás un panel lateral con la opción **Configurar SLA**. Desde ahí puedes gestionar todas las políticas de tiempo para ese tipo de ticket.

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Antes de crear una política, define:

* **Nombre de la política** — ponle un nombre descriptivo (ej: "**SLA Soporte**").
* **Horario laboral** — asocia un horario para que el temporizador se pause automáticamente fuera del horario de tu equipo (ej: noches y fines de semana). Usa la zona horaria correcta para tu operación.

> ⚠️ **Importante:** El SLA nunca se pausa automáticamente por otros motivos. Si tu equipo está de vacaciones o hay un feriado, debes pausar el SLA manualmente para que no afecte tus métricas.

#### Paso 3 — Configurar las métricas de medición

Puedes activar hasta tres tipos de métricas independientes. Cada una mide una parte distinta del ciclo de atención:

**Primera respuesta** Mide el tiempo desde que el cliente envía su primer mensaje hasta que el agente responde por primera vez. Es la métrica más crítica: nadie quiere esperar mucho para recibir una respuesta inicial.

**Siguiente respuesta** Mide el tiempo de respuesta para cada interacción posterior. Cada vez que el cliente vuelve a escribir, se genera un nuevo evento de SLA de siguiente respuesta.

**Tiempo de resolución** Mide el tiempo total desde que se crea el ticket hasta que se marca como ganado o perdido. Es un SLA más holgado, puede medirse en horas o días en lugar de minutos.

> 💡 **Recomendación para empezar:** Si eres nuevo en esto, activa primero solo la métrica de **Primera respuesta**. Mídela, contrólala y luego avanza con las demás.

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

#### Paso 4 — Definir tiempos y alertas

Para cada métrica activada puedes configurar:

* **Tiempo objetivo** — el tiempo máximo en que quieres generar esa respuesta (ej: 30 minutos para soporte).
* **Tiempo de advertencia** — cuándo quieres que el sistema te avise antes de incumplir (ej: alerta a los 20 minutos si el objetivo es 30).
* **Modo de visualización** — elige entre:
  * **Temporizador:** muestra la cuenta regresiva exacta en la tarjeta del ticket en el pipeline.
  * **Indicador de color:** verde (a tiempo), amarillo (en advertencia) o rojo (incumplido).

> 💡 El temporizador es la opción más recomendada para que tu equipo pueda priorizar visualmente.

#### Paso 5 — Configurar tiempos por campo (opcional)

Si quieres aplicar tiempos distintos según el tipo de consulta, puedes usar la opción **Tiempo por campo**. Esto te permite definir reglas basadas en un campo del ticket.

Por ejemplo: si el ticket tiene el campo "Prioridad" con opciones Alta, Media y Baja, puedes asignar 5 minutos para Alta, 15 para Media y 60 para Baja.

#### Consideración importante: un SLA por ticket

Por el momento, se puede configurar **un solo SLA por tipo de ticket**. Esto significa que puedes medir la respuesta de ejecutivos humanos **o** de asistentes de IA, pero no ambos al mismo tiempo dentro del mismo ticket.

Si necesitas medir ambos, crea dos tipos de ticket distintos.

***

### Parte 2: Dashboard de analítica SLA

Una vez que tienes tu política activa y comienzan a generarse tickets, puedes monitorear el cumplimiento desde el dashboard de SLA.

#### Cómo acceder

Ve al menú lateral y selecciona **Analítica → SLA**. Desde ahí puedes crear un dashboard nuevo o trabajar con uno existente.

Al crear un dashboard puedes elegir:

* El **embudo** que quieres analizar.
* Si el dashboard será **público** (visible para todo el equipo) o **privado** (solo para ti como administrador).

> 💡 Si acabas de configurar el SLA, es normal que el dashboard no muestre datos aún. La información aparecerá a medida que se vayan generando y resolviendo tickets.

#### Widgets disponibles

Desde **Agregar widget** puedes construir tu dashboard con los siguientes bloques:

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

**Resumen**

| Widget                            | Para qué sirve                                                                                                             |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **Tasa de cumplimiento SLA**      | Porcentaje de SLAs cumplidos en el periodo seleccionado, con comparación al periodo anterior.                              |
| **Mapa de calor SLA**             | Visualiza el cumplimiento por día de la semana y hora del día. Ideal para identificar en qué franjas colapsa la operación. |
| **Tendencia SLA**                 | Evolución de la tasa de cumplimiento en el tiempo.                                                                         |
| **Incumplimientos vs. cumplidos** | Gráfico que muestra cuántos SLAs se cumplieron y cuántos no en el periodo.                                                 |
| **Tiempo de resolución SLA**      | Tiempo promedio o percentil de resolución en minutos.                                                                      |

<figure><img src=".gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

**Resolución y detalle**

| Widget                                          | Para qué sirve                                                                                                               |
| ----------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Tiempo de respuesta de resolución**           | Tiempo promedio por ticket de la métrica de resolución.                                                                      |
| **Incumplimientos SLA**                         | Lista detallada de todos los tickets que no cumplieron el SLA, con opción de ir directamente al chat para analizar qué pasó. |
| **Tendencia de tiempo de resolución SLA**       | Evolución del tiempo de resolución a lo largo del tiempo.                                                                    |
| **Desglose del tiempo de resolución**           | Cuántos tickets se resolvieron en cada rango de tiempo.                                                                      |
| **Tendencia tiempo de respuesta de resolución** | Evolución del tiempo promedio por ticket en el tiempo.                                                                       |

<figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

#### Cómo leer el percentil de resolución

El widget de **Tiempo de resolución** permite ver el resultado por percentil. Por ejemplo, si tu percentil 90 es muy alto, significa que el 90% de tus tickets se están resolviendo en un tiempo largo, lo cual es una señal de alerta. El objetivo es que ese percentil sea lo más bajo posible.

#### Información accionable por widget

* **Mapa de calor:** si ves rojo en ciertos horarios, tu operación está colapsando en esas franjas. Puedes redistribuir los turnos de almuerzo o agregar cobertura en esos momentos.
* **Tendencia:** te permite ver si estás mejorando o empeorando semana a semana, o si hay días específicos (como viernes o lunes) donde el rendimiento cae.
* **Tabla de incumplimientos:** es el widget más accionable para seguimiento puntual — te dice exactamente qué ticket falló y te lleva directamente al chat.

***

### Buenas prácticas

* **Empieza con tiempos realistas.** Configura tiempos que tu equipo realmente pueda cumplir y ajústalos gradualmente a medida que mejora la capacidad de respuesta.
* **Usa siempre el horario laboral.** Sin él, los tickets generados fuera de horario contarán como incumplidos aunque tu equipo no esté operativo.
* **Comienza solo con Primera respuesta.** Es la métrica más crítica y la más fácil de controlar. Una vez que la domines, activa Siguiente respuesta y luego Tiempo de resolución.
* **Revisa la tabla de incumplimientos regularmente.** No solo mires el porcentaje global — entra al detalle para entender por qué fallaron esos tickets específicos.
* **Pausa el SLA en períodos de cierre.** Si tu equipo está de vacaciones o hay un feriado prolongado, pausa manualmente el SLA para no contaminar tus métricas históricas.
