---
description: >-
  Filtra tu tráfico. Configura a tu Asistente IA para que detecte
  automáticamente si un cliente no califica (por sus respuestas) y lo elimine
  del embudo para mantener el orden.
---

# ¿Cómo hacer que la IA elimine un contacto del embudo si no califica durante el chat o es spam?

Esta configuración permite que tu Asistente Inteligente actúe como un filtro de calidad en tiempo real. Si durante la conversación la IA detecta que el cliente no cumple con tus requisitos (ej: no tiene presupuesto, es menor de edad, o busca un servicio que no das), puede **sacarlo automáticamente del embudo.**

**El objetivo:** Que tu equipo de ventas no pierda tiempo revisando chats que la IA ya identificó como "**no viables**" o "**spam**".

***

#### ⚠️ Advertencia: ¿Eliminar o Mover a "Perdidos"?

Antes de configurar esta limpieza automática, considera lo siguiente:

Al usar la función **Quitar contacto del embudo**, el rastro de ese cliente desaparece de tu vista en ese proceso. Nuestra recomendación general es que, en lugar de eliminarlo, configures a la IA para **Cambiarlo de Etapa** a una columna de "**Perdidos**" o "**No Calificados**".

* **Usa "Eliminar" solo si**: Es spam, insultos o tráfico basura que definitivamente ensucia tus métricas.
* U**sa "Mover a Perdidos" si**: Es un cliente real pero que no califica hoy (quizás en el futuro sí).

***

#### Configuración Paso a Paso

Si decides que la IA debe descartar y eliminar a estos contactos basándose en sus respuestas, sigue estos pasos:

**Paso 1: Ingresar al Cerebro de la IA**

1. [Ve al menú Asistente.](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md)
2. Entra a editar tu bot.
3. Dirígete a los bloques de **Pasos a Seguir** (si es una pregunta de filtro lineal) o **Casos Posibles** (si puede ocurrir en cualquier momento).

**Paso 2: Dar la Instrucción de Descarte**

Debes escribir explícitamente qué mensaje del "cliente" detonará la eliminación.

* _**Fórmula**:_ `Si el cliente menciona [Frase de Spam].`&#x20;
* &#x20;**Acción**: `Debes ejecutar la función [Nombre de la función]`.

> Ejemplo Anti-Spam: "Si el cliente me pregunta si quiero contratar el servicio de 'Seguros Masterplop' o intenta venderme algo, debes ejecutar la función Eliminar Spam".



**Paso 3: Crear la Función de Eliminación**

Justo debajo de esa instrucción, haz clic en + Agregar Función y busca Quitar contacto del embudo.

<p align="center"><img src="../.gitbook/assets/image (35).png" alt="" data-size="original"><br></p>

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

\
Configura la tarjeta:

1. Nombre: Ej: "Descartar por edad" o "Eliminar Spam".
2. Descripción (Lo más importante): Aquí le confirmas a la IA la lógica de activación.
   * _Ejemplo:_ "Cuando el cliente nos intente vender algun servicio".

**Paso 4: Verificación Visual**

Revisa que debajo de tu texto de "filtro" haya aparecido la tarjeta blanca de la función. Ahora, cuando el usuario caiga en esa condición durante el chat, la IA lo borrará del listado para que no te distraiga.

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>
