Revisa la versión actual de `explorador_de_vocabulario.html`.

Quiero mejorar la continuidad pedagógica de la aplicación y hacer que las situaciones iniciales sean más concretas.

**No generes una nueva herramienta. Modifica la aplicación existente, conservando el diseño, las cinco pestañas, los tres casos, la navegación libre, la persistencia local y la descarga Markdown.**

### 1. Sustituir las necesidades iniciales

Utiliza estas tres situaciones:

**Caso A — Investigación científica**

«Tengo un archivo CSV con 200 títulos y resúmenes de artículos sobre resistencia a antibióticos en bacterias. Quiero identificar cuáles estudian mecanismos de resistencia y registrar qué mecanismo menciona cada artículo».

Conceptos centrales:
- Criterios de selección.
- Cribado de literatura.
- Extracción de información.

**Caso B — Análisis de secuencias**

«Tengo un archivo FASTA con secuencias de ADN de un genoma. Quiero una herramienta que lea el archivo, cuente cuántas A, C, G y T aparecen y me entregue una tabla con los resultados».

Conceptos centrales:
- Formato FASTA y estructura de sus registros.
- Frecuencia absoluta y frecuencia relativa.
- Entradas, salidas y criterios de aceptación de una herramienta.

Adapta los tres microdesafíos del caso a estas nociones, con situaciones expresadas en lenguaje cotidiano antes de revelar los términos.

Incluye como cuestiones para explorar el tratamiento de caracteres ambiguos y si el cálculo se realiza por registro o para todo el archivo. No anticipes respuestas ni presupongas que el archivo contiene una sola secuencia.

**Caso C — Gestión de datos científicos**

«Tengo un Excel con valores de expresión de cinco genes medidos en tres condiciones. Quiero compartirlo para que otro equipo sepa qué representa cada columna, cómo se obtuvieron los valores y qué información falta documentar».

Conceptos centrales:
- Metadatos.
- Diccionario de datos.
- Procedencia.

Este ejemplo es didáctico. No afirmes que existe información experimental que no esté proporcionada.

### 2. Mejorar la primera pestaña

En lugar de pedir simplemente que la persona repita la necesidad inicial, pregunta:

- ¿Qué resultado concreto necesitas obtener?
- ¿Qué detalles tendrías que aclarar para que otra persona pueda realizar la tarea?

Conserva ambas respuestas como punto de partida.

### 3. Conectar las pestañas 2, 3 y 4

La pestaña «Reformular mi solicitud» debe recuperar automáticamente el trabajo previo del caso activo.

Mostrar tres áreas claramente diferenciadas:

**A. Mi solicitud inicial**
- Situación del caso.
- Resultado concreto que registró el participante.
- Detalles que identificó como pendientes.

**B. Lo que aprendí**
- Conceptos marcados como «Sí, lo necesito».
- Conceptos marcados como «Tal vez», distinguiéndolos de los anteriores.
- Revisiones registradas en los microdesafíos.
- Distinciones conceptuales trabajadas en la pestaña 3.
- Pregunta formulada para aprender.

No presentar como hechos aprendidos las explicaciones que la persona todavía no consultó.

**C. Mi solicitud reformulada**
- Campo editable para redactar una nueva versión.
- Pregunta: «¿Qué cambió y qué sigue siendo ambiguo?».
- Campo para registrar información que todavía necesita verificarse.

La aplicación puede mostrar los conceptos como apoyo para la escritura, pero NO debe generar automáticamente una solicitud completa ni inventar decisiones del participante.

### 4. Fortalecer la continuidad

Cada microdesafío de vocabulario debe estar directamente relacionado con la necesidad concreta del caso.

Las comparaciones de la pestaña 3 deben apoyar decisiones relevantes para reformular esa misma necesidad.

Evita actividades aisladas o definiciones que no tengan una aplicación clara.

### 5. Actualizar el Reporte

El Reporte visible y el Markdown deben incluir:

- Situación original del caso.
- Resultado esperado según el participante.
- Detalles pendientes identificados.
- Términos descubiertos y seleccionados.
- Revisiones de los microdesafíos.
- Distinciones exploradas, pistas consultadas y explicaciones abiertas.
- Pregunta formulada para aprender.
- Solicitud reformulada.
- Reflexión sobre qué cambió.
- Ambigüedades y verificaciones pendientes.

No inventes respuestas ni declares verificaciones que no ocurrieron.

El mapa debe utilizar únicamente las decisiones reales.

### 6. Requisitos

- Mantener funcionamiento offline con HTML, CSS y JavaScript embebidos.
- Mantener datos separados por caso.
- Mantener navegación libre.
- Mantener accesibilidad por teclado.
- No utilizar calificaciones.
- No generar automáticamente respuestas técnicas.
- No modificar Quarto.
- No publicar.

Revisa también que los cambios de estructura del estado no rompan la restauración de datos anteriores: usa normalización o una clave de versión nueva si es necesario.

Entrega el HTML completo actualizado y un resumen de lo modificado. Distingue las pruebas realmente ejecutadas de las pendientes.


