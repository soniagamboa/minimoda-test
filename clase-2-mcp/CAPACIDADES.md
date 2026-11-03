# Capacidades y Evaluación - Clase 2: Conexión con MCP

## 1. ¿Qué pudo hacer el agente con Playwright MCP?
- Pudo interactuar de manera autónoma con un navegador web real a través de las herramientas del protocolo MCP.
- Navegó de forma automática hacia la tienda de práctica (`https://minimoda-navy.vercel.app/`).
- Realizó búsquedas de productos con stock, hizo clic en los elementos de la interfaz, examinó el contenido de las pantallas y completó el flujo de agregar un producto al carrito de compras sin intervención manual paso a paso.

## 2. ¿Qué pudo hacer nuestro propio MCP (Generador de Casos)?
- Conectarse localmente a Codex mediante `StdioServerTransport` para exponer herramientas personalizadas (`crear_caso_prueba` y `listar_casos`).
- Recibir los datos estructurados enviados por el agente y procesarlos mediante validación con esquemas (Zod).
- Limpiar los títulos de los casos mediante una función de normalización (slug) para asegurar que el nombre del archivo sea seguro y válido.
- Guardar automáticamente el archivo en formato Markdown (`.md`) dentro de la carpeta `casos/` con el título, requisito, pasos, datos, resultado esperado y prioridad definidos.

## 3. Tiempo ahorrado frente a hacerlo a mano
- **Ahorro estimado:** Aproximadamente entre **25 y 30 minutos**.
- **Detalle:** Crear un caso de prueba detallado a mano (formateando las secciones, escribiendo los pasos uno a uno y estructurando el archivo) toma tiempo de redacción. Automatizarlo mediante la herramienta del MCP permite generar la estructura completa instantáneamente con solo una instrucción en lenguaje natural. Lo mismo aplica para la navegación exploratoria con Playwright, que automatiza la verificación visual inicial.

## 4. Límites encontrados
- **Dependencia del contexto y las descripciones:** Si las descripciones de las herramientas (tools) o los prompts no son lo suficientemente claros, el agente puede dudar sobre qué parámetros enviar o qué herramienta invocar.
- **Validaciones estrictas:** Los esquemas de entrada (como Zod) imponen límites estrictos en los tipos de datos y longitudes máximas; si el modelo envía datos fuera de ese rango, la ejecución falla y requiere corrección.
- **Uso limitado en cuentas gratuitas:** El uso intensivo de agentes conversacionales para pruebas de navegación consume rápidamente los límites de las cuotas gratuitas de los modelos.
