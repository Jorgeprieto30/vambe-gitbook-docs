---
cover: ../.gitbook/assets/Portada 20.png
coverY: 0
---

# Cómo analizar el avance de tus clientes en el embudo desde tus publicidades

Deja de mirar solo clics e impresiones y comienza a medir resultados reales. Con la vista de Atribución en Vambe Ads puedes ver exactamente cuántos clientes llegaron a cada etapa de tu embudo desde cada anuncio, cuánto te costó cada resultado y cuánto dinero real generó cada campaña.

***

### ¿Qué puedes medir con la atribución?

Con esta vista podrás responder preguntas como:

* ¿Cuántos clientes llegaron a cada etapa del embudo desde una campaña específica?
* ¿Qué anuncio genera más clientes que avanzan hasta "Agendados" o "Comprados"?
* ¿Cuánto me cuesta realmente un cliente que agenda?
* ¿Cuánto me cuesta un cliente que compra?
* ¿Cuánto dinero en tickets generó cada plataforma o anuncio?

Todo esto se puede analizar por campaña, por conjunto de anuncios, por anuncio y por plataforma.

***

### Ingresar a la sección de Atribución

1. Ingresa a Vambe Ads: [Cómo ingresar a Vambe Ads](https://academy.vambe.ai/v1/docs/c%C3%B3mo-ingresar-a-vambe-ads)
2. En el menú lateral izquierdo, haz clic en **Atribución**.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Desde aquí puedes navegar entre cuatro niveles de análisis usando las pestañas superiores:

| Pestaña                  | Qué muestra                                   |
| ------------------------ | --------------------------------------------- |
| **Plataformas**          | Resultados agrupados por Google, Meta, TikTok |
| **Campañas**             | Resultados por cada campaña activa            |
| **Conjunto de anuncios** | Resultados por grupo de anuncios              |
| **Anuncios**             | Resultados por cada anuncio individual        |

También puedes filtrar por **rango de fechas**, usar el botón **Filtrar** para segmentar resultados y alternar entre vista **Tabla** y **Gráficos**.

***

### Métricas nativas de tickets

La vista de Atribución incluye dos columnas nativas para negocios de servicios o ventas consultivas que no dependen de un carrito de compras:

| Columna                       | Descripción                                                                       |
| ----------------------------- | --------------------------------------------------------------------------------- |
| **Monto de Tickets**          | Total de dinero generado en tickets atribuido a esa plataforma, campaña o anuncio |
| **Monto Promedio por Ticket** | Promedio del valor de los tickets generados                                       |

Estas métricas conectan el ticket → contacto → UTM/evento del anuncio, permitiendo ver en tiempo real cuánto dinero genera cada plataforma o anuncio individualmente.

💡 Estas columnas son especialmente útiles para clientes de servicios, ya que permiten optimizar el presupuesto publicitario basándose en ingresos reales y no solo en cantidad de contactos.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

***

### Personalizar columnas

Haz clic en **Administrar Columnas** (arriba a la derecha) para gestionar qué columnas aparecen en la tabla.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

Desde aquí puedes:

* Activar o desactivar columnas existentes.
* Reordenar las columnas visibles.
* Crear columnas personalizadas con el botón **+ Crear columna**.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

***

### Crear columnas para ver el avance por etapas del embudo

Para analizar cuántos clientes de cada anuncio llegan a una etapa específica de tu embudo, debes crear una columna personalizada por etapa.

#### Paso a paso: Crear una columna por etapa

1. Haz clic en **Administrar Columnas** → **+ Crear columna**.
2.  Asigna un nombre claro. Ej: _"Clientes en Agendados"_.\
    <br>

    <figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>
3. En tipo de columna, elige **Por condiciones**.
4. Agrega un filtro con la siguiente lógica:
   *   Condición: **Etapas**<br>

       <figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>
   *   Ha estado en etapa\
       <br>

       <figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>
   *   Selecciona el embudo y la etapa que quieres analizar.\
       <br>

       <figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>
5. Guarda la columna, actívala y reordénala si es necesario.

> 👉 Repite este proceso para cada etapa relevante de tu embudo.

***

### Análisis del avance por etapa

Una vez activadas las columnas, en la tabla podrás ver por cada anuncio o campaña:

* Total de contactos que iniciaron conversación.
* Cuántos de esos contactos llegaron a cada etapa del embudo.

**Ejemplo:** Si 272 contactos iniciaron conversación y 20 llegaron a la etapa "Agendados", significa que de cada 272 leads, 20 avanzaron hasta el agendamiento. Puedes comparar esto entre campañas, conjuntos de anuncios y anuncios individuales para saber desde dónde vienen los clientes que más avanzan.

***

### Calcular cuánto cuesta cada cliente por etapa

Una vez que tienes las columnas de avance por etapa, puedes calcular el costo real por resultado creando una columna de operación.

#### Paso a paso: Crear una columna de costo por cliente

1. Haz clic en **Administrar Columnas** → **+ Crear columna**.
2. Asigna un nombre. Ej: _"Costo por Agendado"_.
3. Selecciona **Operación** como tipo de columna.
4.  Configura la operación:

    * Primer valor: **Gasto** (métricas de rendimiento)
    * Operación matemática: **División**
    * Segundo valor: la columna de etapa creada anteriormente. Ej: _"Clientes en Agendados"_

    <br>

    <figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>


5. Guarda la columna, actívala y reordénala.

**Ejemplo de resultado:**

* Gasto total de la campaña: $94.000
* Clientes que llegaron a "Agendados": 20
* **Costo por cliente agendado: $4.700**

***

### ¿Qué información obtienes con todo esto?

Con estas columnas podrás ver de forma clara:

* Cuánto te cuesta que un cliente agende o compre.
* Qué campañas empujan mejor a los clientes por el embudo.
* En qué etapa se están cayendo los leads.
* Cuánto dinero real en tickets genera cada plataforma o anuncio.

Todo esto visible por anuncio, campaña, conjunto de anuncios y plataforma — para tomar decisiones de inversión basadas en resultados reales, no solo en métricas de alcance.
