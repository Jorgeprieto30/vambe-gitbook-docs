# Funciones en Asistentes con Escenarios (V3)

Las Funciones son las acciones que tu asistente puede ejecutar: cambiar de etapa, enviar una plantilla, crear una nota, ejecutar un Flow, entre otras. En los asistentes V3, las funciones se gestionan de forma centralizada a nivel de asistente y se referencian desde las rutas.

***

### ¿Cómo funcionan las funciones en V3?

En los asistentes V2 (con bloques), las funciones se configuraban dentro de cada bloque de Pasos a seguir o Casos posibles. En V3 el modelo cambia:

1. **Primero asocias la función al asistente** — la registras una vez a nivel global.
2. **Luego la referencias en las rutas** — le dices en qué momento debe ejecutarla.

Esto significa que una misma función puede usarse en múltiples rutas y escenarios sin tener que configurarla cada vez.

***

### Cómo agregar una función al asistente

1. Dentro de tu asistente, haz clic en la pestaña **Funciones**.
2. Haz clic en **+ Agregar función** (o el botón de búsqueda para encontrar una existente).
3. Selecciona el **tipo de función** que necesitas:

| Tipo de función                | Qué hace                                                              |
| ------------------------------ | --------------------------------------------------------------------- |
| **Cambio de Etapa**            | Mueve el ticket a otra etapa del embudo cuando se cumple la condición |
| **Quitar contacto del embudo** | Elimina al contacto del embudo si se cumple la condición              |
| **Enviar Plantilla**           | Envía una plantilla pre-creada desde la sección "Plantillas"          |
| **Enviar Audio**               | Envía un audio con voz seleccionada                                   |
| **Llamada Webhook**            | Ejecuta un webhook al cumplirse la condición                          |
| **Crear Nota**                 | Genera una nota automáticamente (las notas no se envían al cliente)   |
| **Enviar Documento o Imagen**  | Envía un archivo cuando se cumple la condición                        |
| **Ejecutar Flow**              | Activa un Flow con parámetros personalizados                          |
| **Gatillar Evento**            | Dispara un evento cuando se cumple la condición                       |
| **Buscar en Internet**         | Realiza una búsqueda en internet según la condición definida          |
| **Obtener Estado de Orden**    | Obtiene el estado de una orden desde un proveedor específico          |

4. Completa los datos de la función (nombre, descripción y configuración según el tipo).
5. Guarda. La función quedará asociada al asistente y disponible para ser usada en cualquier ruta.

***

### La descripción de la función: lo más importante

> ⚠️ **La descripción de la función es crítica.** La IA la usa para saber cuándo ejecutarla. Si la descripción es vaga, la función se ejecutará en momentos incorrectos o no se ejecutará cuando debería.

**Ejemplo de descripción mala:** _"Cambiar etapa"_

**Ejemplo de descripción buena:** _"Ejecutar cuando el cliente haya confirmado que quiere agendar una cita y haya entregado su nombre, RUT y fecha deseada."_

Mientras más específica y descriptiva sea, más precisa será la IA al usarla.

***

### Cómo referenciar una función en una Ruta

Una vez que la función está asociada al asistente, puedes referenciarla en cualquier ruta de dos formas:

**Forma 1 — Nombrarla en las instrucciones:** Simplemente menciona el nombre de la función dentro del texto de la ruta. La IA reconocerá que debe ejecutarla cuando corresponda.

Ejemplo: _"Una vez que el cliente confirme que quiere comprar, ejecuta la función 'Cambiar etapa a Venta'."_

**Forma 2 — Agregarla explícitamente como acción de la ruta:** En el editor de la ruta, puedes agregar la función como una acción directa, igual que en los casos posibles de V2.

> 💡 No es obligatorio mencionar la función en cada ruta. Si está asociada al asistente y su descripción es clara, la IA puede activarla por contexto sin que se lo indiques explícitamente en la ruta. Sin embargo, para funciones críticas (como cambios de etapa), siempre es mejor ser explícito.

***

### Ejemplo práctico

**Contexto:** Tienda de ropa que quiere cambiar de etapa cuando el cliente confirma una compra.

**Función asociada al asistente:**

* Nombre: _"Cambiar etapa a Compra confirmada"_
* Descripción: _"Ejecutar cuando el cliente haya elegido un producto, confirmado la talla y dicho que quiere comprarlo."_

**Ruta donde se referencia:**

* Escenario: _"Proceso de compra"_
* Ruta: _"Confirmación de compra"_
* Instrucciones: _"Cuando el cliente confirme que quiere el producto, agradece su elección, indícale los pasos para pagar y ejecuta la función 'Cambiar etapa a Compra confirmada'."_

***

### Puntos clave a recordar

* Las funciones se configuran **una vez a nivel de asistente** y se reutilizan en todas las rutas que las necesiten.
* La **descripción de la función** es lo que la IA usa para saber cuándo ejecutarla — escríbela con detalle.
* Puedes referenciar una función nombrándola en el texto de la ruta o agregándola como acción explícita.
* Una función bien descrita puede activarse por contexto sin necesidad de mencionarla en cada ruta.
