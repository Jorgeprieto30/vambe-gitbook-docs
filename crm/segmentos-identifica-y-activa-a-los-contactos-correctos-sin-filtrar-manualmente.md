# Segmentos: identifica y activa a los contactos correctos, sin filtrar manualmente

Segmentos permite construir audiencias reutilizables dentro del CRM a partir de reglas que tú defines: etapa del embudo, historial de compras, agendamientos, etiquetas, o cualquier combinación de estos criterios. En lugar de revisar contacto por contacto para determinar a quién reactivar o a quién ofrecer un nuevo producto, la condición se define una sola vez y Vambe entrega de inmediato la lista completa de los contactos que la cumplen.

> Para acceder: en el menú de la izquierda, dirígete a **CRM** y luego a **Segmentos**.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FKygP1uc7aLei16DBuvYB%2Fimage.png?alt=media&#x26;token=13dff3b0-0ff7-425d-971a-3496211128ac" alt="" width="201"><figcaption></figcaption></figure>

***

## Qué se puede definir en un segmento

Un segmento es una regla aplicada sobre la base de contactos. Es posible construir condiciones como:

* Contactos que pasaron por la etapa X y también por la etapa Y del embudo.
* Contactos que compraron el producto A hace un año.
* Contactos que agendaron el tratamiento X hace 4 meses.
* Contactos que llevan comprando durante los últimos 2 meses consecutivos.

Estas condiciones pueden combinarse según las necesidades del negocio. Esta funcionalidad resulta particularmente útil para las verticales de e-commerce y appointments, donde permite identificar con precisión quién compró un producto determinado en un rango de fechas, o quién agendó un tratamiento específico hace un período definido, y actuar sobre esa lista de inmediato.

***

## Cómo crear un segmento

Existen dos formas de crear un segmento, y ambas producen el mismo resultado.

La primera consiste en describirle a Pandai, en lenguaje natural, qué contactos se necesitan — por ejemplo, "contactos que agendaron un botox hace 4 meses" o "contactos que compran alimento para mascotas todos los meses". Pandai construye las reglas correspondientes y deja el segmento listo para su revisión.

La segunda es crearlo manualmente desde el formulario de segmentos, agregando las reglas de forma individual: etiquetas, etapas del embudo (si el contacto pasó por una etapa o si se encuentra actualmente en ella), canal de contacto, campos personalizados y, en cuentas que trabajan con la vertical de appointments, el tratamiento asociado. Un ejemplo simple: es posible filtrar a todos los contactos que realizaron un pedido de un producto específico entre dos fechas, y el segmento devuelve esa lista completa de inmediato.

> El campo de tratamiento solo está disponible en cuentas que trabajan con la vertical de appointments; en e-commerce no aparece, ya que no aplica.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2FZH0avSVXcfXoqRnwYw0u%2Fimage.png?alt=media&#x26;token=d4d1deb8-b81e-4e75-95ec-97307ea1009a" alt=""><figcaption></figcaption></figure>

***

## Segmentos RFM automáticos

Además de los segmentos que creas tú —con Pandai o manualmente—, cada tienda de e-commerce conectada cuenta con 11 segmentos que Vambe calcula y actualiza solo, sin que definas ninguna regla. Aparecen agrupados bajo la etiqueta **RFM · automático** en el listado de segmentos.

<figure><img src=".gitbook/assets/Captura de pantalla 2026-09-14 a la(s) 6.42.03 p.m. (1).png" alt=""><figcaption></figcaption></figure>

### Qué es RFM

RFM resume a cada comprador en tres preguntas:

* **Recencia:** ¿hace cuánto compró?
* **Frecuencia:** ¿cuántas veces ha comprado?
* **Monto:** ¿cuánto gasta por compra?

Cada una de las tres recibe una nota del 1 al 5, y la combinación de esas tres notas determina en qué segmento cae el comprador.

### Cómo se calcula

Las notas son relativas a cada tienda, no absolutas: un ticket de $50.000 puede considerarse alto en una tienda y bajo en otra, así que cada tienda se compara únicamente consigo misma. Los cortes entre notas quedan fijos una vez calculados, lo que permite ver si un cliente mejora o empeora de segmento con el tiempo.

<figure><img src=".gitbook/assets/Captura de pantalla 2026-09-14 a la(s) 6.55.05 p.m..png" alt=""><figcaption></figcaption></figure>

El mapa completo de los 11 segmentos se lee así:

* Los tres bloques agrupan por frecuencia de compra: compra seguido (F4-5), volvió a comprar (F2-3), o hizo una sola compra (F1).
* Dentro de cada bloque, mientras más arriba, más reciente es la última compra (de R1 a R5); mientras más a la derecha, más gasta el cliente (de M1 a M5).
* Cada celda representa un tipo de cliente, y su color indica a qué segmento pertenece. Cada cliente cae en un solo segmento, por lo que los 11 segmentos siempre suman el total de compradores de la tienda.

### Limitaciones a tener en cuenta

{% hint style="warning" %}
⚠️ Los segmentos RFM tienen algunas condiciones propias, distintas a las de los segmentos que creas manualmente:

* Solo están disponibles para tiendas de e-commerce conectadas que tengan al menos 200 compradores.
* Se actualizan una vez por semana, no en tiempo real.
* Son de solo lectura: no se pueden editar ni eliminar.
* En la mayoría de las tiendas, **Recompra activa** y **Recompra detenida** van a aparecer con 0 contactos. Esto es esperado: significa que esa tienda todavía no tiene suficiente recompra como para separar ese nivel, y no indica un error.
{% endhint %}

### Cómo se usan

Una vez calculados, los segmentos RFM se usan exactamente igual que cualquier otro segmento: puedes previsualizar los contactos que los componen y enviarles una campaña de mensajes o llamadas con IA directamente desde el segmento.

***

## Consulta de segmentos

Una vez creados, todos los segmentos quedan disponibles en un listado único, con su nombre, una descripción de la regla que los define, el usuario que los creó y la cantidad de contactos que califican en cada momento. Por ejemplo, un segmento como "En Touchpoint mes 1 (Nutrición)" puede agrupar miles de contactos que se encuentran actualmente en esa etapa específica del pipeline.

***

## Acciones disponibles sobre un segmento

Sobre un segmento ya creado existen dos acciones disponibles. La primera es **previsualizar** los contactos que lo componen, para conocer el tamaño y la composición de esa audiencia antes de tomar una decisión. La segunda es **enviar una campaña** directamente desde el segmento: es posible lanzar una campaña de mensajes o activar llamadas con IA hacia todos los contactos que lo componen, sin necesidad de exportar listas ni de reconstruir la audiencia en otra herramienta.

<figure><img src="https://310161448-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRUgcMYDLALCYrWDqh6tC%2Fuploads%2F4lX4aaeuYWcsxwjk6pTv%2Fimage.png?alt=media&#x26;token=641b7ab7-45f6-442d-b11a-53d434d0bff2" alt=""><figcaption></figcaption></figure>

***

## En resumen

Segmentos convierte la información disponible sobre los contactos —qué compraron, qué agendaron, en qué etapa se encuentran, o qué tan seguido y cuánto compran— en audiencias accionables, sin depender de filtros manuales ni de exportación de datos. Ya sea que el segmento lo construya Pandai, se arme regla por regla, o se calcule solo con RFM, el resultado es el mismo: identificar con precisión a quién dirigirse, y actuar de inmediato.
