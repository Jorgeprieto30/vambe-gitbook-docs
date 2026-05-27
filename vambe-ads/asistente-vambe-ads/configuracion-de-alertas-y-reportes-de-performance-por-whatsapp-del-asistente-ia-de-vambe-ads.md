# Configuración de alertas y reportes de performance por WhatsApp del Asistente IA de Vambe Ads

El asistente de Vambe Ads ahora puede enviarte mensajes por WhatsApp de forma proactiva: reportes periódicos con el resumen de tus campañas y alertas automáticas cuando alguna métrica sale del objetivo. La configuración se hace una sola vez y el sistema funciona de forma autónoma.

***

### Requisitos previos

Antes de configurar esta funcionalidad asegúrate de tener:

* Acceso a Vambe Ads con cuenta activa y campañas conectadas.
* Un número de WhatsApp disponible para recibir reportes y alertas.
* Al menos un KPI objetivo definido (costo por agenda, ROAS, etc.).

***

### Configuración del asistente

Ingresa a la vista del asistente en Vambe y haz clic en el ícono de ajustes ⚙️. Esto abre el panel **Configuración del asistente**.

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

#### 1. Conectar WhatsApp

Activa el toggle de WhatsApp e ingresa tu número con código de país, sin el signo `+`.

> **Ejemplo:** `56912345678`

Al guardar, recibirás un mensaje de bienvenida confirmando la conexión.

#### 2. Elegir métricas objetivo (KPI)

Selecciona el tipo de métrica que el asistente usará como referencia para sus análisis, reportes y alertas:

| Opción            | Descripción                           |
| ----------------- | ------------------------------------- |
| **Estándar**      | Métricas nativas de Meta y Google     |
| **Vambe**         | Métricas de negocio como agenda total |
| **Personalizada** | Una columna configurada por ti        |

#### 3. Definir presupuesto mensual

Ingresa cuánto planeas invertir por mes. El panel muestra el gasto real de los últimos 30 días como referencia.

#### 4. Definir objetivo del KPI

Ingresa el valor al que quieres llegar en tu métrica objetivo (por ejemplo, USD 500 por agenda). El panel también muestra el valor real de los últimos 30 días como punto de comparación.

> 💡 Puedes configurar estos valores conversando directamente con el asistente o manualmente desde este panel. Ambas formas quedan guardadas en el mismo lugar.

***

### Reportes programados

Desde la sección **Reportes programados**, haz clic en **+ Nuevo reporte**.

| Campo                     | Descripción                                       | Opciones                         |
| ------------------------- | ------------------------------------------------- | -------------------------------- |
| **Nombre**                | Etiqueta para identificar el reporte              | Texto libre                      |
| **Frecuencia**            | Periodicidad del envío                            | Diario / Semanal / Mensual       |
| **Día y hora**            | Cuándo se envía (zona horaria: America/Santiago)  | Día + hora                       |
| **¿Qué quieres recibir?** | Tipo de contenido del reporte                     | Resumen general u otras opciones |
| **Descripción**           | Instrucción en lenguaje natural para el asistente | Texto libre (opcional)           |

> ⚠️ El reporte se envía al número de WhatsApp registrado en la configuración. Asegúrate de tenerlo conectado antes de programar reportes.

***

### Alertas de performance

Las alertas te avisan automáticamente cuando algo sale de control. Existen dos tipos:

#### Variación

Se activa cuando una métrica **cambia más de un porcentaje definido** respecto al período anterior. Útil para detectar deterioros graduales.

> **Ejemplo:** "Avísame si el costo por agenda sube un 20% en los últimos 7 días en alguna campaña."

#### Umbral

Se activa cuando una métrica **supera o cae bajo un valor fijo** que tú defines. Útil para establecer límites duros de eficiencia.

> **Ejemplo:** "Avísame si algún conjunto de anuncios supera los USD 600 por agenda."

#### Campos de configuración

| Campo                            | Descripción                                                       |
| -------------------------------- | ----------------------------------------------------------------- |
| **Tipo de alerta**               | Variación (%) o Umbral (valor absoluto)                           |
| **Métrica**                      | El KPI a monitorear                                               |
| **Ventana (días)**               | Período de evaluación, ej. últimos 7 días                         |
| **Dirección / Condición**        | Cuándo se activa: cuando sube, cuando baja, mayor o igual a, etc. |
| **Cambio mínimo / Valor umbral** | El porcentaje o valor que dispara la alerta                       |
| **Nivel**                        | A qué nivel se evalúa: Campaña, Conjunto o Anuncio                |
| **Gasto mínimo** (opcional)      | Filtra campañas con poco gasto para evitar falsos positivos       |

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

### ¿Cómo se ve en WhatsApp?

Cuando el asistente genera un reporte, te llega un **PDF directamente al chat de WhatsApp** con:

* Headline con el gasto total, cantidad de resultados y costo por resultado del período.
* Tabla desglosada por campaña con gasto, agendas y estado respecto al KPI.
* Hallazgos clave: anomalías críticas, campañas a escalar, campañas a revisar o pausar, y recomendaciones de reasignación de presupuesto.
* Próximo paso sugerido por el asistente.

Las **alertas puntuales** llegan como mensajes de texto indicando la campaña afectada, la variación registrada y el valor actual de la métrica.

{% hint style="info" %}
💡 Puedes responderle al asistente directamente desde WhatsApp para hacer preguntas de seguimiento, como "¿cuántas agendas tuvimos esta semana?" o "¿qué campaña tuvo el mejor ROAS?".
{% endhint %}

### Configuraciones recomendadas

Estas son algunas combinaciones de reportes y alertas que recomendamos según el tipo de operación. Úsalas como punto de partida y ajústalas a tu negocio.

***

#### 🗓 Reporte de inicio de semana

**Para quién:** Clientes que quieren arrancar el lunes con contexto claro antes de tomar decisiones de presupuesto.

**Configuración:**

* Frecuencia: Semanal, lunes a las 9:00 AM
* Contenido: Resumen general
* Descripción: _"Resumen de la semana anterior. Indica qué campañas estuvieron dentro del objetivo, cuáles lo superaron y cuál es la recomendación de presupuesto para esta semana."_

***

#### 📊 Reporte de cierre de mes

**Para quién:** Clientes que reportan resultados a un equipo interno o a un cliente final.

**Configuración:**

* Frecuencia: Mensual, día 1 a las 8:00 AM
* Contenido: Resumen general
* Descripción: _"Resumen del mes cerrado. Incluye gasto total, total de resultados, costo por resultado promedio, comparación con el mes anterior y las 3 campañas con mejor y peor desempeño."_

***

#### 🚨 Alerta de campaña fuera de control

**Para quién:** Cualquier cliente con un objetivo de costo por resultado definido. Evita que una campaña ineficiente consuma presupuesto sin que nadie lo note.

**Configuración:**

* Tipo: Umbral
* Métrica: Costo por agenda (o tu KPI objetivo)
* Condición: Mayor o igual a `[valor objetivo × 1.5]`
* Ventana: 7 días
* Nivel: Campaña
* Gasto mínimo: USD 100 (para ignorar campañas con muy poco gasto)

> ⚠️ Si tu objetivo es USD 500 por agenda, pon el umbral en USD 750. Así la alerta se activa solo cuando hay una desviación real, no por fluctuaciones normales del día a día.

***

#### 📉 Alerta de caída de volumen

**Para quién:** Clientes donde la cantidad de resultados importa tanto como el costo. Detecta cuando una campaña que venía funcionando se apaga de golpe.

**Configuración:**

* Tipo: Variación
* Métrica: Costo por agenda (o tu KPI objetivo)
* Dirección: Cuando sube
* Cambio mínimo: 50%
* Ventana: 7 días
* Nivel: Conjunto de anuncios

***

#### 🌙 Reporte de viernes para el fin de semana

**Para quién:** Clientes que no quieren revisar el dashboard durante el fin de semana pero sí quieren saber si hay algo urgente que atender el lunes.

**Configuración:**

* Frecuencia: Semanal, viernes a las 6:00 PM
* Contenido: Resumen general
* Descripción: _"Resumen rápido del rendimiento de esta semana. Solo destacar si hay alguna campaña crítica que requiera acción urgente el lunes. Si todo está dentro del objetivo, confirmarlo en una línea."_
