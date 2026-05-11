# Conectar tu calendario de Outlook a Vambe

Vambe puede integrarse con tu calendario de Microsoft Outlook para que el asistente de IA pueda consultar la disponibilidad de los vendedores y agendar reuniones automáticamente con los clientes.

Esta integración requiere dos pasos: primero, un **administrador de la organización** debe autorizar el acceso a nivel de empresa (una sola vez); luego, **cada vendedor** agrega su propia cuenta.

***

### Requisitos previos

* Tener una cuenta activa en Vambe.
* Contar con acceso de **administrador de Microsoft 365** de tu organización (o la posibilidad de reenviar el enlace de autorización a quien lo tenga).

***

### Paso 1: Autorizar la conexión como organización

Este paso lo realiza **una sola vez** el administrador de Microsoft 365 de la empresa.

1. En Vambe, ve al menú lateral izquierdo y haz clic en **Ajustes**.
2.  Ingresa a **Integraciones** y busca la tarjeta **Outlook Calendar** dentro de la sección **Citas**.\
    <br>

    <figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>


3. Al abrir la integración, verás la sección **Cuenta de Organización** con el texto: _"Conéctate usando la cuenta Microsoft 365 de tu empresa. Esto utiliza el tenant de tu organización para la autenticación."_
4.  Haz clic en **Conectar Cuenta de Organización**.\
    <br>

    <figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>


5. Se abrirá una ventana de Microsoft. Inicia sesión con la **cuenta de administrador** de tu organización y acepta los permisos solicitados.

{% hint style="danger" %}
**¿El administrador no usa Vambe?** No es necesario que tenga cuenta en Vambe. Haz clic en **Copiar enlace de autorización para administrador** y envíaselo. Él solo debe abrir el enlace, iniciar sesión con su cuenta de Microsoft y aceptar los permisos.
{% endhint %}

Una vez completado este paso, la organización quedará autorizada y podrás agregar las cuentas individuales.

***

### Paso 2: Agregar cuentas individuales (por cada vendedor)

Con la organización ya autorizada, cada vendedor debe agregar su propia cuenta. Este proceso lo realiza cada persona con su propio correo corporativo.

1. En Vambe, ve a **Ajustes → Integraciones → Outlook Calendar**.
2.  Haz clic en **+ Agregar Cuenta**.\
    <br>

    <figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>
3. Se abrirá una ventana de Microsoft. Inicia sesión con **tu cuenta corporativa** y autoriza el acceso.
4. Al completar el proceso, tu calendario quedará vinculado y aparecerá listado en la integración.

{% hint style="info" %}
**Nota:** Conectar tu calendario no significa que inmediatamente comenzarán a llegarte reuniones. El asistente solo usará tu disponibilidad cuando el flujo de ventas esté activo y configurado para hacerlo.
{% endhint %}

***

### ¿Cómo funciona después de conectar?

* El asistente de IA consulta en tiempo real tu calendario de Outlook para conocer tu disponibilidad.
* Solo propone horarios en los que estás libre, respetando los **horarios de trabajo** que tengas configurados en tu calendario de Microsoft.
* Si quieres restringir los horarios disponibles (por ejemplo, solo de lunes a miércoles después de las 15:00), puedes indicárselo al asistente a través de sus instrucciones.
* Si hay varios vendedores conectados, el asistente puede revisar cada calendario de forma independiente y asignar la reunión según criterios configurables (por disponibilidad, por turno rotativo, por especialidad, etc.).

***

### Preguntas frecuentes

**¿Puedo conectar un calendario compartido en lugar del mío?** Sí. Si los vendedores comparten su calendario contigo en Microsoft, puedes conectar tu propia cuenta y ver la disponibilidad de todos desde un solo token. Sin embargo, para equipos grandes esto puede volverse complejo; lo recomendado es que cada vendedor conecte su propio calendario.

**¿El asistente puede agendar fuera de mi horario laboral?** No. El asistente respeta los horarios de trabajo que tienes definidos en tu calendario de Outlook. Solo propondrá horarios dentro de esos rangos.

**¿Qué pasa si el administrador cambia o se va de la empresa?** La habilitación de administrador queda registrada a nivel de organización en Microsoft. No es necesario repetirla si cambia el administrador, salvo que se revoquen los permisos manualmente desde el portal de Microsoft.

**¿Puedo ver qué vendedores ya conectaron su calendario?** Sí. Desde la vista interna de Vambe es posible ver los tokens generados y a qué usuario corresponde cada uno.
