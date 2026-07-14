# Paso 1 - Cómo crear un campo en Vambe

## Paso 1 - Cómo crear un campo en Vambe

Los campos son contenedores de datos que permiten que la inteligencia artificial y tu equipo almacenen información del cliente o del ticket. Estos campos son ahora fundamentales para las nuevas estrategias de asignación automática avanzada, permitiendo reglas de enrutamiento basadas en datos específicos.

Antes de asignarlos o usarlos, primero deben crearse.

{% stepper %}
{% step %}
#### Ingresar a la sección de Campos

En el menú lateral selecciona:

CRM → Campos

Luego haz clic en:

Crear campo (arriba a la derecha)

![](https://content.gitbook.com/content/RUgcMYDLALCYrWDqh6tC/blobs/IJgjkgEtJqKYV1fqMtRe/image%20png%20Dec%2011%202025%2002%2033%2050%202893%20PM.png)
{% endstep %}

{% step %}
#### Completar los datos del campo

**A) Nombre del campo**

Debe ser claro y autoexplicativo.

Ejemplos:

* _producto\_interes_
* _telefono\_formateado_
* _fecha\_visita_

![](https://content.gitbook.com/content/RUgcMYDLALCYrWDqh6tC/blobs/rN5FfNPSs2UUgxSFvOkQ/image%20png%20Dec%2011%202025%2002%2034%2053%202866%20PM.png)

***

**B) Tipo de campo**

Selecciona el formato adecuado:

* **Texto** (palabras, frases)
* **Número**
* **Fecha**
* **Sí/No**
* **Opciones** (lista de alternativas predefinidas)

Nota: En “Opciones”, debes escribir cada una de las alternativas que deseas que aparezcan

![](https://content.gitbook.com/content/RUgcMYDLALCYrWDqh6tC/blobs/SN82F72afdafpii0Ru3y/image%20png%20Dec%2011%202025%2002%2035%2052%202422%20PM.png)

***

**C) Descripción del campo**

Esta es la parte más importante del campo.

La IA leerá esta descripción para saber **qué debe guardar y en qué formato**.

Ejemplos:

* “Aquí debes guardar el número telefónico del cliente en formato +569XXXXXXXX.”
* “Aquí debes guardar el producto o los productos de interés del cliente. Si son varios, guardarlos como lista.”
* “Guardar la fecha en formato AAAA-MM-DD.”

Mientras más clara sea la descripción, mejor será el dato registrado.

![](https://content.gitbook.com/content/RUgcMYDLALCYrWDqh6tC/blobs/DaKZGYtXbksdqY5AJeBz/image%20png%20Dec%2011%202025%2002%2036%2057%205114%20PM.png)

***

**D) Configuraciones del campo (switches)**

* Campo requerido La IA intentará siempre completarlo cuando pueda.
* Editable por la IA Permite que la IA cree o modifique este dato automáticamente.
* Visible en UI Hace que el campo sea visible para los usuarios dentro del ticket o perfil del cliente.
* Editable por los usuarios Permite que agentes y administradores modifiquen el dato manualmente.
* **Validación de Formato (Exclusivo para campos de tipo Texto)** Define un formato específico (como Email o Teléfono) para los datos que se ingresen en este campo. Esta configuración opcional asegura la calidad de los datos, previene errores de llenado y evita problemas de fusión de contactos en el CRM. Disponible actualmente para formatos de Email y Teléfono.

![](https://content.gitbook.com/content/RUgcMYDLALCYrWDqh6tC/blobs/DUA03hAkkHMQrjEjamXb/image%20png%20Dec%2011%202025%2002%2037%2037%205969%20PM.png)
{% endstep %}

{% step %}
#### Guardar el campo

Haz clic en **Crear campo**.

El campo ya está listo para usarse en clientes o tickets (pero aún no está asignado a ninguno). Recuerda que los campos personalizados son esenciales para definir las condiciones en las nuevas estrategias de asignación automática de tickets. [Aprende a configurarlas aquí.](https://academy.vambe.ai/usuarios/notificaciones/como-elegir-que-agente-recibe-un-ticket-y-activar-notificaciones-automaticas)

Para que la IA comience a recopilarlos, debes asignarlos a un contacto o a un tipo de ticket.

![](https://content.gitbook.com/content/RUgcMYDLALCYrWDqh6tC/blobs/8hMaiFi228FQVF7uWAT3/image%20png%20Dec%2011%202025%2002%2038%2012%201917%20PM.png)
{% endstep %}
{% endstepper %}
