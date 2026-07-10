---
description: >-
  Convierte comentarios en ventas. Accede al panel de automatización de
  Instagram y elige entre estrategias Globales, por Post o Futuras todas estas
  impulsadas por IA.
cover: ../.gitbook/assets/instagrams comments.png
coverY: 0
---

# Automatización de Comentarios en Instagram

## Automatización de Comentarios en Instagram

### Automatización de Comentarios en Instagram: Panel Principal

La sección de **Comentarios** en Vambe es tu centro de control para convertir interacciones públicas en conversaciones privadas y ventas. Desde aquí, podrás definir cómo responde tu IA cuando alguien escribe en tus publicaciones.

#### Cómo llegar

1. Menú lateral → **Canales.**
2. Submenú → **Comentarios** (icono Instagram).
3. Selecciona tu cuenta de Instagram.

***

#### Cómo funciona

Cuando alguien comenta en tu post:

```
Comentario → Vambe detecta → IA evalúa condición → Si cumple:
                                                    ├── Crea ticket en la etapa
                                                    ├── Responde comentario (público)
                                                    └── Envía DM (privado)
```

***

#### Cómo configurar una automatización

Todas las automatizaciones usan el mismo formulario:

**1. Seleccionar Tipo**

Elige cómo funciona la automatización. La opción que elijas afecta tu contador de conversaciones.

| Tipo            | Qué hace                                                                                                   | Contador de conversaciones                |
| --------------- | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| **Inteligente** | La IA entiende el contexto y decide cuándo y cómo responder, tanto en el comentario como en el DM.         | Cada activación suma **1 conversación**.  |
| **Template**    | Publica el comentario y envía por DM el mensaje textual que tú defines, tal cual, **sin pasar por la IA**. | **No suma** conversaciones a tu contador. |

{% hint style="info" %}
**¿Cuándo conviene el tipo Template?** Es ideal para publicaciones muy virales o concursos, donde solo quieres enviar un mensaje predefinido a quienes comentan sin consumir conversaciones. La contraparte es que pierdes el conocimiento de la IA en ese flujo.
{% endhint %}

{% hint style="warning" %}
**Importante:** aunque la automatización sea de tipo Template, si el cliente final **responde el DM**, la IA toma la conversación normalmente según la etapa en la que haya quedado el contacto.
{% endhint %}

**2. Seleccionar Etapa**

Elige qué etapa del CRM manejará los contactos. Esta etapa determina:

* Qué **Asistente IA** responde los DMs y comentarios.
* Qué **base de conocimiento** usa.
* A qué parte del **embudo** entra el contacto.

> **Importante**: La etapa debe tener un Asistente IA activo. Sin asistente, no funcionará la automatización.

**3. Tipo de Activación**

| Acción              | Qué hace                          |
| ------------------- | --------------------------------- |
| **Comentar**        | Responde públicamente en el post. |
| **Mensaje DM**      | Envía mensaje privado.            |
| **DM + Comentario** | Ambas.                            |
| **Eliminar**        | Borra el comentario.              |

**4. Detector de Activación**

**Condición IA** (recomendado): Instrucción en lenguaje natural.

```
Ejemplo: "Si pregunta por precio, disponibilidad o muestra interés en comprar".
```

**Palabras clave**: Términos exactos.

```
precio, costo, info, quiero, envío.
```

> **Pro Tip**: La Condición IA es más flexible y puede entender sinónimos, errores de ortografía y variaciones. Las palabras clave son más precisas pero menos adaptables.

**5. Instrucciones para Comentarios**

Guía a la IA sobre cómo responder públicamente.

```
Actúa como un experto amigable de nuestra marca. Cuando alguien pregunte
por información:

1. Agradece su interés de forma genuina
2. Menciona que le enviarás los detalles por mensaje privado
3. Usa un tono cercano pero profesional
4. Incluye un emoji relevante

No menciones precios públicamente. Mantén la respuesta breve (máximo 2 líneas).
```

**6. Instrucciones para DMs**

Guía a la IA sobre cómo iniciar la conversación privada.

```
Saluda al cliente de forma cálida.

1. Agradécele por comentar en nuestra publicación
2. Pregunta cómo puedes ayudarle
3. Si preguntó por precio, comparte la información completa
4. Ofrece resolver cualquier duda adicional
5. Si es apropiado, invítalo a visitar: https://www.tutienda.com
```

**7. Contexto Adicional (opcional)**

Información extra: precios, links, promociones, detalles del producto.

```
Ejemplo: "Producto: Zapatillas Pro. Precio: $89.990.
Link: mitienda.com/zapatillas. Envío gratis sobre $50.000"
```

***

#### Tipos de Automatización

**Automatización Futura**

**Qué es**: Regla que se activa con tu **próximo post**.

**Cómo llegar**: Panel de Comentarios → Tarjeta "Automatización Futura"

**Cuándo usarla**:

* Programas posts desde Instagram y quieres la automatización lista.

**Limitación**: Solo 1 activa por cuenta. Se aplica al siguiente post que publiques.

> Luego de detectar el post respectivo para la automatización futura, la automatización pasa a ser una automatización individual para el post identificado, permitiéndote generar una nueva automatización futura para un nuevo post.

***

**Automatización Global**

**Qué es**: Regla que aplica a **todos tus posts** (pasados, actuales y futuros).

**Cómo llegar**: Panel de Comentarios → Tarjeta "Automatización Global"

**Cuándo usarla**:

* Quieres automatizar toda la cuenta sin configurar post por post.

> **Prioridad**: Si un post tiene automatización individual, esa tiene prioridad sobre la global.

***

**Post Individual**

**Qué es**: Regla para un **post específico** que ya existe.

**Cómo llegar**: Panel de Comentarios → Tarjeta "Post Individual" → Selecciona el post → "Administrar".

**Cuándo usarla**:

* Post antiguo.
* Sorteo o concurso con reglas particulares (aquí el tipo **Template** es especialmente útil para no consumir conversaciones).
* Probar automatización antes de activar global

**Ventaja**: Puedes tener múltiples automatizaciones en el mismo post (ej: una para ventas, otra para moderación).

***

#### Resumen de diferencias

| Tipo           | Alcance           | Ideal para                            |
| -------------- | ----------------- | ------------------------------------- |
| **Futura**     | Próximo post      | Lanzamientos programados.             |
| **Global**     | Todos los posts   | Automatización completa de la cuenta. |
| **Individual** | 1 post específico | Posts virales, promociones puntuales. |

#### Gestionar Automatizaciones

Desde el panel de **Gestionar Automatizaciones** podrás tener una vista global de todas tus automatizaciones, permitiéndote accede de manera más rápida a cada una de ellas

#### Registro de Actividad

En cada post podrás ver el historial de decisiones que tomó la IA sobre dicho post.

***
