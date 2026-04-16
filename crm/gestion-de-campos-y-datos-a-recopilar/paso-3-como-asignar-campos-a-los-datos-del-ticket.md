# Paso 3 - Cómo asignar campos a los datos del ticket

Los tickets representan cada conversación activa con un cliente.

A diferencia del contacto (que es permanente), los datos del ticket describen el caso actual, por ejemplo:

* Producto específico que está cotizando
* Fecha de visita
* Motivo de atención
* Monto de la compra
* Dirección de retiro

Para asignar campos a un ticket debemos trabajar con tipos de ticket.

{% stepper %}
{% step %}
### Crear un tipo de ticket (si aún no existe)

Ruta: CRM → Ticket → +

![Crear tipo de ticket](../.gitbook/assets/image\(58\).png)

Configurar:

* Nombre del tipo de ticket
* Activar o no el monto (si se requiere mostrarlo en el embudo — un monto que detecta el asistente de IA sobre a cuánto precio equivale ese ticket)
* Guardar

![Guardar tipo de ticket](../.gitbook/assets/image\(59\).png)
{% endstep %}

{% step %}
### Asociar campos al tipo de ticket

1. Selecciona el tipo de ticket creado.
2. Haz clic en **Asociar campos**.

![Asociar campos — paso 1](../.gitbook/assets/image\(60\).png)

3. Marca los campos que quieres incluir.
4. Haz clic en **Asociar campos**.
5. Finalmente, clic en asociar campos.

![Asociar campos — paso 2](<../.gitbook/assets/image png Dec 11 2025 03 07 00 5877 PM.png>)

A partir de ahora, esos campos estarán visibles en todos los tickets de ese tipo.
{% endstep %}

{% step %}
### Asignar el tipo de ticket a un embudo o etapa

Este paso es fundamental: si un embudo o etapa no tiene asignado un tipo de ticket, los campos nunca se guardarán.

Cómo hacerlo:

1. Ir al embudo correspondiente.
2. Arriba a la derecha → **Editar embudo**.

![Editar embudo](<../.gitbook/assets/image png Dec 11 2025 03 10 09 3534 PM.png>)

3. En el panel izquierdo seleccionar **Ticket**.

![Seleccionar Ticket en panel izquierdo](<../.gitbook/assets/image png Dec 11 2025 03 11 26 2712 PM.png>)

Ahora puedes elegir:

A) Asignar un tipo de ticket a todo el embudo (recomendado)\
Ideal para procesos simples en los cuales en todo el embudo debemos recopilar los mismos datos.

![Asignar tipo a todo el embudo](<../.gitbook/assets/image png Dec 11 2025 03 12 57 0440 PM.png>)

B) Asignar un tipo de ticket etapa por etapa\
Útil para procesos que requieren recopilar información distinta en cada etapa (por ejemplo, ventas vs servicio).\
Al asignar el tipo de ticket, debes hacer click en guardar cambios.

![Guardar cambios al asignar tipo por etapa](<../.gitbook/assets/image png Dec 11 2025 03 15 25 1436 PM.png>)
{% endstep %}

{% step %}
### Regla clave: el tipo de ticket debe permanecer consistente

* Si un ticket entra a una etapa con un tipo de ticket distinto, el sistema reemplazará los datos anteriores del tipo previo.
* Por eso se recomienda: un embudo = un tipo de ticket, salvo casos muy específicos.
{% endstep %}

{% step %}
### Cómo recopila la IA la información en el ticket

Cuando:

* el campo existe
* está asociado al tipo de ticket
* está marcado como editable por la IA

Entonces la IA comenzará a registrar datos automáticamente cuando aparezcan en la conversación.

Ejemplos:

* “Quiero la batería modelo X500.” → se guarda en _producto\_interes\_ticket_.
* “Puedo este viernes.” → se guarda en _fecha\_visita_.
* “Mi dirección es Avenida Italia 1234.” → se almacena en _direccion\_servicio_.

![Información recopilada en el ticket](../.gitbook/assets/image\(61\).png)
{% endstep %}
{% endstepper %}

<details>

<summary>¿Dónde podemos ver la información recopilada?</summary>

En cada uno de los tickets podemos revisar los datos recopilados (ver imagen anterior).

</details>
