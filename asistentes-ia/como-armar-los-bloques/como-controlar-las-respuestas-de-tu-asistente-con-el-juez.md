# Cómo controlar las respuestas de tu asistente con el Juez

Por más bien configurado que esté un asistente, puede que en algún momento mencione a la competencia, revele información sensible, o responda fuera del tema que le corresponde. El **Juez** es un segundo asistente que revisa cada respuesta antes de que llegue al usuario y, si detecta que rompe alguna regla definida, la corrige en el momento.

Se configura una sola vez y puede aplicarse a uno o varios asistentes al mismo tiempo.

***

### ¿Qué puedes lograr?

* Evitar que el asistente mencione marcas de la competencia
* Prevenir que se revele información sensible del negocio o del cliente
* Mantener al asistente dentro de un tema específico, como agendamiento o soporte
* Medir cuántas veces se habría aplicado una corrección antes de activarla formalmente

***

### Cómo crear un Juez

1. Entra al asistente donde quieres configurarlo
2.  Haz clic en el botón **"Juez"** que aparece en la vista del asistente\
    <br>

    <figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>
3. Haz clic en **"Crear nuevo"**
4. Ingresa un **nombre** para identificarlo
5. Selecciona el **tipo** de regla:

| Tipo                  | Qué hace                                                 |
| --------------------- | -------------------------------------------------------- |
| Fuga de datos         | Detecta cuando la IA podría revelar información sensible |
| Mención de competidor | Bloquea menciones a competidores                         |
| Fuera de alcance      | Mantiene al asistente dentro de su alcance               |
| Personalizado         | Define tu propia política con texto libre                |

6. En el campo **Regla**, describe con tus propias palabras la política que quieres aplicar. Puedes agregar más de una regla con el botón **"+ Añadir regla"**
7. Revisa la **Política aplicada**: Vambe toma tus reglas y genera automáticamente una versión más precisa que es la que el Juez usará para evaluar cada respuesta

> 💡 No es necesario editar la política aplicada — está pensada para que la IA la interprete de forma más precisa que la regla original.

8. Haz clic en **"Guardar cambios"** y luego en **"Volver"**

<figure><img src="../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

***

### Cómo asignar el Juez a un asistente

Una vez creado, verás la pantalla de **"Juez personalizado"** con todos los jueces disponibles en tu biblioteca.

1. Selecciona el Juez que quieres usar — aparecerá como **"Juez asignado"** en la parte superior
2. Desde esa misma vista puedes ver el resumen de la regla, la política aplicada y el estado actual (Activo / Inactivo) para ese asistente
3. Para editarlo o cambiar su configuración, haz clic en **"Configurar"**

> ⚠️ Cada asistente solo puede tener **un Juez asignado** a la vez.

<figure><img src="../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

***

### Activo vs. Inactivo

El estado del Juez se controla con un toggle y se configura por asistente:

*   **Activo:** cuando el asistente genera una respuesta que rompe la regla, el Juez la detiene y le pide que la reformule antes de enviarla al usuario. Si el asistente vuelve a romper la regla, se registra como un incidente.
*   **Inactivo:** el Juez detecta y registra las infracciones, pero no interviene en la conversación.

> 💡 **Tip:** Empieza en modo **Inactivo** para validar que las reglas están bien definidas y ver con qué frecuencia se activan, antes de habilitarlo formalmente. Para un monitoreo más eficiente, Vambe ahora ofrece un **indicador de activaciones** que muestra la cantidad de veces que el Juez se ha activado en los últimos 30 días, lo que te permite evaluar su impacto y ajustar las reglas si es necesario.

Puedes revisar las infracciones detectadas en los logs del asistente, igual que con los guardrails.

<figure><img src="../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

***

### Cómo funciona el Juez entre varios asistentes

* Un mismo Juez puede estar **compartido entre varios asistentes** — se crea una vez en la biblioteca y se asigna a los que lo necesiten
* Si editas las reglas de un Juez compartido, el cambio se aplica a todos los asistentes que lo tienen asignado
* El estado Activo / Inactivo se configura **por asistente** — el mismo Juez puede estar activo en uno e inactivo en otro

***

### Diferencia entre el Juez y el "Do not"

El **Do not** actúa antes de que el asistente genere su respuesta: le indica qué no debe hacer al momento de construirla.

El **Juez** actúa después: revisa la respuesta ya generada y la corrige si incumple una regla. Son complementarios y pueden usarse juntos.

***