# Analítica: Dashboards Personalizados y Reportes

La sección de **Analítica** te permite construir tus propios dashboards para visualizar y cruzar la información de tu operación en Vambe: ventas, conversaciones, satisfacción, cumplimiento de SLA y automatización de Instagram. Puedes armarlos desde cero, partir de una plantilla, o simplemente pedírselo a **PandAI** en lenguaje natural.

{% hint style="info" %}
¿Buscas el análisis automático semanal con recomendaciones? Esa es la sección **Insights**, distinta de los Dashboards Personalizados que se explican aquí.
{% endhint %}

> Para entrar: en el menú lateral, ve a **Analítica**.

***

### Cómo funciona

Cada dashboard se arma con **widgets**: bloques de visualización que eliges y configuras uno por uno. Un dashboard puede combinar tantos widgets como necesites, y cada widget tiene su propio tipo de gráfico, sus métricas y sus filtros.

Existen **5 tipos de dashboard**, cada uno enfocado en un área distinta del negocio:

1. **Tickets** (embudo/pipeline de ventas y atención)
2. **Conversaciones** (mensajería y actividad del asistente)
3. **Nivel de Servicio** (CSAT / NPS)
4. **SLA** (cumplimiento de acuerdos de servicio)
5. **Instagram** (automatización de comentarios)

Puedes crear un dashboard **desde cero** o partir de una **plantilla** ya armada con widgets predefinidos, y luego ajustarla a tu gusto.

#### Cómo crear un dashboard: paso a paso

{% stepper %}
{% step %}
**Elige el tipo de dashboard**

Elige primero el tipo: **Tickets**, **Conversaciones**, **Nivel de Servicio**, **SLA** o **Instagram**. Esta decisión es la que determina qué widgets y filtros vas a tener disponibles después, así que es el punto de partida.
{% endstep %}

{% step %}
**Nómbralo y define el filtro obligatorio**

Dale un nombre al dashboard. Según el tipo elegido, hay un filtro de entrada obligatorio:

* **Tickets:** debes elegir el embudo (pipeline).
* **Nivel de Servicio:** debes elegir el tipo de encuesta (CSAT o NPS) y el o los embudos.
* **SLA:** debes elegir el o los embudos.
* **Conversaciones** e **Instagram** no piden un filtro obligatorio de entrada.

Si no defines un rango de fechas, el dashboard parte por defecto mostrando los **últimos 30 días** (lo puedes cambiar cuando quieras).
{% endstep %}

{% step %}
**Crea en blanco o desde plantilla**

Puedes dejarlo **vacío** y agregar widgets uno por uno, o partir de una **plantilla** que ya viene poblada con un set de widgets predefinidos para ese tipo de dashboard.
{% endstep %}

{% step %}
**Agrega widgets uno por uno**

Para cada widget: elige su tipo (ej. "Tráfico de etapas", "Conversaciones por canal"), dale un nombre y configura sus filtros propios (métricas, intervalo de tiempo, tipo de visualización si aplica, etapas, canales, campos personalizados, etc.). Si no le das filtros propios, el widget hereda los filtros generales del dashboard. El widget se ubica solo en el layout, no necesitas ordenarlo manualmente.

{% hint style="warning" %}
Agrega los widgets **de a uno por vez**. Crear varios al mismo tiempo puede desordenar el layout del dashboard.
{% endhint %}
{% endstep %}
{% endstepper %}

Los cambios se guardan de inmediato al confirmarlos: no existe un botón separado de "guardar" ni un estado de borrador.

***

### 1. Dashboard de Tickets

Este tipo requiere elegir un **embudo específico** y es el más completo en widgets disponibles.

**Métricas generales**

* **Métricas de negocio** (tarjetas numéricas): total de oportunidades, tickets creados, resueltos, ganados, perdidos, cerrados, tasa de éxito, tiempo promedio de resolución, total vendido, precio promedio de venta. Se puede comparar contra el periodo anterior.

**Embudo y flujo**

* **Conversión de embudo:** vista tipo pipeline con entrantes, % de conversión, acumulado y % de abandono por etapa. Incluye la opción de "transiciones estrictas" (solo cuenta avances directos) y de contar los creados directamente en la etapa inicial.
* **Tráfico de etapas** (barras): entradas, salidas, creados/ganados/perdidos/resueltos/cerrados por etapa, monto de entrada, tiempo promedio de permanencia y tiempo promedio hasta llegar a la etapa. Al hacer clic en una etapa se abre el detalle de flujo: de dónde vienen y hacia dónde van los tickets.
* **Recorrido de tickets** (diagrama de Sankey): rutas que siguen los tickets desde una etapa inicial hacia adelante, con profundidad configurable y filtro de ruido para ocultar rutas de bajo volumen.
* **Procedencia de tickets** (Sankey inverso): de dónde vinieron los tickets que llegaron a una etapa objetivo, trazado hacia atrás.

**Series de tiempo**

* **Tickets en el tiempo** (líneas): evolución de creados/ganados/perdidos, con intervalo configurable (hora, día, semana, mes, año).
* **Ventas en el tiempo** (líneas): evolución del monto vendido.
* **Tasa de éxito en el tiempo** (líneas o áreas apiladas 100%): tendencia del % de tickets ganados sobre resueltos.
* **Lead score en el tiempo** (líneas): evolución del lead score promedio.

**Distribuciones y desgloses**

* **Tickets por canal** (barras): creados, ganados y perdidos por canal de comunicación.
* **Distribución de etiquetas** (barras): cuántos tickets tienen cada tag.
* **Distribución de lead score** (barras): cómo se reparten los tickets según su puntaje.
* **Resolución humano vs. IA** (dona o tabla): compara tickets resueltos solo por IA vs. con intervención humana, con ganados/perdidos/pendientes/tasa de conversión.
* **Mapa de calor de tickets** (día de semana × hora): según resolución (ganado/perdido), cierre o creación.

**Campos personalizados**

* **Distribución de campo de opciones** (pie o tabla): distribución de valores de un campo personalizado tipo opciones, con ganados/perdidos/pendientes/tasa de éxito por valor.
* **Distribución de campo sí/no** (pie o tabla): igual, para campos booleanos.
* **Distribución de campo de texto** (pie o tabla): distribución de valores de un campo de texto libre.
* **Estadísticas de campo numérico** (boxplot): mínimo, máximo, media, mediana, moda, suma, desviación estándar, varianza, cuartiles, conteo y conteo nulo, para campos numéricos de ticket o de contacto.

**Filtros disponibles:** etapa, estado del ticket (ganado/perdido/pendiente), ejecutivo, canal, intervención humana, y cualquier campo personalizado de ticket o contacto.

{% hint style="info" %}
Un dashboard de Tickets queda anclado a **un solo embudo**: no es posible que un widget de este tipo compare o mezcle datos de dos embudos distintos en el mismo gráfico. Si necesitas comparar dos embudos, crea un dashboard de Tickets para cada uno y revísalos en paralelo.
{% endhint %}

**Plantillas:** _Dashboard Ecommerce_ (14 widgets: ingresos, conversión, recorrido, rendimiento por canal) y _Dashboard de Postventa_ (10 widgets: tickets, recorrido, campos personalizados, resoluciones).

***

### 2. Dashboard de Conversaciones

Cubre toda la mensajería y la actividad del asistente, a nivel de todo el workspace.

**Métricas generales**

* **Métricas conversacionales** (tarjetas): mensajes enviados, mensajes IA, mensajes humanos, mensajes recibidos, contactos creados, contactos activos, conversaciones con IA, conversaciones totales, conversaciones con humano.
* **Ahorro:** dinero y tiempo ahorrado por las conversaciones atendidas por IA, según el costo de hora humana, divisa (CLP, USD, MXN, BRL, UF, ARS, COP, UYU, PEN, EUR y otras) y cuántas conversaciones puede atender un ejecutivo al día.

**Volumen y actividad**

* **Mensajes en el tiempo / Conversaciones en el tiempo** (líneas): agrupable por remitente, tipo (Humano/IA) o canal, con intervalo configurable.
* **Contactos en el tiempo** (líneas): activos o creados.
* **Contactos atendidos en el tiempo** (líneas): por remitente o tipo.
* **Mensajes por agente / Conversaciones por agente / Mensajes por canal / Conversaciones por canal** (barras o pie): con opción de desglosar Humano/IA dentro de cada barra.
* **Mapa de calor de mensajes** (día × hora): volumen entrante o saliente.
* **Cobertura de IA:** distribución de carga entre IA y humanos.
* **Carga fuera de horario:** mensajes recibidos dentro vs. fuera del horario laboral configurado.

**Calidad y desempeño de la IA**

* **Llamadas a funciones en el tiempo / conteo** (líneas, barras o pie): uso de funciones del asistente, agrupable por función o por estado (exitoso/fallido).
* **Latencia de respuesta IA** (líneas): percentiles de latencia.
* **Alertas de latencia IA** (por razón, por asistente, por función, en el tiempo): alta latencia del modelo, timeout, error del modelo, alta latencia de función.
* **Tasa de alucinaciones en el tiempo** (líneas): % de respuestas marcadas como alucinación.
* **Alucinaciones por tipo de guardrail / por asistente** (pie, barras).
* **Casos atrapados por juez personalizado** (tabla).
* **Detalle de alucinaciones** (tabla): listado con enlace directo al chat, filtrable por pendientes/resueltas/todas.

**Agendamiento**

* **Reuniones de calendario en el tiempo** (líneas): agrupable por estado, canal, origen del agendamiento (IA/no IA), pipeline, etapa o asistente.
* **Reuniones de calendario (total)** (número), con comparación de periodo.

**Filtros disponibles:** canal, tipo de remitente (humano/IA), remitentes específicos.

**Plantillas:** _Analíticas generales_ (6 widgets), _Analíticas de un canal_ (3 widgets, uno por canal), _Comparación de canales_ (vista lado a lado).

***

### 3. Dashboard de Nivel de Servicio (CSAT / NPS)

Requiere elegir el tipo de encuesta (CSAT o NPS) y el o los embudos a analizar.

* **Puntaje de satisfacción** (número): NPS o CSAT del periodo, con método de cálculo estándar o promedio simple.
* **Satisfacción del cliente en el tiempo** (líneas): evolución del puntaje.
* **Tasa de respuesta** (número): % de encuestas respondidas.
* **Distribución de puntajes** (barras).
* **Distribución por categoría** (pie): promotores, pasivos, detractores (aplica a NPS).
* **Total de respuestas** (número).
* **Respuestas de feedback** (tabla): listado individual con contacto, ticket y atribución humano/IA.

**Filtros disponibles:** canal, intervención humana.

{% hint style="info" %}
A diferencia de Tickets, aquí sí puedes elegir **varios embudos a la vez**. Los datos se muestran agregados en conjunto (no lado a lado, uno contra otro).
{% endhint %}

**Plantillas:** _Analíticas CSAT_ (8 widgets), _Analíticas NPS_ (7 widgets).

***

### 4. Dashboard de SLA

Mide el cumplimiento de tus acuerdos de nivel de servicio.

* **Tasa de cumplimiento SLA** (número): % cumplido, por tipo de métrica (primera respuesta, siguiente respuesta, resolución) y atribución (humano/IA).
* **Mapa de calor SLA** (día × hora): cumplimiento o cantidad de eventos.
* **Tendencia SLA** (líneas): cumplimiento en el tiempo.
* **Incumplimientos vs. cumplidos** (pie).
* **Tiempo de resolución SLA** (número): promedio, P50 (mediana) o P90.
* **Tiempo de respuesta de resolución** (número): tiempo total de resolución, tiempo de gestión interna, o tiempo de espera del cliente.
* **Desglose del tiempo de resolución** (pie): gestión interna vs. espera del cliente.
* **Tendencia de tiempo de resolución / de respuesta** (líneas).
* **Incumplimientos SLA** (tabla): detalle de incumplimientos activos o completados.

**Filtros disponibles:** pipeline, canal, agente, tipo de métrica, atribución (humano/IA), percentil.

{% hint style="info" %}
Igual que en Nivel de Servicio, aquí puedes elegir **varios embudos a la vez**, y los datos se agregan en conjunto, no se comparan lado a lado.
{% endhint %}

**Plantillas:** _Cumplimiento de servicio_ (10 widgets, enfocado en resultado) y _Control de niveles de servicio_ (16 widgets, enfocado en gestión activa y detección de dónde intervenir).

***

### 5. Dashboard de Instagram

Enfocado en la automatización de comentarios.

* **KPIs generales** (número): métricas clave de la automatización.
* **Actividad de automatización** (líneas): respuestas por tipo de acción.
* **Mapa de calor de actividad**: distribución horaria del procesamiento de comentarios.
* **Posts destacados** (tabla): posts con más respuestas automatizadas.

**Filtro:** cuenta de Instagram específica.

**Plantilla:** _Estadísticas de Instagram_ (4 widgets).

***

### Configuración común a todos los dashboards

* **Crear desde cero o desde plantilla:** las plantillas traen widgets ya configurados que puedes editar libremente.
* **Agregar, editar o quitar widgets** de un dashboard existente: cambia nombre, tipo de visualización (ej. barra ↔ pie, pie ↔ tabla) y filtros en cualquier momento.
* **Filtros a dos niveles:** a nivel de todo el dashboard (aplican a todos los widgets) o a nivel de cada widget individual. En Tickets, algunos filtros son "universales" —estado del ticket, ejecutivo, canal y campos personalizados— y funcionan en cualquier widget aunque no aparezcan listados explícitamente.
* **Rango de fechas y comparación automática** contra el periodo anterior en los widgets numéricos.
* **Intervalos de agregación temporal:** hora, día, semana, mes o año, en los widgets de series de tiempo.
* **Cruce con campos personalizados:** cualquier campo de ticket o de contacto (texto, número, opciones, sí/no) puede analizarse en su propia visualización.
* **Renombrar y actualizar** filtros o configuración de un dashboard ya creado, en cualquier momento.

**Compartir dashboards**

Cada dashboard tiene una **visibilidad** general —pública o privada— que solo quien lo creó puede cambiar. Además, se puede compartir explícitamente con personas específicas del equipo, con dos niveles de acceso:

* **Lectura:** la persona solo puede ver el dashboard.
* **Escritura:** además puede editarlo.

Para que alguien invitado pueda abrir un dashboard compartido, su rol dentro de la cuenta necesita el permiso correspondiente habilitado; si no lo tiene, el share queda registrado pero no podrá abrirlo hasta que se actualice su rol. Quienes tengan permiso general de ver analítica pueden ver todos los dashboards marcados como públicos, sin necesidad de un share explícito.

***

### Crea tus análisis pidiéndoselo a PandAI

No necesitas construir cada widget manualmente: puedes pedirle a **PandAI** que arme el gráfico, la tabla o el dashboard completo en lenguaje natural.

{% hint style="info" %}
👉 [**Pídele a PandAI que cree tus análisis**](https://academy.vambe.ai/pandai/pidele-a-pandai-que-cree-tus-analisis) — cómo formular un buen pedido, qué puede y qué no puede hacer, y ejemplos por tipo de negocio.
{% endhint %}

***

### En resumen

La Analítica de Vambe te deja construir el reporte exacto que tu negocio necesita: desde tarjetas simples hasta Sankeys de recorrido de tickets, mapas de calor y cruces con tus propios campos personalizados. Si no sabes por dónde partir, usa una plantilla o simplemente pídeselo a PandAI en lenguaje natural, siendo específico sobre la métrica, el corte de datos y el periodo que te importa.
