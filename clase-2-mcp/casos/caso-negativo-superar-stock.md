# Intentar agregar una cantidad superior al stock en MiniModa

- **ID:** CP-NEG-01
- **Prioridad:** alta
- **Requisito / objetivo:** Verificar que el sistema impida agregar al carrito una cantidad superior al stock disponible para la variante seleccionada, ya sea limitando la cantidad o mostrando un mensaje claro, y que el carrito nunca quede con una cantidad mayor al stock.
- **Estado:** ejecutado — fallido

## Precondiciones
- MiniModa está accesible y el usuario puede ingresar a la tienda.
- El carrito está vacío antes de iniciar la prueba.
- Confirmar nuevamente el stock de la variante al momento de ejecutar, ya que puede cambiar.

## Datos de prueba
- **Producto:** Body Manga Larga Estrellitas
- **Variante visible en la página:** color azul, talle 6M
- **Stock visible en la página al ejecutar:** 12 unidades
- **Cantidad solicitada:** 13 unidades (una más que el stock visible)

## Pasos
1. Abrir MiniModa e ingresar a la tienda como visitante o con una cuenta válida.
2. Buscar y abrir la página del producto **Body Manga Larga Estrellitas**.
3. Confirmar que la variante azul / 6M muestre stock 12. Si el stock cambió, actualizar la cantidad solicitada para que sea una unidad mayor al stock vigente.
4. Con el carrito vacío, activar **Agregar al carrito** 13 veces para solicitar 13 unidades, ya que la ficha no presenta un selector de cantidad.
5. Abrir el carrito y verificar la cantidad del producto y si aparece un mensaje de límite o error.

## Resultado esperado
El sistema no agrega una cantidad superior al stock disponible: limita la cantidad al máximo de stock o muestra un mensaje claro que impide la operación. El carrito no queda con una cantidad mayor al stock disponible.

## Resultado observado
**Fallido.** Con stock visible de 12 unidades, al activar **Agregar al carrito** 13 veces, el sitio mostró **13 productos** en el contador y **13 unidades** del Body Manga Larga Estrellitas en el carrito, con un total de **$110.500**. No limitó la cantidad ni mostró un mensaje de advertencia; el carrito quedó por encima del stock. Al finalizar la comprobación, se vació el carrito.
