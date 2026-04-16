---
description: >-
  Configura tu integración. Conoce los permisos de Administrador necesarios en
  Meta y Google Ads para conectar Vambe Ads correctamente y evitar errores.
---

# Conectar Vambe Ads: Permisos y Accesos Necesarios

## Conectar Vambe Ads: Permisos y Accesos Necesarios

Para que Vambe Ads pueda gestionar tus campañas, optimizar presupuestos y leer tus datos, necesitamos que una persona de tu equipo conecte sus cuentas publicitarias con nuestra plataforma.

Esta conexión se realiza mediante OAuth (inicio de sesión seguro), lo que significa que Vambe operará utilizando únicamente los permisos que tenga el usuario que realiza la conexión.

> ⚠️ Regla de Oro: Si el usuario que conecta no tiene permisos de administrador, Vambe tampoco los tendrá y la integración fallará.

#### 1. Define al Responsable

Antes de empezar, elige a una persona de tu equipo (ej: el encargado de marketing) para realizar la conexión.

* Recomendación: Debe ser un usuario con acceso Administrador en todas las plataformas para evitar problemas de compatibilidad futuros.

***

#### 2. Requisitos para Meta Ads (Facebook e Instagram)

Para conectar el ecosistema de Meta, el usuario elegido debe cumplir con tres niveles de acceso dentro del Business Manager o Portfolio Comercial:

**A. Rol en el Negocio**

El usuario debe tener Control Total o ser Administrador del Business Manager (Portfolio Comercial).

**B. Acceso a la Cuenta Publicitaria**

No basta con estar en el negocio; el usuario debe tener asignada la cuenta publicitaria específica que se va a conectar.

* Permiso requerido: Administrador de la cuenta publicitaria (Control total para administrar campañas y configuración).

**C. Acceso a Activos**

Asegúrate de que el usuario también tenga permisos sobre los activos asociados para que Vambe pueda rastrear conversiones correctamente:

* ✅ Píxel.
* ✅ Catálogo (si aplica para tu negocio).

{% hint style="success" %}
¿Cómo verificarlo? En la configuración de tu Business Manager, ve a **Usuarios > Personas**, selecciona al usuario y revisa que en "**Activos asignados**" tenga la cuenta publicitaria con permisos de "**Administrar cuenta publicitaria**".
{% endhint %}

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>



#### Al hacer todo correctamente debería verse de la siguiente forma:

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

***

#### 3. Requisitos para Google Ads

La conexión con Google es más directa, pero igual de estricta con los permisos.

**Nivel de Acceso**

El correo electrónico que utilices para conectar debe tener el rol de Administrador en la cuenta de Google Ads.

* **¿Dónde lo veo?** En Google Ads, ve a **Herramientas > Configuración > Acceso y seguridad**. En la tabla de usuarios, la columna "Nivel de acceso" debe decir "Administrador".

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

***

#### 4. Seguridad y Privacidad

Entendemos que la seguridad es crítica. Por eso, el proceso de conexión está diseñado para proteger tus datos:

* 🔒 **Conexión Segura** (OAuth): No compartes tu contraseña con nosotros. La validación se hace directamente en las ventanas de Meta y Google.
* 🛡️ **Permisos Espejo**: Vambe no tiene "superpoderes"; solo tiene los mismos permisos que el usuario que conectó.
* 🚫 **Revocable**: Puedes desconectar Vambe y revocar el acceso en cualquier momento desde la configuración de tus plataformas.
