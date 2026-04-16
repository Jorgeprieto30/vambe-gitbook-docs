---
description: >-
  Automatiza el flujo de tus clientes. Aprende a configurar la función "Cambio
  de Etapa" desde tu Asistente IA para mover leads automáticamente y evita el
  error más frecuente: escribir la instrucción si
---

# ¿Cómo cambiar un ticket de una etapa a otra de forma automática?

La función de Cambio de Etapa es una de las más utilizadas y potentes de Vambe. Permite que tu Asistente de Inteligencia Artificial mueva automáticamente a un cliente de una columna a otra en tu embudo de ventas (Pipeline) basándose en lo que ocurre en la conversación.

¿Para qué sirve? Para mantener tu CRM ordenado sin intervención manual.

* _Ejemplo:_ Si el cliente entrega todos sus datos (Nombre, RUT, Correo) -> Mover a "Datos Completos".
* _Ejemplo:_ Si el cliente dice que no tiene presupuesto -> Mover a "Perdidos".

***

#### 1. La Lógica: Causa y Efecto

Para que esta función opere correctamente, debes estructurar la instrucción en dos partes:

1. **La Instrucción en el Texto (Prompt)**: Debes decirle explícitamente a la IA en el paso a paso _cuándo_ debe activar la función.
2. **La Configuración de la Función**: Debes crear la herramienta técnica que realiza el movimiento.

***

#### ⚠️ Error Común: Instrucción sin Función

Este es el error más típico al configurar asistentes.

Muchas personas escriben en el texto del paso: _"Cuando el cliente responda, cambia de etapa"_... **pero olvidan crear el botón de la función.**

**¿Qué pasa si hago esto?** La IA leerá tu instrucción, tendrá la intención de hacerlo, pero no tendrá la herramienta técnica para ejecutarlo. Es como decirle a un carpintero "clava ese clavo" pero no darle el martillo.

{% hint style="danger" %}
**Regla de Oro:** Siempre debes ver la tarjeta de la función creada justo debajo del texto del paso. Si solo está escrito en el texto, NO funcionará.
{% endhint %}

***

#### 2. Configuración Paso a Paso

Para empezar, es fundamental que ingreses a la configuración de tu cerebro de IA.

**Paso 1: Ingresar al Asistente**

1. [Ingresar al asistente](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md)
2. Selecciona el asistente que deseas editar (o crea uno nuevo).
3. Una vez dentro, ubica los bloques de Pasos a Seguir o Casos Posibles. Recuerda que las funciones solo viven dentro de estos dos bloques.

**Paso 2: Escribir la Instrucción**

Dentro del bloque (Pasos o Casos), redacta la condición gatillante en el texto.

* _Fórmula:_ `Cuando [ocurra X cosa], debes ejecutar la función [Nombre de la función]`.

> Ejemplo Real: "Cuando el cliente me responda las preguntas del RUT y Nombre, debes ejecutar la función Cambio de Etapa a Pendiente Cotización".

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

**Paso 3: Crear la Función (¡Indispensable!)**

Justo debajo del texto donde escribiste la instrucción, haz clic en **Agregar Función** y **selecciona Cambio de Etapa**.

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

Se abrirá un panel de configuración donde debes llenar dos campos vitales:

1. **Etapa de Destino**: Selecciona a qué columna del embudo quieres mover al cliente (Ej: "Pendiente Enviar Cotización").
2. **Descripción (¡CRUCIAL!)**: Aquí debes explicarle a la IA cuándo es el momento correcto de usar esta herramienta.
   * _Tip:_ Copia y pega la misma "Causa" que escribiste en el texto del Paso 2.
   * _Ejemplo de Descripción:_ "Cuando el cliente me responda las preguntas".

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>



**Paso 4: Verificación Visual (¿Cómo debe verse?)**

Una vez que hagas clic en "Crear", es vital confirmar que la función quedó adjunta correctamente.

Así se ve una configuración correcta: Debes ver el texto de tu instrucción arriba y, justo debajo, una tarjeta blanca con el icono de la función y el nombre que le asignaste. Si no ves la tarjeta, la función no existe.

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

***

#### 3. Manejo de Múltiples Caminos

Una de las grandes ventajas de esta función es que la IA puede decidir entre **varios caminos** en un mismo paso, basándose en la **Descripción** que le diste a cada función.

**Caso de Ejemplo**: Imagina que estás pidiendo el RUT.

* **Camino A:** El cliente da el RUT correcto -> Mover a etapa "Datos Ok".
* **Camino B:** El cliente dice que es extranjero y no tiene RUT -> Mover a etapa "Sin RUT".

**Configuración**: En el mismo paso agregarías dos funciones de Cambio de Etapa distintas:

1. **Función A:**
   * _Destino:_ Datos Ok.
   * _Descripción:_ "Cuando el cliente me entrega su RUT correctamente".
2. **Función B:**
   * _Destino:_ Sin RUT.
   * _Descripción:_ "Cuando el cliente indica que no tiene RUT por ser extranjero".

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

Gracias a la descripción, la IA sabrá cuál de las dos herramientas "sacar de la caja" según la respuesta del usuario.
