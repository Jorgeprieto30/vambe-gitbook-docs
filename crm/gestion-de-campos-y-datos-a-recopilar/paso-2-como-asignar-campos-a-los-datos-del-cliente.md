# Paso 2 - Cómo asignar campos a los datos del cliente

Una vez que el campo está creado, podemos asignarlo al perfil del cliente para que quede registrado como información permanente del contacto (ej.: correo, ciudad, intereses, etc.).

{% stepper %}
{% step %}
### Ir a la sección de Clientes

En el menú lateral:

CRM → Clientes

![](<../.gitbook/assets/image png Dec 11 2025 02 44 03 3898 PM.png>)
{% endstep %}

{% step %}
### Asociar los campos

Arriba a la derecha hacer clic en:

**Asociar campos**

Luego:

* Seleccionar el campo que creaste.
* Clic en **Asociar campos**.

![](<../.gitbook/assets/image png Dec 11 2025 02 53 18 9409 PM.png>)

Listo.

El campo ahora forma parte del perfil del cliente y podrá ser rellenado manualmente o automáticamente por la IA (si está configurado para ello).
{% endstep %}
{% endstepper %}

<details>

<summary>¿Qué tipo de información suele ir en los datos del cliente?</summary>

* Nombre
* Correo electrónico
* Teléfono
* Ciudad o comuna
* Preferencias generales
* Productos o servicios de interés
* RUT o identificación (si aplica)

</details>

<details>

<summary>Cómo lo usará la IA</summary>

Si el campo es **editable por la IA** y la información aparece en la conversación:

* “Mi correo es [juan@mail.com](mailto:juan@mail.com)” → la IA lo guardará en _correo\_cliente_.
* “Vivo en Providencia” → se guardará en _ciudad_.

</details>
