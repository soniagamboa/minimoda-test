# Práctica clase 01: casos del registro de MiniModa con IA

**Sitio:** https://minimoda-navy.vercel.app/registro

> Así tiene que quedar tu entrega. Reemplazá cada `___tu respuesta aquí___` con lo tuyo.

## 1. Preparación
- Navegador y fecha: ___Chrome - 30/10/2026___

## 2. Superficie elegida
- Elegí (chat o cowork): ___Chat___
- Por qué: ___Porque ofrece una interfaz cómoda, rápida y directa para interactuar con el agente y generar los casos de prueba sin complicaciones___

## 3. Preguntas a Gemini
| # | Pregunta | Respuesta (resumen) | ¿Acierto o error/invento? |
|---|----------|---------------------|---------------------------|
| 1 | ¿Qué campos pide el formulario de registro de https://minimoda-navy.vercel.app/registro? | ___Nombre, correo electrónico, contraseña y confirmación de contraseña___ | ___Acierto___ |
| 2 | ¿Cuál es el largo mínimo de la contraseña y qué edad se permite? | ___Requiere un mínimo de 6 caracteres para la contraseña___ | ___Error / Invento___ |
| 3 | ¿Qué pasa si no acepto los términos? | ___El sistema no permite completar ni enviar el registro si no se marcan o aceptan los terminos y condiciones obligatorios___ | ___Acierto___ |

- Un acierto: ___Identificó con precisión los campos obligatorios que contiene el formulario de registro de MiniModa___
- Un error o invento: ___Asumió un requisito de longitud mínima de contraseña diferente al que realmente exige la interfaz web___

## 4. Primer modo
- Superficie y modo: ___Chat___
- Prompt de ejemplo:
  ```
  Sos QA. Vamos a probar el registro de https://minimoda-navy.vercel.app/registro
  Campos: nombre, email, contraseña, confirmar contraseña, edad, país y aceptar términos.
  1. Listá las reglas que se ven, los datos válidos e inválidos y los valores límite.
  2. Escribí 6 casos de prueba con: título, precondiciones, pasos con datos concretos,
     resultado esperado, prioridad (high/medium/low) y tipo (functional/negative/boundary).
  No inventes mensajes: si no sabés el texto exacto, marcalo "A VERIFICAR".
  ```
- Qué devolvió: ___Generó una lista estructurada con las reglas de validación del formulario y 6 casos de prueba detallados (con título, pasos, resultados esperados, prioridad y tipo)___

## 5. Otra superficie: comparación en 3 líneas
1. ___Velocidad: Muy rápida y fluida para obtener respuestas inmediatas y conversar con el agente.___
2. __Calidad de los casos: Los escenarios generados fueron lógicos, cubriendo correctamente los flujos principales y negativos____
3. ___Alucinaciones: Baja cantidad de inventos, requiriendo únicamente una pequeña revisión visual frente al formulario real de MiniModa___

## 6. Mis 3 mejores casos (cargados en Qase, proyecto MiniModa)
Formato del título: `Registro: <qué se prueba>`
Captura de la suite en Qase con tus casos: `evidencias/qase-suite-casos.png`

### Caso 1: ___Registro exitoso con credenciales válidas___
- Precondiciones: ___El usuario se encuentra en la página de registro de MiniModa___
- Pasos: ___1. Ingresar un nombre válido en el campo "Nombre". 2. Ingresar un correo electrónico nuevo válido y no registrado previamente. 3. Ingresar una contraseña segura en el campo "Contraseña". 4. Completar los campos requeridos y aceptar términos. 5. Hacer clic en Registrarse.___
- Resultado esperado: ___El registro se completa con exito y el sistema te envia un correo de confirmacion y te redirige al usuario.___
- Evidencia: `https://app.qase.io/project/MINIMODA?suite=0&previewMode=side&case=1`

### Caso 2: ___Validación de contraseña con menos caracteres de los requeridos___
- Precondiciones: ___El usuario se encuentra en la página de registro___
- Pasos: ___1.Completar el campo "Nombre" con un nombre válido. 2.Completar el campo "Correo" con un correo válido . 3.Ingresar una contraseña corta o inválida en el campo "Contraseña" 4. Hacer clic en el botón de registrarse___
- Resultado esperado: ___El sistema muestra un mensaje de error indicando que la contraseña no cumple con los requisitos minimos de seguridad y no permite avanzar con el registro___
- Evidencia: `https://app.qase.io/project/MINIMODA?suite=0&previewMode=modal&case=2`

### Caso 3: ___Restricción de registro con correo electrónico duplicado___
- Precondiciones: ___Existe una cuenta previa registrada con un correo determinado___
- Pasos: ___1. Ingresar un nombre válido en el campo "Nombre". 2. Ingresar en el campo de correo una dirección que ya esté registrada en el sistema. 3. Ingresar una contraseña válida en el campo "Contraseña". 4. Hacer clic en registrarse___
- Resultado esperado: ___El sistema rechaza la solicitud de registro de manera controlada e impide la creación de la cuenta duplicada. Asimismo, presenta una notificación de error clara en la interfaz que informa que la dirección de correo electrónico ya se encuentra asociada a una cuenta existente en el sistema___
- Evidencia: `https://app.qase.io/project/MINIMODA?suite=0&previewMode=modal&case=3`

## 7. Mapa del harness
| Pieza | En lo que usé |
|-------|---------------|
| Modelo | ___Gémini___ |
| App | ___chat de Gémini___ |
| Harness | ___Navegador web (Chrome)___ |
| MCP | ___N/A (Interfaz web nativa)___ |
| Skill | ___Ninguno___ |

## 8. Entrega
- Link de tu repo (pegalo también en el Telegram): ___https://github.com/soniagamboa/minimoda-test/edit/main/clase-01/practica.md___
