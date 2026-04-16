---
description: >-
  Automatiza tu logística. Configura a tu IA para calcular costos de envío y
  distancias exactas entre tu tienda y el cliente usando Google Maps.
---

# ¿Cómo calcular costos de envío y distancias con Google Maps?

La función de **Google Maps** permite que tu Asistente tenga noción espacial. Puede calcular qué tan lejos está un cliente de tu local y, lo más importante, cuánto **cobrarle por el despacho automáticamente.**

Existen dos formas de usar esta herramienta según lo que necesites:

1. **Desde un Punto Fijo (Fixed Start):** Ideal para Delivery (Tienda -> Cliente).
2. **Puntos Dinámicos (Dynamic Points)**: Para medir distancias entre varios puntos variables (Punto A -> Punto B).

***

#### Configuración Paso a Paso

Sigue estos pasos para conectar la conversación con tu automatización:

**Paso 1: Ingresar al Asistente**

1. Ve al menú [Asistente](../como-armar-los-bloques/como-ingresar-al-asistente-de-inteligencia-artificial.md).
2. Entra a Pasos a Seguir (recomendado) o Casos Posibles.

**Paso 2: La Instrucción (El Gatillo)**

Debes decirle a la IA en qué momento exacto debe calcular la ruta.

* _Fórmula:_ `Una vez tengas [La dirección], ejecuta la función [Calcular Envío]`.

{% hint style="success" %}
**Ejemplo Real:** "Una vez tienes el rut del cliente, su nombre completo y dirección debes: 1. Ejecutar la función calcular el precio de envío".
{% endhint %}

**Paso 3: Crear la Función**

Haz clic en **+ Agregar Función** y selecciona **Google Maps.**

<figure><img src="../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

Aquí debes elegir cuál de las dos opciones usarás:

**Opción A:** Calculadora de Delivery (Fixed Start) Ideal si tienes una dirección fija (tu bodega) y quieres calcular el envío al cliente.

1.  Selecciona **Get distance from fixed start directions.**

    <figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>
2.  Campos de Entrada del Usuario (Tus datos fijos):

    * **Directions (Required)**: Escribe **TU dirección fija** (Ej: "Av. Providencia 1234, Santiago")
    * **Max distance (mts):** Define el radio máximo de atención en metros (Ej: `5000` para 5km).
    * **Cost per meter:** Coloca cuánto cobras por cada metro de viaje. La IA multiplicará la distancia por este valor para dar el precio final.

    <figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>
3. **Contenido Generado por IA:**
   * **User Destination:** Dale la instrucción para buscar la dirección del cliente (Ej: "Obtén la dirección de destino del usuario en formato calle, comuna, ciudad").



**Opción B:** Distancia entre **Puntos Dinámicos** Ideal para medir distancias entre dos puntos variables (A y B) sin una base fija.

1.  Selecciona Get distance from dynamic points.

    <figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>
2.  Contenido Generado por IA (recomendado no editar):

    * **List Description:** Explica el formato de las direcciones.
    * **Item Description:** Dile a la IA qué puntos debe buscar y comparar.

    <figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

**Paso 4: Verificación Visual**

Asegúrate de ver la tarjeta de la función "🗺️ Get distance..." justo debajo de tu texto de instrucción. Si la tarjeta está ahí, tu IA ya está lista para calcular rutas.

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

