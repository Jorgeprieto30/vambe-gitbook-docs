# Analítica de plantillas

## Analítica de plantillas

La **Analítica de plantillas** te muestra, en un solo lugar, cómo está funcionando cada plantilla que envías por WhatsApp: cuántas se entregan, cuántas se leen, cuántas generan respuesta y por qué fallan las que fallan. Es mucho más rápida que antes, sin importar el tamaño de tu cuenta.

> Para entrar: en el menú lateral, ve a **Canales → Plantillas → Analítica plantillas**.

Tiene dos vistas: una **vista general** con todas tus plantillas, y una **vista de plantilla específica** a la que entras haciendo clic en cualquiera de ellas.

***

### Vista general

Al entrar ves los KPIs de conversión de todas tus plantillas en el rango de fechas elegido:

* **Plantillas enviadas**
* **Contactos únicos**
* **Entregados**
* **Leídos**
* **Respondidos**
* **Fallidos**

Debajo, la tabla **Plantillas analizadas** lista cada plantilla con su actividad, envíos, contactos, entregados, leídos, respondidos y fallidos. Puedes ordenarla por cualquier columna, buscar por nombre y hacer clic en una plantilla para abrir su analítica específica.

Al final de la página, **Por qué fallaron los envíos** agrupa los motivos de falla con su descripción, cantidad de envíos y contactos afectados, y una acción recomendada para cada caso. Puedes **descargar** este detalle con el botón _Descargar_.

***

### Vista de plantilla específica

Al hacer clic en una plantilla desde la tabla, entras a su analítica individual, con los mismos KPIs de conversión pero enfocados solo en esa plantilla, más:

* **Envíos por día:** gráfico con la frecuencia diaria de envíos, entregados, leídos, respondidos y fallidos.
* **Tiempo de respuesta:** mediana, promedio y percentil 90 (p90) del tiempo desde el envío hasta la primera respuesta, con su histograma.
* **Por qué fallaron los envíos:** el mismo detalle de motivos de falla, pero específico de esta plantilla.
* **Contactos:** tabla con cada contacto individual —envíos, entregadas, leídas, fallidas, si respondió, último envío, primera respuesta y último fallo—, filtrable y descargable.

***

### Parámetros que puedes ajustar

#### Rango de fechas

Filtra por la **fecha de envío de la plantilla** (por ejemplo, "Últimos 30 días"). Todos los KPIs y tablas se recalculan según el rango elegido.

#### Configuración de respuesta

Este es el parámetro más importante para interpretar bien tus datos: define **qué cuenta como una respuesta** a una plantilla enviada. Se configura desde el selector **Respuesta**, arriba de los KPIs.

**Criterio:**

* **Directa:** solo cuenta como respuesta si el contacto responde sin que se le haya enviado ningún otro mensaje en medio.
* **Última plantilla:** cuenta como respuesta si el contacto responde dentro de la ventana de tiempo y no se envió otra plantilla en medio (es decir, se atribuye a la última plantilla que lo tocó).
* **Libre:** cuenta como respuesta cualquier mensaje del contacto dentro de la ventana de tiempo, sin importar qué pasó en medio.

**Ventana máxima:** el tiempo máximo tras la entrega dentro del cual una respuesta cuenta como tal (por ejemplo, 2 días).

#### Contar por envío o por contacto

En varios widgets puedes alternar entre:

* **Por envío:** cada envío de plantilla cuenta individualmente.
* **Por contacto:** un mismo contacto que recibió varias plantillas se cuenta como máximo una vez por métrica (entregado, leído, respondido, etc.), sin duplicarse.

***

### Exportar información

Tanto en la vista general como en la vista de plantilla específica, puedes descargar el detalle de **errores** y de **contactos** con el botón _Descargar_, para trabajarlos fuera de Vambe.

***

### En resumen

La Analítica de plantillas te deja ver, plantilla por plantilla o de forma agregada, qué tan bien está funcionando tu mensajería saliente: cuánto se entrega, cuánto se lee, cuánto convierte en respuesta y por qué fallan los envíos que fallan. Ajusta el criterio de atribución de respuesta según cómo definas tú una conversación exitosa, y usa las exportaciones para profundizar en los casos que te importan.
