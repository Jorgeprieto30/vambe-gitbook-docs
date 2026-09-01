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

<figure><img src="https://1176996256-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FjZ46rFloLOG1hJ2JQGi0%2Fuploads%2FOssLdcHg2tawaII781X8%2Fimage.png?alt=media&#x26;token=5b57d39f-a935-4b52-895d-7d166b385a3a" alt=""><figcaption></figcaption></figure>

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

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Cambio de Etapa</td><td></td></tr><tr><td>Quitar contacto del embudo</td><td></td></tr></tbody></table>

**Comunicación y Envío de Información:**

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Enviar Plantilla</td><td></td></tr><tr><td>Enviar Audio</td><td></td></tr><tr><td>Enviar Documento o Imagen</td><td></td></tr><tr><td>Crear Nota</td><td></td></tr></tbody></table>

**Herramientas y Cálculos:**

* Búsqueda Base Vectorial (Buscar en documentos específicos)
* Drive File Transformer

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Búsqueda Base Vectorial</td><td></td></tr></tbody></table>

**Integraciones y Conectividad:**

* Llamada Webhook
* Ejecutar Flow
* Google Sheets (Agregar Fila / Buscar Fila)
* Google Calendar
* Google Maps
* Outlook
* Reservo
* [Link de pago (Fintoc o Mercado Pago)](como-cobrar-dentro-del-chat-con-un-link-de-pago.md)
* Vambe

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>Llamada Webhook</td><td></td></tr></tbody></table>

**Ecommerce**:

* Obtener Estado de Orden
* Cambiar Dirección de Envío
