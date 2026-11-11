
# Práctica MCP – MiniModa

## Objetivo

Realizar una prueba de automatización utilizando Playwright MCP en Codex para comprobar que un producto con stock disponible puede agregarse correctamente al carrito de compras de MiniModa.

## Caso de prueba

Se trabajó con el producto Body Manga Larga Estrellitas, verificando sus datos:

- **Color:** Azul.
- **Talla:** 6M.
- **Stock disponible:** 12 unidades.
- **Cantidad agregada:** 1.
- **Precio unitario:** $8.500.
- **Total esperado:** $8.500.

## Ejecución y verificaciones

Se ejecutó el flujo con Playwright y se comprobaron correctamente los siguientes pasos:

1. Apertura de la tienda MiniModa.
2. Selección del producto con stock disponible.
3. Incorporación de una unidad al carrito.
4. Verificación del producto, la cantidad y el total en el carrito.

**Resultado:** los cuatro pasos finalizaron correctamente.

## Evidencias

- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/evidencia/01-tienda.png
- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/evidencia/02-carrito.png
- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/casos/agregar-al-carrito-un-producto-con-stock-en-minimoda-c2dd980e.md
- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/casos/impedir-agregar-mas-unidades-que-stock-en-minimoda-cp-02.md
- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/CAPACIDADES.md
- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/evidencia/evidencia-minimoda-playwright.md

## Resultado final

La prueba permitió comprobar que Playwright MCP pudo navegar por la tienda, seleccionar un producto disponible y agregarlo correctamente al carrito.

No se realizó el proceso de compra ni el checkout.
