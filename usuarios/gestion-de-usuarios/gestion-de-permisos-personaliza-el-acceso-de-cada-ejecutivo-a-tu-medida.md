# Gestión de Permisos: personaliza el acceso de cada Ejecutivo a tu medida

Los rangos de usuario (Ejecutivo, Administrador y Super Administrador) definen un punto de partida razonable para la mayoría de los equipos, pero no todas las organizaciones funcionan igual. Puede que necesites que alguien de marketing gestione campañas sin tocar contactos, que una persona vea solo la analítica sin poder editar nada más, o que un encargado de equipos administre miembros sin acceder a la configuración general. Para estos casos, Vambe te permite editar los permisos de cada rango y crear roles completamente nuevos, ajustados a lo que esa persona realmente necesita hacer.

Para entrar: en el menú de la izquierda, ve a **Ajustes > Equipos > Permisos**.

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

***

### Qué puedes hacer desde Permisos

Dentro de la sección de **Permisos** vas a encontrar una tabla con todos los permisos disponibles en Vambe, organizados por área (Contactos, Tickets, Equipos, Analítica, Configuración, y más). Cada columna representa un rol —Administrador, Ejecutivo, Encargado de equipos y Super Administrador— y cada fila un permiso específico que puedes activar o desactivar con un simple check.

Esto significa que ya no dependes únicamente de la definición estándar de cada rango: si quieres que tus Ejecutivos puedan exportar contactos, o que los Administradores dejen de ver ciertos dashboards, lo defines aquí directamente. El único rol que no se puede modificar es **Super Administrador**, ya que por diseño mantiene siempre todos los permisos activos.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

***

### Cuándo crear un rol nuevo en vez de editar uno existente

Editar los permisos de Administrador o Ejecutivo tiene sentido cuando el ajuste aplica a todas las personas que ya tienen ese rango. Pero si necesitas un perfil de acceso muy específico —por ejemplo, alguien de marketing que solo gestione campañas y plantillas, o una persona encargada únicamente de revisar analítica sin acceso a tickets ni contactos— lo recomendable es crear un rol nuevo en lugar de modificar los rangos generales. Así evitas afectar a todo el equipo y mantienes cada perfil de acceso limpio y fácil de entender.

Para crear un rol nuevo, ve al menú de la izquierda dentro de Ajustes, entra a **Equipos** y luego a **Roles**. Desde ahí puedes definir un nombre para el rol y asignarle, permiso por permiso, exactamente lo que esa persona debe poder ver y hacer en Vambe.

Como referencia rápida: si el cambio debería aplicar a todos los que ya tienen un rango (por ejemplo, todos los Ejecutivos), edítalo en Permisos. Si el cambio es para un perfil puntual y distinto a los rangos existentes, créalo como un rol nuevo en Roles.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

***

### Los permisos disponibles, área por área

A continuación se detallan todos los permisos que puedes editar en Vambe, agrupados por la sección a la que pertenecen. Usa esta lista como referencia al momento de decidir qué activar para cada rol.

#### Contactos

Controlan qué tanto puede ver y hacer un usuario con la base de contactos.

* **Crear**: crear nuevos contactos en el sistema.
* **Leer**: ver todos los contactos del workspace.
* **Leer Propios**: ver solo los contactos asignados al usuario.
* **Actualizar**: editar información y detalles de contactos.
* **Exportar**: exportar datos de contactos a formatos externos.
* **Gestionar Ejecutivos**: asignar y reasignar ejecutivos a contactos.
* **Bloquear**: bloquear contactos para que no puedan enviar mensajes.
* **Gestionar Etiquetas**: agregar, eliminar y gestionar etiquetas de contactos.
* **Descargar Archivos**: descargar archivos compartidos en las conversaciones.

#### Tickets

Definen el acceso a la gestión operativa del embudo de ventas o atención.

* **Crear**: crear nuevos tickets en el sistema.
* **Leer**: ver todos los tickets del workspace.
* **Leer Propios**: ver solo los tickets cuyo contacto está asignado al usuario.
* **Actualizar**: editar información y detalles de tickets.
* **Cambiar Etapa**: mover tickets entre etapas del pipeline.
* **Gestionar Ejecutivos**: asignar y reasignar ejecutivos a tickets.
* **Cerrar**: cerrar y archivar tickets.

#### Equipos

Regulan la administración de los equipos dentro de la organización.

* **Crear**: crear nuevos equipos en la organización.
* **Leer**: ver detalles del equipo e información de miembros.
* **Actualizar**: editar configuración y ajustes del equipo.
* **Eliminar**: eliminar equipos de la organización.
* **Gestionar Miembros**: agregar y eliminar miembros del equipo.
* **Asignar Líder**: asignar líderes y gerentes de equipo.

#### Analítica

Controlan quién puede ver, crear y compartir dashboards e insights.

* **Escritura**: permite crear, actualizar y eliminar dashboards y widgets.
* **Leer**: ver todos los dashboards de todas las secciones de análisis.
* **Leer por invitación**: ver solo los dashboards compartidos con el usuario.
* **Insights**: acceder a la función de Insights.
* **Suscripciones de informes**: gestionar suscripciones de informes programados.

{% hint style="info" %}
Este es el punto donde más se nota la diferencia entre rangos: por defecto, un Ejecutivo no tiene acceso a analítica salvo que reciba un permiso de "Lectura por invitación" sobre un dashboard puntual, mientras que un Administrador ya cuenta con "Leer" sobre todos los dashboards públicos.
{% endhint %}

#### Configuración

Agrupan el acceso a los ajustes generales del sistema, seguridad e integraciones.

* **Crear**: crear nuevas configuraciones del sistema.
* **Leer**: ver configuraciones y ajustes del sistema.
* **Actualizar**: modificar configuraciones y preferencias del sistema.
* **Gestionar Integraciones**: configurar y gestionar integraciones de terceros.
* **Gestionar Webhooks**: configurar y gestionar endpoints de webhooks.
* **Gestionar Facturación**: gestionar configuración de facturación y métodos de pago.
* **Gestionar Permisos**: configurar roles de usuario y permisos —es decir, el permiso que controla quién puede entrar a esta misma sección.
* **Gestionar Eventos de la App**: configurar y gestionar eventos de la app.

#### Usuarios

Controlan la administración de las cuentas de las personas que usan Vambe.

* **Crear**: crear nuevas cuentas de usuario.
* **Leer**: ver perfiles de usuario e información.
* **Actualizar**: editar detalles y configuración de usuarios.
* **Eliminar**: eliminar cuentas de usuario.
* **Suspender**: suspender temporalmente el acceso de usuarios.
* **Restablecer Contraseña**: restablecer contraseñas de usuarios.

#### Plantillas

Regulan la gestión de las plantillas de mensajes.

* **Crear**: crear nuevas plantillas de mensajes.
* **Leer**: ver plantillas de mensajes existentes.
* **Actualizar**: editar contenido y configuración de plantillas.
* **Eliminar**: eliminar plantillas de mensajes.

#### Campaña

Controlan la creación y ejecución de campañas de marketing.

* **Crear**: crear nuevas campañas de marketing.
* **Leer**: ver detalles y rendimiento de campañas.
* **Actualizar**: editar configuración y contenido de campañas.
* **Eliminar**: eliminar campañas de marketing.
* **Enviar**: enviar y ejecutar campañas de marketing.

#### Asistentes

Definen quién puede configurar y entrenar a los asistentes de IA.

* **Crear**: crear nuevos asistentes de IA.
* **Leer**: ver configuraciones y ajustes de asistentes.
* **Actualizar**: editar comportamiento y respuestas de asistentes.
* **Eliminar**: eliminar asistentes de IA.
* **Gestionar Conocimiento**: gestionar base de conocimientos y datos de entrenamiento del asistente.
* **Probar**: probar respuestas y funcionalidad del asistente.

#### Pipelines

Regulan la configuración de los pipelines de ventas.

* **Crear**: crear nuevos pipelines de ventas.
* **Leer**: ver configuraciones y etapas de pipelines.
* **Actualizar**: editar configuración y flujo de trabajo de pipelines.
* **Eliminar**: eliminar pipelines de ventas.
* **Leer Propios**: ver solo los pipelines a los que se tiene acceso.

#### Automatizaciones

* **Gestionar**: crear, editar y eliminar flujos de automatización.

#### Configuración CRM

* **Leer**: ver configuraciones de CRM.
* **Gestionar**: gestionar configuraciones de CRM.

#### Intenciones de Pago

* **Crear**: crear intenciones de pago.
* **Leer**: ver intenciones de pago.
* **Actualizar**: editar intenciones de pago.

#### Espacio de Trabajo

* **Leer**: ver configuraciones del espacio de trabajo.
* **Actualizar**: editar configuraciones del espacio de trabajo.
* **Gestionar Miembros**: gestionar miembros del espacio de trabajo.

#### Comentarios

* **Gestionar**: gestionar automatizaciones de comentarios de Instagram.

#### Anuncios

* **Acceso**: acceder a la plataforma de anuncios.
* **Gestionar Campañas**: crear, editar y gestionar campañas de anuncios.

***

### En resumen

La sección de Permisos te da control total sobre lo que cada rango puede hacer en Vambe, y la sección de Roles te permite ir un paso más allá, creando perfiles de acceso hechos a la medida de un equipo o una función específica —marketing, analítica, atención al cliente, o cualquier combinación que tu operación necesite. Antes de modificar un permiso, pregúntate si el cambio debe aplicar a todo un rango o solo a un perfil puntual: eso te dirá si conviene editar los rangos existentes o crear un rol nuevo, manteniendo así una gestión de accesos clara y ordenada para todo tu equipo.
