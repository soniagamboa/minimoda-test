# Agregar un producto con stock al carrito en MiniModa

- **ID:** CP-01
- **Prioridad:** alta
- **Requisito / objetivo:** Verificar que el usuario pueda agregar el producto indicado al carrito y que se muestren correctamente su nombre, cantidad, precio unitario y total esperado.

## Precondiciones
- MiniModa está accesible y el usuario puede ingresar a la tienda.
- El carrito está vacío antes de iniciar la prueba.

## Datos de prueba
- **Producto:** Body Manga Larga Estrellitas
- **Variante visible en la página:** color azul, talle 6M
- **Stock visible en la página:** 12 unidades
- **Cantidad a agregar:** 1
- **Precio unitario:** $8.500
- **Total esperado:** $8.500

## Pasos
1. Abrir MiniModa e ingresar a la tienda como visitante o con una cuenta válida.
2. Buscar y abrir la página del producto **Body Manga Larga Estrellitas**.
3. Verificar que la página muestre la variante azul / 6M, el stock 12 y el precio unitario de **$8.500**.
4. Agregar una unidad al carrito.
5. Abrir el carrito desde su enlace de navegación.
6. Verificar que el carrito muestre el nombre **Body Manga Larga Estrellitas**, la cantidad **1**, el precio **$8.500** y el total **$8.500**.

## Resultado esperado
El producto **Body Manga Larga Estrellitas** se agrega correctamente al carrito. El carrito muestra el nombre del producto, cantidad **1**, precio unitario **$8.500** y total **$8.500**.

## Evidencia
- [Página del producto (variante, stock y precio)](evidencia-CP-01-producto.png)
- [Carrito (producto, cantidad, precio y total)](evidencia-CP-01.png)
