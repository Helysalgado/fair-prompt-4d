# Diseño pedagógico v2.0

**Antes del prompt: pensar, delegar y verificar con IA en la investigación científica**

| Campo | Valor |
|---|---|
| Estado | Segunda revisión pedagógica incorporada. Base aceptada. No autoriza cambios en el sitio ni la especificación funcional del Explorador. |
| Versión de partida | v1.4, publicada en <https://helysalgado.github.io/fair-prompt-4d/> |
| Rama de trabajo | `feat/taller-interactivo-v2` (mismo commit que `main` al redactar este documento: `24cb967`) |
| Qué es este archivo | Referencia para futuras páginas Quarto y para el diseño de herramientas interactivas |
| Qué no es | Una metodología validada, un informe de piloto ni una instrucción de implementación |

En este documento, **comprobado en v1.4** significa que el contenido está en los archivos actuales del repositorio. **Propuesta v2** significa una decisión de diseño nueva, sujeta a revisión, que todavía no está implementada.

No se ha documentado un piloto con participantes. La v1.4 lo dice en `contenido/08-referencias.qmd` y en el README. Este diseño no debe presentarse como si esa prueba ya hubiera ocurrido.

---

## 1. Propósito y público

### Propósito

El taller ayuda a una investigadora o un investigador a pasar de una necesidad científica, a veces expresada con palabras imprecisas, a un encargo que pueda revisar: qué se pidió, qué respondió la IA, qué está en los datos, qué es una inferencia y qué sigue pendiente.

La v2 conserva ese propósito, ya formulado en `contenido/01-contexto.qmd`, y cambia la experiencia: la ruta principal deja de sentirse como una lectura lineal de seis etapas y pasa a ser una secuencia de cinco desafíos sobre un mismo caso.

### Público

**Comprobado en v1.4.** El taller está pensado para dos situaciones que comparten preguntas, descritas en `contenido/01-contexto.qmd`: quien prepara un dataset para publicarlo y quien mantiene una base de datos. No exige programación. La sesión dura 120 minutos, presencial o híbrida, y forma parte del programa ELIXIR-México 2026.

**Propuesta v2.** El público se precisa así: personas que conocen su problema científico y, en algunas tareas, necesitan vocabulario de otra disciplina. Ese vocabulario puede ser de síntesis de literatura, programación, análisis de datos, formatos, metadatos o estándares. La IA puede servir para descubrir términos, comparar alternativas y entender una decisión antes de pedir una solución definitiva.

El caso común sigue siendo el Excel simulado de expresión génica. Quien participa no necesita ser especialista en FAIR ni en expresión génica para empezar. Sí necesita poder abrir el archivo, mantener un chat y distinguir lo que ve de lo que el archivo no dice.

### Qué debe poder hacer alguien al terminar

Conservar el éxito descrito en v1.4: una persona que comprende mejor el encargo y puede justificar su plan y los límites de lo que produjo la IA. El producto sigue siendo un diagnóstico documental preliminar, con preguntas pendientes y una bitácora. Queda fuera certificar FAIR o depositar el dataset.

---

## 2. Alcance y límites de la propuesta

### Dentro de estas dos horas

**Comprobado en v1.4** (`contenido/01-contexto.qmd`, `contenido/04-caso-fair.qmd`, `contenido/05-practica.qmd`):

- Partir de una necesidad ambigua y de un archivo pequeño.
- Descubrir vocabulario que falta y contrastarlo.
- Delimitar un diagnóstico: unidades, condiciones, réplicas y celda vacía.
- Decidir qué se delega a la IA y qué confirma la persona investigadora.
- Etiquetar afirmaciones como observadas, inferidas, por confirmar o comprobadas en una fuente.
- Documentar el proceso en la bitácora.
- Usar cuatro prompts en un mismo chat: P0, P1, P5 y P6. Las decisiones de especificación y de delegación las toma la persona. En la numeración de la v1.4, P2–P4 no son prompts.

**Propuesta v2, además:**

- Tratar las seis etapas como recomendaciones flexibles.
- Practicar cuándo conviene no usar IA, usar otra herramienta o combinarlas.
- Ajustar la profundidad de la verificación a la consecuencia de la tarea.
- Reconocer cuándo seguir reformulando un prompt ya no mejora el problema.
- Recorrer el caso con cinco desafíos, como ruta principal, y dejar las páginas de fundamentos como consulta.
- Ver tres ejemplos breves de vocabulario: resumir literatura, desarrollar software y preparar datos. Esos ejemplos no son un segundo caso completo.
- Completar en la sesión una bitácora mínima. La plantilla extensa de la v1.4 queda como recurso complementario.

### Fuera de estas dos horas

Queda fuera, como ya establece la v1.4:

- Un curso de ingeniería de prompts, de fundamentos de modelos de lenguaje o de programación.
- Certificar conformidad FAIR, diseñar un esquema de metadatos completo o depositar datos.
- Resolver identificadores génicos, cepa, procesamiento y responsabilidad del experimento. En v1.4 esos puntos se excluyen de P5 por tiempo y se anotan como exclusiones.
- Convertir la comparación de dos chats en una prueba de causalidad. `contenido/05-practica.qmd` ya advierte que un segundo chat, si sobra tiempo, es una demostración informal.

**Propuesta v2.** También queda fuera presentar las seis recomendaciones, los cinco desafíos o las herramientas como un método validado, una secuencia obligatoria o un requisito para toda tarea. Hay consultas triviales que no justifican las seis recomendaciones ni el uso de IA.

### Datos y responsabilidad

**Comprobado en v1.4.**

- Los datos de `descargas/expresion_genica_caso_simulado.xlsx` y de `descargas/expresion_genica_caso_simulado.txt` son ficticios.
- El archivo tiene dos hojas, `Expresion_genica` y `Notas_experimento`.
- La hoja de datos tiene cinco filas (`recA`, `rpoS`, `b0014`, `katG`, `dnaK`), las columnas `Gen`, `Control`, `Estrés A (prom.)` y `Estrés B`, y una celda vacía en `Estrés B` para `b0014`.
- Las notas dicen, entre otras cosas: datos del experimento de marzo, *E. coli* sin cepa confirmada, valores procesados, réplicas sin registro y responsable por confirmar.
- No se suben datos reales ni confidenciales (`contenido/00-preparacion.qmd`).
- La autorrevisión de la IA (P6) no sustituye abrir una fuente. Si la fuente no se abrió, el registro dice «pendiente» o «verificación externa pendiente», nunca «verificado».

---

## 3. Principios pedagógicos

Los principios 1 a 7 y 9 ya están, con otra redacción, en las páginas de la v1.4. El principio 8 y la formulación explícita del 10 como límite de toda la v2 son propuestas de esta versión. Ninguno autoriza a llamar al conjunto una metodología validada.

1. **Partir de lo que la persona ya sabe y de lo que necesita.** El problema científico es suyo. El taller no empieza por la herramienta ni por una plantilla de prompt. En el caso, la persona observa las dos hojas y formula preguntas antes de recibir la explicación de lo que falta.
2. **Aceptar instrucciones imperfectas o poco técnicas.** P0 es una solicitud abierta y razonable. Sirve para ver qué decide la IA cuando el encargo todavía es amplio.
3. **Usar la IA para explorar vocabulario, alternativas y decisiones** antes de pedir el producto definitivo. P1 pide conceptos y preguntas, no un archivo listo para publicar.
4. **Definir mejor la tarea y los criterios de aceptación.** La especificación la escribe la persona: resultado, alcance, evidencia aceptable y límites. En v1.4 eso ocurre antes de P5.
5. **Decidir qué delegar, qué información puede compartirse y cuándo usar otra herramienta.** Delegar incluye elegir el canal, los datos que sí pueden subirse y el momento en que conviene un artículo, una hoja de cálculo, un script, una persona experta o ninguna IA.
6. **Contrastar resultados con los datos y con las fuentes que correspondan.** Cada afirmación se separa en observación, inferencia, información pendiente o recomendación que depende de una fuente externa.
7. **Ajustar la verificación a la importancia y a las consecuencias.** La v1.4 ya dice que el recorrido completo se usa cuando la decisión tiene consecuencias y se comprime cuando la consulta es trivial. Publicar, compartir o interpretar datos exige más contraste que una pregunta exploratoria.
8. **Reconocer cuándo dejar de iterar el prompt.** Si las respuestas siguen inventando metadatos, confundiendo el objetivo o puliendo una tabla sin nueva evidencia, el siguiente paso es replantear el problema, los datos o la herramienta. Una instrucción más detallada puede hacer la respuesta más fácil de revisar. La v1.4 ya dice que eso no la hace más verdadera.
9. **Documentar decisiones y verificaciones cuando corresponda.** Durante las dos horas basta una bitácora mínima: necesidad, tres incertidumbres, especificación, una verificación real y siguiente acción. La plantilla extensa de la v1.4 queda como recurso complementario. No toda consulta mínima exige esa plantilla completa.
10. **Hablar de recomendaciones, no de un método formal validado.** `contenido/03-metodo.qmd` atribuye la secuencia a una síntesis didáctica del equipo, apoyada en fuentes que respaldan componentes, no la eficacia de la secuencia completa. La v2 mantiene ese límite en la portada, en la práctica y en cualquier herramienta.

---

## 4. Las seis recomendaciones flexibles

**Comprobado en v1.4.** `contenido/03-metodo.qmd` presenta seis etapas iterativas. No son un flujo lineal obligatorio: un resultado incorrecto puede devolver a la persona al vocabulario, a la especificación o al problema. Los nombres cortos son Necesidad, Vocabulario, Especificación, Colaboración, Verificación y Registro. La anatomía del prompt es el puente entre la especificación y la colaboración, no una séptima etapa (`contenido/03b-estructura-prompt.qmd`).

**Propuesta v2.** En la interfaz y en la facilitación se llaman **recomendaciones**. Se usan las que hagan falta. Se pueden repetir, comprimir u omitir. El diagrama `recursos/metodologia-seis-etapas.svg` puede seguir como mapa, con un texto que diga que es una ayuda para decidir, no una secuencia exigible.

| Recomendación | Pregunta de la persona | Qué se conserva de v1.4 | Qué añade la v2 |
|---|---|---|---|
| 1. Decir lo que se tiene y lo que se necesita | ¿Qué quiero lograr, con qué información y con qué palabras tengo ahora? | Etapa 1, Necesidad. P0 como encargo imperfecto. | El punto de partida puede ser poco técnico. No hace falta nombrar el estándar antes de explorar. |
| 2. Aprender el vocabulario que la tarea exige | ¿Qué términos, estándares o alternativas necesito entender antes de decidir? | Etapa 2, Vocabulario. P1: cinco conceptos y cinco preguntas, sin inventar lo que el archivo no dice. | El vocabulario puede venir de otra disciplina. La IA propone candidatos; la persona y las fuentes confirman cuáles sirven. |
| 3. Delimitar la tarea y el criterio de aceptación | ¿Qué entradas, alcance, entregable y prueba de «suficientemente bien» necesito? | Etapa 3. La persona escribe la especificación en la bitácora antes de P5. P5 limita el diagnóstico común a cuatro asuntos. | La especificación propia nace de las incertidumbres de la persona. Los cuatro asuntos no se adelantan como pauta inicial. El criterio de aceptación incluye cuándo parar. |
| 4. Decidir la colaboración | ¿Qué delego, qué conservo, qué puedo compartir y qué herramienta uso? | Etapa 4 y competencias 4D. Rol del prompt opcional. Un solo chat para P0, P1, P5 y P6. | Entra de forma explícita la opción de no usar IA o de usar otra herramienta. |
| 5. Contrastar con una profundidad proporcional | ¿Qué evidencia permite aceptar, corregir o dejar pendiente este resultado? | Etapa 5. P5, P6 y la verificación humana de Wilkinson et al. (2016). Cuatro etiquetas en `recursos/escala-evidencia.svg`. | La profundidad depende de la consecuencia. Iterar el mismo prompt no sustituye cambiar de pregunta. |
| 6. Dejar constancia cuando haga falta | ¿Qué decisión, fuente o pendiente debe poder reconstruir otra persona? | Etapa 6. Bitácora extensa y revisión por pares. | En la sesión se completa la bitácora mínima. La plantilla de v1.4 permanece disponible para quien quiera continuar después. |

### Recomendación transversal, no una séptima

**Propuesta v2.** En cualquier momento se puede decir: «este prompt ya no es el problema». Señales para replantear, en vez de pedir otra variante:

- La IA rellena unidades, tratamientos, réplicas, cepa o el sentido de «prom.» después de que se le pidió no hacerlo.
- La respuesta mejora el formato y no la evidencia.
- El objetivo sigue siendo «hacer FAIR» o «dejarlo listo para publicar» cuando la tarea acordada era diagnosticar ausencias.
- La persona no puede señalar en qué celda, nota o párrafo se apoya una frase que piensa aceptar.

Esas señales se enseñan con el caso. No se presentan como una lista diagnóstica validada.

---

## 5. Resultados de aprendizaje

Al finalizar los 120 minutos, quien participa puede hacer lo siguiente. Los resultados 1 a 6 reformulan la lista de `contenido/01-contexto.qmd`. Los resultados 7 y 8 son extensión de la v2.

1. Expresar la necesidad con sus palabras y señalar ambigüedades y supuestos, aunque el primer encargo sea impreciso.
2. Reconocer vocabulario que le falta —de su campo o de otro— y usar la IA para proponer términos, alternativas y preguntas, contrastados después con una fuente o con el archivo.
3. Delimitar objetivo, información disponible, restricciones, entregable y criterios de aceptación.
4. Decidir qué delega a la IA, qué decisión científica conserva, qué información puede compartir y cuándo conviene otra herramienta o ninguna.
5. Separar en un resultado lo observado, lo inferido, lo pendiente y lo que solo una fuente externa podría sostener. Corregir «no existe» cuando lo defendible es «no está documentado».
6. Dejar, en la bitácora mínima, la necesidad, tres incertidumbres, la especificación, una verificación hecha por la persona y la siguiente acción. Con esos cinco campos, otra persona puede reconstruir el recorrido de la sesión.
7. Elegir una verificación más breve o más exigente según la consecuencia de la tarea, y decir por qué.
8. Detener una cadena de reformulaciones y volver al problema, a los datos o a la herramienta cuando el prompt deja de ser el cuello de botella.

**Criterio de éxito del taller**, heredado de v1.4: justificar el plan y los límites del producto de la IA. Un diagnóstico con celdas citadas y huecos explícitos cumple mejor el objetivo que una tabla completa de metadatos inventados.

---

## 6. Narrativa de los cinco desafíos

**Decisión propuesta en esta segunda revisión.** Los cinco desafíos constituyen la ruta principal. Las páginas de fundamentos quedan como material de consulta: se abren cuando hace falta un concepto, un ejemplo o la procedencia de las recomendaciones. No se leen en bloque antes de mirar el archivo.

La ruta principal es una historia con el Excel simulado. Cada desafío tiene una pregunta que la persona debe poder responder en voz alta. Las seis recomendaciones se usan por dentro. Los tiempos y la prioridad de cada pieza están en la sección 9.

### Desafío 1. ¿Qué tengo y qué necesito?

La investigadora del caso tiene una tabla pequeña y una petición amplia: preparar los datos «siguiendo FAIR» para un artículo. Quien participa todavía no recibe una explicación de lo que falta.

Entra la recomendación 1, en este orden:

1. En el Explorador, observa la hoja `Expresion_genica` y después la hoja `Notas_experimento`.
2. Formula preguntas y anota incertidumbres con sus propias palabras.
3. Solo después envía P0, conservado literalmente desde `contenido/_prompts/p0.md`, en un chat nuevo, con el Excel adjunto:

> Tengo este Excel de expresión génica de cinco filas y tres condiciones. Voy a publicar un artículo y me piden que los datos sigan los principios FAIR. ¿Me ayudas a prepararlo?

La pausa de la v1.4 se mantiene después de P0: anotar si la IA preguntó, explicó, ofreció archivos o atribuyó un significado experimental que el Excel no muestra.

Los cuatro asuntos del diagnóstico —unidades, condiciones, réplicas y celda vacía— son un criterio interno para diseñar y facilitar el recorrido. Sirven para comprobar, después, si las estaciones permiten descubrirlos. No se muestran como lista de respuestas al abrir el Explorador ni al empezar este desafío. `contenido/04-caso-fair.qmd` y `recursos/datos-y-metadatos.svg` ya explican esas ausencias: quedan como consulta posterior a la exploración.

**Producto.** La necesidad, en lenguaje propio, y tres incertidumbres. Esos dos campos abren la bitácora mínima.

### Desafío 2. Sé lo que quiero, pero ¿cómo se llama?

La persona llega con las preguntas que ella formuló. Puede conocer el problema científico y, aun así, faltarle el nombre técnico de lo que ve: un tipo de revisión, una prueba de software, un metadato, un identificador o un valor ausente.

Entra la recomendación 2. La microactividad de vocabulario usa tres ejemplos breves —resumen de literatura, desarrollo de software y preparación de datos— para mostrar ese desfase. No son prácticas completas. En el ejemplo de los datos, los términos se anclan al Excel. P1 se conserva literalmente, en el mismo chat, desde `contenido/_prompts/p1.md`: cinco conceptos prioritarios, cinco preguntas críticas, distinción entre lo observado, lo que falta confirmar y lo que exige consulta externa, sin inventar unidades, tratamiento, cepa, método, replicación ni el significado de «prom.».

La puesta en común de la v1.4 sigue siendo útil: asistentes distintos harán cosas distintas. Eso ilustra variación, no un experimento.

**Producto.** Cinco términos que la persona puede explicar con el archivo, y cinco preguntas para quien hizo el experimento. Los términos que no pueda anclar a una celda, una nota o una fuente quedan marcados como candidatos, no como vocabulario aprendido.

### Desafío 3. ¿Qué le voy a pedir a la IA?

Aquí la persona pasa de las preguntas a un encargo propio. Entran las recomendaciones 3 y 4, y la anatomía ya enseñada en `contenido/03b-estructura-prompt.qmd`: rol opcional, contexto, objetivo, tarea, salida, restricciones y verificación. El Constructor de prompts ayuda a redactar esa especificación y ese prompt para aprender a formular instrucciones. No envía el texto a un modelo ni lo trata como la respuesta correcta.

Ese prompt propio no entra en el chat común. El grupo sigue la secuencia P0, P1, P5 y P6. El diagnóstico compartido se hace con P5, tal como está en `contenido/_prompts/p5.md`, para que las respuestas se puedan comparar. P5 nombra los cuatro asuntos; esa lista aparece en este momento del taller, como encargo común, no como pista inicial del Explorador.

Antes de redactar, dos microactividades cortas:

- Situaciones de `contenido/02-ejemplos.qmd` relacionadas con Delegation, Description, Discernment y Diligence.
- Una decisión explícita: IA, otra herramienta o una combinación. En este caso, la hoja de cálculo y la fuente primaria no se sustituyen por el chat. El chat puede inventariar y ordenar; no puede recuperar el protocolo que no está en el archivo.

La especificación se escribe en la bitácora mínima antes de P5. Sale de las tres incertidumbres de la persona y de los componentes que ella elija. No tiene que coincidir con los cuatro asuntos: ese alcance es el de P5, el encargo común posterior.

Quien facilita sí conoce el alcance de P5 y la plantilla extensa de `contenido/07-bitacora.qmd`: diagnóstico documental; evidencia localizable en celda, nota o fuente; la IA inventaría y ordena; la persona confirma el experimento; no se rellenan vacíos ni se inventan metadatos. Esa orientación no se proyecta como formulario al inicio del Explorador.

**Producto.** Una especificación propia y un prompt delimitado, con objetivo, tarea, salida, al menos una restricción y un criterio de verificación. El rol se justifica solo si se usa. El prompt queda escrito para aprender a formular. El diagnóstico del grupo se ejecuta después con P5.

### Desafío 4. La IA respondió. ¿Qué puedo aceptar?

Entran la recomendación 5 y la transversal de saber parar. P5 y P6 se conservan literales, en el mismo chat, desde `contenido/_prompts/p5.md` y `contenido/_prompts/p6.md`.

P5 pide el diagnóstico de cuatro asuntos, con ubicación en hoja o celda, sin completar datos ni declarar cumplimiento FAIR. P6 pide clasificar cada afirmación y no declarar como verificada una fuente que solo se mencionó.

El Auditor de afirmaciones y evidencia pide a la persona colocar cada frase en una etiqueta:

- **Observado:** está en el archivo y se puede señalar.
- **Inferido:** es plausible y el archivo no lo dice.
- **Por confirmar:** solo puede responderlo quien generó los datos.
- **Verificación externa:** hace falta una fuente primaria. Pasa a «verificado» solo si la persona abrió la fuente, localizó el pasaje y anotó la fecha.

La actividad obligatoria de `contenido/06-verificacion.qmd` se mantiene. La afirmación es: «FAIR exige que todos los datos sean completamente abiertos». La fuente primaria es Wilkinson et al. (2016), <https://doi.org/10.1038/sdata.2016.18>, en particular el principio Accessible (Box 2: A1.1, A1.2 y A2). Mons et al. (2017) puede aclarar FAIR y apertura, como ya indica esa página. Si la fuente no se abre, se escribe «pendiente».

Si el tiempo se acaba, se prioriza esta verificación sobre leer completa la respuesta de P6, igual que en v1.4.

El ejercicio opcional de la cita del 80 %, ligado al ejemplo 2, queda como ampliación, no como requisito de los 120 minutos.

**Producto.** Un diagnóstico de cuatro asuntos con etiquetas, más una comprobación de la afirmación sobre apertura: respalda, contradice o no permite decidir, con pasaje y fecha, o bien «verificación externa pendiente».

### Desafío 5. ¿Qué decidí y qué queda pendiente?

Entra la recomendación 6. Durante la sesión se completa la bitácora mínima, no todas las secciones de la plantilla extensa. Los cinco campos deben permitir que otra persona reconstruya qué se necesitaba, qué no estaba claro, qué se encargó, qué se contrastó en una fuente y qué sigue abierto. La revisión por pares de la v1.4 se conserva como actividad ajustable: una observación concreta y una pregunta, no un dictamen. Si el reloj aprieta, se protege la verificación externa y la bitácora mínima antes que el intercambio.

El cierre pide una frase de transferencia a un problema propio, sin resolverlo. Los ejemplos de literatura, software y datos ya se habrán visto, en corto, en la microactividad de vocabulario. No se repiten aquí como segunda práctica.

**Producto.** Bitácora mínima completa. La frase de transferencia es deseable y puede ceder su minuto a la verificación.

### Lo que la narrativa no debe hacer

- Obligar a pasar por los cinco desafíos en tareas ajenas al taller.
- Presentar P0 como un error y el prompt delimitado como la verdad.
- Usar el Explorador, el Constructor o el Auditor como si sus salidas estuvieran verificadas.
- Resolver `b0014`, «prom.», la cepa o la celda vacía dentro de la herramienta.

---

## 7. Actividades interactivas y productos esperados

Hay tres laboratorios y tres microactividades. **Propuesta v2:** la primera herramienta que se implementa es el Explorador del dataset. Los otros dos laboratorios quedan especificados para poder diseñarlos después. Hasta que existan, la sesión puede hacerse con las páginas y los diagramas actuales.

El Explorador se inspirará en una aplicación HTML llamada GFF3 Explorer. La segunda revisión fija el patrón que se quiere tomar: estaciones, selección de elementos, retroalimentación contextual y reporte Markdown. Esa referencia se proporcionará por separado. No está en este repositorio, y este documento no afirma haber inspeccionado su código.

Ninguna herramienta se implementa con este documento.

### Laboratorio 1. Explorador del dataset FAIR

**Función.** Hacer que la persona observe el Excel simulado y formule sus propias incertidumbres antes de recibir una explicación.

**Recorrido previsto**

1. **Estación de la hoja de datos.** Muestra `Expresion_genica`, con sus encabezados y celdas, sin un texto que anticipe qué falta.
2. **Estación de las notas.** Muestra `Notas_experimento` del mismo modo.
3. **Estación de preguntas.** La persona escribe qué ve, qué pregunta y qué no puede decidir todavía.
4. **Retroalimentación contextual.** Aparece después de una selección o de una pregunta, referida a ese elemento. Puede ayudar a precisar la pregunta. No abre con la solución del caso.
5. **Reporte Markdown.** Reúne lo observado, las preguntas y las incertidumbres para copiarlas a la bitácora mínima.

**Debe permitir**

- Recorrer las dos hojas por estaciones y seleccionar celdas, encabezados o campos de notas.
- Escribir preguntas e incertidumbres antes de cualquier explicación del caso.
- Recibir retroalimentación ligada a lo que la persona seleccionó, no un informe inicial.
- Copiar un reporte Markdown.

**Criterio interno de diseño.** Unidades, condiciones, réplicas y celda vacía sirven al equipo para revisar si el recorrido hace posible descubrirlos. No son etiquetas, metas ni respuestas de la primera pantalla. Quien facilita las usa después, al escuchar las preguntas del grupo. No las proyecta al inicio.

**No debe**

- Mostrar al inicio los cuatro asuntos, la tabla «qué observar» de `contenido/04-caso-fair.qmd` ni el contraste ya resuelto de `recursos/datos-y-metadatos.svg`.
- Rellenar la celda vacía, ni con cero ni con un valor imputado.
- Traducir «prom.», asignar unidades o resolver `b0014` a otro símbolo.
- Convertir una incertidumbre en un hecho dentro de la retroalimentación.
- Mostrar un puntaje FAIR, un sello de cumplimiento o un botón de «arreglar datos».
- Aceptar otro archivo en la primera versión. El caso común es el Excel ya publicado en `descargas/`. Esta restricción sigue siendo una propuesta hasta la especificación funcional.

**Producto de quien participa.** Preguntas e incertidumbres propias. Alimentan la necesidad y las tres incertidumbres de la bitácora mínima. El diagnóstico de cuatro asuntos llega más tarde, con P5.

**Material de partida ya existente:** `descargas/expresion_genica_caso_simulado.xlsx`, `descargas/expresion_genica_caso_simulado.txt`, `recursos/vista-excel.svg`. `contenido/04-caso-fair.qmd` y `recursos/datos-y-metadatos.svg` se consultan después de explorar, porque ya explican las ausencias.

### Laboratorio 2. Constructor de prompts

**Función.** Ayudar a escribir una especificación y un prompt propios, para aprender a formular instrucciones con los siete componentes de `contenido/03b-estructura-prompt.qmd`. El grupo no usa ese prompt para el diagnóstico. El diagnóstico común se hace con P5.

**Debe permitir**

- Redactar objetivo, contexto, tarea, salida, restricciones y verificación.
- Dejar el rol vacío y pedir una justificación solo si se completa.
- Mostrar, como referencia de solo lectura, P0 y la versión delimitada que ya está en `03b-estructura-prompt.qmd`.
- Copiar el texto. El botón de `_prompt-copy.html` ya hace eso en las páginas; el laboratorio puede ofrecer lo mismo.

**No debe**

- Enviar el prompt a un modelo ni puntuarlo.
- Presentar la versión delimitada como respuesta correcta al problema FAIR.
- Añadir componentes obligatorios más allá de los siete, ni convertirlos en una etapa nueva.
- Enviar el prompt propio al chat común, ni sustituir con él el texto canónico de P5. El grupo ejecuta P5 tal como está en `contenido/_prompts/p5.md`.

**Producto.** La especificación y el prompt propio del desafío 3, más una frase sobre qué responsabilidad de verificación queda fuera del texto. P5 sigue siendo el encargo con el que todo el grupo pide el diagnóstico.

### Laboratorio 3. Auditor de afirmaciones y evidencia

**Función.** Obligar a clasificar frases antes de aceptarlas.

**Debe permitir**

- Tomar afirmaciones del diagnóstico (las que devuelva P5 en la sesión, o un conjunto fijo de ejemplo si la IA no respondió).
- Asignar una etiqueta: observado, inferido, por confirmar, verificación externa.
- Exigir una localización para «observado»: hoja y celda o campo de notas.
- Exigir fuente, pasaje y fecha para pasar de «verificación externa» a «verificado».
- Dejar «pendiente» como estado válido y visible.
- Incluir la afirmación sobre apertura total de FAIR y el enlace DOI de Wilkinson et al. (2016).

**No debe**

- Consultar la fuente por la persona ni marcar «verificado» automáticamente.
- Corregir en silencio «no existe» por «no está documentado»: puede preguntar si esa corrección hace falta.
- Calificar el desempeño con una nota.

**Producto.** El conjunto etiquetado del desafío 4. A la bitácora mínima pasa una verificación real. El resto puede copiarse a las secciones 5 y 5b de la plantilla extensa si la persona continúa después de la sesión.

**Material de partida:** `contenido/06-verificacion.qmd`, `recursos/revisar-vs-verificar.svg`, `recursos/escala-evidencia.svg`, P6.

### Microactividad A. Descubrir y relacionar vocabulario técnico

Dentro del desafío 2, antes de dar por aprendida la respuesta a P1. Es ajustable en duración. Si la verificación externa necesita tiempo, se conserva un ejemplo y el regreso al Excel.

El propósito es uno: una persona puede conocer bien su problema científico y, aun así, necesitar conceptos técnicos de otra práctica para definir la tarea. La IA puede ayudar a descubrir esos nombres. Confirmarlos sigue siendo trabajo de la persona, con el archivo o con una fuente. Los tres ejemplos se miran en pocos minutos. No se convierten en prácticas completas ni en un segundo caso.

| Ejemplo | Lo que la persona ya sabe | El concepto que puede faltarle | Qué no se hace en la sesión |
|---|---|---|---|
| Resumir literatura | La pregunta del campo y los textos que le importan | Distinguir una búsqueda, un tipo de revisión y una cita que realmente sostiene la frase. El ejemplo 2 de `contenido/02-ejemplos.qmd` muestra ese último riesgo. | No se revisa un corpus ni se escribe un resumen. |
| Desarrollar software | El análisis o el procedimiento que quiere obtener | Nombrar entrada, prueba, dependencia o formato. Un programa que corre todavía no demuestra que el criterio científico sea el adecuado. | No se escribe ni se ejecuta código. |
| Preparar datos | Que debe dejar utilizable una tabla de expresión | Metadato, identificador, réplica, valor ausente, procedencia. Aquí los términos vuelven a las dos hojas del Excel. | No se completa ni se deposita el archivo. |

Después del tercer ejemplo, cada persona toma términos de la tabla y los relaciona con una evidencia del archivo, con una pregunta al responsable o con «no sé todavía». Cuando llegue la respuesta a P1, repite el mismo gesto con esos cinco conceptos. Un término sin ancla no se da por aprendido.

Puede hacerse en parejas. No requiere HTML en la primera entrega.

**Producto.** La lista de cinco conceptos de P1, cada uno con un ancla o con la marca «candidato».

### Microactividad B. Relacionar situaciones con competencias 4D

Unos 4 minutos, al entrar al desafío 3. Se usan los tres ejemplos ya escritos en `contenido/02-ejemplos.qmd`:

1. Respuesta válida a un encargo ambiguo («combinar» tablas: concatenar, unir por clave o armonizar). Diagrama: `recursos/combinar-tablas.svg`.
2. La referencia existe, pero no demuestra lo que se le atribuye.
3. La IA inventa metadatos experimentales.

Quien participa indica qué competencia se pone a prueba de forma más visible en cada ejemplo: Delegation, Description, Discernment o Diligence. Puede haber más de una. La puesta en común busca la justificación, no una clave única. El propio `contenido/03-metodo.qmd` advierte que las competencias no corresponden una a una con las etapas.

**Producto.** Tres justificaciones breves, orales o en una línea de la bitácora.

### Microactividad C. Decidir cuándo usar IA, otra herramienta o una combinación

Unos 4 minutos, en el desafío 3, antes de escribir la especificación.

Tres situaciones del mismo caso, en este orden de decisión:

| Situación | Decisión que se espera argumentar |
|---|---|
| Contar las hojas y leer un encabezado | Puede hacerlo la persona en el Explorador o en la hoja de cálculo. La IA es opcional. |
| Proponer qué significan «prom.», la celda vacía y «valores procesados» | La IA puede listar hipótesis. Aceptar una hipótesis exige el archivo y, si hace falta, a quien hizo el experimento. |
| Afirmar qué exige el principio Accessible | La fuente primaria es la herramienta decisiva. La IA, como mucho, sugiere dónde mirar. |

**Producto.** Una línea en la especificación: qué parte hará la IA, qué parte hará la persona con el archivo y qué parte queda en una fuente o en el responsable experimental.

### Bitácora mínima y plantilla extensa

**Propuesta v2.** En las dos horas se completa una bitácora mínima. No existe todavía un archivo con ese formulario: habrá que crearlo cuando se autorice la implementación. La plantilla extensa ya está escrita y se conserva.

| | Bitácora mínima | Plantilla extensa de la v1.4 |
|---|---|---|
| Para qué | Reconstruir la sesión en el tiempo disponible | Continuar después, o facilitar con el detalle completo |
| Dónde está hoy | Propuesta. Sin archivo propio | `contenido/07-bitacora.qmd`, `descargas/bitacora-plantilla.md`, `descargas/bitacora-plantilla.docx` |
| Qué pide | Necesidad; tres incertidumbres; especificación; una verificación real; siguiente acción | Datos generales, secciones 1 a 6, 5b, transferencia y declaración de uso de IA |

La verificación real de la bitácora mínima es la de Wilkinson et al. (2016), o la marca «pendiente» si la fuente no se abrió. Las tres incertidumbres salen de la exploración, antes de la explicación. La especificación es la del prompt propio y se escribe antes de ejecutar P5. La siguiente acción dice quién debe resolver lo que quedó abierto.

Quien desee el detalle de P0, P1, las cuatro competencias, todas las etiquetas del diagnóstico y la declaración de uso de IA lo encuentra en la plantilla extensa. Completarla durante la sesión es opcional.

### Orden de construcción

1. Explorador del dataset, primera herramienta HTML.
2. Auditor de afirmaciones, porque sostiene la verificación obligatoria.
3. Constructor de prompts, porque la v1.4 ya puede realizarse con la página `03b` y la bitácora mientras el constructor no exista.

Ese orden es una propuesta de implementación, no una jerarquía pedagógica. En la sesión, el orden de uso sigue siendo desafío 1, 2, 3, 4 y 5.

---

## 8. Integración del marco AI Fluency 4D

**Comprobado en v1.4.** El marco se presenta en `contenido/03-metodo.qmd` como AI Fluency de Rick Dakan y Joseph Feller, en colaboración con Anthropic. Se conservan los nombres en inglés. El taller aplica el marco y no se presenta como metodología oficial de Anthropic. Las cuatro competencias acompañan todas las recomendaciones; no hay una correspondencia uno a uno. El diagrama `recursos/4d-y-proceso.svg` y el mapa didáctico de esa página son la referencia.

| Competencia | Pregunta útil, ya usada en v1.4 |
|---|---|
| Delegation | ¿Qué le encargo a la IA y qué hago o decido yo? |
| Description | ¿He explicado datos, condiciones y resultado esperado? |
| Discernment | ¿Qué parte está comprobada y qué parte debo cuestionar? |
| Diligence | ¿Qué debo registrar, proteger, atribuir y revisar antes de difundir? |

**Propuesta v2.** El mismo marco se vuelve visible en los desafíos, sin redefinir las competencias:

| Desafío | Competencias más visibles | Dónde queda en la bitácora mínima | Si se usa la plantilla extensa |
|---|---|---|---|
| 1. ¿Qué tengo y qué necesito? | Delegation, Description | Necesidad y tres incertidumbres | Sección 1 (P0) |
| 2. ¿Cómo se llama? | Description, Discernment | Las incertidumbres pueden afinarse con los términos de P1 | Sección 2 (P1) y microactividad A |
| 3. ¿Qué le voy a pedir? | Delegation, Description, Diligence | Especificación | Secciones 3 y 4. Microactividades B y C |
| 4. ¿Qué puedo aceptar? | Discernment, Diligence | Una verificación real | Secciones 5 y 5b. Auditor |
| 5. ¿Qué decidí y qué queda pendiente? | Diligence | Siguiente acción | Sección 6, declaración de uso de IA y transferencia |

Diligence incluye, en la v2, la decisión de no compartir datos reales y de no declarar como verificado lo que no se abrió. Eso ya está pedido en `contenido/00-preparacion.qmd` y en la bitácora; la v2 lo coloca dentro de la decisión de delegar, no solo como aviso previo.

La microactividad B existe para evitar que 4D se quede como tabla memorizada. Si una persona no distingue las cuatro palabras en cuatro minutos, el taller no se detiene: el mapa de `contenido/03-metodo.qmd` sigue disponible como lectura.

---

## 9. Distribución de los 120 minutos

### Lo que hace hoy la v1.4

**Comprobado** en `contenido/05-practica.qmd` y en `recursos/agenda-practica.svg`. La sesión publicada está relojada de 11:30 a 13:30:

| Minuto | Reloj publicado | Bloque v1.4 |
|---|---|---|
| 0–20 | 11:30–11:50 | Apertura, tres ejemplos y método |
| 20–40 | 11:50–12:10 | P0 y P1 |
| 40–60 | 12:10–12:30 | Especificación humana y 5–7 minutos de anatomía del prompt |
| 60–90 | 12:30–13:00 | P5, P6 y contraste con la fuente |
| 90–110 | 13:00–13:20 | Bitácora y revisión por pares |
| 110–120 | 13:20–13:30 | Cierre y problema propio |

Esa agenda cabe porque las actividades son de lectura, chat y bitácora. No incluye tres laboratorios.

### Agenda propuesta para v2

**Propuesta de esta segunda revisión.** Se mantienen 120 minutos. No se fijan horas de reloj hasta conocer el horario de la sesión. La verificación externa tiene prioridad sobre los ejercicios secundarios: si el reloj se atrasa, se recortan primero las filas ajustables y ese tiempo pasa a abrir y leer la fuente.

| Minuto | Prioridad | Desafío | Qué ocurre |
|---|---|---|---|
| 0–6 | Imprescindible | Apertura | Datos simulados, recomendaciones flexibles, un solo chat. La explicación del caso viene después de mirar las hojas. |
| 6–20 | Imprescindible | 1 | Explorador: dos estaciones de observación, preguntas e incertidumbres. Sin mostrar los cuatro asuntos. |
| 20–28 | Imprescindible | 1 | P0 y pausa: qué hizo la IA. |
| 28–36 | Ajustable | 2 | Microactividad A: tres ejemplos breves de vocabulario. Si falta tiempo, queda un ejemplo y el regreso al Excel. |
| 36–46 | Imprescindible | 2 | P1. Los últimos minutos de puesta en común son ajustables. |
| 46–52 | Ajustable | 3 | Microactividades B y C: 4D y elección de herramienta. |
| 52–60 | Imprescindible | 3 | Especificación propia en la bitácora mínima, antes de P5. |
| 60–64 | Ajustable | 3 | Prompt propio en el Constructor o en papel. No se envía al chat común. |
| 64–74 | Imprescindible | 4 | P5, prompt común del diagnóstico. |
| 74–80 | Ajustable | 4 | P6. Si falta tiempo, se enuncia que la autorrevisión no verifica y se pasa a la fuente. |
| 80–98 | Imprescindible, protegida | 4 | Verificación externa con Wilkinson et al. (2016). Puede absorber los minutos recortados. |
| 98–110 | Imprescindible | 5 | Bitácora mínima: cinco campos. |
| 110–116 | Ajustable | 5 | Una observación y una pregunta entre pares, sobre la bitácora mínima. |
| 116–120 | Ajustable | Cierre | Una frase de transferencia. La siguiente acción ya está en la bitácora. |

Las seis recomendaciones se nombran en la apertura y se vuelven a encontrar dentro de cada desafío. No se explican las seis por extenso antes de tocar el archivo. El Auditor y el Constructor, mientras no existan, usan `contenido/06-verificacion.qmd`, `recursos/escala-evidencia.svg` y `contenido/03b-estructura-prompt.qmd`. Sus minutos no se suman encima de esta tabla.

### Orden en que se recorta

1. Cierre de transferencia y revisión por pares.
2. Microactividades B y C.
3. Microactividad A, hasta dejar un solo ejemplo.
4. Lectura completa de P6.
5. Redacción del prompt propio, conservando la especificación.

No se recortan la observación previa a la explicación, P0, P1, la especificación anterior a P5, la ejecución de P5, la verificación externa ni la bitácora mínima.

### Qué cambia respecto de la agenda publicada

- La apertura baja de 20 a 6 minutos. Los tres ejemplos de `contenido/02-ejemplos.qmd` quedan para la microactividad B, que es ajustable, y las páginas siguen como consulta.
- Los ejemplos de literatura, software y datos viven en la microactividad A, no en el cierre.
- La bitácora de la sesión es la mínima. La plantilla extensa no ocupa un bloque obligatorio.
- La revisión por pares queda en 6 minutos y es la primera pieza ajustable. En la v1.4 el bloque conjunto de bitácora y pares dura unos 20 minutos.
- La verificación externa queda en 18 minutos, con permiso explícito de crecer a costa de lo ajustable. En la v1.4 comparte el bloque de 30 minutos con P5 y P6.

### Si el HTML del Explorador todavía no existe

La observación se hace en el Excel o, si no se puede adjuntar, en `descargas/expresion_genica_caso_simulado.txt`. Quien facilita no proyecta al inicio `contenido/04-caso-fair.qmd` ni `recursos/datos-y-metadatos.svg`. El resto de la tabla se mantiene. Los minutos de una herramienta ausente no se rellenan con más explicación: vuelven a la verificación o a la bitácora mínima.

### Ritmo que no se debe romper

- Primero se observan las dos hojas y se formulan incertidumbres. Después viene P0.
- P0, P1, P5 y P6 van en un solo chat, en ese orden, como en `recursos/un-solo-chat.svg`. El prompt propio se queda fuera de ese chat.
- La especificación humana ocurre después de P1 y antes de P5.
- La verificación de Wilkinson tiene prioridad frente a P6, el Auditor, los pares, el Constructor y las microactividades.
- Un segundo chat de comparación sigue siendo opcional y no se presenta como experimento. El ejercicio de la cita del 80 % también sigue siendo opcional.

---

## 10. Relación con los archivos actuales del repositorio

Rutas comprobadas en `feat/taller-interactivo-v2`. No hay, en este repositorio, carpeta `interactivos/`, archivo de GFF3 Explorer ni carpeta `privado-docente/`. Esta última está nombrada en el README, en `CONTRIBUTING.md` y en `_quarto-publicacion-nota.md`, y excluida en `.gitignore`; no está en el árbol de trabajo.

### Páginas del sitio

| Archivo | Papel en v1.4 | Uso propuesto en v2 |
|---|---|---|
| `index.qmd` | Portada, ruta de lectura, aviso de datos simulados | Cuando se autorice la implementación, la ruta visible serán los cinco desafíos. Los fundamentos se enlazan como consulta. Conservar autoría, duración, modalidad y el límite sobre FAIR. |
| `contenido/00-preparacion.qmd` | Requisitos, prueba de 2 minutos, plan B en texto, privacidad | Se conserva. La prueba sigue comprobando las hojas `Expresion_genica` y `Notas_experimento`. |
| `contenido/01-contexto.qmd` | Sentido, dos públicos, seis aprendizajes, alcance | Consulta. Fuente de los resultados 1 a 6. Cualquier reescritura debe conservar el alcance: no se certifica FAIR ni se deposita un dataset. |
| `contenido/02-ejemplos.qmd` | Tres situaciones simuladas | Consulta y banco de la microactividad B. El ejemplo 2 también ilustra, en corto, el vocabulario de una cita. No presentarlas como ejecuciones reales. |
| `contenido/03-metodo.qmd` | Seis etapas, 4D, procedencia y límites de lo que puede afirmarse | Consulta. Pasar el lenguaje visible de «etapas de un método» a «recomendaciones flexibles», sin borrar la sección de procedencia ni el mapa 4D. |
| `contenido/03b-estructura-prompt.qmd` | Siete componentes, P0 frente a versión delimitada, actividad de 5–7 minutos | Consulta y base del Constructor. El prompt que ahí se redacta es de aprendizaje. El rol sigue siendo opcional. |
| `contenido/04-caso-fair.qmd` | Escenario, tabla de observaciones, FAIR como contexto | Consulta posterior a la exploración. Abrirla al inicio mostraría los huecos que el Explorador pide descubrir. |
| `contenido/05-practica.qmd` | Agenda de 120 minutos, inclusión de los cuatro prompts, autoevaluación | La agenda de la sección 9 la sustituiría solo después de autorizar la implementación. La autoevaluación sigue como criterio de la plantilla extensa. |
| `contenido/06-verificacion.qmd` | Actividad obligatoria y regla de evidencia | Base del Auditor y del desafío 4. |
| `contenido/07-bitacora.qmd` | Plantilla en la página: datos generales, secciones 1 a 6, 5b, transferencia y declaración de uso de IA | Recurso complementario. La bitácora mínima de la sesión todavía no tiene archivo. |
| `contenido/tarjeta-practica.qmd` | Hoja imprimible con los cuatro prompts y las cuatro etiquetas | Se conserva como apoyo de quien no quiera alternar páginas. |
| `contenido/08-referencias.qmd` | Bibliografía, descargas, cita y estado del material | Se conserva. El estado debe seguir diciendo que no hay piloto documentado, hasta que exista uno y se registre aparte. |

### Prompts canónicos

Estos archivos son la única fuente que la práctica y la tarjeta incluyen hoy. La v2 los conserva literales.

| Archivo | Función comprobada |
|---|---|
| `contenido/_prompts/p0.md` | Solicitud abierta. Etiqueta: «nuevo chat · adjunta el Excel». |
| `contenido/_prompts/p1.md` | Cinco conceptos y cinco preguntas, en el mismo chat. |
| `contenido/_prompts/p5.md` | Diagnóstico de cuatro asuntos. |
| `contenido/_prompts/p6.md` | Autorrevisión. No declara haber verificado una fuente. |

**Diferencia ya existente, a resolver en la revisión editorial y no en este documento:** `contenido/03b-estructura-prompt.qmd` vuelve a escribir el texto de P0 dentro de la página, con la etiqueta «solicitud abierta», en lugar de incluir `contenido/_prompts/p0.md`. El texto de la solicitud coincide. La etiqueta no.

No existen archivos `p2.md`, `p3.md` ni `p4.md`. La v2 no los crea: esas decisiones siguen siendo de la persona.

### Datos, bitácora y figuras

| Archivo | Uso |
|---|---|
| `descargas/expresion_genica_caso_simulado.xlsx` | Archivo del caso y de la prueba de 2 minutos. |
| `descargas/expresion_genica_caso_simulado.txt` | Plan B si el asistente no admite adjuntos. Celdas vacías marcadas como `[vacía]`. |
| `descargas/bitacora-plantilla.md` | Plantilla extensa en texto. Complemento de la bitácora mínima; no es el formulario de los 120 minutos. |
| `descargas/bitacora-plantilla.docx` | La misma plantilla extensa para Word o Google Docs. |
| `recursos/metodologia-seis-etapas.svg` | Mapa de las seis recomendaciones. Está en `index.qmd` y en `contenido/03-metodo.qmd`. |
| `recursos/4d-y-proceso.svg` | 4D junto a las seis recomendaciones. |
| `recursos/anatomia-prompt.svg` | Siete componentes entre especificación y colaboración. |
| `recursos/vista-excel.svg` | Las dos hojas del caso. |
| `recursos/datos-y-metadatos.svg` | Observable frente a lo que requiere confirmación. Consulta posterior: al inicio anticipa la explicación. |
| `recursos/agenda-practica.svg` | Agenda v1.4. Habría que redibujarlo si cambia la distribución. |
| `recursos/combinar-tablas.svg` | Ejemplo 1: concatenar, unir por clave, armonizar. |
| `recursos/revisar-vs-verificar.svg` | P6 frente a verificación humana. |
| `recursos/escala-evidencia.svg` | Cuatro etiquetas. |
| `recursos/un-solo-chat.svg` | P0, P1, P5 y P6 en un chat; la persona especifica y verifica. El prompt propio de la v2 queda fuera de ese chat. |

### Material docente

**Comprobado.** El README, `CONTRIBUTING.md` y `_quarto-publicacion-nota.md` describen `privado-docente/` como material de la instructora, excluido en `.gitignore`. Esa carpeta no está en el árbol de trabajo.

**Decisión de esta revisión.** Antes de la sesión hay que recuperar ese material o reconstruir las orientaciones y las respuestas esperadas. Incluyen, como mínimo, qué preguntas es razonable que aparezcan al explorar el Excel, cómo se reconoce una verificación hecha de verdad y qué hacer si P5 devuelve metadatos inventados. Ese material se queda fuera del sitio público y fuera del repositorio publicado. No se enlaza desde la navegación ni se copia a `contenido/`.

### Piezas técnicas que no son contenido pedagógico

| Archivo | Hecho comprobado | Implicación para más adelante |
|---|---|---|
| `_quarto.yml` | Renderiza `index.qmd` y `contenido/*.qmd`. Copia al sitio `descargas/**` y `recursos/**`. | Un HTML nuevo no se publicará solo por existir en el disco. Habrá que decidir su carpeta y registrarla como recurso. Eso no se hace en este paso. |
| `_prompt-copy.html` | Añade el botón «Copiar» a cada bloque `.prompt`. | Es el único JavaScript propio. No es un laboratorio. |
| `tema.scss`, `styles.css` | Tema visual. | Sin cambios en esta fase. |
| `README.md` | Describe la estructura, la publicación con `quarto publish gh-pages` y el historial hasta v1.4. | Actualizarlo solo cuando la v2 esté aceptada e implementada. |
| `PROMPT_PARA_CURSOR.md` | Brief de construcción de la v1, incluida la nota de v1.1 sobre `03b`. | No es la especificación de la v2. Este archivo la sustituye como referencia pedagógica. |
| `_quarto-publicacion-nota.md` | Advierte que `privado-docente/` no debe versionarse. | Sigue vigente. |
| `_site/` | Salida local de Quarto, ignorada por Git. | No es fuente de contenido. |

El sitio publicado sale de la rama `gh-pages`, no de esta rama. Redactar este documento no cambia <https://helysalgado.github.io/fair-prompt-4d/>.

---

## 11. Criterios de calidad pedagógica y científica

Una implementación o una sesión se considera fiel a este diseño si cumple lo siguiente.

### Sobre el caso y los datos

- Los números y las notas se tratan como simulados en la portada, en el caso, en la práctica y en el Explorador.
- La celda vacía no aparece como cero.
- «prom.», la cepa, las unidades, las réplicas y el procesamiento permanecen sin resolver mientras el archivo no los diga.
- `b0014` no se iguala a otro símbolo génico sin cepa, ensamblaje y anotación.
- El alcance de P5 sigue siendo cuatro asuntos. Identificador, procesamiento, cepa y responsable se pueden nombrar como exclusiones por tiempo.
- Esos cuatro asuntos no aparecen al abrir el Explorador. La persona los encuentra, si los descubre, a partir de sus preguntas, y el grupo los recibe más tarde como encargo de P5.

### Sobre la IA

- P0, P1, P5 y P6 se usan completos y en un solo chat.
- La especificación de las recomendaciones 3 y 4 la escribe la persona antes de P5.
- El prompt propio sirve para aprender a formular. P5, sin cambios, es el prompt común del diagnóstico y es el que se envía al chat.
- P6 se presenta como autorrevisión. El diagrama `recursos/revisar-vs-verificar.svg` sigue siendo la distinción correcta.
- Ninguna herramienta declara «verificado» sin pasaje y fecha anotados por la persona.
- «No existe» se distingue de «no está documentado».
- Una respuesta más ordenada no se enseña como una respuesta más verdadera.
- Variar de asistente en la puesta en común sirve para observar diferencias. No se reporta como comparación experimental.

### Sobre las recomendaciones y el marco 4D

- El texto visible dice recomendaciones flexibles.
- Se conserva la procedencia: síntesis didáctica apoyada en fuentes, no método validado por Anthropic, ACRL, NIST o ELIXIR.
- Se puede omitir una recomendación cuando la tarea es trivial, y se dice por qué.
- Las competencias 4D no se asignan como casillas obligatorias de cada desafío.
- El rol del prompt sigue siendo opcional.

### Sobre la verificación

- La actividad de Wilkinson et al. (2016) permanece y tiene prioridad sobre microactividades, P6 completo, pares, Constructor y Auditor.
- Si la fuente no abre, el estado válido es pendiente.
- La profundidad puede bajar en una viñeta de transferencia y no en el caso principal: el caso principal tiene consecuencia de publicación simulada y por eso se verifica de verdad.
- Iterar el prompt no cuenta como verificación.

### Sobre la bitácora

La sesión queda cumplida cuando la bitácora mínima tiene cinco campos: necesidad, tres incertidumbres, especificación, una verificación real y siguiente acción. La verificación real incluye fuente, pasaje y fecha, o dice «pendiente» si la fuente no se abrió.

La autoevaluación de `contenido/05-practica.qmd` sigue vigente para quien use la plantilla extensa:

- Quedó registrado qué hizo la IA con P0 antes de corregirla.
- La especificación es anterior a P5 y la escribió la persona.
- Hay cuatro asuntos y cada afirmación tiene etiqueta.
- Nada figura como verificado sin fuente abierta, pasaje y fecha.
- «No existe» y «no está documentado» están distinguidos.
- Otra persona puede reconstruir el proceso.

Esas etiquetas del diagnóstico son deseables. Si hay que elegir, se conserva la verificación externa de la bitácora mínima antes que una tabla completamente etiquetada.

### Sobre las herramientas, cuando existan

- Inspeccionan, organizan o clasifican. No certifican.
- El Explorador muestra las dos hojas y pide preguntas antes de explicar. Su primera pantalla no lista los cuatro asuntos.
- La retroalimentación del Explorador responde a lo seleccionado y no convierte una incertidumbre en un dato.
- El reporte Markdown se puede copiar a la bitácora mínima.
- El Explorador no edita el dataset.
- El Constructor no llama a un modelo.
- El Auditor no abre la fuente en lugar de la persona.
- Una actividad hecha con la página Quarto equivalente cumple el mismo criterio pedagógico mientras el HTML no esté.

### Sobre lo que no debe afirmar el material

- Que hubo un piloto o una evaluación de aprendizajes, mientras eso no esté documentado.
- Que el grupo certificó el Excel como FAIR.
- Que los ejemplos breves de literatura y de software se practicaron con la misma profundidad que el Excel.
- Que las seis recomendaciones son una metodología científica validada.

---

## 12. Decisiones pendientes antes de implementar

### Registradas en esta segunda revisión

Quedan como propuesta de diseño. Todavía no cambian páginas ni herramientas.

- Los cinco desafíos son la ruta principal. `contenido/01-contexto.qmd`, `contenido/02-ejemplos.qmd`, `contenido/03-metodo.qmd`, `contenido/03b-estructura-prompt.qmd` y `contenido/08-referencias.qmd` quedan como consulta. `contenido/04-caso-fair.qmd` se consulta después de explorar.
- El Explorador hace observar las dos hojas, formular preguntas y anotar incertidumbres antes de explicar. Unidades, condiciones, réplicas y celda vacía son criterio interno de diseño, no texto de apertura.
- El patrón que se tomará de GFF3 Explorer es: estaciones, selección de elementos, retroalimentación contextual y reporte Markdown. La referencia se entregará aparte. No se afirma haber inspeccionado su código.
- La microactividad de vocabulario usa tres ejemplos breves —literatura, software y datos— y no los convierte en prácticas.
- La sesión usa una bitácora mínima de cinco campos. La plantilla de `contenido/07-bitacora.qmd` y de `descargas/` queda como complemento.
- La agenda distingue actividades imprescindibles y ajustables. La verificación externa se protege.
- El participante escribe una especificación y un prompt propios para aprender a formular. Ese texto no se envía al chat común. El diagnóstico del grupo usa P5.
- Antes de la sesión hay que recuperar o reconstruir orientaciones y respuestas esperadas, y mantenerlas fuera de la publicación pública.

### Pendientes antes de la especificación funcional del Explorador

Estas decisiones definen qué hará la primera herramienta. Conviene cerrarlas antes de escribir esa especificación.

1. **Referencia de GFF3 Explorer.** Falta el archivo o la URL que se proporcionará por separado. El patrón ya está descrito; todavía no se ha contrastado con la aplicación.
2. **Estaciones.** Confirmar si bastan tres —hoja de datos, notas y preguntas— o si el recorrido necesita otras, y qué se puede seleccionar en cada una.
3. **Límite de la retroalimentación.** Decidir qué puede decir al seleccionar una celda o un campo sin anticipar los cuatro asuntos ni resolver «prom.», la cepa, `b0014` o la celda vacía.
4. **Reporte Markdown.** Fijar sus apartados y cómo se corresponden con la necesidad y las tres incertidumbres de la bitácora mínima.
5. **Alcance del archivo.** Confirmar que la primera versión solo muestra el Excel simulado de `descargas/`, sin edición de celdas y sin abrir otro archivo.
6. **Plan B sin HTML.** Confirmar que, si la herramienta no está lista, se miran el `.xlsx` o el `.txt` sin proyectar `contenido/04-caso-fair.qmd` ni `recursos/datos-y-metadatos.svg`.
7. **Respuestas esperadas del recorrido.** Hacen falta para redactar la retroalimentación. Forman parte del material docente que hay que recuperar o reconstruir, y no se publican con el sitio.

### Pendientes para el sitio o la sesión, no para ese primer Explorador

1. **Reloj.** La v1.4 publica 11:30–13:30. La agenda de la v2 usa minutos relativos hasta que haya fecha.
2. **Nombre visible.** Decidir si «etapas» se reemplaza en `contenido/03-metodo.qmd`, en los SVG y en la portada, o si se conserva y se añade que son recomendaciones flexibles.
3. **P0 duplicado.** `contenido/03b-estructura-prompt.qmd` repite el texto de P0 con otra etiqueta. Falta decidir si pasa a incluir `contenido/_prompts/p0.md`.
4. **Versión delimitada de `03b`.** Sigue propuesta como comparación de solo lectura dentro del Constructor, sin enviarse al chat común.
5. **Auditor.** Si P5 no responde, falta decidir si habrá un paquete breve de afirmaciones de ejemplo. No bloquea al Explorador.
6. **Formulario final de la v1.4.** `contenido/05-practica.qmd` pide dos respuestas anónimas y dice que es la primera edición con participantes. Falta decidir si ese cierre se conserva, se reescribe o se retira hasta que el formulario exista.
7. **Publicación.** El sitio en vivo solo cambia con una decisión explícita de publicar. Este documento no la autoriza.

Mientras la v2 no esté implementada, la referencia para una sesión real sigue siendo la v1.4 publicada.
