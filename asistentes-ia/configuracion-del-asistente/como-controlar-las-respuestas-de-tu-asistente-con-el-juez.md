# Cómo controlar las respuestas de tu asistente con el Juez

Por más completa que esté la configuración de un asistente, en algún momento puede llegar a mencionar a la competencia, revelar información sensible o responder fuera del tema que le corresponde. El **Juez** es un segundo asistente que revisa cada respuesta antes de que llegue al usuario y, si detecta que incumple una política definida, la corrige en el momento.

Los Jueces se crean a partir de plantillas: se elige qué se quiere proteger y se completa una lista simple con la información relevante (direcciones, datos confidenciales, temas, competidores, etc.). Un mismo asistente puede tener varios Jueces asignados a la vez, cada uno revisando una política distinta de forma independiente.

***

### ¿Qué se puede lograr con los Jueces?

* Evitar que el asistente mencione marcas de la competencia
* Evitar que revele direcciones o ubicaciones que no coincidan con las oficiales
* Prevenir que revele información sensible del negocio, como valores o criterios internos
* Mantener al asistente dentro de un tema específico, como agendamiento o soporte
* Evitar que confirme acciones —una cita agendada, un pago, un envío— sin que exista una ejecución real detrás
* Evitar que entregue precios sin respaldo en el catálogo, la base de conocimiento o las funciones del asistente
* Detectar respuestas que contradicen las instrucciones del asistente, especialmente sus prohibiciones explícitas (Do Not)
* Medir cuántas veces se habría aplicado una corrección, antes de activar el Juez de forma definitiva

***

### Los 7 tipos de Juez disponibles

Cada Juez se crea a partir de una plantilla. El nombre y el comportamiento del Juez quedan definidos por la plantilla elegida; solo es necesario completar la información específica que cada una solicita.

| Tipo                               | Qué bloquea                                                                                   |
| ---------------------------------- | --------------------------------------------------------------------------------------------- |
| **Direcciones oficiales**          | Direcciones o ubicaciones que no coincidan con las oficiales que se definan                   |
| **Información confidencial**       | Respuestas que revelan valores, umbrales o criterios internos definidos como confidenciales   |
| **Temas fuera de alcance**         | Respuestas que desarrollan temas definidos como prohibidos                                    |
| **Mención de competidor**          | Menciones a los competidores definidos en la lista                                            |
| **Confirmaciones sin ejecutar**    | Confirmar acciones (cita agendada, pago, envío) sin que exista una ejecución real detrás      |
| **Precios inventados**             | Precios sin respaldo en el catálogo, la base de conocimiento o las funciones del asistente    |
| **Contradicción de instrucciones** | Respuestas que contradicen las instrucciones del asistente o rompen una prohibición explícita |

> 💡 La plantilla **Contradicción de instrucciones** no requiere configuración adicional: evalúa cada respuesta usando el contexto del asistente de forma automática.

<figure><img src="../.gitbook/assets/image (21) (1).png" alt=""><figcaption></figcaption></figure>



***

### Cómo crear un Juez

1. Ingresar al asistente donde se desea configurar.
2. Hacer clic en el botón **Juez** en la vista del asistente.
3. Hacer clic en **Crear nuevo** (o en **Asignar** si el asistente ya tiene otros Jueces).
4. Seleccionar el tipo de Juez entre las 7 plantillas disponibles.
5. Si la plantilla lo requiere, completar la lista correspondiente: direcciones oficiales, datos confidenciales, temas prohibidos, competidores, etc.
6. Hacer clic en **Crear juez**.

> 💡 El nombre del Juez lo define la plantilla elegida; no es necesario escribirlo ni redactar la política en texto libre.

***

### Cómo asignar Jueces a un asistente

Un asistente puede tener **varios Jueces asignados a la vez**, uno por política, y cada uno revisa las respuestas de forma independiente.

1. Dentro del asistente, hacer clic en **Juez** para ver los Jueces ya asignados y, más abajo, los disponibles en la biblioteca.
2. Hacer clic en **Asignar** para agregar otro Juez de la biblioteca a este asistente.
3. Para cada Juez asignado se puede ver la política aplicada y el estado (Activo / Inactivo) correspondiente a este asistente en particular.
4. Para editar la configuración de un Juez de plantilla, hacer clic en **Configurar**.

> ⚠️ Al asignar un Juez, este queda **Activo de inmediato** y comienza a revisar las respuestas desde ese momento. Puede pausarse en cualquier momento desde el mismo panel, sin necesidad de desasignarlo.

<figure><img src="../.gitbook/assets/image (22) (1).png" alt=""><figcaption></figcaption></figure>

***

### Activo vs. Inactivo

El estado de cada Juez se controla con un interruptor y se configura de forma independiente por asistente:

* **Activo:** cuando el asistente genera una respuesta que incumple la política, el Juez la detiene y le solicita reformularla antes de enviarla al usuario. Si el asistente vuelve a incumplirla, queda registrado como un incidente.
* **Inactivo:** el Juez detecta y registra las infracciones, pero no interviene en la conversación.

> 💡 Se recomienda comenzar en modo **Inactivo** para validar que la política está bien definida y observar con qué frecuencia se activaría, antes de habilitarla de forma definitiva. El indicador de activaciones muestra cuántas veces se ha activado el Juez en los últimos 30 días, lo que permite evaluar su impacto y ajustar la configuración si es necesario.

Las infracciones detectadas se pueden revisar en los logs del asistente, igual que con los guardrails.

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FUetO7TZyQHePewt69kqh%2Fimage.png?alt=media&#x26;token=9ca9d65e-3f5c-4cf8-98a6-a7af5c18ffba" alt=""><figcaption></figcaption></figure>

***

### Cuántos Jueces asignar

Cada Juez asignado representa una revisión adicional de IA sobre cada respuesta del asistente, antes de que esta llegue al usuario. Se recomienda asignar únicamente los que la operación realmente necesita: sumar Jueces innecesarios agrega latencia y costo sin un beneficio adicional.

***

### Cómo funciona el Juez entre varios asistentes

* Un mismo Juez de plantilla puede estar **compartido entre varios asistentes**: se crea una vez en la biblioteca y se asigna a los que lo necesiten.
* Si se edita la configuración de un Juez compartido, el cambio se aplica a todos los asistentes que lo tienen asignado.
* El estado Activo / Inactivo se configura **por asistente**: el mismo Juez puede estar activo en uno e inactivo en otro.

***

### Jueces personalizados existentes (modo solo lectura)

Los Jueces personalizados con reglas en texto libre que ya existan en la biblioteca siguen funcionando exactamente igual: no se eliminan ni se migran de forma obligatoria. En la biblioteca aparecen marcados con la etiqueta **Solo lectura**: se pueden seguir usando y pausando, pero no se pueden editar ni se pueden crear Jueces nuevos de este tipo.

<figure><img src="../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>

Para modificar la política de un Juez personalizado existente, el camino es crear el o los Jueces de plantilla equivalentes, asignarlos al asistente y luego desasociar el Juez personalizado.

***

### Diferencia entre el Juez y el "Do not"

El **Do not** actúa antes de que el asistente genere su respuesta: le indica qué no debe hacer al momento de construirla.

El **Juez** actúa después: revisa la respuesta ya generada y la corrige si incumple una política. Son complementarios y se pueden usar juntos —de hecho, la plantilla **Contradicción de instrucciones** está pensada específicamente para reforzar los Do Not del asistente.

***
