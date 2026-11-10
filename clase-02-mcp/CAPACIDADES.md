# Prácticas de MCP – MiniModa

## 1. MCP

El MCP oficial de Playwright se instaló correctamente en Codex mediante el comando:

`codex mcp add playwright -- npx @playwright/mcp@latest`

Inicialmente presentó algunos problemas de conexión, pero posteriormente conseguimos conectarlo correctamente y comprobar que tenía **25 herramientas disponibles**.

Durante las primeras pruebas tuvimos dificultades para ejecutar las acciones del navegador debido a errores de `node_repl`. Sin embargo, en una ejecución posterior logramos completar correctamente el flujo de navegación y automatización de MiniModa utilizando Playwright.

## 2. Mi MCP

El agente revisó el proyecto, comprobó que todavía no existían casos de prueba y creó el caso **«Agregar al carrito un producto con stock en MiniModa»** en formato Markdown, incluyendo los datos, los pasos y el resultado esperado.

## 3. Ejecución con Playwright y verificaciones

Se ejecutó correctamente el caso de prueba en la tienda MiniModa.

El agente realizó las siguientes acciones:

1. Abrió la página de MiniModa y comprobó que el carrito estaba vacío.
2. Seleccionó el producto **«Body Manga Larga Estrellitas»**, color azul, talla 6M, y verificó que tenía **12 unidades en stock**.
3. Agregó una unidad al carrito y comprobó que aparecía el mensaje de confirmación.
4. Ingresó al carrito y verificó que el producto estuviera agregado, con cantidad **1** y un total de **$8.500**.

**Resultado:** los cuatro pasos finalizaron correctamente.

Codex guardó el registro de ejecución en el archivo `evidencia-minimoda-playwright.md`, incluyendo las llamadas a las herramientas de Playwright y los resultados de las verificaciones. También dejó referencias a las capturas de pantalla del producto y del carrito.

## 4. Tiempo ahorrado

El agente tardó **54 segundos en crear el caso de prueba**, según el registro de ejecución.

Estimo que realizar esta tarea manualmente me habría llevado aproximadamente 30 minutos. Por lo tanto, el ahorro potencial sería de unos 29 minutos.

Estos 30 minutos y el ahorro calculado son **estimaciones personales y no mediciones comprobadas**. Para obtener un resultado preciso sería necesario medir cuánto tiempo lleva realizar la misma tarea manualmente y compararlo con el tiempo utilizado por el agente.

El tiempo de creación del caso de prueba no debe confundirse con el tiempo de ejecución del flujo de compra con Playwright.

## 5. Límites encontrados

Durante las primeras pruebas encontramos dificultades técnicas relacionadas con `node_repl`, que impedían ejecutar las acciones del navegador.

Posteriormente conseguimos superar esas dificultades y completar correctamente el flujo con Playwright.

La prueba permitió verificar la selección de un producto con stock, su incorporación al carrito y la comprobación de sus datos.

**No se probó el proceso de compra ni el checkout.**
