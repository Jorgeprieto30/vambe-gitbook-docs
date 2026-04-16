---
description: >-
  Automatiza tu logística inversa. Conecta Reversso para gestionar devoluciones
  completas vía chat con IA y derivar cambios de producto automáticamente.
---

# Integración Reversso: Devoluciones Automáticas

**Reversso** es la plataforma líder en gestión de logística inversa para e-commerce. Esta integración permite que tu Asistente IA gestione devoluciones y cambios de forma ordenada, mejorando la experiencia de postventa.

#### ⚠️ Importante: Configuración Previa

Antes de conectar Vambe, es crucial que **ya tengas configurado tu flujo de devolución dentro de Reversso**.

La Inteligencia Artificial no "inventa" las reglas; se conecta a tu portal para leer lo que tú hayas definido allí. Por lo tanto, asegúrate de tener listo en tu panel de Reversso:

* Las **preguntas** de motivo de devolución.
* Los **métodos de reembolso** permitidos.
* Los **couriers** y opciones de envío.

Si esto no está configurado en Reversso, la IA no podrá completar el proceso correctamente.

#### ¿Qué permite esta integración?

Es importante distinguir los dos flujos disponibles en esta versión:

1. **Devoluciones (Conversacional)**: El usuario gestiona **todo el proceso dentro del chat**. La IA identifica el pedido, pregunta qué productos devolver, solicita fotos, motivos y método de reembolso, creando el ticket automáticamente en Reversso.
2. **Cambios (Derivación)**: Si el cliente desea _cambiar_ un producto (por talla o color), la IA le entregará automáticamente el enlace directo a tu portal de cambios para que lo gestione manualmente.

***

#### 1. Obtener URL del Portal Reversso

Para conectar ambas plataformas, necesitamos la dirección exacta de tu portal de devoluciones.

1. Ingresa a tu cuenta de Reversso.
2. Copia la URL de tu portal (generalmente tiene el formato `tutienda.reversso.dev` o similar).

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

***

#### 2. Conectar en Vambe

1. En Vambe, ve a Ajustes en el menú lateral.
2. Selecciona la pestaña Integraciones.
3.  Baja hasta la sección Ecommerce y busca la tarjeta de Reversso.<br>

    <figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
4.  Haz clic en Conectar.\
    <br>

    <figure><img src="../.gitbook/assets/Captura de pantalla 2026-02-03 a la(s) 12.35.24 p.m..png" alt=""><figcaption></figcaption></figure>


5.  Pega la URL del portal que copiaste en el paso anterior y haz clic en Siguiente.<br>

    <figure><img src="../.gitbook/assets/image (4).png" alt="" width="375"><figcaption></figcaption></figure>

***

#### 3. Configurar el Asistente

Para que la IA sepa cómo procesar estos casos, debes agregar un bloque de conocimiento especial.

1. [Ve a tu Asistente](https://academy.vambe.ai/asistentes-ia/como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial) (se recomienda usar un asistente específico para Postventa).
2.  En la librería de bloques, busca y agrega "Devoluciones de Productos".<br>

    <figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>


3.  En la configuración del bloque, selecciona el Token de Reversso (la integración que acabas de crear) para vincularlo.\
    <br>

    <figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

***

#### 4. Estrategia de Embudo (Recomendada)

Para mantener el orden, te sugerimos la siguiente estructura en tu Embudo de Ventas:

1.  Crear una Etapa "Postventa": Dedicada exclusivamente a reclamos, cambios y devoluciones.<br>

    <figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
2. Asignar Asistente Especializado: Coloca en esta etapa al asistente que configuraste en el paso 3.
3. Configurar Derivación Automática:
   * En tu Asistente Inicial (el que recibe a todos los clientes), agrega un Caso Posible.
   * _Instrucción:_ "Si el cliente quiere devolver o cambiar un producto".
   * _Acción:_ Cambiar de etapa -> "Postventa".

De esta forma, el asistente principal no se distrae y deriva el caso al "experto" en devoluciones.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

***

#### 5. ¿Cómo es el flujo para el cliente?

Una vez activo, la IA guiará al usuario paso a paso:

1. Identificación: Solicita el número de pedido y el email de compra.
2. Selección: Muestra los productos disponibles y pregunta cuál devolver.
3. Motivos y Estado: Pregunta la razón (ej: "No cumplió expectativas") y el estado del producto (ej: "Nuevo sin etiquetas").
4. Evidencia: Solicita subir fotos del producto directamente al chat.
5. Reembolso y Envío: Coordina el método de reembolso (crédito/transferencia) y selecciona el courier (ej: Blue Express o tienda).
6. Finalización: Genera el ticket y entrega el link de pago (si aplica costo de devolución) para generar la etiqueta de envío.
