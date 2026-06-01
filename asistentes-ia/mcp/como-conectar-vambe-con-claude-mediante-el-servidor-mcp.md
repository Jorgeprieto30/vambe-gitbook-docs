# Cómo conectar Vambe con Claude mediante el Servidor MCP

#### ¿Qué es el MCP y para qué sirve?

MCP (Model Context Protocol) es un protocolo que permite conectar herramientas de inteligencia artificial externas — como Claude — directamente con los datos y funcionalidades de Vambe. En términos simples: es el puente que le permite a Claude "hablar" con tu cuenta de Vambe para leer información, ejecutar acciones y ayudarte a gestionar tu operación sin tener que cambiar de pestaña.

Con esta conexión activa, puedes pedirle a Claude cosas como consultar contactos, revisar etapas del embudo, crear asistentes o listar compromisos pendientes, todo desde la misma conversación.

{% hint style="danger" %}
Esta integración está disponible para cualquier cliente que tenga acceso a Claude Desktop o a Claude.ai.&#x20;
{% endhint %}

***

#### ¿Qué puedes hacer con el MCP de Vambe?

Una vez conectado, Claude tendrá acceso a más de 100 herramientas de Vambe. Algunos ejemplos de lo que puedes hacer:

* Consultar y listar contactos, ejecutivos, asistentes, etapas y pipelines
* Crear o editar asistentes y escenarios
* Revisar compromisos y métricas de reuniones
* Configurar flujos y acciones directamente desde la conversación con Claude

***

#### Cómo configurar la conexión

**Paso 1 — Obtén la URL del servidor MCP en Vambe**

1. Ingresa a Vambe y dirígete a **Ajustes** (ícono inferior izquierdo).
2. Dentro de Ajustes, entra a **Desarrolladores** → **Servidor MCP**.
3. Copia la URL que aparece en el bloque **"Conectar con Claude Desktop"**:

```
   https://api.vambe.me/api/public/mcp
```

**Paso 2 — Agrega el conector en Claude**

1. Abre **Claude** (Desktop o web en claude.ai).
2. En el panel lateral izquierdo, haz clic en **Customize**.
3. Selecciona la pestaña **Connectors**.
4. Haz clic en el ícono **+** y luego en **Add custom connector**.
5. Completa los campos:
   * **Name:** Vambe (o el nombre que prefieras)
   * **Remote MCP server URL:** pega la URL copiada en el paso anterior
6. Haz clic en **Add**.

**Paso 3 — Autoriza la conexión**

1. Claude te mostrará una pantalla indicando que aún no estás conectado a Vambe.
2. Haz clic en **Connect**.
3. Serás redirigido a Vambe para autorizar el acceso. Haz clic en **Autorizar**.
4. Listo — la conexión queda activa automáticamente.

{% hint style="success" %}
Una vez autorizado, verás un listado de todas las herramientas disponibles del MCP de Vambe directamente en Claude. Puedes controlar qué acciones requieren aprobación manual y cuáles se ejecutan automáticamente.
{% endhint %}

***

#### ¿Qué acciones puede ejecutar Claude con esta conexión?

Al revisar el listado de herramientas, verás que Claude puede ayudarte con una gran variedad de tareas dentro de Vambe. Algunos ejemplos prácticos:

| Acción                            | Ejemplo de uso                                       |
| --------------------------------- | ---------------------------------------------------- |
| Listar contactos o ejecutivos     | "Muéstrame los contactos que entraron esta semana"   |
| Crear o editar asistentes         | "Crea un asistente nuevo para el pipeline de ventas" |
| Revisar etapas del embudo         | "¿Cuáles son las etapas actuales del pipeline X?"    |
| Consultar reuniones y compromisos | "¿Qué compromisos quedaron de las reuniones de hoy?" |
| Gestionar configuraciones         | "Actualiza el nombre de esta etapa"                  |

{% hint style="warning" %}
Recuerda que Claude ejecuta acciones reales dentro de tu cuenta de Vambe. Revisa bien las instrucciones antes de confirmar cambios importantes como editar asistentes o modificar configuraciones del embudo.&#x20;
{% endhint %}
