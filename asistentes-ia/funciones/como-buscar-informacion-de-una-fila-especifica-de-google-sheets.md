---
description: >-
  Consulta datos exactos. Configura tu IA para que busque el estado de un
  pedido, la dirección de un cliente o el saldo de una cuenta buscando una fila
  específica en Google Sheets.
---

# ¿Cómo buscar información de una fila específica de Google Sheets?

La función Buscar fila en hoja permite que tu Asistente vaya a tu Excel en la nube, busque un dato específico (como un RUT, un ID de pedido o un correo) y traiga toda la información de esa fila para responderle al cliente.

**¿Para qué sirve?** Para consultas de datos únicos y exactos:

* **Estado de Pedido:** El cliente da su número de orden -> La IA busca esa fila y responde "Tu pedido está en camino".
* **Validación de Cliente:** El cliente da su RUT -> La IA verifica si existe en la base de datos.
* **Consulta de Saldo/Puntos:** El cliente da su DNI -> La IA le dice cuántos puntos tiene acumulados.

***

#### 🛑 ¡Espera! ¿Quieres buscar en todo el documento?

Es vital entender la diferencia:

* **Buscar Fila (Esta función):** Busca única y exclusivamente una sola fila basándose en un dato exacto (ej: RUT 123-4).
* Búsqueda Vectorial: Busca información general en todo el documento (ej: "¿Qué productos tienen para el dolor de cabeza?").

> Si lo que necesitas es que la IA lea el documento completo para responder preguntas generales, NO uses esta función. 👉 [\[Ve al artículo de Búsqueda de Base Vectorial aquí\]](como-indicar-al-asistente-donde-buscar-informacion-dentro-de-la-base-de-conocimiento.md)

***

#### Configuración Paso a Paso

Para que esto funcione, necesitamos un Dato Llave (el dato único por el cual vamos a buscar, como el RUT o el ID).

**Paso 1: La Instrucción (El Gatillo)**

Dile a la IA que cuando reciba el "Dato Llave", vaya a buscar.

* _Fórmula:_ `Cuando el cliente me entregue su [Dato Llave], ejecuta la función [Nombre de la función] para ver su información`.

> Ejemplo: "Cuando el cliente me dé su RUT, ejecuta la función Buscar Cliente para ver si está registrado".

**Paso 2: Crear la Función**

Haz clic en + Agregar Función, selecciona Google Sheets y luego Buscar fila en hoja (Search Row).

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>



1. **Nombre:** Ej: "Buscar Cliente por RUT".
2. **Descripción:** "Cuando tenga el RUT del cliente".
3. **Conexión (Token):** Selecciona tu cuenta de Google (Recuerda refrescar la página si acabas de conectarla y no aparece).
4. **Selección de Hoja:** Elige el archivo (Spreadsheet) y la pestaña (Sheet) donde están los datos.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

**Paso 3: Configuración de Columnas (¡Lo más importante!)**

Al cargar la hoja, verás todas las columnas (Nombre, RUT, Dirección, Estado, etc.).

Debes decirle a la IA **cuál es la columna por la que debe buscar.**

1. Ubica la columna del **Dato Llave** (Ej: Columna "RUT").
2. En la **Descripción** de esa columna escribe: _"Este es el dato por el cual debes buscar la fila"_.
3. **ACTIVA el interruptor "¿Requerido?"** en esa columna específica.
   * _¿Por qué?_ Esto le dice a la IA: "Sin este dato (RUT), no puedes buscar nada". Es la llave que abre la puerta de esa fila.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

**Paso 4: Verificación**

Haz clic en Crear. Ahora, cuando un cliente entregue ese dato llave, la IA leerá esa fila específica y podrá responder cosas como: _"Hola \[Nombre de la columna A], veo que tu pedido está en estado \[Columna B]" o encontrara la informacion de ese cliente_

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

Por ejemplo, en esta función se buscaría por el RUT de un cliente y se traería para la IA toda la información correspondiente (solo de esa línea de Google Sheets).



