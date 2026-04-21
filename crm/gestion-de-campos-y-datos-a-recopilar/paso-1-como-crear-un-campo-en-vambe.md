# Paso 1 - Cómo crear un campo en Vambe

Los campos son contenedores de datos que permiten que la inteligencia artificial y tu equipo almacenen información del cliente o del ticket. Estos campos son ahora fundamentales para las nuevas estrategias de asignación automática avanzada, permitiendo reglas de enrutamiento basadas en datos específicos.

Antes de asignarlos o usarlos, primero deben crearse.

{% stepper %}
{% step %}
### Ingresar a la sección de Campos

En el menú lateral selecciona:

CRM → Campos

Luego haz clic en:

Crear campo (arriba a la derecha)

![](<../.gitbook/assets/image png Dec 11 2025 02 33 50 2893 PM.png>)
{% endstep %}

{% step %}
### Completar los datos del campo

#### A) Nombre del campo

Debe ser claro y autoexplicativo.

Ejemplos:

*   _producto\_interes_
*   _telefono\_formateado_
*   _fecha\_visita_

![](<../.gitbook/assets/image png Dec 11 2025 02 34 53 2866 PM.png>)

***

#### B) Tipo de campo

Selecciona el formato adecuado:

*   **Texto** (palabras, frases)
*   **Número**
*   **Fecha**
*   **Sí/No**
*   **Opciones** (lista de alternativas predefinidas)

Nota: En “Opciones”, debes escribir cada una de las alternativas que deseas que aparezcan

![](<../.gitbook/assets/image png Dec 11 2025 02 35 52 2422 PM.png>)

***

#### C) Descripción del campo

Esta es la parte más importante del campo.

La IA leerá esta descripción para saber **qué debe guardar y en qué formato**.

Ejemplos:

*   “Aquí debes guardar el número telefónico del cliente en formato +569XXXXXXXX.”
*   “Aquí debes guardar el producto o los productos de interés del cliente. Si son varios, guardarlos como lista.”
*   “Guardar la fecha en formato AAAA-MM-DD.”

Mientras más clara sea la descripción, mejor será el dato registrado.

![](<../.gitbook/assets/image png Dec 11 2025 02 36 57 5114 PM.png>)

***

#### D) Configuraciones del campo (switches)

*   Campo requerido
    La IA intentará siempre completarlo cuando pueda.
*   Editable por la IA
    Permite que la IA cree o modifique este dato automáticamente.
*   Visible en UI
    Hace que el campo sea visible para los usuarios dentro del ticket o perfil del cliente.
*   Editable por los usuarios
    Permite que agentes y administradores modifiquen el dato manualmente.

![](<../.gitbook/assets/image png Dec 11 2025 02 37 37 5969 PM.png>)
{% endstep %}

{% step %}
### Guardar el campo

Haz clic en **Crear campo**.

El campo ya está listo para usarse en clientes o tickets (pero aún no está asignado a ninguno). Recuerda que los campos personalizados son esenciales para definir las condiciones en las nuevas estrategias de asignación automática de tickets. [Aprende a configurarlas aquí.](usuarios/notificaciones/como-elegir-que-agente-recibe-un-ticket-y-activar-notificaciones-automaticas.md)

Para que la IA comience a recopilarlos, debes asignarlos a un contacto o a un tipo de ticket.

![](<../.gitbook/assets/image png Dec 11 2025 02 38 12 1917 PM.png>)
{% endstep %}
{% endstepper %}
