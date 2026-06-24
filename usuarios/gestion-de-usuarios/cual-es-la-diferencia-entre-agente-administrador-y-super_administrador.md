# ¿Cuál es la diferencia entre ejecutivo, Administrador y Super\_administrador?

En Vambe existen tres rangos de usuario. Cada uno determina el nivel de acceso, visibilidad y control que una persona puede ejercer dentro del sistema. Comprender estas diferencias es fundamental para asignar correctamente los permisos y mantener una operación organizada y segura.

A continuación se detalla cada rango de manera clara y formal, incluyendo cómo interactúan con las funcionalidades de analíticas y dashboards.

{% stepper %}
{% step %}
**Ejecutivo**

El **Ejecutivo** es el rol con acceso más limitado y está orientado al trabajo operativo individual.

**Capacidades**

* Puede ver únicamente **los tickets que le sean asignados**.
* Las asignaciones pueden configurarse de forma manual o mediante **asignaciones automáticas** dentro del embudo.
* En cuanto a analíticas, su acceso es nulo por defecto. Podrá **ver dashboards solo si un creador le otorga un permiso de "Lectura con invitación"** sobre un dashboard específico.

**Restricciones**

* No puede ver tickets que no le correspondan.
* No tiene permisos para modificar la inteligencia artificial ni acceder a configuraciones avanzadas o gestionar analíticas.

Este rango es adecuado para ejecutivos de ventas o atención que gestionan únicamente su propia cartera de tickets.
{% endstep %}

{% step %}
**Administrador**

El **Administrador** cuenta con mayor visibilidad, pero sigue teniendo restricciones en funciones críticas.

**Capacidades**

* Puede ver **todos los tickets y todos los contactos** presentes en Vambe.
* Puede supervisar la operación completa del equipo.
* Tiene **permiso de "Lectura" en analíticas**, lo que le permite ver todos los widgets públicos. Además, puede recibir permisos de "Lectura con invitación" o "Escritura" sobre dashboards específicos si un creador los comparte.

**Restricciones**

* No puede modificar configuraciones de la inteligencia artificial.
* No tiene acceso a la lógica interna ni a funciones avanzadas de automatización.
* Por defecto, no posee permisos para crear, actualizar o eliminar dashboards y widgets de analíticas globales.

Este rol es ideal para líderes, supervisores o coordinadores que requieren una visión amplia sin intervenir en elementos técnicos.
{% endstep %}

{% step %}
**Superadministrador**

El **Superadministrador** es el rol con acceso total dentro de Vambe.

**Capacidades**

* Puede ver **todos los tickets y contactos**.
* Puede **modificar la inteligencia artificial**, automatizaciones, asistentes, embudos, etapas y reglas internas.
* Puede crear, editar y gestionar usuarios, canales y configuraciones generales.
* Posee **control total sobre las analíticas y dashboards**, incluyendo la creación, actualización, eliminación y capacidad de compartir dashboards con permisos de "Lectura" o "Escritura", así como gestionar todos los tipos de permisos de analíticas (Escritura, Lectura, Lectura con invitación, Insights y suscripción de reportes).

**Restricciones**

* No presenta restricciones de acceso.

Este rol debe asignarse únicamente a las personas responsables de administrar Vambe a nivel técnico o estratégico.
{% endstep %}
{% endstepper %}

### Resumen comparativo

| Rango                  | Ve todos los tickets | Ve solo tickets asignados | Modifica IA | Gestiona/Accede a Analíticas                          | Recomendado para…                    |
| ---------------------- | :------------------: | :-----------------------: | :---------: | ----------------------------------------------------- | ------------------------------------ |
| **Ejecutivo**          |          No          |             Sí            |      No     | Solo "Lectura con invitación" si se le comparte       | Ejecutivos operativos                |
| **Administrador**      |          Sí          |             No            |      No     | "Lectura" de widgets públicos; puede ser invitado     | Supervisores y líderes               |
| **Superadministrador** |          Sí          |             No            |      Sí     | Control total (creación, edición, compartición, etc.) | Administradores generales / Técnicos |
