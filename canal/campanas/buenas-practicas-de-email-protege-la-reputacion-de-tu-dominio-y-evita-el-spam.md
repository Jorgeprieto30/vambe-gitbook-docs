---
description: >-
  Qué mide tu reputación de envío, cómo mantener tu bounce rate y tu tasa de
  spam bajo control, y cómo mantener tu lista de contactos sana.
---

# Buenas prácticas de email: protege la reputación de tu dominio y evita el spam

Enviar un correo no garantiza que llegue a la bandeja de entrada. Los proveedores de correo (Gmail, Outlook, Yahoo y el resto) evalúan constantemente el comportamiento de cada dominio que les envía correo, y usan esa evaluación para decidir si tus próximos envíos entran directo a la bandeja principal, caen en promociones, terminan en spam o simplemente no se entregan. Esta guía reúne las prácticas que más pesan en esa evaluación, para que tus campañas de email sigan llegando a quienes quieres que lleguen.

{% hint style="info" %}
Si todavía no configuraste tu canal de correo, parte por Cómo conectar el canal de Email; si ya envías campañas, revisa también Desuscripción en campañas de email, que cubre cómo Vambe gestiona las bajas de tus contactos.
{% endhint %}

***

## Qué mide tu reputación de envío

Cada dominio que envía correo construye, con el tiempo, una reputación ante los proveedores de bandeja de entrada. Dos métricas concentran la mayor parte de esa evaluación:

* **Bounce rate (tasa de rebote):** el porcentaje de tus envíos que nunca llegan a destino, ya sea porque la dirección no existe, el dominio no existe, o el servidor del destinatario rechaza el correo. El estándar de la industria es mantenerlo **bajo 4%**.
* **Spam rate (tasa de quejas):** el porcentaje de destinatarios que marcan tu correo como spam. Aquí el margen es mucho más estrecho: se considera saludable mantenerlo **bajo 0,08%**, es decir, menos de 1 queja cada 1.250 correos enviados.

Cruzar cualquiera de los dos umbrales de forma sostenida suele traer el mismo resultado: los proveedores de correo empiezan a filtrar tus envíos hacia spam, y si el proveedor de tu infraestructura de envío detecta el problema, puede pausar tus envíos hasta que la métrica baje. Recuperar una reputación dañada toma semanas; evitar que se dañe es mucho más simple.

{% hint style="warning" %}
Si tu bounce rate supera el 4%, lo más efectivo no es seguir enviando con la esperanza de que baje solo. Pausa los envíos a la porción de tu lista que está generando los rebotes, limpia esas direcciones y retoma cuando la tasa vuelva a un rango sano.
{% endhint %}

***

## Cómo mantener tu bounce rate bajo control

No todos los rebotes son iguales, y la diferencia importa para saber qué hacer con cada uno:

* **Rebote duro (permanente):** la dirección no existe, el dominio no existe, o el servidor rechaza el correo de forma definitiva. Esa dirección nunca va a recibir tus correos: sácala de tu lista de inmediato.
* **Rebote blando (transitorio):** la casilla está llena, el correo pesa demasiado, o hay un problema temporal del servidor del destinatario. Puede resolverse solo; si un mismo contacto acumula varios rebotes blandos seguidos, trátalo igual que un rebote duro.
* **Rebote indeterminado:** el servidor del destinatario rechazó el correo, pero no entregó información suficiente para saber por qué. Si se repite con el mismo contacto, lo más seguro es removerlo.

Para mantener la tasa baja de forma sostenida:

* Solo envía a contactos que dieron su consentimiento para recibir tus correos. Una lista comprada o recolectada sin permiso siempre va a tener una tasa de rebote más alta.
* Retira de tu lista las direcciones que ya sabes que no existen o llevan mucho tiempo sin responder.
* Nunca uses direcciones inventadas o de prueba al probar una plantilla o una campaña; usa tu propio correo o el de un compañero.
* Si haces seguimiento de aperturas y clics, revisa periódicamente qué contactos nunca interactúan y sácalos de tus próximos envíos masivos.

***

## Cómo evitar que te marquen como spam

Un reporte de spam pesa más que un rebote: le dice al proveedor de correo que un ser humano decidió activamente que no quería recibirte. Tres prácticas concentran casi todo el efecto:

* **Dale a cada contacto una forma clara y visible de darse de baja.** Si no la encuentra, la alternativa que le queda es reportarte como spam. Vambe incluye este mecanismo de punta a punta en las campañas de email — revisa Desuscripción en campañas de email para configurarlo en tus plantillas.
* **Envía contenido relevante y oportuno.** Un contacto que recibe correos que no le interesan, con una frecuencia que no pidió, tiene muchas más probabilidades de reportarte.
* **Envía solo a quien dio su consentimiento.** Igual que con el bounce rate, una lista no consentida genera más quejas, no solo más rebotes.

***

## Higiene de tu lista de contactos

Una lista sana no se mantiene sola; requiere revisión activa en dos frentes: evitar que entren contactos de mala calidad, y sacar a tiempo los que dejaron de estar interesados.

### Al momento de sumar contactos

* Si capturas correos desde un formulario público, agrega un CAPTCHA (Google reCAPTCHA, hCaptcha o similar) para evitar que bots infecten tu lista con direcciones falsas.
* Considera el doble opt-in: pedirle al contacto que confirme su suscripción haciendo clic en un enlace de confirmación, antes de sumarlo a tus envíos. Esto certifica que la persona realmente quiere recibirte y que la dirección es válida.
* Para listas grandes o compradas, un servicio de verificación de correos (Kickbox, ZeroBounce y similares) puede confirmar qué direcciones son entregables antes de que las agregues a una campaña.

### De forma continua

* Limita tus envíos no transaccionales a contactos que abrieron o hicieron clic en algún correo tuyo en los últimos 6 meses. Es el estándar que usan Gmail y Outlook como referencia de una lista activa.
* A los contactos que llevan más de 6 meses sin interactuar, dales una última oportunidad con una campaña de reactivación antes de sacarlos. Si tampoco responden a esa, es momento de retirarlos de tus envíos masivos — seguir insistiendo solo erosiona tu reputación sin ganar nada a cambio.

***

## La base técnica: la autenticación de tu dominio

Todo lo anterior asume que tu dominio ya está correctamente autenticado ante los proveedores de correo — sin eso, ni la lista más sana te salva de terminar en spam. Si conectaste el canal de Email en Vambe con tu propio dominio, esta parte ya está resuelta: al conectar el canal agregaste los registros DNS que autentican tus envíos, tal como se explica en Cómo conectar el canal de Email. Si en cambio usas un dominio provisto por Vambe, la autenticación corre por cuenta nuestra y no necesitas configurar nada.

***

## En resumen

Proteger tu reputación de envío es, en el fondo, una disciplina de mantenimiento: mantén tu bounce rate bajo 4% sacando a tiempo las direcciones que no existen, mantén tu tasa de quejas bajo 0,08% dándole a cada contacto una salida clara y enviando solo a quien te dio permiso, y revisa tu lista con regularidad para quedarte con los contactos que de verdad quieren saber de ti. Ese mantenimiento constante es lo que mantiene tus correos —y los de tus próximas campañas— llegando a la bandeja de entrada.
