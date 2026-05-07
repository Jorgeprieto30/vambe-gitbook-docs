# ¿Cómo probar tu asistente de inteligencia artificial en Vambe?

Antes de probar, su asistente debe estar completamente creado y configurado.

En Vambe existen tres formas de probar cómo responde su IA, dependiendo de si quiere evaluar una sola inteligencia artificial, todo el embudo o hacer simulaciones avanzadas. A continuación, le explicamos cada una.

***

{% stepper %}
{% step %}
#### Probar una inteligencia artificial individual

Esta opción sirve cuando quiere evaluar solo un asistente en particular, aislado del resto del embudo.

**¿Cómo hacerlo?**

[Debe ingresar al asistente](https://academy.vambe.ai/c%C3%B3mo-ingresar-al-asistente-de-inteligencia-artificial)

**Probar el asistente**

Una vez dentro del asistente, verá arriba a la derecha un botón llamado **Probar**.

![](<../.gitbook/assets/image png Dec 03 2025 03 59 21 0818 PM.png>)

Al hacer clic:

* Podrá enviar mensajes de prueba directamente a ese asistente.
* Simulará conversaciones como si ese asistente estuviera atendiendo un cliente real, pero solo dentro de esa etapa.

**Consideraciones importantes**

* Esta prueba sirve únicamente para asistentes aislados.
* Si su embudo usa varias inteligencias artificiales, esta prueba NO muestra cómo fluyen los clientes entre etapas.
* Es ideal para revisar errores puntuales, lógica interna o bloques específicos, así como para validar que los `guard rails` del asistente funcionan según lo esperado.
{% endstep %}

{% step %}
#### Probar todo el embudo completo (Playground)

Esta es la prueba más representativa del mundo real. Simula a un cliente entrando por primera vez a su embudo y avanzando etapa por etapa.

**Cómo acceder**

{% stepper %}
{% step %}
En el menú izquierdo, entre a **Asistentes**.
{% endstep %}

{% step %}
Seleccione la opción **Playground**.
{% endstep %}

{% step %}
Escriba un mensaje para comenzar la prueba.
{% endstep %}
{% endstepper %}

![](<../.gitbook/assets/image png Dec 03 2025 04 02 15 8775 PM.png>)

**¿Qué puede probar aquí?**

* El flujo completo del cliente.
* Cómo interactúan todas las inteligencias artificiales entre sí.
* Si las funciones (cambio de etapa, agendamientos, búsquedas, etiquetas, etc.) están operando correctamente.
* Qué ocurre cuando el cliente cumple ciertas condiciones dentro del proceso.
* La efectividad de los `guard rails` configurados para prevenir respuestas no deseadas o **alucinaciones**.

Es la prueba ideal cuando:

* Está revisando un embudo nuevo.
* Hizo cambios recientes en pasos a seguir o casos posibles.
* Necesita validar la experiencia completa del usuario, incluyendo el comportamiento de los `guard rails`.
{% endstep %}

{% step %}
#### Probar con IA (simulación automatizada)

Esta opción permite generar pruebas automáticas, donde múltiples perfiles simulados interactúan con su embudo al mismo tiempo. Es una forma avanzada de testeo que ayuda a identificar errores que podrían pasarse por alto en pruebas manuales.

**Cómo acceder**

{% stepper %}
{% step %}
En el menú izquierdo, entre a **Asistentes**.
{% endstep %}

{% step %}
Haga clic en **Probar con IA**.
{% endstep %}
{% endstepper %}

![](<../.gitbook/assets/image png Dec 04 2025 02 22 50 5392 PM.png>)

**Cómo ejecutar un test**

{% stepper %}
{% step %}
Haga clic en **Crear nuevo test**.

![](<../.gitbook/assets/image png Dec 04 2025 02 23 28 6603 PM.png>)
{% endstep %}

{% step %}
Seleccione el embudo que quiere probar.

![](<../.gitbook/assets/image png Dec 04 2025 02 23 58 1378 PM.png>)
{% endstep %}

{% step %}
Elija los **perfiles simulados**.

* Vambe genera algunos perfiles automáticamente.
* Puede editar perfiles o crear otros completamente nuevos.

![](<../.gitbook/assets/image png Dec 04 2025 02 25 56 1586 PM.png>)
{% endstep %}

{% step %}
Haga clic en **Siguiente** para iniciar las simulaciones.
{% endstep %}
{% endstepper %}

**¿Qué hace este sistema?**

* Simula varias personas hablándole a su embudo.
* Prueba diferentes rutas, casos posibles y variaciones.
* Recorre todo el flujo buscando inconsistencias y posibles **alucinaciones** que los `guard rails` deberían evitar.

![](<../.gitbook/assets/image png Dec 04 2025 02 28 46 4196 PM.png>)

**Resultados**

Una vez finalizado el test, recibirá:

* Respuestas generadas por los asistentes ante cada situación.
* Alertas de comportamiento inesperado.
* Sugerencias de mejoras en pasos a seguir, casos posibles, información faltante, o ajustes en los `guard rails` para prevenir **alucinaciones**.

![](<../.gitbook/assets/image png Dec 04 2025 02 32 36 8652 PM.png>)
{% endstep %}

{% step %}
#### IA VS IA Masivo: Comparación y optimización a escala

Esta funcionalidad es la herramienta más avanzada para asegurar la máxima calidad y precisión de sus asistentes de IA. Permite comparar y optimizar diferentes modelos y configuraciones de forma masiva, superando las limitaciones de las pruebas manuales unitarias. Con IA VS IA Masivo, puede enfrentar sus inteligencias artificiales entre sí para identificar la versión con mejor rendimiento.

Con la implementación de nuevos **`guard rails`** para los asistentes de IA, esta herramienta cobra aún mayor relevancia para la evaluación de las **métricas de alucinaciones**. Aunque la adición de más `guard rails` pueda, paradójicamente, hacer que las métricas de alucinaciones "parezcan" empeorar inicialmente al cubrir un espectro más amplio de incidentes, en realidad se está logrando una mejor detección y prevención de respuestas no deseadas.

**¿Cómo funciona?**

1. **Configure sus versiones de IA**: Defina las distintas configuraciones o modelos de asistente que desea poner a prueba, incluyendo variaciones en sus **`guard rails`**.
2. **Ejecute la comparativa**: Vambe enfrentará a sus asistentes en miles de interacciones simultáneas.
3. **Analice los resultados**: Acceda a nuevas interfaces en el Dashboard de Vambe, diseñadas para visualizar claramente qué versión de la IA está "ganando" y por qué, basándose en métricas de éxito predefinidas. Podrá identificar patrones, fortalezas y debilidades de cada configuración, y **evaluar cómo los `guard rails` influyen en la reducción de las alucinaciones y la cobertura de incidentes**.

**Beneficios clave para sus asistentes**

* **Mayor Calidad y Precisión**: Al comparar cientos de interacciones, se asegura que el cliente reciba la respuesta más exacta y refinada, **minimizando alucinaciones gracias a `guard rails` robustos y una definición de incidentes más completa**.
* **Implementaciones más rápidas**: Reduzca drásticamente los tiempos de validación para nuevas funcionalidades de IA, pasando de días a minutos y entregando valor al cliente mucho más rápido, **con la confianza de que los `guard rails` están protegiendo el comportamiento de la IA**.
* **Consistencia Garantizada**: Detecte posibles fallos antes de que lleguen a producción, garantizando un servicio más estable y confiable, y **entendiendo el impacto real de los `guard rails` en la prevención de alucinaciones**.

**¿Cuándo usar IA VS IA Masivo?**

* Al desarrollar nuevas funcionalidades o estrategias para sus asistentes, **especialmente cuando se implementan o ajustan `guard rails`**.
* Para validar cambios en los prompts o la lógica interna de la IA, **y su efecto en las métricas de alucinaciones**.
* En la búsqueda constante de la máxima eficiencia y rendimiento de sus modelos de IA, **aprovechando la visibilidad que ofrecen los `guard rails` sobre el comportamiento de la IA**.
{% endstep %}

{% step %}
#### Probar con código QR

Esta opción le permite llevar la experiencia de prueba directamente a su dispositivo móvil, simulando la interacción real de un cliente a través de WhatsApp.

**¿Cómo hacerlo?**

1. Vaya a la sección de Embudo en el menú lateral izquierdo.
2. Haga clic en el icono de código QR que aparece en la parte superior derecha de la pantalla.
3.  Se abrirá una ventana emergente con un código QR único para ese embudo.\
    <br>

    <figure><img src="../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>
4. Escanee el código con la cámara de su teléfono o compártalo mediante el enlace generado.
5. **Importante**: Al escanearlo, se abrirá un chat de WhatsApp con un mensaje predeterminado. Debe enviar ese mensaje exacto para iniciar la simulación del embudo.

**Consideraciones importantes**

* Este método sirve única y exclusivamente si el embudo no tiene todavía un canal oficial (como un número de API de WhatsApp) conectado.
* Permite que hasta 20 contactos diferentes prueben el flujo simultáneamente para validar la experiencia de usuario.
* Es la forma más fiel de ver cómo se visualizan los mensajes, botones y tiempos de respuesta en la interfaz real de WhatsApp, **y para observar el comportamiento del asistente bajo los `guard rails` configurados en un entorno de comunicación real**.
{% endstep %}
{% endstepper %}

***

### Resumen general

| **Método**                  | **Para qué sirve**                      | **Cuándo usarlo**                                                                                                                 |
| --------------------------- | --------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Probar asistente individual | Testear solo un asistente               | Revisar lógica interna o bloques específicos, validar **`guard rails`**                                                           |
| Playground (flujo completo) | Simular el recorrido de un cliente real | Validar que el embudo completo funciona y que los **`guard rails`** operan correctamente                                          |
| Probar con IA               | Pruebas masivas con perfiles simulados  | Buscar errores complejos, validar robustez y la efectividad de los **`guard rails`**                                              |
| IA VS IA Masivo             | Comparar y optimizar modelos de IA      | Escalar la calidad, velocidad y consistencia de sus IA, **evaluando el impacto de `guard rails` y las métricas de alucinaciones** |
| Código QR                   | Prueba real en WhatsApp móvil           | Validar la experiencia final antes de conectar un canal, observando el comportamiento con **`guard rails`**                       |
