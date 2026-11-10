# Impedir agregar al carrito más unidades que el stock en MiniModa



- **ID:** CP-02
- **Objetivo:** Verificar que MiniModa impida agregar al carrito una cantidad superior al stock disponible del producto.
- **Estado:** falló en ejecución (2026-11-10)

## Precondiciones

- El producto Body Manga Larga Estrellitas está publicado con stock de 12 unidades.
- La variante de color azul y talle 6M está disponible.
- El carrito está vacío.

## Datos

Producto: Body Manga Larga Estrellitas. Color: azul. Talle: 6M. Stock disponible: 12 unidades. Cantidad solicitada: 13.

## Pasos

1. Ingresar a MiniModa y abrir el catálogo de productos.
2. Abrir el producto Body Manga Larga Estrellitas.
3. Seleccionar el color azul y el talle 6M.
4. Ingresar una cantidad de 13 unidades.
5. Intentar agregar el producto al carrito.
6. Revisar la respuesta de la tienda y el contenido del carrito.

## Resultado esperado

La tienda impide agregar más unidades que el stock disponible, ya sea mostrando un mensaje o limitando la cantidad. El carrito no queda con 13 unidades del producto.

## Resultado de ejecución

Al intentar aumentar la cantidad desde 12, el carrito aceptó una unidad adicional y mostró 13 unidades. No se presentó un mensaje ni un límite que impidiera superar el stock. El resultado esperado no se cumplió.
