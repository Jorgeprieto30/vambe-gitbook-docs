---
description: >-
  Deja de adivinar. Configura un sistema de puntuación automático para
  identificar y priorizar a tus clientes más valiosos (0 a 100) en tiempo real.
---

# Lead Scoring: Prioriza tus oportunidades de venta

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

El **Lead Scoring** es una funcionalidad que permite asignar automáticamente una puntuación (de 0 a 100) a tus tickets basándose en los datos del cliente.

**¿Para qué sirve?** Para que tu equipo de ventas sepa a quién llamar primero. Si tienes 50 leads nuevos, el sistema destacará con una "llama" 🔥 y un puntaje alto a aquellos que cumplen con tus criterios ideales (ej: empresas grandes, presupuesto alto, urgencia inmediata), dejando al final a los leads fríos.

***

#### ⚠️ Requisitos Previos

Para que el sistema pueda calcular puntos, necesita datos estructurados. El Lead Scoring solo funciona con campos de tipo:

* 🔢 Número (Ej: Cantidad de empleados, Presupuesto).
* ⏹️ Opciones (Ej: Rubro, Interés).
* ✅ Sí/No (Ej: ¿Tiene deuda?, ¿Es propietario?).

{% hint style="info" %}
Nota: Los campos de texto libre NO sirven para puntuar. _Si necesitas configurar estos datos primero, revisa el artículo:_ 👉 [\[Cómo crear campos personalizados y asignarlos al Ticket o Contacto\]](https://academy.vambe.ai/crm/gestion-de-campos-y-datos-a-recopilar)
{% endhint %}

***

#### 1. Acceder a la Configuración

1. En el menú lateral izquierdo, ve a la sección CRM.
2. Despliega el menú de Ajustes y selecciona Configurar Tickets.
3. Selecciona el Tipo de Ticket que usas en tu embudo de ventas (por ejemplo, "Ventas") y haz clic en Ir a editar.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

***

#### 2. Activar y Administrar Puntaje

Dentro del editor del ticket:

1. Busca la tarjeta llamada Score o puntaje.
2. Haz clic en el botón azul Administrar.
3. Activa el interruptor "Activar Puntaje".

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

***

#### 3. Definir Métricas y Pesos

El Lead Score se compone de distintas métricas, y cada una tiene un "Peso" (importancia) en la nota final.

{% hint style="success" %}
**Regla de Oro**: La suma de los "Pesos" de todas tus métricas debe dar exactamente 100%. Si no suma 100%, el sistema no te dejará guardar.
{% endhint %}

Haz clic en + Agregar métrica y selecciona un campo (del contacto o del ticket).

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

**A. Configuración para Campos Numéricos**

Si eliges un campo de número (ej: "Número de empleados"), debes definir rangos o umbrales. El sistema evalúa en orden y se queda con la última condición que coincida.

_Ejemplo:_

* Mayor que 300 → 20 puntos.
* Mayor que 700 → 50 puntos.
* Mayor que 1500 → 75 puntos.
* _(Si el cliente tiene 1000 empleados, cumplió la primera y la segunda, pero no la tercera. Se queda con 50 puntos)._

<figure><img src="../.gitbook/assets/image (6).png" alt="" width="375"><figcaption></figcaption></figure>

**B. Configuración para Campos de Opciones**

Si eliges un campo de opciones (ej: "Vertical" o "Industria"), simplemente asignas un puntaje fijo a cada opción disponible.

_Ejemplo:_

* Ecommerce → 100 puntos (Cliente ideal).
* Salud → 70 puntos.
* Educación → 90 puntos.

<figure><img src="../.gitbook/assets/image (7).png" alt="" width="375"><figcaption></figcaption></figure>

***

#### 4. Visualización y Uso

Una vez guardada la configuración, el sistema empezará a calificar tus tickets. Puedes usar el botón "Recalcular" para puntuar tickets antiguos con las nuevas reglas.

**En el Embudo (Pipeline)**

Verás una etiqueta de color con el puntaje en cada tarjeta. Utiliza el filtro de "Ordenar por" y selecciona "Por lead score" para que los clientes más importantes (Mayor puntaje) aparezcan automáticamente arriba o al principio de tu lista.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

**En Analítica**

Puedes ir al módulo de Analítica > Tickets y verás widgets específicos de Lead Score para entender la calidad de tus prospectos:

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



* Lead Score en el tiempo: ¿Están llegando mejores leads que antes?
* Distribución: ¿La mayoría de mis leads son "Bajos" (rojo) o "Altos"?
