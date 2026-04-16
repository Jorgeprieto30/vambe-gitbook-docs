# Cómo crear Escenarios y Rutas en un Asistente con Escenarios

Los Escenarios y las Rutas son el corazón de los asistentes V3. Reemplazan los antiguos bloques de "Pasos a seguir" y "Casos posibles", dándole a la IA la flexibilidad de navegar la conversación de forma natural según lo que necesite cada cliente.

***

### Antes de empezar: entiende el concepto

#### ¿Qué es un Escenario?

Un **Escenario** es una carpeta que agrupa rutas relacionadas bajo un mismo propósito. Piénsalo como un "tema" o "área de acción" del asistente.

Ejemplos de escenarios:

* _**"Conversación con el cliente"**_
* _**"Información de productos y precios"**_
* _**"Gestión de pedidos"**_

#### ¿Qué es una Ruta?

Una **Ruta** es una instrucción específica dentro de un escenario. Es lo que la IA ejecutará cuando detecte que esa situación aplica. Cada ruta tiene:

* Una **descripción** que le dice a la IA cuándo debe activarse.
* El **contenido** con las instrucciones o información que debe usar.

#### ¿Cómo decide la IA qué ruta usar?

La IA lee la descripción de cada escenario y de cada ruta, y en tiempo real decide cuál se aplica mejor al mensaje del cliente. **Por eso las descripciones son lo más importante de todo el sistema** — deben ser claras, específicas y no genéricas.

***

### Ejemplo súper simple para entender la lógica

Imagina que tienes un restaurante y contratas a un mesero nuevo. El primer día le das un manual con tres secciones:

* 📋 **Sección "Bienvenida":** Qué hacer cuando llega un cliente.
* 🍽️ **Sección "Tomar pedido":** Qué hacer cuando el cliente quiere ordenar.
* 💳 **Sección "Cobro":** Qué hacer cuando el cliente pide la cuenta.

Cada sección tiene instrucciones específicas para distintas situaciones dentro de ella. El mesero no sigue un guion rígido — lee la situación y saca la instrucción correcta del manual.

En Vambe:

* Las **secciones del manual** = **Escenarios**
* Las **instrucciones dentro de cada sección** = **Rutas**
* El **mesero** = la IA

***

### Ejemplo del día a día: tienda de ropa online

Supongamos que tienes una tienda de ropa y quieres que tu asistente maneje ventas, consultas de talla y seguimiento de pedidos.

#### Estructura de escenarios:

**Escenario 1: "Atención inicial"**

* _Descripción del escenario:_ "Cuando el cliente nos escribe por primera vez o saluda sin especificar qué necesita."
* Ruta 1.1 — _"Saludo inicial":_ Descripción: "Cuando el cliente saluda sin indicar qué necesita." → Instrucción: Saludar, presentarse y preguntar en qué puede ayudar.
* Ruta 1.2 — _"Cliente que vuelve":_ Descripción: "Cuando el cliente menciona que ya compró antes o tiene un pedido." → Instrucción: Saludar de forma más cálida y derivar a la sección de seguimiento.

**Escenario 2: "Información de productos"**

* _Descripción del escenario:_ "Cuando el cliente pregunta por productos, tallas, colores o precios."
* Ruta 2.1 — _"Consulta de tallas":_ Descripción: "Cuando el cliente pregunta qué talla le queda o cómo son las tallas." → Instrucción: Entregar la guía de tallas + preguntar si quiere ayuda para elegir.
* Ruta 2.2 — _"Consulta de precios":_ Descripción: "Cuando el cliente pregunta cuánto cuesta algo." → Instrucción: Entregar los precios disponibles y mencionar medios de pago.

**Escenario 3: "Seguimiento de pedidos"**

* _Descripción del escenario:_ "Cuando el cliente quiere saber el estado de su compra o tiene un problema con su pedido."
* Ruta 3.1 — _"Rastrear pedido":_ Descripción: "Cuando el cliente pregunta dónde está su pedido." → Instrucción: Ejecutar función de rastreo de orden.
* Ruta 3.2 — _"Devolución":_ Descripción: "Cuando el cliente quiere devolver o cambiar un producto." → Instrucción: Explicar el proceso de devolución y derivar a agente humano.

#### ¿Cómo navega la IA?

Cuando un cliente escribe _"Hola, quiero saber si el vestido negro viene en talla M"_, la IA:

1. Lee las descripciones de todos los escenarios.
2. Identifica que aplica **Escenario 2 → Ruta 2.1** (consulta de tallas).
3. Ejecuta las instrucciones de esa ruta.

Si después el mismo cliente pregunta _"¿Y cuánto cuesta?"_, la IA cambia automáticamente a **Ruta 2.2** — sin que nadie lo programe explícitamente.

> 💡 Una ruta también puede "llamar" a otra ruta de otro escenario. Por ejemplo, después de entregar los precios (Ruta 2.2), la IA puede pasar a la Ruta 1.1 de cierre de conversación si el cliente no dice nada más.

***

### Cómo crear un Escenario paso a paso

#### Paso 1: Ir a la pestaña Escenarios

Dentro de tu asistente, haz clic en la pestaña **Escenarios**.

#### Paso 2: Agregar un escenario

Haz clic en **+ Agregar escenario**. Verás tres opciones:

* **Crear desde cero:** Para un escenario nuevo vacío.
* **Escenarios existentes:** Para reutilizar un escenario que ya creaste en otro asistente (como compartido o como copia).
* **Plantillas:** Escenarios pre-configurados por Vambe listos para usar.

#### Paso 3: Crear el escenario

Si eliges **Crear desde cero**:

1. **Nombre:** Dale un nombre descriptivo. Ej: _"Atención inicial"_, _"Información de productos"_.
2. **Instrucciones de cuándo usar este escenario:** Este campo es crítico. Escribe cuándo debe activarse este escenario. Ej: _"Este escenario debe activarse cuando el cliente nos saluda por primera vez o cuando no ha especificado qué necesita."_
3. Haz clic en **Crear**.

> ⚠️ **La descripción del escenario es la clave.** La IA la usa para decidir si debe entrar a ese escenario o no. Si es vaga o genérica, la IA no sabrá cuándo activarlo. Sé específico.

#### Paso 4: Agregar Rutas dentro del escenario

Una vez creado el escenario, verás el editor de rutas. Haz clic en **+ Agregar ruta** para crear la primera.

Cada ruta tiene:

* **Nombre:** Identifica la ruta dentro del escenario. Ej: _"Saludo inicial"_.
* **Descripción:** Cuándo debe activarse esta ruta específica. Ej: _"Cuando el cliente saluda sin indicar qué necesita."_
* **Instrucciones:** Qué debe hacer la IA cuando se activa esta ruta. Aquí va tanto el comportamiento como la información relevante.

> 💡 Puedes agregar tantas rutas como necesites dentro de un escenario. Cada ruta es independiente y la IA elige la más adecuada según el contexto.

***

### Reutilizar escenarios en otros asistentes

Una de las grandes ventajas de V3 es que puedes reutilizar escenarios entre asistentes.

Al agregar un escenario, si eliges uno **existente**, tienes dos opciones:

* **Crear una copia:** Se genera una copia independiente. Los cambios en uno no afectan al otro.
* **Usar como compartido:** El mismo escenario se comparte entre los dos asistentes. Si modificas una ruta, el cambio aplica en todos los asistentes que lo usen.

> ⚠️ Si usas un escenario como compartido y lo modificas, los cambios afectarán a todos los asistentes que lo tengan asociado. Úsalo cuando quieras mantener coherencia entre múltiples asistentes.

***

### Puntos clave a recordar

* Un **Escenario** es una carpeta de rutas agrupadas por propósito.
* Una **Ruta** es la instrucción específica que la IA ejecuta cuando detecta que aplica.
* La IA decide qué escenario y qué ruta usar basándose en sus **descripciones** — escríbelas con detalle.
* Una ruta puede referenciar o "llamar" a rutas de otros escenarios.
* Los escenarios pueden reutilizarse entre asistentes (como copia o como compartido).
* La información del negocio que antes iba en bloques de "Información clave" ahora va **dentro de las rutas** donde corresponde.
