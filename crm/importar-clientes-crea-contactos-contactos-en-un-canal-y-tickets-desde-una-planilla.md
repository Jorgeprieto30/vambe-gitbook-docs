---
description: >-
  Configura qué crea Vambe al importar una planilla de clientes: solo contactos,
  o también contactos en un canal, tickets y una plantilla de Meta.
---

# Importar clientes: crea contactos, contactos en un canal y tickets desde una planilla

Importar clientes te permite cargar una base completa de contactos desde una planilla, sin necesidad de escribirle a cada uno para que quede registrado en Vambe. Por defecto, la importación solo crea los clientes con sus datos, pero puedes activar dos pasos adicionales: crear un contacto en un canal para cada fila y crear o mover tickets hacia una etapa del embudo, con una plantilla de Meta opcional para avisarles que ya pueden escribirte.

Esto te da dos usos distintos según lo que necesites: si solo quieres poblar tu base de datos y todavía no has definido por qué canal vas a contactar a esas personas, puedes limitarte a crear los clientes. Y si ya sabes por dónde vas a escribirles y quieres que entren de inmediato a un embudo, activas los pasos de canal y tickets para que el proceso de importación haga todo el trabajo.

{% hint style="info" %}
**Para entrar:** en el menú de la izquierda, ve a **CRM** y luego a **Clientes**. Ahí encontrarás el botón **Importar**.
{% endhint %}

<figure><img src=".gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

***

## Crear solo clientes

Este es el comportamiento por defecto. Al abrir **Importar clientes**, Vambe te arma una planilla de ejemplo con las columnas obligatorias **telefono**, **email** y **nombre**, más una columna por cada campo del cliente que agregues en **Campos del cliente**. Descargas la planilla, la completas con tus datos y la subes para revisar antes de confirmar.

<figure><img src=".gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

Con esta opción, cada fila de tu planilla queda registrada como un cliente en Vambe, sin crear ningún contacto en un canal ni ningún ticket. Es la opción más simple cuando quieres tener tu base de datos al día pero todavía no vas a contactar a esas personas, o cuando no has decidido por qué canal lo harás.

***

## Crear contactos en un canal

Si activas **Crear contactos en un canal**, cada fila de la planilla también genera un contacto en el número de WhatsApp (u otro canal) que elijas. Esto habilita a esas personas para conversar contigo por ese canal, aunque todavía no les hayas escrito.

Dentro de este paso puedes activar **Asignar ejecutivo desde la planilla**, para que el ejecutivo responsable de cada contacto se defina fila por fila en lugar de asignarse manualmente después.

***

## Crear tickets y avisar con una plantilla de Meta

Si además activas **Crear tickets**, cada contacto entra a la etapa del embudo que elijas, tal como si hubiera llegado por sí solo a esa parte del proceso. Esto es lo que te permite que una base completa de contactos importados empiece a moverse por tus asistentes y flujos de trabajo desde el primer momento, en lugar de quedar solo registrada.

Como estos contactos no te han escrito antes, necesitas una plantilla de Meta aprobada para poder contactarlos por WhatsApp. Por eso este paso incluye un selector de **Plantilla de Meta (opcional)**: al elegir una, Vambe se la envía a cada ticket creado apenas se confirma la importación, así la persona recibe un primer mensaje tuyo y puede responder para seguir la conversación.

<figure><img src=".gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

En **Campos del ticket** puedes mapear columnas de tu planilla a datos propios del ticket, además de los que ya mapeaste como campos del cliente. Estos campos se escriben al importar, en el ticket que se crea o en el que ya existía para ese contacto.

***

## En resumen

Importar clientes va desde cargar una base de datos simple hasta activar un embudo completo para todos tus contactos importados, según cuántos de estos pasos actives. La misma lógica que usas aquí es la que ya conoces de las campañas: campos para el contacto, campos para el ticket y asignación de ejecutivo, todo centralizado en una sola planilla que completas una vez.
