# Cómo indicar al asistente dónde buscar información dentro de la Base de Conocimiento

Para que el asistente pueda entregar respuestas precisas, es fundamental enseñarle **cómo**, **cuándo** y **dónde** debe buscar información dentro de los documentos conectados a Vambe.

Existen **dos métodos diferentes** para realizar búsquedas de información en la Base de conocimiento:

* **Vector Based Search** (búsqueda semántica en textos).
* **Buscar fila en hoja** (búsqueda exacta por columna en Google Sheets).

Cada método funciona distinto y se utiliza según el tipo de información que necesitamos encontrar.

Antes de explicar cómo configurarlos, dos conceptos esenciales:

***

#### Información que la IA puede y no puede leer

* La IA **sí puede leer**:
  * Texto dentro de PDF (si el PDF es texto real).
  * Google Sheets.
  * Google Docs.
  * Archivos de Drive, Notion, Dropbox y otros conectados.
* La IA **NO puede leer**:
  * Imágenes.
  * PDF escaneados que contienen imágenes en lugar de texto.
  * Documentos donde la información no es seleccionable.

Esto es crítico: si el documento no contiene texto real, la búsqueda fallará.

***

### ¿Dónde deben configurarse las funciones de búsqueda?

Las funciones de búsqueda **solo pueden configurarse en los siguientes bloques de instrucción:**

* **Pasos a seguir**
* **Casos posibles**

Esto ocurre porque son los únicos bloques que permiten agregar funciones.

***

## Método 1: Vector Based Search (Búsqueda de Base Vectorial)

### ¿Qué hace este método?

Realiza una **búsqueda semántica**, comparando lo que escribe el cliente con el contenido de los documentos para encontrar el texto más parecido.

Ideal para:

* Buscar descripciones de productos.
* Buscar precios.
* Buscar políticas o preguntas frecuentes.
* Encontrar texto similar dentro de documentos extensos.

Ejemplo:

> Si el cliente escribe “¿tienen martillos percutores?”, la IA puede encontrar textos relacionados a _martillos_, _martillo percutor_, _set de martillos_, etc., aunque no coincidan exactamente palabra por palabra.

{% stepper %}
{% step %}
### Entrar al asistente

* Dirigirse al embudo.
* Abrir la etapa donde está el asistente.
* Configuración → Editar asistente.

(Enlace de referencia: https://academy.vambe.ai/es/academy/c%C3%B3mo-ingresar-al-asistente-de-inteligencia-artificial)
{% endstep %}

{% step %}
### Seleccionar el paso donde se ejecutará la búsqueda

Debe definirse **cuándo** queremos buscar la información.\
Ejemplo: “Cuando el cliente pregunte por un producto”. Ese será el detonante de la búsqueda.

![captura](<../.gitbook/assets/image png Nov 26 2025 04 00 08 3700 PM.png>)
{% endstep %}

{% step %}
### Agregar la función

* Ir al paso correspondiente.
* Clic en **Agregar función**.
* Seleccionar **Búsqueda de base vectorial**.
* Crear nueva función.

![agregar función](<../.gitbook/assets/image png Nov 26 2025 04 00 55 7743 PM.png>) ![seleccionar](<../.gitbook/assets/image png Nov 26 2025 04 02 37 1573 PM.png>) ![crear](<../.gitbook/assets/image png Nov 26 2025 04 04 11 7474 PM.png>)
{% endstep %}

{% step %}
### Configurar parámetros

Dentro de la función se debe definir:

*   Selección de documentos: seleccionar los documentos previamente cargados en la **Base de Conocimiento** desde donde la IA podrá extraer información.

    ![selección de documentos](<../.gitbook/assets/image png Nov 26 2025 04 06 34 3787 PM.png>)
*   Número de documentos o resultados: indica cuánta información traer desde los documentos. Ejemplo: **12** → los “12 fragmentos más similares”.

    ![número de resultados](<../.gitbook/assets/image png Nov 26 2025 04 07 05 6971 PM.png>)
*   Umbral de similitud (opcional): define qué tan parecido debe ser el contenido encontrado (valor entre 0 y 1). Ejemplos:

    * 0.2 → búsqueda amplia.
    * 0.5 → coincidencias moderadas.
    * 0.8 → coincidencias muy estrictas.

    ![umbral](<../.gitbook/assets/image png Nov 26 2025 04 07 33 0331 PM.png>)
* Palabra clave de búsqueda: la pista que le damos a la IA. Ejemplo: “Usar el producto mencionado por el cliente como palabra clave de búsqueda.”
*   Estructura del documento: describir cómo está organizado el documento para que la IA interprete correctamente la información.\
    Ejemplo: “Esta hoja tiene 5 columnas: nombre del producto, descripción, precio, categoría y stock.”

    ![estructura](<../.gitbook/assets/image png Nov 26 2025 04 08 30 9283 PM.png>)
{% endstep %}

{% step %}
### Guardar y usar la función

En el paso correspondiente escribir la instrucción para ejecutar la función, por ejemplo:

> “Debes ejecutar la función buscar\_información\_producto.”

![usar función](<../.gitbook/assets/image png Nov 26 2025 04 10 51 5922 PM.png>)
{% endstep %}
{% endstepper %}

***

## Método 2: Buscar fila en hoja (solo Google Sheets)

### ¿Qué hace este método?

Permite buscar un valor exacto en una columna de Google Sheets y obtener toda la fila completa.

Se usa cuando necesitamos:

* Buscar un cliente por su teléfono o correo.
* Buscar un producto por un código exacto.
* Buscar información perfectamente estructurada.

Ejemplo:

> La IA busca en la columna “Producto” el valor exacto “Martillo Industrial N°4” y trae toda la fila que incluye precio, proveedor, stock, peso, etc.

{% stepper %}
{% step %}
### Entrar al asistente

Mismo procedimiento que en el método anterior.
{% endstep %}

{% step %}
### Seleccionar el paso donde ocurrirá la búsqueda

Ejemplo: “Cuando el cliente mencione un producto específico.”
{% endstep %}

{% step %}
### Crear la función

* Agregar función.
* Seleccionar **Buscar fila en hoja**.
* Crear nueva función.
{% endstep %}

{% step %}
### Configurar parámetros

La función permite dos formas de conexión:

* Conexión directa a Google: conectar con tu cuenta de Google → seleccionar el Google Sheet.
* Mediante URL: requiere dar permiso al correo que aparece en la interfaz.

Luego:

* Seleccionar la hoja.
* Definir los nombres de las columnas.
* Marcar como “Requerida” la columna desde donde se hará la búsqueda exacta.
{% endstep %}
{% endstepper %}

### Errores comunes

<details>

<summary>Ver errores comunes</summary>

1. Las columnas del Google Sheet cambian a mitad de la hoja.
   * Esto confunde a la IA. Todas las filas deben seguir la misma estructura.
2. El documento contiene imágenes en vez de texto.
   * La IA no puede leerlas.
3. Se cargó mal la URL o no se asignaron permisos.

</details>

***

### Resumen claro de ambos métodos

| Método                  |          Tipo de búsqueda | Ideal para                                         | Limitaciones                    |
| ----------------------- | ------------------------: | -------------------------------------------------- | ------------------------------- |
| **Vector Based Search** | Semántica / por similitud | Productos, textos largos, políticas, descripciones | No sirve para valores exactos   |
| **Buscar fila en hoja** |        Exacta por columna | Precios, clientes, catálogos estructurados         | Solo funciona con Google Sheets |
