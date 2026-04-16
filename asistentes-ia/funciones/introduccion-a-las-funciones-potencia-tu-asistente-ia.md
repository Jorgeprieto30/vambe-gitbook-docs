---
description: >-
  Descubre el poder de las funciones. Aprende qué son, dónde se configuran
  (Pasos a Seguir y Casos Posibles) y conoce el listado completo de herramientas
  para potenciar a tu asistente IA.
---

# Introducción a las Funciones: Potencia tu Asistente IA

Las Funciones son herramientas avanzadas que permiten a tu Asistente de Inteligencia Artificial realizar acciones concretas más allá de simplemente conversar. Gracias a ellas, tu asistente puede interactuar con el CRM, enviar archivos, conectarse con plataformas externas o realizar cálculos, transformándose en un agente operativo completo.

#### ¿Dónde se pueden usar las funciones?

Dentro de la configuración de tu Asistente, existen múltiples bloques (como personificación, base de conocimiento, etc.), pero las funciones únicamente se pueden utilizar en dos bloques específicos:

1. **Pasos a Seguir**: Puedes instruir a la IA para que ejecute una acción como parte de su flujo de conversación lineal (ej: _Pasos 1, 2, 3... Ejecutar función_).
2. **Casos Posibles:** Puedes configurar que una función se active si ocurre una situación específica durante la charla (ej: _Si el cliente pide devolución -> Ejecutar función_).

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

**¿Cómo funcionan?**

Para que una función se ejecute correctamente, la IA necesita una Causa (un gatillante). El proceso consta de dos partes fundamentales:

1. **La Instrucción en el Texto**: Debes escribir explícitamente en el paso o caso posible cuándo debe actuar.
   * _Ejemplo:_ "**Cuando el cliente me responda las preguntas, debes ejecutar la función \[Nombre de la función]".**
2. **La Descripción Interna:** Al crear la función, debes configurar una descripción que le diga a la IA cuándo es el momento óptimo para activarse. Esta descripción debe coincidir con la instrucción que diste en el texto.

#### Listado de Funciones Disponibles

Actualmente, Vambe cuenta con una amplia variedad de funciones para cubrir distintas necesidades operativas. A continuación, el listado completo que iremos explorando en detalle:

**Gestión del Embudo y Contactos:**

* Cambio de Etapa
* Quitar contacto del embudo

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Cambio de Etapa</td><td><a href="como-cambiar-un-ticket-de-una-etapa-a-otra-de-forma-automatica.md">como-cambiar-un-ticket-de-una-etapa-a-otra-de-forma-automatica.md</a></td></tr><tr><td>Quitar contacto del embudo</td><td><a href="como-hacer-que-la-ia-elimine-un-contacto-del-embudo-si-no-califica-durante-el-chat-o-es-spam.md">como-hacer-que-la-ia-elimine-un-contacto-del-embudo-si-no-califica-durante-el-chat-o-es-spam.md</a></td></tr></tbody></table>

**Comunicación y Envío de Información:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Enviar Plantilla</td><td><a href="como-hacer-que-la-ia-envie-una-plantilla-de-whatsapp-automaticamente.md">como-hacer-que-la-ia-envie-una-plantilla-de-whatsapp-automaticamente.md</a></td></tr><tr><td>Enviar Audio</td><td><a href="dale-voz-a-tu-ia-configuracion-de-la-funcion-enviar-audio.md">dale-voz-a-tu-ia-configuracion-de-la-funcion-enviar-audio.md</a></td></tr><tr><td>Enviar Documento o Imagen</td><td><a href="como-hacer-que-la-ia-envie-un-pdf-imagen-o-archivo-automaticamente.md">como-hacer-que-la-ia-envie-un-pdf-imagen-o-archivo-automaticamente.md</a></td></tr><tr><td>Crear Nota</td><td><a href="como-hacer-que-la-ia-deje-notas-internas-en-el-chat.md">como-hacer-que-la-ia-deje-notas-internas-en-el-chat.md</a></td></tr></tbody></table>

**Herramientas y Cálculos:**

* Búsqueda Base Vectorial (Buscar en documentos específicos)
* Drive File Transformer

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Búsqueda Base Vectorial</td><td><a href="como-indicar-al-asistente-donde-buscar-informacion-dentro-de-la-base-de-conocimiento.md">como-indicar-al-asistente-donde-buscar-informacion-dentro-de-la-base-de-conocimiento.md</a></td></tr></tbody></table>

**Integraciones y Conectividad:**

* Llamada Webhook
* Ejecutar Flow
* Google Sheets (Agregar Fila / Buscar Fila)
* Google Calendar
* Google Maps
* Outlook
* Reservo
* Link Fintoc
* Vambe

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Llamada Webhook</td><td><a href="como-conectar-tu-asistente-con-sistemas-externos-apis-usando-webhooks.md">como-conectar-tu-asistente-con-sistemas-externos-apis-usando-webhooks.md</a></td></tr></tbody></table>

**Ecommerce**:

* Obtener Estado de Orden
