---
description: >-
  Configura tu IA para que guarde automáticamente las respuestas de tus clientes
  (encuestas, leads, pedidos) en una hoja de cálculo de Google.
---

# ¿Cómo guardar datos del chat automáticamente en un Google Sheet?

La función **Agregar fila a Google Sheets** permite que tu Asistente actúe como un digitador automático. Cada vez que recopile información importante (como los datos de un cliente, respuestas de una encuesta o un nuevo pedido), la IA tomará esos datos y creará una **nueva fila** en tu excel en la nube.

**¿Para qué sirve?**

* **Encuestas**: Guardar satisfacción y comentarios.
* **Captación de Leads**: Registrar Nombre, Correo y Teléfono en tu base de datos.
* **Pedidos**: Anotar qué producto pidió el cliente y sus especificaciones.

***

#### ⚠️ Requisito Previo

Debes tener creada una Hoja de Cálculo en Google Sheets y **las columnas deben tener título** en la primera fila (Ej: Nombre, Email, Producto). Si la hoja está en blanco, la IA no sabrá dónde escribir.

***

#### Configuración Paso a Paso

**Paso 1: La Instrucción (El Gatillo)**

Primero, dile a la IA en el bloque de texto cuándo debe ir a guardar la información.

* _Fórmula:_ `Cuando el cliente termine de dar [Datos X], debes ejecutar la función [Nombre de la función]`.

> Ejemplo: "Cuando el cliente me responda las tres preguntas de la encuesta, guarda sus respuestas ejecutando la función Guardar Encuesta".

**Paso 2: Conectar la Cuenta**

Haz clic en + Agregar Función, selecciona Google Sheets y luego Agregar fila a Google Sheets.

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>



1. **Nombre y Descripción:** Ponle un nombre claro (Ej: "Guardar Lead") y en la descripción repite cuándo se activa (Ej: "Cuando tenga los datos del cliente").
2. **Conexión (Token)**: Selecciona tu cuenta de Google.
   * _Si es tu primera vez:_ Haz clic en Add New Google Account.
   * **💡 Tip Importante**: Si conectas tu cuenta y no aparece en la lista de inmediato, **refresca la página completa del navegador.** Al volver a entrar, tu cuenta ya estará disponible para seleccionar.

**Paso 3: Selección de la Hoja**

Una vez conectada la cuenta:

1. Selecciona la Hoja de Cálculo (Spreadsheet): Busca el archivo por su nombre.
2. Selecciona la Pestaña (Sheet): Elige en qué hoja específica se guardarán los datos (Ej: Hoja 1).
3. Haz clic en Sincronizar (o espera que cargue).

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

**Paso 4: Mapeo de Columnas (La parte vital)**

Aquí verás una lista con todas las columnas que tiene tu archivo (Columna A, B, C...). Debes decirle a la IA qué poner en cada una.

Tienes 3 configuraciones por columna:

1. **¿Valor constante? (Opcional)**:
   * Úsalo solo si quieres que en esa columna **siempre se escriba lo mismo**, sin importar lo que diga el cliente.
   * _Ejemplo:_ En una columna "Fuente", podrías poner el valor fijo "WhatsApp" para saber que todos vienen de ahí.
2. **Descripción (Para la IA):**
   * Aquí debes escribir qué dato debe extraer la IA de la conversación para ponerlo en esa celda.
   * _Ejemplo:_ "Colocar aquí el correo electrónico del cliente" o "Colocar aquí el producto de interés".
3. **¿Requerido?:**
   * Activa este interruptor si el dato es obligatorio. Si la IA no tiene este dato, intentará conseguirlo antes de ejecutar la función.

Así se ve una configuración de columnas lista: En este ejemplo, vemos cómo se configuran las columnas "Modelo", "Nombre del servicio", etc., esperando que agregues la descripción para que la IA sepa qué rellenar.

<figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

**Paso 5: Verificación**

Haz clic en Crear y asegúrate de ver la tarjeta de la función debajo de tu instrucción de texto. ¡Listo! Ahora tu asistente llenará tu Excel por ti.

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>
