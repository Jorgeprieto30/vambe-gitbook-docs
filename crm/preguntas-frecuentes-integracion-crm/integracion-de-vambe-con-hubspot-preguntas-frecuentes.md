# Integración de Vambe con HubSpot — Preguntas Frecuentes

#### ¿Qué información envía exactamente Vambe a HubSpot?

Actualmente, Vambe se integra con **HubSpot Deals** y **HubSpot Tickets**.\
Se envía información asociada a los **tratos y tickets generados desde Vambe**, incluyendo:

* Campos del contacto
* Campos del trato o ticket
* Agentes configurados en HubSpot

No se envían conversaciones completas ni intenciones de compra como tal, **a menos que estas estén previamente mapeadas en campos específicos** dentro de la integración.

***

#### ¿Vambe puede crear contactos nuevos en HubSpot?

Sí. Vambe puede **crear nuevos contactos** en HubSpot de forma automática.

***

#### ¿Vambe puede actualizar contactos existentes en HubSpot?

Sí. Vambe puede **actualizar contactos ya existentes** en HubSpot.

***

#### ¿Vambe puede cambiar etapas del pipeline en HubSpot?

No. Vambe **no modifica directamente** las etapas del pipeline de HubSpot.\
Sin embargo, es posible **conectar o crear un “espejo”** entre las etapas configuradas en Vambe y las etapas existentes en HubSpot.

***

#### ¿Vambe puede leer información de HubSpot para personalizar respuestas de la IA?

No. Vambe **no extrae información desde HubSpot** para que la IA responda en base a esos datos (como nombre, empresa, etapa o vendedor asignado).\
No obstante, puedes **agregar manualmente la información que estimes relevante** para que la IA la utilice en sus respuestas.

***

#### ¿Se puede usar la información de HubSpot para segmentar respuestas del bot?

No. La información proveniente de HubSpot **no se utiliza para segmentar respuestas**.\
La segmentación se realiza directamente dentro de **Vambe**, utilizando sus herramientas actuales.

***

#### ¿Qué permisos necesita Vambe dentro de HubSpot?

Vambe requiere **permisos de lectura y escritura**, necesarios para:

* Crear o actualizar contactos
* Crear o actualizar tratos
* Crear o actualizar tickets

***

#### ¿Qué sucede si el cliente revoca el acceso a HubSpot?

La integración **deja de funcionar inmediatamente**.\
No se crearán ni actualizarán contactos, tratos o tickets desde Vambe hacia HubSpot.

***

#### ¿Qué datos se almacenan y dónde?

Se almacenan y sincronizan los **datos asociados a contactos, tratos y tickets** que se generan desde Vambe hacia HubSpot, de acuerdo con los campos configurados en la integración.

***

#### ¿La integración con HubSpot tiene un costo extra?

No. La integración con HubSpot **no tiene costo adicional**.

***

#### ¿La integración depende del plan contratado en Vambe?

No. La integración con HubSpot **no depende del plan** que tengas en Vambe.

***

#### ¿La integración depende del plan de HubSpot?

La integración está disponible, pero **los límites de uso sí pueden depender del plan de HubSpot** contratado.

***

#### ¿Existe un límite de contactos sincronizados?

Sí. Pueden existir **límites según el plan de HubSpot**, lo cual debe revisarse directamente en HubSpot.

***

#### ¿Existe un límite de eventos o acciones?

Sí. También pueden existir **límites de eventos o acciones**, definidos por el plan de HubSpot contratado.
