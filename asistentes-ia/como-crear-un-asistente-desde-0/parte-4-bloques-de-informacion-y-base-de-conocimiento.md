---
description: >-
  Entregue los datos técnicos a su IA. Aprenda a estructurar los Bloques de
  Información y a conectar la Base de Conocimiento para que su asistente
  responda con precisión sobre nuestra información
---

# Parte 4: Bloques de Información y Base de Conocimiento

## Parte 4: Bloques de Información y Base de Conocimiento

Existe una máxima fundamental al configurar su Inteligencia Artificial: **El asistente será tan inteligente como la información que usted le entregue.** Para evitar que la IA asuma, adivine o "alucine" datos, toda la información de su negocio debe estar documentada explícitamente dentro de Vambe. Para esto, Vambe divide el conocimiento en dos grandes áreas: los **Bloques de Información** (para datos directos y rápidos) y la **Base de Conocimiento** (para archivos extensos y bases de datos).

***

**1. Los Bloques de Información (Conocimiento Inmediato)**

Estos bloques representan la memoria a corto plazo de su asistente. Es información que la IA siempre tendrá en consideración de forma inmediata al conversar con el cliente.

**A. Información de la tienda**

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2F4qTdKP1Q8oyoug3PIAe9%2Fimage.png?alt=media&#x26;token=3040d36d-f71f-4be0-bf07-709f1bcaad5b" alt=""><figcaption></figcaption></figure>

Es un espacio de texto libre diseñado específicamente para que la IA comprenda la logística básica de su negocio. Aquí debe redactar las direcciones físicas, horarios de atención, días feriados y datos de contacto directo.

**B. Información clave**

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FEVfGLsVuu5ZuNiCoXEOD%2Fimage.png?alt=media&#x26;token=72af6267-4fca-48c9-ba35-be972002718a" alt=""><figcaption></figcaption></figure>

Este es el bloque más versátil. Consiste en un formato de texto libre donde puede ingresar absolutamente toda la información miscelánea que el asistente necesita saber.

**💡 Tip de estructuración**: No está limitado a un solo bloque de información clave. Puede (y debe) crear múltiples bloques divididos por temáticas para mantener el orden. Por ejemplo, puede crear:

* Un bloque llamado "Precios".
* Un bloque llamado "Garantías y Devoluciones".
* Un bloque llamado "Métodos de Pago".
* Un bloque llamado "Listado de Profesionales".

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FILhThlNXjNhJV4xfwPkn%2Fimage.png?alt=media&#x26;token=71bfe4ba-65ff-4926-952b-7f08130f12e2" alt=""><figcaption></figcaption></figure>

**C. Bloques de Integraciones (Reserva y Productos)**

Si usted utiliza plataformas externas conectadas a Vambe, utilizará estos bloques especializados:

* Aplicaciones de reserva: Se utiliza si tiene integraciones de agendamiento (como Reservo, Agenda pro, Dentalink o Medilink). 👉 [\[Ver guía de integraciones de agendamiento aquí\]](https://academy.vambe.ai/asistentes-de-agendamiento)
* Información de productos (ProductBlock): Este bloque se utiliza si tiene su e-commerce conectado (como Shopify o WooCommerce) o si carga productos manualmente en Vambe. Si sus productos se cargan de forma manual, Vambe permite gestionar **múltiples catálogos de productos independientes**. Al configurar este bloque, podrá **seleccionar el catálogo específico** que desea asignar a este asistente, asegurando que acceda únicamente a la información de los productos relevantes (ej. un catálogo de _Verano 2026_ o _Marca A_).
  * Aprenda a gestionar múltiples catálogos de productos en la guía general de e-commerce.
  * [\[Vea la guía general de e-commerce aquí\]](https://academy.vambe.ai/asistente-ecommerce)

***

**2. La Base de Conocimiento (Conocimiento Extendido)**

_¿Qué ocurre si la información que necesita subir es demasiado extensa y el sistema le indica que ha alcanzado el límite de caracteres en los Bloques de Información?_ En ese caso, debe recurrir a la **Base de Conocimiento.**

Esta sección le permite conectar archivos pesados, documentos PDF, hojas de cálculo o carpetas enteras de Google Drive y Notion.

**Paso 1: Cargar la información al sistema**

Antes de asignarla a su asistente, los documentos deben estar previamente cargados o conectados en el módulo general del sistema. 👉 \[Visite este artículo para aprender a conectar documentos en la Base de Conocimiento General]

**Paso 2: Asociar las carpetas a su Asistente**

Una vez que sus archivos estén cargados en el sistema, debe indicarle a este asistente específico que tiene permiso para leerlos:

1.  En la configuración de su asistente, diríjase a la pestaña superior central llamada "Base de conocimiento".<br>

    <figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2Fi2HBAcRegiNigOx4tG3I%2Fimage.png?alt=media&#x26;token=ef0325e2-f6e2-4b71-a7da-dc8c14f7b50f" alt=""><figcaption></figcaption></figure>
2. En el panel izquierdo ("**Disponibles en base de conocimiento**"), verá todas las carpetas que conectó en el paso anterior.
3. **Marque la casilla de verificación** de las carpetas que este asistente debe recordar. Al hacerlo, pasarán al panel derecho, confirmando la asociación.

**🛑 Importante: Búsqueda Activa vs. Pasiva**

Al asociar las carpetas, la IA tiene una "noción general" de esos documentos. Sin embargo, si usted tiene bases de datos gigantes (ejemplo: un Excel con miles de repuestos de automóviles o el estado de miles de pedidos) y necesita que la IA vaya a buscar un dato _exacto y obligatorio_ a ese archivo externo, debe utilizar la **Función de Búsqueda Vectorial.**

Esta función se configura dentro de los bloques de **Pasos a seguir o Casos Posibles** que vimos en la Parte 3, **obligando a la IA a escanear el documento antes de responder**. 👉 \[Aprenda a configurar la Función de Búsqueda Vectorial aquí]

***

**Conclusión del proceso**

**¡Felicidades!** Si ha completado estas 4 partes, ha construido un Asistente de IA robusto.

* Le ha dado una Identidad para que sepa quién es.
* Le ha dictado Instrucciones para que sepa cómo vender o atender.
* Lo ha educado con Información para que responda con la verdad.

El último paso es dirigirse a la pestaña de "Prueba" [(Playground)](https://www.vambeai.com/playground) y simular conversaciones reales para afinar los detalles de su configuración antes de publicarlo frente a sus clientes.\
\
Una vez que haya probado y validado que su asistente funciona correctamente, este no comenzará a hablar con los clientes de forma automática. Para que la IA entre en acción, debe asociar este nuevo asistente a una etapa específica dentro de su embudo.

👉 [\[Aprenda cómo asignar un asistente a una etapa del embudo aquí\]](https://academy.vambe.ai/embudo/gestion-de-etapas-y-asistentes-ia/paso-3-asignar-un-asistente-de-ia-a-una-etapa)
