# Evidencia de ejecución Playwright — MiniModa

- Fecha de ejecución: 2026-11-09
- URL: https://minimoda-navy.vercel.app/
- Navegador: Playwright MCP, pestaña aislada `minimoda-evidencia` (carrito inicialmente vacío; contador 0).
- Alcance: agregar una unidad al carrito y validar sus datos. No se inició checkout.

## Recorrido y resultados observados

| Paso | Acción / llamada Playwright | Resultado real | Estado |
|---|---|---|---|
| 1 | `browser_tabs({action: "new", isolatedContext: "minimoda-evidencia", url: "https://minimoda-navy.vercel.app/"})` | Abrió MiniModa; título `MiniModa — Ropa para niños`; contador del carrito 0. | PASÓ |
| 2 | `browser_click({target: "e53", element: "Body Manga Larga Estrellitas"})`; luego `browser_snapshot({})` | Navegó a `/producto/1`. Snapshot accesible: nombre `Body Manga Larga Estrellitas`; `Color: Azul · Talla: 6M`; precio ` $ 8.500`; stock 12. | PASÓ |
| 3 | `browser_click({target: "e188", element: "Agregar al carrito, una unidad"})` | Playwright ejecutó `page.getByTestId('add-to-cart-1').click()`; contador cambió a `Carrito, 1 producto` y la página anunció `Listo, lo sumamos al carrito.` | PASÓ |
| 4 | `browser_click({target: "e216", element: "Carrito con 1 producto"})`; luego `browser_snapshot({})` | Navegó a `/carrito`; aparece el producto, cantidad `1` y `Total $ 8.500`; encabezado/contador indica 1 producto. | PASÓ |

## Capturas

- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/evidencia/01-tienda.png
- https://github.com/rosalpanabelysqa-spec/minimoda-test/blob/main/clase-02-mcp/evidencia/02-carrito.png

Las llamadas Playwright citadas fueron realizadas durante esta ejecución; las comprobaciones se basan en los snapshots de accesibilidad obtenidos después de cada navegación y acción. El sitio indica que es una tienda de demostración con datos ficticios.
