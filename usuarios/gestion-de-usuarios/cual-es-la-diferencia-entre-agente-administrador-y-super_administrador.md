# ¿Cuál es la diferencia entre Agente, Administrador y Super\_administrador?

En Vambe existen tres rangos de usuario. Cada uno determina el nivel de acceso, visibilidad y control que una persona puede ejercer dentro del sistema. Comprender estas diferencias es fundamental para asignar correctamente los permisos y mantener una operación organizada y segura.

A continuación se detalla cada rango de manera clara y formal.

{% stepper %}
{% step %}
#### Agente

El **Agente** es el rol con acceso más limitado y está orientado al trabajo operativo individual.

**Capacidades**

* Puede ver únicamente **los tickets que le sean asignados**.
* Las asignaciones pueden configurarse de forma manual o mediante **asignaciones automáticas** dentro del embudo.

**Restricciones**

* No puede ver tickets que no le correspondan.
* No tiene permisos para modificar la inteligencia artificial ni acceder a configuraciones avanzadas.

Este rango es adecuado para ejecutivos de ventas o atención que gestionan únicamente su propia cartera de tickets.
{% endstep %}

{% step %}
#### Administrador

El **Administrador** cuenta con mayor visibilidad, pero sigue teniendo restricciones en funciones críticas.

**Capacidades**

* Puede ver **todos los tickets y todos los contactos** presentes en Vambe.
* Puede supervisar la operación completa del equipo.

**Restricciones**

* No puede modificar configuraciones de la inteligencia artificial.
* No tiene acceso a la lógica interna ni a funciones avanzadas de automatización.

Este rol es ideal para líderes, supervisores o coordinadores que requieren una visión amplia sin intervenir en elementos técnicos.
{% endstep %}

{% step %}
#### Superadministrador

El **Superadministrador** es el rol con acceso total dentro de Vambe.

**Capacidades**

* Puede ver **todos los tickets y contactos**.
* Puede **modificar la inteligencia artificial**, automatizaciones, asistentes, embudos, etapas y reglas internas.
* Puede crear, editar y gestionar usuarios, canales y configuraciones generales.

**Restricciones**

* No presenta restricciones de acceso.

Este rol debe asignarse únicamente a las personas responsables de administrar Vambe a nivel técnico o estratégico.
{% endstep %}
{% endstepper %}

### Resumen comparativo

| Rango                  | Ve todos los tickets | Ve solo tickets asignados | Modifica IA | Recomendado para…                    |
| ---------------------- | -------------------: | ------------------------: | ----------: | ------------------------------------ |
| **Agente**             |                   No |                        Sí |          No | Ejecutivos operativos                |
| **Administrador**      |                   Sí |                        No |          No | Supervisores y líderes               |
| **Superadministrador** |                   Sí |                        Sí |          Sí | Administradores generales / Técnicos |
