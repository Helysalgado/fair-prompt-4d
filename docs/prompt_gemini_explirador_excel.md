# Prompt maestro para Gemini Canvas
## Explorador FAIR — Antes del prompt v2.0

Actúa como **diseñador instruccional y desarrollador front-end especializado en aprendizaje activo, alfabetización en IA, gestión de datos científicos, principios FAIR y herramientas educativas interactivas**.

Construye desde cero una aplicación web educativa, completa y funcional, en **un único archivo HTML autónomo**, para el taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica»**

La aplicación se llama:

# Explorador FAIR

**Subtítulo:** ¿Qué puedes saber realmente observando estos datos?

Será integrada posteriormente en un sitio web Quarto. No necesitas modificar Quarto ni generar páginas adicionales.

---

# 1. Propósito pedagógico

La actividad enseña a una persona investigadora a explorar un conjunto de datos, distinguir lo que puede observar de lo que necesita confirmar y formular preguntas antes de solicitar ayuda a una IA.

El caso es un Excel simulado de expresión génica que una investigadora necesita preparar para compartir como parte de una publicación.

El objetivo **no es corregir el dataset, certificar FAIR ni producir un diagnóstico automáticamente**.

Al finalizar, el participante deberá poder:

1. Reconocer la estructura básica del archivo y sus dos hojas.
2. Identificar observaciones respaldadas directamente por el archivo.
3. Distinguir datos, metadatos, interpretaciones e información pendiente.
4. Reconocer los límites de una abreviatura, una celda vacía y una nota parcial.
5. Formular preguntas útiles para la persona responsable del experimento.
6. Elaborar un inventario breve de observaciones e incertidumbres que utilizará después al interactuar con IA.

Idea principal:

**Un archivo puede mostrar datos sin contener toda la información necesaria para interpretarlos o reutilizarlos.**

La actividad debe desarrollar razonamiento científico y no funcionar como un examen.

---

# 2. Restricción pedagógica más importante

## No revelar las respuestas antes de la exploración

**La aplicación debe guiar al participante a descubrir las respuestas, no proporcionarlas anticipadamente.**

No muestres al inicio:

- Una lista de las cuatro incertidumbres previstas en el diseño.
- Un diagnóstico FAIR ya elaborado.
- Las interpretaciones esperadas de encabezados o notas.
- Un reporte de ejemplo que contenga las conclusiones.
- Respuestas preseleccionadas, señales de correcto o incorrecto o campos completados.

Implementa descubrimiento guiado:

**Observar → intentar → solicitar una pista → revisar → comprender.**

Para cada desafío:

1. Presenta una pregunta neutral.
2. Permite que el participante responda o seleccione evidencia.
3. Si necesita ayuda, ofrece una primera pista sin revelar la solución.
4. Ofrece una segunda pista más concreta si persiste la dificultad.
5. Permite corregir la respuesta.
6. Después del intento, permite abrir voluntariamente una explicación contextual.
7. Nunca obligues a responder correctamente para continuar.

Las pistas deben orientar la observación, no convertirse en respuestas disfrazadas.

**Ejemplo de pista adecuada:**

«Compara esa posición con las demás filas de la misma columna. ¿Qué observas?»

**Ejemplo inadecuado:**

«La celda D7 está vacía y ese es uno de los cuatro problemas del dataset».

Las explicaciones posteriores podrán aclarar la diferencia entre evidencia e interpretación, pero nunca inventarán información experimental.

Cuando una pregunta sea abierta o admita varias respuestas razonables, **no simules una evaluación semántica automática**. Solicita una justificación y ofrece criterios de reflexión.

---

# 3. Fuente de datos obligatoria

Utiliza exactamente el siguiente contenido, extraído del Excel original `expresion_genica_caso_simulado.xlsx`.

Los datos son ficticios y se utilizan exclusivamente para enseñanza.

## Hoja 1: `Expresion_genica`

`A1`: DATOS DE EXPRESIÓN GÉNICA · EJEMPLO SIMULADO

`A2`: Datos ficticios para una actividad docente. No corresponden a resultados experimentales reales.

La fila 3 está vacía.

Encabezados en `A4:D4`:

| Celda | Contenido |
|---|---|
| A4 | Gen |
| B4 | Control |
| C4 | Estrés A (prom.) |
| D4 | Estrés B |

Datos en `A5:D9`:

| Fila | Gen | Control | Estrés A (prom.) | Estrés B |
|---|---|---:|---:|---:|
| 5 | recA | 125 | 310 | 180 |
| 6 | rpoS | 85 | 245 | 290 |
| 7 | b0014 | 200 | 420 | [celda realmente vacía] |
| 8 | katG | 45 | 170 | 115 |
| 9 | dnaK | 190 | 390 | 375 |

**Importante:** `D7` está realmente vacía. No contiene el número cero, texto, fórmula ni marcador de dato faltante.

En la visualización de la hoja, representa `D7` como una celda vacía. La etiqueta «celda vacía» se puede mostrar en un detalle accesible de la interfaz después de seleccionarla, pero no debe colocarse como contenido original de la celda.

No alteres los nombres de genes, encabezados ni valores.

## Hoja 2: `Notas_experimento`

`A1`: NOTAS EXPERIMENTALES PARCIALES

La fila 4 contiene:

- `A4`: Campo
- `B4`: Registro disponible
- `C4`: Observación

Filas 5 a 10:

| Fila | Campo | Registro disponible |
|---|---|---|
| 5 | Nota suelta | Datos del experimento de marzo |
| 6 | Organismo | E. coli (sin cepa confirmada) |
| 7 | Proceso | Valores procesados |
| 8 | Condiciones | Control, Estrés A, Estrés B |
| 9 | Réplicas | Sin registro en este archivo |
| 10 | Responsable | Por confirmar |

Las celdas `C5:C10` no contienen información.

No conviertas esos vacíos en afirmaciones científicas.

## Restricciones científicas

Nunca:

- Supongas unidades de medición.
- Definas automáticamente el significado de «prom.».
- Concluyas que no se realizaron réplicas.
- Interpretes una celda vacía como cero.
- Asignes una causa experimental a la ausencia de un valor.
- Identifiques la cepa de *E. coli*.
- Equivalgas `b0014` a otro identificador sin información adicional.
- Inventes métodos, normalizaciones, tratamientos, fechas completas ni responsables.
- Declares que el archivo cumple o incumple todos los principios FAIR.

La anotación «Sin registro en este archivo» no equivale a «no hubo réplicas».

«Valores procesados» no describe por sí mismo el procedimiento de procesamiento.

El objetivo es reconocer esas limitaciones, no resolverlas inventando información.

---

# 4. Arquitectura general

Implementa cuatro estaciones:

1. **Observar el archivo**
2. **Interpretar con evidencia**
3. **Formular preguntas**
4. **Construir mi inventario**

Mostrar un indicador como:

`Estación 2 de 4`

La navegación debe ser libre.

No bloquees estaciones, no impongas un orden obligatorio y no exijas respuestas correctas para avanzar.

El progreso debe reflejar actividades realmente realizadas, no simplemente la última estación visitada.

No usar puntos, medallas, rankings, notas, porcentajes de acierto ni cronómetros competitivos.

La experiencia principal está diseñada para realizarse en aproximadamente **10 minutos**, con explicaciones adicionales opcionales.

---

# 5. Estación 1 — Observar el archivo

## Objetivo

Que el participante explore la estructura del Excel antes de recibir explicaciones sobre sus posibles problemas.

## Interfaz

Mostrar una representación interactiva de las dos hojas.

Usa pestañas:

- `Expresion_genica`
- `Notas_experimento`

La presentación debe recordar visualmente a una hoja de cálculo:

- Encabezados de filas y columnas.
- Coordenadas visibles.
- Celdas seleccionables.
- Distinción visual entre encabezados y valores.
- Panel lateral o inferior que muestre la celda seleccionada, su coordenada y su contenido literal.

Mantén el archivo original intacto.

## Actividad A — Explorar

Pregunta:

**¿Qué información puedes reconocer directamente en este archivo?**

Permite seleccionar celdas y registrar observaciones mediante campos breves.

No ofrezcas inicialmente una lista de respuestas correctas.

El participante puede escribir observaciones como:

- Algo que ve.
- Dónde lo ve.
- Qué cree que significa.
- Qué necesita confirmar.

Estos ejemplos son internos para orientar el diseño. **No los precargues como respuestas del participante.**

## Actividad B — Reconocer la estructura

Plantea preguntas breves que permitan descubrir:

- Cuántas hojas contiene el archivo.
- Qué representa cada fila de la tabla principal.
- Qué tipo de información contienen las columnas.
- Para qué podría servir una hoja de notas.

Usa respuestas seleccionables para hechos verificables y campos abiertos para interpretaciones.

Si alguien se equivoca, ofrece una pista para regresar al archivo.

## Cierre

Pregunta:

**¿Qué podrías describir con seguridad si únicamente tuvieras este Excel?**

Guarda la respuesta real.

No generes la respuesta automáticamente.

---

# 6. Estación 2 — Interpretar con evidencia

## Objetivo

Distinguir entre:

- Observación directa.
- Interpretación plausible.
- Información que requiere confirmación.

## Interfaz

Permite seleccionar encabezados, valores, celdas vacías y campos de notas.

Después de seleccionar un elemento, muestra preguntas contextuales sin adelantar su interpretación.

Por ejemplo:

**¿Qué puedes afirmar sobre el elemento seleccionado usando únicamente el archivo?**

**¿Tu afirmación describe algo visible o añade una interpretación?**

Ofrece las categorías:

- Lo observo en el archivo.
- Es una interpretación o hipótesis.
- Necesito más información para afirmarlo.

Exige una justificación breve cuando resulte pertinente.

## Situaciones internas que debes contemplar

Diseña interacciones para que, durante la exploración, puedan surgir preguntas sobre:

- La abreviatura en el encabezado `C4`.
- La ausencia de contenido en `D7`.
- La frase «Valores procesados».
- La información sobre réplicas.
- La descripción de condiciones.
- La cepa del organismo.
- El responsable por confirmar.

**No presentes esta enumeración como una lista inicial de problemas que deban encontrarse.**

## Retroalimentación

Para hechos observables, utiliza comprobación contra los datos fijos.

Para interpretaciones abiertas, no uses reconocimiento superficial de palabras ni finjas que una comparación de texto equivale a validar el razonamiento.

Ofrece preguntas orientadoras como:

- ¿En qué celda o nota aparece esa información?
- ¿El archivo lo afirma literalmente?
- ¿Estás describiendo un valor o proponiendo su significado?
- ¿Qué dato adicional permitiría distinguir entre dos interpretaciones?

Permite que el participante revise su interpretación y conserve, cuando corresponda, su respuesta inicial y la revisada.

---

# 7. Estación 3 — Formular preguntas

## Objetivo

Transformar incertidumbres en preguntas útiles para la persona responsable del experimento.

Comienza recuperando las observaciones e incertidumbres que el participante registró.

No muestres respuestas modelo antes del intento.

Pregunta:

**¿Qué necesitarías preguntar para interpretar o reutilizar estos datos con mayor confianza?**

Solicita al menos tres preguntas prioritarias, pero permite continuar si el participante no completa todas.

Para cada pregunta ofrece campos de:

- Elemento del archivo relacionado.
- Pregunta formulada.
- A quién habría que dirigirla.
- Por qué es importante.

No presupongas que todas las preguntas deben dirigirse a la misma persona. Algunas pueden requerir una fuente documental o una definición técnica externa.

## Pistas graduadas

Si alguien necesita orientación, utiliza pistas como:

**Pista 1:** «Piensa en qué información necesitas para comparar los valores de dos columnas».

**Pista 2:** «¿Qué tendrías que conocer sobre cómo se obtuvieron o procesaron esos valores?»

Estas pistas pueden ajustarse al elemento seleccionado, pero no deben completar la pregunta del participante.

## Reflexión

Pregunta:

**¿Cuáles de tus dudas podría ayudarte a explorar una IA y cuáles necesitarían información de quien realizó el experimento?**

Permite una respuesta libre.

No clasifiques automáticamente preguntas abiertas usando palabras clave.

---

# 8. Estación 4 — Construir mi inventario

## Objetivo

Revisar lo aprendido y producir un registro que sirva para continuar el taller.

Mostrar una síntesis construida exclusivamente con las respuestas reales del participante.

Secciones:

1. Mi necesidad.
2. Lo que observé en el Excel.
3. Mis interpretaciones iniciales.
4. Lo que revisé después de explorar.
5. Tres incertidumbres prioritarias.
6. Mis preguntas para continuar.
7. Qué podría delegar a la IA.
8. Qué sigue pendiente de confirmación.

Cada sección debe permitir editar las respuestas.

Si falta información, mostrar claramente:

`Sin respuesta`

No completar con contenido inventado.

Incluye una pregunta final:

**Antes de pedirle ayuda a una IA, ¿qué cambió en tu comprensión del problema?**

No evalúes automáticamente esa reflexión.

## Transición

Al finalizar, muestra:

**Ahora puedes conversar con una IA sobre el archivo. Compara lo que te proponga con tus propias observaciones y revisa cualquier afirmación que no puedas localizar en los datos.**

El siguiente paso del taller utiliza P0, pero la aplicación no debe ejecutar ese prompt ni conectarse a ningún modelo.

---

# 9. Persistencia y exportación

Utiliza `localStorage` para conservar, dentro del mismo navegador:

- Estación activa.
- Respuestas.
- Celdas seleccionadas.
- Interpretaciones iniciales y revisadas.
- Pistas solicitadas.
- Preguntas.
- Reflexión final.

Incluye un botón **Reiniciar actividad** con confirmación.

No recopiles nombres, correos ni identificadores personales.

Muestra un aviso discreto:

«Tus respuestas se guardan únicamente en este navegador. Puedes descargar tu registro o reiniciar la actividad».

La aplicación no enviará información a ningún servicio externo.

## Descarga Markdown

Incluye:

**Descargar mi exploración**

Debe producir localmente:

`explorador-fair-resultados.md`

El documento debe contener:

```markdown
# Explorador FAIR — Mi exploración

## Contexto
Taller: Antes del prompt
Caso: Expresión génica simulada
Fecha: [fecha local]

## 1. Mi necesidad
[respuesta real]

## 2. Observaciones
- Hoja y celda:
- Contenido observado:
- Mi interpretación:

## 3. Interpretaciones que revisé
- Primera interpretación:
- Evidencia consultada:
- Interpretación revisada:

## 4. Tres incertidumbres prioritarias
[respuestas reales]

## 5. Preguntas para continuar
[preguntas reales]

## 6. Qué podría delegar a la IA
[respuesta real]

## 7. Qué sigue pendiente
[respuesta real]

## 8. Reflexión
[respuesta real]
```

Incluye únicamente información realmente proporcionada o registrada durante la interacción.

Para campos incompletos, escribe «Sin respuesta».

No incluyas soluciones modelo ni afirmes que se realizaron verificaciones externas.

El reporte debe poder descargarse incluso si la actividad está incompleta.

---

# 10. Requisitos visuales

Diseño:

- Científico, universitario y moderno.
- Limpio y de excelente legibilidad.
- Fondo claro, encabezados sobrios y detalles de color discretos.
- Coherente con un sitio Quarto académico.
- Sin estética infantil.
- Sin personajes ni decoración excesiva.
- Responsive para escritorio y tabletas.
- Tabla legible, con desplazamiento horizontal cuando sea necesario.
- Panel contextual que no tape los datos.
- Animaciones mínimas y funcionales.

La estética debe transmitir exploración y análisis, no una evaluación escolar.

Las celdas y notas deben ser el centro visual de la experiencia.

---

# 11. Accesibilidad

Implementa:

- HTML semántico.
- Navegación completa por teclado.
- Foco visible.
- Botones reales.
- Etiquetas explícitas.
- `fieldset` y `legend` cuando corresponda.
- `aria-live` para retroalimentación.
- Contraste suficiente.
- No comunicar estados únicamente mediante color.
- Alternativas accesibles a interacciones de arrastrar y soltar.
- Nombres accesibles de celdas, por ejemplo: hoja, coordenada y contenido.
- Campos editables con etiquetas comprensibles.

No dependas del uso de mouse.

---

# 12. Requisitos técnicos

Entregar:

- **Un único archivo HTML completo**.
- CSS embebido.
- JavaScript embebido.
- Sin React ni frameworks.
- Sin backend.
- Sin Node.
- Sin login.
- Sin APIs externas.
- Sin herramientas analíticas de seguimiento.
- Sin dependencias externas obligatorias.
- Funcional offline.
- Sin IA en tiempo real.
- Fácil de alojar en un sitio estático.

No es necesario leer el archivo `.xlsx` desde el navegador: los datos exactos del caso están incorporados en esta especificación.

Almacena la representación de las dos hojas como datos estructurados dentro de JavaScript. Distingue claramente las celdas sin contenido de las celdas con números.

No utilices valores de demostración distintos de los proporcionados.

Sugiere el nombre:

`interactivos/explorador-fair.html`

No modifiques ningún archivo del proyecto Quarto.

---

# 13. Verificación funcional

Antes de entregar, revisa los siguientes casos:

1. La aplicación abre en estado neutral.
2. Ninguna respuesta aparece preseleccionada.
3. Ambas hojas contienen los datos exactos de esta especificación.
4. La celda `D7` permanece vacía.
5. Se pueden seleccionar celdas con mouse y teclado.
6. Las coordenadas se muestran correctamente.
7. Las pistas aparecen únicamente cuando se solicitan.
8. La primera pista no revela la respuesta.
9. Las preguntas abiertas no se califican automáticamente.
10. El participante puede corregir sus respuestas.
11. Las respuestas no desaparecen al cambiar de estación.
12. Las respuestas permanecen al recargar la página.
13. El resumen puede abrirse aunque falten actividades.
14. El reporte Markdown contiene respuestas reales.
15. Los campos incompletos aparecen como «Sin respuesta».
16. El botón de reinicio funciona con confirmación.
17. Ningún dato se envía a servicios externos.
18. No se asigna puntuación.
19. La aplicación funciona sin conexión.
20. No se presenta una certificación FAIR.

Si no tienes un navegador de pruebas disponible, no afirmes haber ejecutado estas comprobaciones. Indica cuáles revisaste por inspección del código y cuáles quedan pendientes de prueba en navegador.

---

# 14. Verificación pedagógica

Confirma que:

- Primero se observa y después se interpreta.
- No se presenta una lista inicial con las respuestas esperadas.
- El participante puede descubrir incertidumbres por sí mismo.
- Las pistas orientan sin resolver automáticamente.
- Existe apoyo adicional cuando alguien tiene dificultades.
- Se reconoce la diferencia entre «no está documentado» y «no existe».
- No se inventa el significado de «prom.».
- La ausencia de réplicas documentadas no se presenta como ausencia de réplicas experimentales.
- Los datos simulados se identifican como tales.
- El resultado es una exploración preliminar, no un diagnóstico de cumplimiento FAIR.
- El proceso prepara al participante para consultar una IA, sin reemplazar su razonamiento.

---

# 15. Entrega

Genera directamente:

1. **El HTML completo y funcional**, no fragmentos ni parches.
2. Una explicación breve de su arquitectura.
3. Una descripción de las cuatro estaciones.
4. Instrucciones para probarlo localmente.
5. Un ejemplo mínimo de enlace o integración mediante `iframe` en Quarto.
6. Una lista de las decisiones de accesibilidad implementadas.
7. Una lista de pruebas realizadas y pruebas pendientes.

No pidas confirmación antes de construir el prototipo.

**Principio final: la herramienta no debe pensar por el participante. Debe ayudarlo a observar mejor, reconocer los límites de la evidencia y formular preguntas más útiles.**

