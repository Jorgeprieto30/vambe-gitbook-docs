# Cómo limpiar y mantener tu embudo ordenado

Un embudo sano refleja la realidad de tu negocio. Si tienes cientos de leads acumulados en etapas sin moverse, tu embudo deja de ser útil — no sabes qué leads son reales, los agentes pierden el foco y los análisis no sirven. En este artículo aprenderás a limpiar tu embudo de una vez y a mantenerlo ordenado de forma automática.

***

### ¿Por qué se acumula el embudo?

Los tickets se acumulan principalmente por dos razones:

1. **No hay criterio claro de cuándo cerrar un lead.** Si nadie define qué pasa con un cliente que no respondió en 3 días, ese ticket se queda flotando para siempre.
2. **El proceso de etapas humanas está subdefinido.** Si tienes una sola etapa de "Asistencia Humana" donde caen todos los clientes, se convierte en un cajón de sastre imposible de gestionar.

> 💡 **Regla general recomendada:** Si un lead no te ha escrito en 2 días, ya no es un lead activo. Intenta recontactarlo y, si no responde, ciérralo. La siguiente vez que te escriba, entrará de nuevo con la IA desde el inicio.

***

### Parte 1: Limpiar el embudo manualmente (una sola vez)

Este es el primer paso: hacer una limpieza general de todos los tickets viejos acumulados. Se hace con filtros y acciones colectivas.

#### Paso 1: Definir qué quieres limpiar

Antes de tocar nada, decide:

* **¿Qué etapas quieres limpiar?** Generalmente las etapas con IA (Inicial, Agendamiento) o etapas humanas donde se acumulan leads sin avance.
* **¿Desde cuándo?** Por ejemplo: todos los leads que no han interactuado desde hace más de una semana.
* **¿Qué harás con ellos?** Moverlos a una etapa de "Clientes Perdidos" o archivarlos directamente.

> 💡 No es necesario limpiar todas las etapas. Si tienes etapas humanas donde tus agentes están activos y al día, no las toques. Enfócate en las etapas donde sabes que hay tickets abandonados.

#### Paso 2: Aplicar filtros en el embudo

1. Ve a tu **Embudo**.
2. Haz clic en el botón de **Filtros**.
3. Configura los siguientes filtros:
   * **Fecha de creación:** Desde una fecha pasada (ej: hace 2 semanas) hasta la fecha que consideres el límite. Los tickets más recientes probablemente no necesitan limpieza.
   * **Etapa:** Selecciona solo las etapas que quieres limpiar (ej: Inicial, Agendamiento, Asistencia Humana).
   * **Agente asignado** _(opcional):_ Si quieres limpiar solo los tickets de un agente específico.

#### Paso 3: Usar acciones colectivas

Una vez aplicados los filtros, esta es la parte más importante:

1. Selecciona todos los tickets filtrados usando el selector de la parte superior.
2.  Haz clic en **Acciones colectivas**.\
    <br>

    <figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>


3. Elige qué hacer con ellos:

| Opción                                | Cuándo usarla                                                                                          |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Mover a etapa "Clientes Perdidos"** | Si tienes una etapa configurada que cierra y archiva el ticket automáticamente al entrar (recomendado) |
| **Archivar directamente**             | Si no tienes esa etapa configurada y quieres hacerlo de forma manual                                   |

> ⚠️ **Importante:** Cerrar o archivar un ticket **no elimina** al contacto ni la conversación. El historial siempre se mantiene en la sección **Chat**. Puedes buscarlo en cualquier momento por nombre, número o contenido del mensaje. Lo que se cierra es el ticket del embudo, no la conversación.

***

### Parte 2: Configurar la etapa "Clientes Perdidos"

Esta etapa es la clave para mantener el embudo limpio de forma automática a largo plazo. Cuando un cliente entra a esta etapa, el ticket se cierra, se marca como perdido y la próxima vez que ese cliente escriba, entra de nuevo al embudo desde el inicio con la IA.

#### Cómo configurarla

Necesitas crear un [**Workflow**](https://app.gitbook.com/o/9CuC7LM0j6YJ7xZrMGfk/s/0xCLgfGby0xiCWJaqr57/) con el siguiente trigger y acciones:

**Trigger:** Ingreso a etapa → _"Clientes Perdidos"_

**Acciones:**

1. Cerrar ticket
2. Marcar como perdido
3. Definir etapa de retorno → _"Inicial"_ (para que la próxima vez que escriba entre desde ahí)

> 💡 Una vez configurado este Workflow, cada vez que muevas un ticket a "Clientes Perdidos" — ya sea manualmente o por automatización — todo se ejecutará solo.

***

### Parte 3: Automatizar el cierre de leads inactivos

La limpieza manual es para poner el embudo al día. Pero para mantenerlo limpio hacia adelante, necesitas automatizaciones que cierren los tickets abandonados sin que tengas que hacerlo tú.

#### Automatización por inactividad

Usa el trigger de **Inactividad del contacto** en un Workflow:

**Ejemplo — Leads inactivos en etapa Inicial:**

```
Trigger: Inactividad del contacto
  └── Duración: 2 días
  └── Etapa: Inicial
  └── Espera Inteligente: Activada

Acción: Cambiar etapa → "Clientes Perdidos"
```

Al llegar a "Clientes Perdidos", el Workflow de esa etapa se encarga del resto (cerrar, marcar como perdido, definir retorno).

Puedes replicar esta lógica para cada etapa que quieras monitorear. Por ejemplo:

* Agendamiento: si no responde en 2 días → Clientes Perdidos
* Pendiente enviar cotización: si no responde en 5 días → Clientes Perdidos

> 💡 **Define el tiempo según el ritmo de tu negocio.** No es lo mismo un negocio de venta rápida donde 2 días es demasiado, que uno de servicios complejos donde el cliente puede tardar una semana en responder.

#### Bonus: Enviar encuesta antes de cerrar

Si quieres aprovechar el momento del cierre para obtener feedback, puedes agregar un paso de espera y encuesta antes de mover el ticket a Clientes Perdidos:

```
Trigger: Inactividad del contacto (2 días, etapa: Inicial)
    └── Espera: 4 horas
    └── Enviar encuesta de feedback (NPS o CSAT)
    └── Espera: 1 día
    └── Cambiar etapa → "Clientes Perdidos"
```

***

### Parte 4: Ordenar las etapas humanas (el tip más importante)

Si tienes muchos tickets acumulados en una sola etapa de "Asistencia Humana", el problema de fondo no es la limpieza — es que el proceso está subdefinido.

**¿Qué pasa cuando tienes una sola etapa humana?**

* Todos los tipos de clientes (interesados, con cotización enviada, en negociación, con problemas) caen en el mismo lugar.
* Los agentes no saben en qué orden atender.
* Es imposible saber cuántos clientes están en cada fase del proceso.

**La solución: abre el proceso en etapas.**

En lugar de una sola etapa "Asistencia Humana", crea etapas específicas que representen los pasos reales de tu proceso. Por ejemplo, para un negocio de cotizaciones:

```
Cita agendada
    ↓
Pendiente enviar cotización
    ↓
Cotización enviada
    ↓
Segunda cotización
    ↓
Visita en terreno
    ↓
Cliente contratado
```

**¿Cómo agregar una nueva etapa?**

1. Ve a tu embudo.
2. Activa el **modo edición** (ícono de lápiz arriba a la derecha).
3. Arrastra las etapas existentes para reorganizarlas.
4. Haz clic en **+ Nueva etapa** para agregar las que necesites.
5. Guarda los cambios.

> 💡 Con etapas bien definidas, cada agente sabe exactamente qué debe hacer cuando recibe un ticket en esa etapa. Y puedes crear automatizaciones específicas por etapa para que los tickets no se queden varados.

***

### Resumen: El sistema completo

```
1. LIMPIEZA INICIAL
   └── Filtrar tickets viejos por fecha y etapa
   └── Acciones colectivas → mover a Clientes Perdidos o archivar

2. ETAPA "CLIENTES PERDIDOS"
   └── Workflow: al entrar → cerrar ticket + marcar perdido + retorno a Inicial

3. AUTOMATIZACIÓN CONTINUA
   └── Workflow por inactividad → 2 días sin respuesta → Clientes Perdidos
   └── Configurar para cada etapa relevante

4. PROCESO BIEN DEFINIDO
   └── Etapas humanas específicas en lugar de una sola
   └── Cada etapa tiene un significado claro para el equipo
```

> ⚠️ **Recuerda siempre:** Ningún contacto se elimina. Los tickets se cierran, pero las conversaciones siempre están disponibles en la sección **Chat**, donde puedes buscarlas por nombre, número o contenido del mensaje.
