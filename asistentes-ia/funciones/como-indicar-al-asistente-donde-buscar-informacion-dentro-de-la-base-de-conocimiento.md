# Cómo indicar al asistente dónde buscar información dentro de la Base de Conocimiento

## Cómo indicar al asistente dónde buscar información dentro de la Base de Conocimiento

Para que el asistente pueda entregar respuestas precisas, es fundamental enseñarle **cómo**, **cuándo** y **dónde** debe buscar información dentro de los documentos conectados a Vambe.

Existen **dos métodos diferentes** para realizar búsquedas de información en la Base de conocimiento:

* **Vector Based Search** (búsqueda semántica en textos).
* **Buscar fila en hoja** (búsqueda exacta por columna en Google Sheets).

Cada método funciona distinto y se utiliza según el tipo de información que necesitamos encontrar.

Antes de explicar cómo configurarlos, dos conceptos esenciales:

***

**Información que la IA puede y no puede leer**

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

#### ¿Dónde deben configurarse las funciones de búsqueda?

Las funciones de búsqueda **solo pueden configurarse en los siguientes bloques de instrucción:**

* **Pasos a seguir**
* **Casos posibles**

Esto ocurre porque son los únicos bloques que permiten agregar funciones.

***

### Método 1: Vector Based Search (Búsqueda de Base Vectorial)

#### ¿Qué hace este método?

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
**Entrar al asistente**

* Dirigirse al embudo.
* Abrir la etapa donde está el asistente.
* Configuración → Editar asistente.

(Enlace de referencia: https://academy.vambe.ai/asistentes-ia/como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial)
{% endstep %}

{% step %}
**Seleccionar el paso donde se ejecutará la búsqueda**

Debe definirse **cuándo** queremos buscar la información.\
Ejemplo: “Cuando el cliente pregunte por un producto”. Ese será el detonante de la búsqueda.

![captura](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/OiQ6PaGcskLYA9oW2JGB/image%20png%20Nov%2026%202025%2004%2000%2008%203700%20PM.png)
{% endstep %}

{% step %}
**Agregar la función**

* Ir al paso correspondiente.
* Clic en **Agregar función**.
* Seleccionar **Búsqueda de base vectorial**.
* Crear nueva función.

![agregar función](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/oGStYgxbrIqocmX7EYW0/image%20png%20Nov%2026%202025%2004%2000%2055%207743%20PM.png) ![seleccionar](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/v6ZRZjneyUFTirk3uleU/image%20png%20Nov%2026%202025%2004%2002%2037%201573%20PM.png) ![crear](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/HtnwH3Cw9J5rqrHaHisE/image%20png%20Nov%2026%202025%2004%2004%2011%207474%20PM.png)
{% endstep %}

{% step %}
**Configurar parámetros**

Dentro de la función se debe definir:

*   Selección de documentos: seleccionar los documentos previamente cargados en la **Base de Conocimiento** desde donde la IA podrá extraer información.

    ![selección de documentos](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/rvg4ouapTVJRrgnsdjL0/image%20png%20Nov%2026%202025%2004%2006%2034%203787%20PM.png)
*   Número de documentos o resultados: indica cuánta información traer desde los documentos. Ejemplo: **12** → los “12 fragmentos más similares”.

    ![número de resultados](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/7ll3aN8eaUDfgN1bXCek/image%20png%20Nov%2026%202025%2004%2007%2005%206971%20PM.png)
*   Umbral de similitud (opcional): define qué tan parecido debe ser el contenido encontrado (valor entre 0 y 1). Ejemplos:

    * 0.2 → búsqueda amplia.
    * 0.5 → coincidencias moderadas.
    * 0.8 → coincidencias muy estrictas.

    ![umbral](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/mDQHaZ94YZTOMeN6k5wU/image%20png%20Nov%2026%202025%2004%2007%2033%200331%20PM.png)
* Palabra clave de búsqueda: la pista que le damos a la IA. Ejemplo: “Usar el producto mencionado por el cliente como palabra clave de búsqueda.”
*   Estructura del documento: describir cómo está organizado el documento para que la IA interprete correctamente la información.\
    Ejemplo: “Esta hoja tiene 5 columnas: nombre del producto, descripción, precio, categoría y stock.”

    ![estructura](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/IKFmRjKA4LnSiOxmNCX9/image%20png%20Nov%2026%202025%2004%2008%2030%209283%20PM.png)
{% endstep %}

{% step %}
**Guardar y usar la función**

En el paso correspondiente escribir la instrucción para ejecutar la función, por ejemplo:

> “Debes ejecutar la función buscar\_información\_producto.”

![usar función](https://content.gitbook.com/content/jZ46rFloLOG1hJ2JQGi0/blobs/E26uUANRZ6UPfJXMeXf8/image%20png%20Nov%2026%202025%2004%2010%2051%205922%20PM.png)
{% endstep %}
{% endstepper %}

***

### Método 2: Buscar fila en hoja (solo Google Sheets)

#### ¿Qué hace este método?

Permite buscar un valor exacto en una columna de Google Sheets y obtener toda la fila completa.

Se usa cuando necesitamos:

* Buscar un cliente por su teléfono o correo.
* Buscar un producto por un código exacto.
* Buscar información perfectamente estructurada.

Ejemplo:

> La IA busca en la columna “Producto” el valor exacto “Martillo Industrial N°4” y trae toda la fila que incluye precio, proveedor, stock, peso, etc.

{% stepper %}
{% step %}
**Entrar al asistente**

Mismo procedimiento que en el método anterior.
{% endstep %}

{% step %}
**Seleccionar el paso donde ocurrirá la búsqueda**

Ejemplo: “Cuando el cliente mencione un producto específico.”
{% endstep %}

{% step %}
**Crear la función**

* Agregar función.
* Seleccionar **Buscar fila en hoja**.
* Crear nueva función.
{% endstep %}

{% step %}
**Configurar parámetros**

La función permite dos formas de conexión:

* Conexión directa a Google: conectar con tu cuenta de Google → seleccionar el Google Sheet.
* Mediante URL: requiere dar permiso al correo que aparece en la interfaz.

Luego:

* Seleccionar la hoja.
* Definir los nombres de las columnas.
* Marcar como “Requerida” la columna desde donde se hará la búsqueda exacta.
{% endstep %}
{% endstepper %}

#### Errores comunes

<details>

<summary>Ver errores comunes</summary>

1. Las columnas del Google Sheet cambian a mitad de la hoja.
   * Esto confunde a la IA. Todas las filas deben seguir la misma estructura.
2. El documento contiene imágenes en vez de texto.
   * La IA no puede leerlas.
3. Se cargó mal la URL o no se asignaron permisos.

</details>

***

#### Resumen claro de ambos métodos

| Método                  |          Tipo de búsqueda | Ideal para                                         | Limitaciones                    |
| ----------------------- | ------------------------: | -------------------------------------------------- | ------------------------------- |
| **Vector Based Search** | Semántica / por similitud | Productos, textos largos, políticas, descripciones | No sirve para valores exactos   |
| **Buscar fila en hoja** |        Exacta por columna | Precios, clientes, catálogos estructurados         | Solo funciona con Google Sheets |
