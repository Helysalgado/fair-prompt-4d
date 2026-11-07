i# Gemini Canvas — Herramienta interactiva 2
## Explorador de vocabulario: «Sé lo que necesito, pero ¿cómo se llama?»

Actúa como **diseñador instruccional especializado en aprendizaje activo, alfabetización en inteligencia artificial, comunicación científica y desarrollo de aplicaciones web educativas interactivas**.

También actúa como desarrollador front-end con experiencia en HTML, CSS, JavaScript y accesibilidad.

Quiero que construyas una aplicación educativa completa, funcional y autónoma para el taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica»**

La aplicación se llamará:

**Explorador de vocabulario**

Subtítulo:

**«Sé lo que necesito, pero ¿cómo se llama?»**

Será la segunda herramienta interactiva del taller, después de Explorador FAIR.

La aplicación se integrará posteriormente en un sitio web Quarto, pero ahora debes crear exclusivamente un archivo HTML independiente.

---

# 1. Propósito pedagógico

Una persona puede saber qué necesita lograr, pero desconocer los términos técnicos que le permitirían describir mejor su problema.

Esta actividad busca que los participantes descubran que:

- La necesidad inicial puede expresarse en lenguaje cotidiano.
- Aprender vocabulario técnico ayuda a distinguir conceptos que parecen similares.
- Conocer un término no equivale a comprenderlo.
- Una IA puede ayudar a explorar vocabulario, pero sus definiciones deben examinarse críticamente.
- No es necesario dominar toda una disciplina antes de pedir ayuda.
- El vocabulario permite delimitar mejor la tarea, pero no sustituye su especificación.

La actividad debe permitir que la persona avance desde:

**«Esto es lo que quiero hacer»**

hasta:

**«Estos son los conceptos que necesito comprender para expresar mejor mi solicitud».**

No se busca memorizar definiciones ni aprobar un examen.

## Resultados de aprendizaje

Al finalizar, el participante podrá:

1. Identificar términos técnicos relacionados con una necesidad concreta.
2. Distinguir conceptos que suelen confundirse.
3. Reconocer qué términos comprende y cuáles necesita investigar.
4. Formular preguntas para aclarar el significado de un concepto.
5. Revisar su descripción inicial usando el vocabulario aprendido.
6. Documentar el proceso mediante un Reporte descargable.

---

# 2. Duración

La herramienta está diseñada para una actividad de **12 a 15 minutos**.

Debe ser posible completar una situación en ese tiempo.

Las otras situaciones estarán disponibles para exploración opcional.

**No obligues a completar los tres casos.**

Esto es importante para mantener el ritmo del taller.

---

# 3. Situaciones de aprendizaje

Incluye tres situaciones independientes.

Cada una debe partir de una necesidad expresada en lenguaje cotidiano, sin utilizar inicialmente los términos técnicos que el participante debe descubrir.

## Caso A — Investigación científica

### Situación inicial

«Tengo muchos artículos científicos relacionados con mi tema. Quiero identificar cuáles me sirven, recuperar información importante y organizar lo encontrado para poder revisarlo después».

### Vocabulario interno de referencia

- Estrategia de búsqueda.
- Criterios de inclusión y exclusión.
- Cribado o selección de literatura (*screening*).
- Extracción de datos.
- Trazabilidad de decisiones.
- Revisión sistemática, solo como un posible tipo de metodología formal, no como sinónimo automático de revisar artículos.

### Distinciones que debe aprender

- Buscar artículos no es lo mismo que seleccionarlos.
- Seleccionar artículos no es lo mismo que extraer datos.
- Una revisión de literatura no es automáticamente una revisión sistemática.
- Documentar decisiones ayuda a revisar cómo se llegó a una selección.

No presentes esas distinciones al inicio como respuestas.

## Caso B — Desarrollo de software

### Situación inicial

«Quiero una herramienta que permita a otras personas subir un archivo, revisar información y descargar un resultado. Sé lo que debería hacer, pero no sé cómo describírselo a alguien que va a programarla».

### Vocabulario interno de referencia

- Requisitos funcionales.
- Entradas y salidas.
- Interfaz de usuario.
- Validación de datos.
- Criterios de aceptación.
- Prototipo.
- Persistencia de datos, solamente si el caso evoluciona hacia conservar información.

### Distinciones que debe aprender

- Una función deseada no equivale a su implementación técnica.
- Describir qué hace una herramienta es distinto de indicar cómo debe verse.
- Una pantalla bonita no garantiza que una herramienta funcione correctamente.
- Un criterio de aceptación define una condición verificable del resultado.

Evita convertir la actividad en una clase de programación.

## Caso C — Gestión de datos científicos

### Situación inicial

«Tengo una tabla con resultados de un experimento y quiero compartirla para que otras personas puedan comprenderla y utilizarla sin tener que preguntarme cada detalle».

### Vocabulario interno de referencia

- Datos.
- Metadatos.
- Diccionario de datos.
- Procedencia.
- Identificadores.
- Formatos reutilizables.
- Interoperabilidad.
- Reproducibilidad.

### Distinciones que debe aprender

- Los datos no siempre explican su significado.
- Los metadatos describen datos, pero no necesariamente todos los detalles del procedimiento experimental.
- Un diccionario de datos describe variables, valores y convenciones.
- Compartir un archivo no garantiza por sí mismo su reutilización.
- Interoperabilidad y reproducibilidad son conceptos relacionados, pero no equivalentes.

No presentes el cumplimiento FAIR como algo que pueda certificarse mediante este ejercicio.

---

# 4. Principio pedagógico fundamental

**No revelar las respuestas antes del intento del participante.**

La aplicación debe seguir una progresión de descubrimiento guiado:

**Necesidad → hipótesis → exploración del vocabulario → contraste → revisión.**

Al presentar una situación:

- Mostrar únicamente la necesidad expresada en lenguaje cotidiano.
- No mostrar de inmediato el glosario.
- No ofrecer una lista inicial con todas las palabras correctas.
- No presentar términos preseleccionados.
- No decir qué conceptos son obligatorios.
- No calificar las respuestas libres mediante coincidencia de palabras.

El participante debe poder escribir sus propias propuestas antes de ver el vocabulario de referencia.

Las ayudas deben ofrecerse gradualmente.

No exigir respuestas correctas para continuar.

---

# 5. Organización de la aplicación

Implementa cinco secciones:

1. **La necesidad**
2. **Descubrir conceptos**
3. **Distinguir y preguntar**
4. **Reformular mi solicitud**
5. **Reporte**

La navegación debe ser libre.

La sección Reporte debe estar disponible siempre.

Al iniciar, el participante puede seleccionar cualquiera de los tres casos.

Conserva el caso seleccionado cuando cambie de sección.

Si cambia de caso, no pierdas las respuestas anteriores.

Las actividades deben estar asociadas con su caso correspondiente, evitando mezclar respuestas de diferentes situaciones.

No utilices puntuaciones, medallas, rankings, porcentajes de aciertos ni cronómetros competitivos.

---

# 6. Sección 1 — La necesidad

## Objetivo

Reconocer qué quiere lograr la persona, antes de utilizar vocabulario especializado.

## Interfaz

Mostrar tres tarjetas para seleccionar el caso:

- Investigación científica.
- Desarrollo de software.
- Gestión de datos científicos.

Cada tarjeta debe incluir una descripción breve y neutral.

No anticipar las respuestas técnicas.

Después de seleccionar un caso, mostrar su situación inicial.

## Primera actividad

Preguntar:

**«¿Cómo describirías esta necesidad con tus propias palabras?»**

Permitir escribir una respuesta libre.

Después preguntar:

**«¿Qué partes del problema todavía no sabes cómo nombrar o explicar?»**

Permitir registrar hasta tres dudas iniciales, sin exigir completar las tres.

Estas respuestas deben conservarse para compararlas con la reformulación final.

No mostrar todavía un glosario.

---

# 7. Sección 2 — Descubrir conceptos

## Objetivo

Explorar qué términos podrían ayudar a explicar el problema.

## Primera fase: propuesta personal

Preguntar:

**«¿Qué palabras o conceptos crees que podrían ayudarte a describir esta tarea?»**

Mostrar tres campos abiertos, con opción de añadir otros.

No presentar respuestas sugeridas automáticamente.

Permitir continuar aunque los campos estén vacíos.

## Segunda fase: exploración guiada

Después de registrar un primer intento, mostrar un botón:

**«Explorar vocabulario relacionado»**

Al activarlo, presentar tarjetas de conceptos correspondientes al caso seleccionado.

Los términos deben aparecer de manera neutral.

No identificar algunos como correctos y otros como incorrectos.

Cada tarjeta mostrará inicialmente:

- Término.
- Una pregunta orientadora breve.

No mostrar automáticamente la definición.

Cuando el participante seleccione un término, podrá indicar:

- Creo que lo comprendo.
- Tengo una idea, pero necesito aclararlo.
- No sé qué significa.

Después de esa decisión, podrá abrir una definición breve y un ejemplo contextual.

Las definiciones deben ser científicamente prudentes, claras y comprensibles para personas de distintas disciplinas.

No inventar normas, metodologías ni equivalencias.

## Reflexión

Preguntar:

**«¿Cuáles de estos conceptos te ayudarían realmente a explicar tu necesidad y por qué?»**

Permitir seleccionar varios términos, agregar una justificación o registrar un concepto adicional.

No obligar a utilizar todos los términos.

---

# 8. Sección 3 — Distinguir y preguntar

## Objetivo

Comprender diferencias entre conceptos próximos y formular preguntas cuando todavía existe incertidumbre.

## Actividad A — Distinciones

Para el caso seleccionado, presenta dos comparaciones relevantes.

Ejemplos internos:

Investigación:
- Selección de literatura y extracción de datos.
- Revisión de literatura y revisión sistemática.

Software:
- Requisitos funcionales y diseño visual.
- Prototipo y producto terminado.

Datos:
- Datos y metadatos.
- Interoperabilidad y reproducibilidad.

**No reveles directamente las diferencias al presentar las comparaciones.**

Primero pregunta:

**«¿En qué crees que se diferencian estos conceptos?»**

Permite una respuesta abierta.

Después ofrece:

- Pista 1: orienta hacia una situación concreta.
- Pista 2: ofrece una comparación más específica.
- Explicación: presenta la distinción razonada después del intento.

No evalúes respuestas abiertas mediante palabras clave.

## Actividad B — Preguntas para aprender

Preguntar:

**«¿Qué necesitarías preguntar para comprender mejor uno de estos términos?»**

Permite registrar preguntas como:

- Qué significa en este contexto.
- Cuándo se utiliza.
- Qué lo distingue de otro concepto.
- Qué ejemplo permitiría comprenderlo.
- En qué fuente podría comprobarse su definición.

Estas son categorías de orientación, no respuestas precargadas.

Solicita al participante formular al menos una pregunta con sus propias palabras.

No hagas obligatoria una fuente externa en esta etapa, pero distingue claramente entre información explicada dentro de la aplicación e información efectivamente contrastada en una fuente externa.

---

# 9. Sección 4 — Reformular mi solicitud

## Objetivo

Utilizar lo aprendido para describir mejor la tarea.

Mostrar al participante su descripción inicial.

Preguntar:

**«Ahora que exploraste algunos conceptos, ¿cómo describirías nuevamente lo que necesitas?»**

Permitir escribir una nueva versión.

Después preguntar:

**«¿Qué términos incorporaste y por qué?»**

Permitir seleccionar los conceptos utilizados y agregar una justificación.

Finalmente preguntar:

**«¿Qué términos todavía necesitas comprender o verificar antes de utilizarlos?»**

Registrar una respuesta libre.

## Comparación

Mostrar dos textos uno al lado del otro cuando haya suficiente espacio:

**Antes**

Descripción inicial.

**Después**

Descripción revisada.

No decir automáticamente que la segunda versión es mejor.

Mostrar una reflexión:

**«¿Qué cambió en la precisión de tu descripción? ¿Qué sigue siendo ambiguo?»**

No calificar la mejora.

## Transición al taller

Mostrar:

«Aprender vocabulario permite explicar mejor una necesidad, pero todavía es necesario delimitar el objetivo, la tarea, las restricciones y el resultado esperado. Ese será el siguiente paso del taller».

No convertir la descripción revisada en un prompt final automáticamente.

---

# 10. Sección 5 — Reporte

Esta sección debe seguir la convención utilizada en Explorador FAIR.

El Reporte es una síntesis del proceso realizado, no un examen.

Debe estar disponible desde el inicio.

## Contenido

Mostrar:

1. **Caso seleccionado.**
2. **Mi necesidad inicial.**
3. **Mis dudas iniciales.**
4. **Conceptos que propuse.**
5. **Vocabulario que exploré.**
6. **Conceptos que elegí y sus justificaciones.**
7. **Distinciones que intenté explicar.**
8. **Pistas consultadas y revisiones.**
9. **Preguntas que formulé para aprender.**
10. **Mi descripción inicial y mi descripción revisada.**
11. **Conceptos pendientes de verificar.**
12. **Reflexión final.**

Mostrar solamente respuestas realmente registradas.

Cuando no exista información, escribir:

**Sin respuesta**

Si se trabajaron varios casos, permitir elegir qué caso se desea consultar y descargar.

No mezclar automáticamente respuestas de distintos casos.

## Visualización: mapa de vocabulario

Incluye una representación visual sencilla que conecte:

**Mi necesidad → Conceptos seleccionados → Preguntas pendientes**

El mapa debe construirse con datos reales del participante.

Puede utilizar HTML/CSS o SVG accesible.

No generar automáticamente conexiones conceptuales no seleccionadas por la persona.

Si el participante no ha elegido conceptos, mostrar un mensaje de estado vacío.

No mostrar un mapa ficticio.

El mapa debe:

- Ayudar a revisar las decisiones.
- Tener etiquetas legibles.
- Ser accesible.
- Funcionar en pantallas pequeñas.
- Utilizar los colores del taller.
- No evaluar si los conceptos elegidos son correctos.
- Incluir una representación textual equivalente.

No conviertas el mapa en una visualización decorativa.

---

# 11. Descarga Markdown

Incluir botón:

**Descargar reporte (.md)**

Nombre del archivo:

`explorador-vocabulario-reporte.md`

El archivo debe generarse en el navegador.

Estructura sugerida:

```markdown
# Explorador de vocabulario — Reporte

**Taller:** Antes del prompt
**Caso seleccionado:** [caso]
**Fecha:** [fecha]

## 1. Mi necesidad
[respuesta]

## 2. Mis dudas iniciales
[respuestas]

## 3. Conceptos que propuse
[respuestas]

## 4. Conceptos explorados
[términos y decisiones reales]

## 5. Conceptos seleccionados
[términos y justificaciones]

## 6. Distinciones
[primeras respuestas, pistas y revisiones]

## 7. Preguntas para aprender
[respuestas]

## 8. Antes y después
**Descripción inicial:**
[respuesta]

**Descripción revisada:**
[respuesta]

## 9. Mapa de vocabulario
[representación textual de las conexiones registradas]

## 10. Aspectos pendientes
[respuesta]

## 11. Reflexión final
[respuesta]
```

El Markdown debe coincidir con la información visible en Reporte.

No generar respuestas automáticamente.

No declarar que se hicieron verificaciones externas si no ocurrió.

Permitir descargar un reporte incompleto.

---

# 12. Identidad visual

Utiliza la identidad visual inspirada en la UNAM que ya definimos para el Explorador FAIR.

## Paleta

- Azul principal: `#00314F`
- Dorado: `#C9A227`
- Blanco: `#FFFFFF`
- Gris claro: `#F3F4F6`
- Gris medio: `#64748B`
- Texto oscuro: `#1F2937`

Colores funcionales:

- Información: `#DCEAF2`
- Confirmación: `#E8F3EA`
- Precaución: `#FFF3D6`

Utiliza variables CSS en `:root`.

## Estilo

- Académico.
- Científico.
- Moderno.
- Sobrio.
- Accesible.
- Consistente con Explorador FAIR.

No utilices logos oficiales de la UNAM.

No presentes la aplicación como una herramienta institucional oficial.

Mantén tarjetas legibles, navegación clara y un diseño responsive.

---

# 13. Persistencia y estado

Utiliza `localStorage`.

Conserva por caso:

- Descripción inicial.
- Dudas iniciales.
- Términos propuestos.
- Términos explorados.
- Nivel de comprensión declarado.
- Conceptos seleccionados.
- Justificaciones.
- Respuestas sobre distinciones.
- Pistas consultadas.
- Preguntas.
- Descripción revisada.
- Pendientes.
- Reflexión.

También conserva:

- Caso activo.
- Sección activa.
- Estado de navegación.

No mezcles las respuestas entre casos.

Incluye:

**Reiniciar actividad**

Solicitar confirmación antes de borrar.

Si el participante cancela, conservar todos sus datos.

El Reporte debe actualizarse cuando cambien las respuestas.

---

# 14. Accesibilidad

Implementa:

- HTML semántico.
- Navegación mediante teclado.
- Enter y Espacio para controles interactivos.
- Foco visible.
- Etiquetas explícitas.
- Mensajes accesibles.
- `aria-live` para retroalimentación.
- Buen contraste de colores.
- Alternativas textuales a la visualización.
- Diseño responsive.
- Formularios utilizables sin mouse.

No depender exclusivamente del color para comunicar información.

---

# 15. Restricciones técnicas

Entregar:

- Un único archivo HTML autónomo.
- CSS embebido.
- JavaScript embebido.
- Sin backend.
- Sin frameworks.
- Sin React.
- Sin Node.
- Sin APIs externas.
- Sin conexión a modelos de IA.
- Sin dependencias externas obligatorias.
- Funcional offline.
- Con persistencia local.
- Con descarga Markdown.

No modificar archivos Quarto.

No realizar despliegues.

No incorporar recopilación de datos personales.

---

# 16. Verificación funcional

Antes de entregar, revisa:

1. Estado inicial vacío.
2. Navegación libre entre cinco secciones.
3. Selección de cualquiera de los tres casos.
4. Conservación de respuestas al cambiar de caso.
5. Separación correcta de datos entre casos.
6. Aparición del vocabulario únicamente después del primer intento.
7. Explicaciones disponibles después de la interacción correspondiente.
8. Pistas progresivas.
9. Posibilidad de continuar sin responder.
10. Comparación entre descripción inicial y revisada.
11. Mapa construido con conceptos realmente seleccionados.
12. Estado vacío del mapa.
13. Reporte disponible desde el inicio.
14. Descarga de reportes incompletos.
15. Coincidencia entre Reporte y Markdown.
16. Restauración después de recargar.
17. Reinicio confirmado.
18. Reinicio cancelado.
19. Uso mediante teclado.
20. Funcionamiento sin conexión.

Si no puedes ejecutar pruebas en navegador, distingue claramente entre inspección de código y pruebas realmente ejecutadas.

---

# 17. Entrega

Genera directamente el HTML completo y funcional.

Sugiere como nombre:

`explorador_vocabulario.html`

Incluye también:

1. Resumen de la arquitectura.
2. Descripción de las cinco secciones.
3. Funcionamiento del mapa de vocabulario.
4. Cómo se genera el Reporte.
5. Cómo se descarga Markdown.
6. Pruebas realizadas y pendientes.

No solicites confirmación antes de construir.

## Principio final

**La finalidad de esta herramienta no es enseñar una lista de palabras, sino ayudar a reconocer qué conceptos necesitamos comprender para describir mejor una tarea científica.**

El participante debe poder explorar, equivocarse, solicitar ayuda, revisar sus ideas y documentar su proceso sin recibir una calificación.

