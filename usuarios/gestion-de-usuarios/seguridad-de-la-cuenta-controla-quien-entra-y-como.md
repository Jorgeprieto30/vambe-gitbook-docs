---
description: >-
  Protege tu cuenta de Vambe desde Perfil → Seguridad: verificación en dos
  pasos, restricción de dominio de correo e inicio de sesión único.
---

# Seguridad de la cuenta: controla quién entra y cómo

Desde **Perfil → Seguridad** puedes reforzar quién puede entrar a tu cuenta de Vambe y de qué manera. Hay tres capas de protección, que puedes usar por separado o combinar según lo que necesite tu empresa:

* **Verificación en dos pasos (2FA):** pide un segundo paso al iniciar sesión.
* **Restringir dominio de correo:** solo entran personas con un correo de la empresa.
* **Exigir inicio de sesión único:** solo se puede entrar con el botón de Google u Outlook.

> Para entrar: ve a **Perfil** y luego a **Seguridad**.

<figure><img src="../.gitbook/assets/Screenshot 2026-10-05 at 4.53.28 PM.png" alt=""><figcaption></figcaption></figure>

***

### Verificación en dos pasos (2FA)

La verificación en dos pasos agrega una capa extra de seguridad: además de la contraseña, se pide un segundo paso al iniciar sesión.

* Se pide un **código único en cada inicio de sesión**, por SMS o desde una app de autenticación.
* **Protege tu cuenta aunque alguien más tenga tu contraseña.**
* Puedes activarla o quitarla cuando quieras.

Mientras no tengas ningún método configurado, la sección **Métodos de verificación** aparece como **Inactivo**, con el mensaje "No tienes métodos de verificación activos". Para empezar, haz clic en **Agregar validación**.

***

### Acceso al espacio de trabajo

En la sección **Acceso al espacio de trabajo** eliges el dominio de correo y el proveedor de inicio de sesión que pueden acceder a tu espacio. Tiene dos opciones, que puedes activar por separado o juntas.

#### Restringir dominio de correo

Solo pueden entrar personas con un correo de la empresa. Por ejemplo, si el dominio es **@empresa.com**, alguien con un correo **@gmail.com** no puede entrar.

#### Exigir inicio de sesión único

Solo se puede entrar con el botón de **Google** o **Outlook**. Aunque alguien tenga el correo y la contraseña correctos, no puede entrar escribiéndolos.

#### Cómo se combinan

| Opciones activadas                     | Qué se bloquea                                                             | Cómo entra la gente                                              |
| -------------------------------------- | -------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| Solo **Restringir dominio de correo**  | Los correos que no son del dominio de la empresa (por ejemplo, @gmail.com) | Como siempre, pero con un correo de la empresa                   |
| Solo **Exigir inicio de sesión único** | Entrar escribiendo el correo y la contraseña                               | Con el botón de Google u Outlook                                 |
| **Ambas**                              | Las dos cosas anteriores                                                   | Con el botón de Google u Outlook, usando un correo de la empresa |

{% hint style="warning" %}
**Antes de activarlas, revisa a tu equipo.** Si activas **Restringir dominio de correo**, quienes usen un correo de otro dominio ya no podrán entrar. Si activas **Exigir inicio de sesión único**, todas las personas tendrán que entrar con Google u Outlook. Confirma que todo tu equipo cumple la condición antes de guardar el cambio.
{% endhint %}

Después de elegir las opciones, usa el botón **Revisar cambios**, al final de la sección.

***

### ¿Qué opción elegir?

* **Quieres asegurarte de que solo entre gente de tu empresa:** activa **Restringir dominio de correo**.
* **Quieres que una contraseña, por sí sola, no alcance para entrar:** activa **Exigir inicio de sesión único**.
* **Quieres ambas protecciones:** actívalas juntas.

***

### En resumen

Si quieres proteger tu cuenta de Vambe, en **Perfil → Seguridad** puedes pedir un segundo paso de verificación al iniciar sesión, limitar el acceso a personas con un correo de tu empresa y exigir que todos entren con Google u Outlook. Las dos opciones de acceso al espacio de trabajo se pueden usar por separado o juntas, según el nivel de control que necesite tu operación.
