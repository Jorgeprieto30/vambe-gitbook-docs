# Cómo evitar respuestas innecesarias con "No responder"

Cuando un usuario manda un "gracias", un emoji, o dice que no le interesa el servicio, el asistente no debería responder — pero sin esta configuración, lo hace igual. Eso genera conversaciones que se extienden sin sentido, o peor, bucles donde el asistente sigue respondiendo indefinidamente.

**"No responder"** le permite al asistente reconocer esos momentos y cerrar la conversación de forma limpia, sin enviarle nada al usuario.

***

### ¿Qué puedes lograr?

* Cerrar conversaciones de forma natural cuando el usuario se despide o ya no necesita respuesta
* Eliminar bucles infinitos donde el asistente seguía respondiendo sin razón
* Dejar registrado internamente por qué el asistente decidió no responder, sin afectar la experiencia del usuario

***

### Cómo activarlo

Esta configuración está disponible en el panel de identidad del asistente, tanto en asistentes v2 como v3.

1. Entra al asistente que quieres configurar
2. En el resumen del asistente, ubica la opción **"No responder"** y activa el switch
3. Se abrirá un cuadro de texto con el campo **"Cuándo no responder"**

> Este campo es **opcional**. Si lo dejas vacío, Vambe usará una guía por defecto que cubre los casos más comunes: cierres sociales como "gracias", "ok", "listo", mensajes con solo emojis, y pedidos explícitos del usuario de no ser contactado.

<figure><img src="../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

***

### Cómo personalizar las instrucciones

Si necesitas que el asistente no responda en situaciones específicas de tu negocio, puedes escribirlo directamente en el campo de texto.

**Ejemplo:**

> _"No respondas cuando el usuario indique que no está interesado en los servicios."_

La IA leerá esas instrucciones y las aplicará en cada conversación.

4. Haz clic en **Guardar**

<figure><img src="../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

***

### ¿Qué pasa cuando el asistente decide no responder?

* No se envía ningún mensaje al usuario
* El asistente deja una **nota interna en el chat** explicando por qué no respondió
* La corrida termina de forma limpia, sin dejar el ticket en un estado inconsistente

***

> ⚠️ **Importante:** Activa esta opción solo en los asistentes donde quieras controlar este comportamiento. Asegúrate de que las instrucciones sean precisas para que el asistente no deje de responder en situaciones donde sí debería hacerlo.
