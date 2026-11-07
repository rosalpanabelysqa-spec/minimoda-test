# Práctica clase 01: casos del registro de MiniModa con IA

**Sitio:** https://minimoda-navy.vercel.app/registro

> Así tiene que quedar tu entrega. Reemplazá cada `___tu respuesta aquí___` con lo tuyo.

## 1. Preparación
- Navegador y fecha: ___Google Chrome, 1 de noviembre de 2026___

## 2. Superficie elegida
- Elegí (chat o cowork): ___Chat___
- Por qué: ___Por que es rápido, interactivo y nos permite armar los casos de prueba conversando paso a paso sin configurar programas complejos___

## 3. Preguntas a Gemini
| # | Pregunta | Respuesta (resumen) | ¿Acierto o error/invento? |
|---|----------|---------------------|---------------------------|
| 1 | ¿Qué campos pide el formulario de registro de https://minimoda-navy.vercel.app/registro? | ___Pide nombre, email, contraseña, confirmar contraseña, edad, país y el selector de términos y condiciones___ | ___Acierto___ |
| 2 | ¿Cuál es el largo mínimo de la contraseña y qué edad se permite? | ___Requiere un formato válido de correo y contraseña (sin validación estricta de longitud mínima visible) y acepta cualquier número en edad___ | ___Error/invento___ |
| 3 | ¿Qué pasa si no acepto los términos? | ___El botón de registro no permite avanzar o requiere marcar obligatoriamente la casilla___ | ___Acierto___ |

- Un acierto: ___Identificó correctamente los campos del formulario___
- Un error o invento: ___En la respuesta resumida de la pregunta 2, Gemini afirmó que no había una longitud mínima visible y que se aceptaba cualquier edad; la página indica mínimo 8 caracteres y edad entera de 13 a 120.___

## 4. Primer modo
- Superficie y modo: ___Gemini/chat___
- Prompt de ejemplo:
  ```
  Sos QA. Vamos a probar el registro de https://minimoda-navy.vercel.app/registro
  Campos: nombre, email, contraseña, confirmar contraseña, edad, país y aceptar términos.
  1. Listá las reglas que se ven, los datos válidos e inválidos y los valores límite.
  2. Escribí 6 casos de prueba con: título, precondiciones, pasos con datos concretos,
     resultado esperado, prioridad (high/medium/low) y tipo (functional/negative/boundary).
  No inventes mensajes: si no sabés el texto exacto, marcalo "A VERIFICAR".
  ```
- Qué devolvió: ___Una lista con reglas y 6 casos de prueba estructurados. Al contrastarla con el formulario, la respuesta resumida sobre contraseña y edad no coincide con las reglas visibles.___

## 5. Otra superficie: comparación en 3 líneas
1. ___En ChatGPT contrasté las respuestas con el formulario y encontré una discrepancia concreta: la página indica contraseña de 8 caracteres como mínimo y edad entre 13 y 120.___
2. ___Gemini fue útil para proponer una estructura de casos, pero la respuesta resumida de la pregunta 2 no reflejó esas reglas visibles.___
3. ___En ambas superficies conviene separar lo observado de lo supuesto y marcar como “A VERIFICAR” lo que requiere enviar el formulario.___

## 6. Mis 3 mejores casos (cargados en Qase, proyecto MiniModa)
Formato del título: `Registro: <qué se prueba>`
Captura de la suite en Qase con tus casos: `evidencias/qase-suite-casos.png`

### Caso 1: ___Registro: Alta exitosa con datos válidos___
- Precondiciones: ___Estar en la página de registro de MiniModa___
- Pasos: ___Ingresar un nombre válido en el campo Nombre. Ingresar un correo electrónico válido (ana.prueba@example.com).Ingresar una contraseña válida que cumpla el mínimo de 8 caracteres (ej. clave123). Repetir la misma contraseña en el campo Confirmar contraseña. Ingresar una edad válida dentro del rango permitido (ej: 15). Seleccionar un país del selector (ej: Argentina). Marcar la casilla de Acepto los términos y condiciones. Hacer clic en "Crear cuenta"___
- Resultado esperado: ___El sistema muestra el mensaje de éxito y un enlace para ver el correo en la bandeja.___
- Evidencia: `evidencias/qase-MM-4-registro-alta-exitosa.png`

### Caso 2: ___Registro: Validar contraseña menor al mínimo permitido___
- Precondiciones: ___Estar en la página de registro de MiniModa___
- Pasos: ___Completar los campos obligatorios con datos válidos. Ingresar una contraseña de 7 caracteres (ej. "clave12"). Confirmar la misma contraseña de 7 caracteres. Intentar enviar el formulario haciendo clic en "Crear cuenta".___
- Resultado esperado: ___la contraseña debe tener al menos 8 caracteres.___
- Evidencia: `evidencias/qase-MM-5-registro-password-7.png`

### Caso 3: ___Registro: Validar edad menor al límite permitido___
- Precondiciones: ___Estar en la página de registro de MiniModa___
- Pasos: ___Completar todos los campos del formulario de manera correcta. Ingresar un valor de 12 años en el campo Edad (el rango válido es de 13 a 120). Intentar enviar el formulario haciendo clic en "Crear cuenta".___
- Resultado esperado: ___Bloqueo del registro y validación del rango de edad (13 a 120).___
- Evidencia: `evidencias/qase-MM-6-registro-edad-12.png`

## 7. Mapa del harness
| Pieza | En lo que usé |
|-------|---------------|
| Modelo | ___Gemini y ChatGPT___ |
| App | ___MiniModa, sitio web de práctica cuya página de registro se probó.___ |
| Harness | ___Interfaz de chat de Gemini y ChatGPT; navegador Chrome para consultar MiniModa; Qase para organizar los casos de prueba.___ |
| MCP | ___N/A no use MCP de forma directa___ |
| Skill | ___N/A no use una especifica___ |

## 8. Entrega
- Link de tu repo (pegalo también en el Telegram): ___https://github.com/rosalpanabelysqa-spec/minimoda-test___
