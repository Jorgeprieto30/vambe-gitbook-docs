# Cómo hacer y gestionar llamadas desde Vambe (Vambe Llamados)

Vambe Llamados te permite llamar a tus clientes directamente desde Vambe, sin salir de Vambe. Puedes gestionar llamadas salientes, ver el historial de llamadas por contacto y analizar el rendimiento de tu equipo desde el panel de analítica.

***

### Requisitos previos

> ⚠️ **Vambe Llamados requiere habilitación previa.** Las llamadas se realizan desde un número externo distinto al número de WhatsApp conectado en Vambe. Para activarlo, debes contactar al **equipo de soporte de Vambe** o al **ingeniero a cargo de tu plataforma**.
>
> Lo mismo aplica si quieres **recibir llamadas entrantes** (cuando un cliente te llama de vuelta): también debe configurarse con soporte o con tu ingeniero asignado.

***

### Cómo realizar una llamada desde un ticket

Una vez que Vambe Llamados está habilitado en tu cuenta:

1.  **Abre el ticket** del cliente al que quieres llamar.
2.  En la parte superior derecha del ticket, haz clic en el **ícono de teléfono**.

    <figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>
3.  Se abrirá el panel de **Opciones de Llamada**, donde podrás elegir desde qué número realizar la llamada (si tienes más de uno conectado).
4.  Selecciona el número y la llamada comenzará.

> 💡 Si necesitas agregar un número adicional desde el cual llamar, haz clic en **+ Agregar número** dentro del panel de Opciones de Llamada.

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

***

### Llamadas a Ejecutivos sin IA: Enrutamiento Especializado

Para situaciones que requieren una atención humana directa y sin intermediación de inteligencia artificial, Vambe introduce una funcionalidad de llamadas a ejecutivos sin IA con un enrutamiento optimizado para tu equipo.

Este sistema está diseñado para asegurar que las llamadas sean atendidas rápidamente por un ejecutivo, priorizando la conexión humana.

**¿Cómo funciona el enrutamiento?**

Cuando se activa una llamada a ejecutivos sin IA:

1.  **Notificación a ejecutivos asignados:** Vambe notificará automáticamente a los ejecutivos que estén específicamente asignados para atender este tipo de llamadas.
2.  **Notificación a todos los ejecutivos (si no hay asignados):** Si no hay ejecutivos asignados a una categoría específica para esta llamada, o si los asignados no responden, Vambe extenderá la notificación a todos los ejecutivos disponibles.
3.  **Primero en contestar, primero en atender:** El primer ejecutivo que conteste la llamada será quien la tome.
4.  **Atención individualizada:** Solo un ejecutivo puede atender una llamada a la vez, garantizando una atención dedicada y evitando duplicidades.

Esta funcionalidad asegura un flujo de atención eficiente, priorizando la respuesta humana directa y sin filtros de IA para las interacciones más críticas.

***

### Controles durante la llamada

Una vez iniciada la llamada, aparecerá una **barra de llamada en la parte inferior de la pantalla** con los siguientes controles:

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

| Control           | Función                                                                                                 |
| ----------------- | ------------------------------------------------------------------------------------------------------- |
| 💬 **Chat**       | Ver la conversación del ticket mientras hablas                                                          |
| ⌨️ **Teclado**    | Abrir el teclado numérico para marcar extensiones o responder menús de voz                              |
| 🎙️ **Micrófono** | Silenciar / activar tu micrófono                                                                        |
| 📵 **Colgar**     | Finalizar la llamada                                                                                    |
| ⠿ **Mover**       | Arrastrar la barra de llamada a cualquier parte de Vambe para seguir trabajando mientras hablas |

***

### Ver el historial de llamadas de un contacto

Para revisar todas las llamadas que has tenido con un cliente específico:

1. Abre el ticket del contacto.
2. En el panel lateral derecho, haz clic en el **ícono de teléfono** (pestaña de llamadas).
3. Ahí verás el historial completo de llamadas con ese contacto: fecha, duración y resultado.

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

***

### Analítica de Llamadas

Vambe cuenta con un panel completo para monitorear y analizar el rendimiento de tu equipo en llamadas.

#### ¿Dónde encontrarlo?

Ve al menú lateral izquierdo → **Analítica** → **Calls**.

Puedes filtrar los datos por **rango de fechas** y por **frecuencia** (Diario, Semanal, etc.).

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

***

#### Pestaña Resumen

Muestra las métricas globales del período seleccionado:

| Métrica                    | Descripción                                                     |
| -------------------------- | --------------------------------------------------------------- |
| **Tasa de contacto**       | Porcentaje de llamadas en las que se logró contactar al cliente |
| **Total de agentes**       | Número de agentes registrados en el sistema                     |
| **Llamadas sin contestar** | Oportunidades perdidas (el cliente no respondió)                |
| **Llamadas contestadas**   | Conexiones exitosas                                             |
| **Duración promedio**      | Tiempo promedio de cada llamada                                 |

Además encontrarás dos gráficos principales:

**Tendencias de volumen de llamadas:** Muestra el volumen diario de llamadas y la tasa de respuesta a lo largo del tiempo. Útil para identificar días de mayor actividad.

**Distribución de resultados de llamadas:** Gráfico circular que desglosa los resultados por tipo (satisfecho, insatisfecho, sin calificación).

**Distribución de llamadas por hora:** Mapa de calor que muestra la intensidad de llamadas a lo largo del día, hora por hora. Incluye la hora pico, el total del período y la duración promedio por llamada. Ideal para identificar los mejores horarios para llamar.

***

#### Pestaña Agentes

Muestra la **tabla de rendimiento por agente**, ordenada por métricas clave:

| Columna                | Descripción                                                                        |
| ---------------------- | ---------------------------------------------------------------------------------- |
| **Rango**              | Posición del agente según su volumen de llamadas                                   |
| **Total de llamadas**  | Llamadas realizadas en el período                                                  |
| **Tasa de conversión** | Porcentaje de llamadas que resultaron en un resultado exitoso                      |
| **Rendimiento**        | Clasificación automática: Bueno / Promedio / Debajo del promedio / Necesita mejora |

Haz clic en **Ver detalles** de cualquier agente para ver su panel individual con:

* Total de llamadas, llamadas contestadas, sin contestar y duración promedio.
* Tiempo total de conversación.
* **Rendimiento:** contactos alcanzados, llamadas por contacto, resultados exitosos y tasa de conversión.
* **Eficiencia:** tasa de respuesta, llamadas perdidas y promedio de llamadas por día.
* Pestañas de **Actividad** e **Historial de llamadas** del agente.

***

### Resumen rápido

*   Vambe Llamados permite realizar llamadas salientes directamente desde cualquier ticket.
*   Requiere habilitación previa por parte del equipo de soporte o el ingeniero de tu cuenta.
*   Ahora, con la funcionalidad de **Llamadas a Ejecutivos sin IA**, las llamadas pueden enrutarse a ejecutivos asignados o a todo el equipo, siendo el primero en responder quien atiende.
*   Durante la llamada puedes silenciar, marcar extensiones y seguir navegando en Vambe.
*   El historial de llamadas por contacto está disponible en el panel lateral derecho del ticket.
*   La analítica de Llamadas (en **Analítica → Calls**) muestra métricas globales, distribución por hora y rendimiento por agente.
*   Para recibir llamadas entrantes también se requiere configuración previa con soporte.
