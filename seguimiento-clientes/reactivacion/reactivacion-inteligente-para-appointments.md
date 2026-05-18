# Reactivación Inteligente para Appointments

### ¿Para qué sirve?

La Reactivación Inteligente para Appointments detecta en qué paso del proceso de agendamiento se detuvo un contacto y le envía automáticamente un mensaje para retomarlo.

Además, incluye una funcionalidad exclusiva para esta vertical: **antes de reactivar a un contacto con un horario, Vambe verifica en tiempo real si ese horario sigue disponible**. Si ya fue tomado, le ofrece directamente una nueva opción.

> 💡 **¿Dónde la encuentro?** Ve a **Workflows → Automatizaciones → Reactivación**.

> ⚠️ **Beta:** Esta funcionalidad está en período beta. Contacta al equipo de Vambe para activarla en tus clientes de Appointments.

***

### ¿Qué puedes lograr?

* Recuperar contactos que se enfriaron en el proceso de agendamiento
* Evitar ofrecer horarios que ya no están disponibles
* Automatizar el seguimiento en cada etapa del agendamiento sin intervención manual

***

### ¿Cómo funciona?

Para embudos de Appointments, Vambe identifica los siguientes **eventos de conversión**:

1. **Datos del contacto** — el lead entrega su información inicial
2. **Elección de servicio** — indica qué servicio quiere agendar
3. **Opciones de disponibilidad ofrecidas** — Vambe muestra horarios del calendario
4. **Confirmación del horario** — el contacto confirma y se crea el appointment

Cada vez que un contacto se detenga entre un evento y el siguiente, Vambe activa un mensaje de reactivación con IA para empujarlo al paso siguiente.

#### Verificación de disponibilidad en tiempo real

Cuando se va a reactivar a un contacto al que ya se le ofrecieron horarios, Vambe consulta el calendario antes de enviar el mensaje:

* **Si el horario sigue disponible** → reactiva al contacto ofreciendo ese mismo horario
* **Si el horario ya fue tomado** → reactiva con una nueva propuesta de disponibilidad

Esto evita la fricción de confirmar un horario que ya no existe.

***

### Cómo activarla

1.  Ve a **Workflows → Automatizaciones → Reactivación**\
    <br>

    <figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

    <figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>
2. Selecciona el embudo de appointments
3. Activa solo las **etapas del proceso de agendamiento** — se recomienda excluir contactos fríos y contactos que ya están agendados
4. Haz clic en **"Crear workflow de reactivación"**

Vambe analizará el embudo y generará el workflow con los mensajes para cada punto de conversión del agendamiento.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

***

### Personalización

El workflow generado es completamente editable. Desde ahí puedes:

* **Modificar los mensajes** de cada etapa: tono, urgencia, tipo de recordatorio
* **Ajustar los tiempos** de espera antes de reactivar
* **Ver las corridas** del workflow para revisar cómo fluyeron los contactos
