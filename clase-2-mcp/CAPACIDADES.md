# Capacidades - Clase 2: Conexión con MCP y Optimización de Tareas

## 1. Playwright MCP (Automatización Web)
- **Qué pudo hacer el agente:** 
  - Navegó de forma autónoma por la tienda [MiniModa](https://minimoda-navy.vercel.app/) hasta la ficha del producto **"Body Manga Larga Estrellitas"** ($8.500, stock de 12, color azul, talle 6M).
  - Validó los elementos de la pantalla y añadió el producto al carrito, confirmando el mensaje de éxito y verificando que el total reflejara exactamente el precio del artículo.
  - Capturó y guardó automáticamente las evidencias visuales: `01-tienda.png` y `02-carrito.png`.
- **Tiempo de ejecución:** 1 minuto y 5 segundos.
- **Límites técnicos encontrados:** La ejecución depende de la estabilidad de los selectores web y de la velocidad de renderizado de la interfaz.

---

## 2. MCP Propio (`casos-de-prueba`)
- **Qué pudo hacer el agente:** 
  - Utilizó la herramienta `crear_caso_prueba` para generar un caso estructurado con prioridad alta sobre el flujo de compra.
  - Creó y guardó automáticamente el archivo Markdown en la ruta `casos/agregar-un-producto-con-stock-al-carrito-en-minimo-797c26d7-6935-4ae8-950e-209ff60dd089.md`.
  - Verificó la existencia y correcta persistencia del archivo utilizando la herramienta `listar_casos`.
- **Tiempo de ejecución:** 1 minuto y 11 segundos.
- **Límites técnicos encontrados:** El sistema utiliza slugs automáticos para evitar colisiones en los nombres de archivos, requiriendo una consulta explícita del listado para obtener el identificador exacto generado.

---

## 3. Comparativa y Ahorro de Tiempo (Manual vs. MCP)
- **Proceso manual:** 
  - Navegar la tienda, tomar capturas de pantalla manualmente y redactar un caso de prueba detallado con formato Markdown, pasos, datos y resultados esperados toma entre **10 y 15 minutos** de trabajo continuo.
- **Proceso con Agente y MCP:** 
  - El flujo combinado completo (ejecución web con Playwright y generación del caso de prueba con el MCP propio) tomó menos de **2 minutos y 30 segundos** en total.
- **Tiempo ahorrado:** Representa un ahorro estimado de **8 a 13 minutos por ciclo**, logrando una optimización y eficiencia superior al **80%** en tareas repetitivas de QA.
