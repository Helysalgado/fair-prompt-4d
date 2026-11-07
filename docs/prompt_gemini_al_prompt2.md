# Rediseño de la actividad 3 — De la solicitud al prompt

Actúa como diseñador instruccional especializado en alfabetización en IA y como desarrollador de aplicaciones web educativas.

Trabaja sobre el archivo existente:

`de_la_solicitud_al_prompt.html`

**No construyas una aplicación desde cero.** Conserva el diseño general y modifica la experiencia pedagógica y las funcionalidades que se indican a continuación.

## 1. Contexto educativo

Esta herramienta forma parte del taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica».**

Los participantes ya realizaron dos actividades:

**Actividad 1. Explorador FAIR**

Observaron un conjunto de datos, identificaron información disponible y distinguieron observaciones de interpretaciones.

**Actividad 2. ¿Qué falta por definir?**

Partieron de una necesidad, identificaron preguntas y decisiones pendientes, consultaron orientaciones y reformularon una solicitud para hacerla más precisa.

Ahora realizarán:

**Actividad 3. De la solicitud al prompt**

Su objetivo es aprender a **comunicarse con precisión y reducir la ambigüedad al dar instrucciones a una IA**.

No buscamos enseñar una fórmula rígida ni que los participantes produzcan prompts extensos.

Queremos que comprendan que una misma solicitud puede interpretarse de diferentes maneras si no se comunica con suficiente claridad.

Duración objetivo: **8–10 minutos**.

## 2. Principio fundamental: no repetir el trabajo anterior

Actualmente, la primera pestaña pide recuperar manualmente la solicitud o escribirla nuevamente.

Esto resulta repetitivo.

**La nueva versión debe recuperar automáticamente la solicitud reformulada en la actividad 2.**

El participante no debe tener que copiarla, pegarla ni pulsar un botón de importación durante el recorrido normal.

La recuperación se realizará al abrir la actividad.

La actividad anterior guarda su estado en `localStorage`, mediante la clave:

`que_falta_por_definir_state_v3`

La estructura relevante es:

- `currentCase`: `"A"` o `"B"`.
- `cases.A.revisedRequest`: cadena con la solicitud reformulada.
- `cases.B.revisedRequest`: cadena con la solicitud reformulada.
- `cases.A.pendingDecisions`: cadena con decisiones pendientes.
- `cases.B.pendingDecisions`: cadena con decisiones pendientes.

**Importante:** `pendingDecisions` es texto, no un arreglo.

No confundir las pistas consultadas de la actividad anterior con decisiones tomadas por el participante.

### Comportamiento de recuperación

Al iniciar:

1. Buscar los datos de la actividad 2 en `localStorage`.
2. Validar los tipos antes de utilizarlos.
3. Recuperar la solicitud reformulada del caso activo de la actividad anterior.
4. Mostrarla directamente en la primera pestaña.
5. Recuperar las decisiones pendientes y mostrarlas por separado.
6. No sobrescribir silenciosamente un prompt que ya se haya trabajado en la actividad 3.

Si existen solicitudes reformuladas de ambos casos, ofrecer un selector sencillo para elegir cuál utilizar.

Si solamente uno tiene una solicitud válida, utilizar ese caso.

Si no se encuentra ninguna solicitud reformulada, permitir escribir una solicitud manualmente.

Si la actividad se abre desde un navegador u origen diferente, explicar brevemente que no se encontraron datos anteriores y ofrecer la alternativa manual.

No mostrar mensajes de error innecesarios en el recorrido normal.

### Protección del trabajo existente

La tercera actividad debe guardar su propio estado en una clave independiente:

`de_la_solicitud_al_prompt_state_v1`

Si ya existe trabajo guardado en la actividad 3:

- Restaurarlo primero.
- No reemplazarlo automáticamente al cargar la página.
- Mostrar la solicitud con la que se estaba trabajando.
- Ofrecer una opción discreta para recuperar o actualizar los datos de la actividad anterior.
- Solicitar confirmación antes de reemplazar datos que puedan afectar el prompt existente.

Si se cambia de caso, conservar el trabajo de cada caso por separado o, como mínimo, evitar cualquier pérdida silenciosa mediante confirmación explícita.

No reconstruir ni sobrescribir un prompt editado manualmente sin consentimiento.

## 3. Rediseñar la primera pestaña

Cambiar el título actual:

«Mi solicitud»

por:

**«1. ¿Qué voy a delegar?»**

Esta pestaña debe ser mucho más breve.

### A. Mostrar mi solicitud anterior

Presentar una tarjeta con el encabezado:

**Tu solicitud de la actividad anterior**

Mostrar directamente el texto recuperado.

Incluir una indicación discreta:

«Recuperada de ¿Qué falta por definir?»

No colocar la solicitud en un textarea grande cuando ya se recuperó correctamente.

Mostrarla como un texto legible.

Si existen decisiones pendientes de confirmar, mostrarlas debajo en un recuadro independiente:

**Decisiones que todavía necesitas confirmar**

Estas decisiones no deben incorporarse automáticamente como requisitos resueltos.

Si el contenido fue escrito manualmente, indicar su procedencia de forma apropiada.

### B. Elegir qué delegar a la IA

Mostrar la pregunta:

**«¿Qué quieres que haga la IA con esta solicitud?»**

Explicar brevemente:

«Una misma necesidad puede dar lugar a tareas diferentes. Elige qué tipo de ayuda necesitas antes de escribir tus instrucciones».

Presentar opciones mediante botones de selección, no un listado de respuestas correctas.

#### Caso A — Analizar secuencias FASTA

Mostrar estas posibilidades:

- Explicarme cómo realizar el análisis.
- Escribir un script para realizarlo.
- Analizar los datos que le proporcione.
- Revisar los resultados que ya obtuve.
- Otra tarea.

#### Caso B — Desarrollar una aplicación web

Mostrar estas posibilidades:

- Ayudarme a definir los requisitos de la aplicación.
- Diseñar un prototipo de la interfaz.
- Escribir el código de la aplicación.
- Revisar o mejorar una implementación existente.
- Otra tarea.

Si selecciona «Otra tarea», ofrecer un campo breve para describirla.

No sugerir que una opción es mejor que las demás.

No elegir una opción automáticamente.

La elección debe quedar registrada y alimentar la siguiente pestaña.

Si el participante selecciona una opción, permitir ajustarla con sus propias palabras cuando lo considere necesario.

### C. Avanzar

Botón:

**«Continuar: comunicar con precisión»**

No añadir más preguntas a esta pestaña.

La primera pestaña debe sentirse como una decisión sencilla, no como otro formulario.

## 4. Segunda pestaña — Comunicar con precisión

Cambiar el título a:

**«2. Construir mis instrucciones»**

Incluir una introducción breve:

«Ahora expresa lo que necesitas de forma que otra persona o una IA pueda comprenderlo sin tener que adivinar decisiones importantes».

Conservar los cuatro componentes:

**Contexto y objetivo**

¿Qué necesita saber la IA para comprender tu situación?

**Tarea**

¿Qué acción concreta debe realizar?

**Condiciones y límites**

¿Qué debe respetar? ¿Qué no debe suponer?

**Resultado y verificación**

¿Qué resultado esperas y cómo podrás comprobarlo?

La solicitud recuperada y la tarea elegida deben estar disponibles como referencia.

**No pedir que el participante copie nuevamente la solicitud anterior.**

La tarea elegida en la primera pestaña debe aprovecharse en la construcción del prompt.

Evitar que el usuario tenga que escribir exactamente la misma tarea en dos campos distintos.

No agregar requisitos automáticamente.

No completar información científica faltante.

No imponer un lenguaje de programación, formato de salida o tecnología.

Los campos pueden permanecer incompletos y la navegación debe ser libre.

No utilizar ejemplos que revelen decisiones específicas en los placeholders.

## 5. Tercera pestaña — Revisar las ambigüedades

Título:

**«3. Revisar mi prompt»**

La aplicación debe reunir únicamente la información proporcionada o seleccionada por el participante.

El borrador debe incorporar:

- La solicitud reformulada recuperada.
- La tarea que el participante decidió delegar.
- El contexto adicional, si lo escribió.
- Las condiciones y límites que especificó.
- El resultado esperado y la verificación, si los especificó.

Evitar duplicaciones innecesarias.

No incluir decisiones pendientes como si ya estuvieran resueltas.

No inventar información para completar espacios vacíos.

### Prompt editable

Mostrar el prompt ensamblado en un textarea editable.

El participante debe poder modificarlo libremente.

Incluir un botón:

**Copiar prompt**

Copiar exactamente la versión final editada.

Conservar el botón:

**Regenerar desde mis respuestas**

Si existe una edición manual del prompt, advertir que se reemplazará y solicitar confirmación.

Si cancela, conservar el texto original.

### Revisión reflexiva

Debajo del prompt, mostrar únicamente dos preguntas breves:

**1. ¿Qué partes de tus instrucciones podrían interpretarse de más de una manera?**

**2. ¿Qué necesitas aclarar o confirmar antes de delegar la tarea?**

Ofrecer espacios para escribir ambas respuestas.

La persona debe poder revisar y corregir el prompt después de responder.

No mostrar respuestas sugeridas.

No realizar calificaciones automáticas.

No añadir indicadores de calidad ni listas extensas de comprobación.

La finalidad es que la persona descubra que escribir un prompt también implica revisar cómo podría ser interpretado.

## 6. Cuarta pestaña — Reporte

Conservar:

**«4. Reporte»**

Mostrar los resultados del trabajo.

Incluir:

1. Solicitud recuperada o escrita.
2. Procedencia de la solicitud.
3. Caso trabajado.
4. Tarea que se decidió delegar.
5. Contexto e instrucciones añadidas.
6. Condiciones y límites.
7. Resultado esperado y verificación.
8. Prompt final editado.
9. Ambigüedades identificadas.
10. Decisiones pendientes de confirmar.

Distinguir claramente:

- Lo que escribió o seleccionó el participante.
- Lo recuperado de la actividad anterior.
- Lo que continúa sin resolverse.

El Reporte visible y el archivo Markdown deben basarse en los mismos datos.

Permitir descargar el reporte incluso si está incompleto.

No afirmar que el prompt fue probado ni que la IA respondió correctamente; eso se trabajará en otra actividad.

## 7. Persistencia y comportamiento entre casos

La aplicación debe funcionar con los dos casos de la actividad anterior.

Si el participante trabajó ambos, debe poder elegir cuál utilizar.

Al cambiar de caso:

- Volver a la primera pestaña.
- Mostrar la solicitud correspondiente.
- Restaurar los datos propios de ese caso cuando existan.
- No mezclar respuestas entre los casos.
- No eliminar silenciosamente un prompt editado.

Al recargar:

- Restaurar el caso activo.
- Restaurar la pestaña.
- Restaurar los campos escritos.
- Restaurar el prompt editado.
- Restaurar las reflexiones sobre ambigüedad.

No es necesario recuperar automáticamente las preguntas ni las pistas de la actividad anterior.

Solo necesitamos la solicitud reformulada y las decisiones pendientes.

## 8. Diseño visual

Conservar la identidad de las otras actividades:

- Azul `#00314F`.
- Dorado `#C9A227`.
- Blanco y grises claros.
- Tipografía legible.
- Interfaz limpia.
- Sin logos institucionales.

Evitar una pantalla inicial recargada.

La primera pestaña debe presentar la solicitud recuperada y la decisión de delegación como los elementos principales.

Mantener compatibilidad con pantallas móviles.

## 9. Requisitos técnicos

Crear y entregar el HTML completo actualizado:

`de_la_solicitud_al_prompt.html`

Debe ser autónomo, con CSS y JavaScript embebidos.

Sin dependencias externas ni llamadas a APIs.

Debe funcionar offline.

Validar defensivamente los datos recuperados de ambas actividades.

Un estado incompleto o malformado no debe bloquear la aplicación.

No convertir objetos o arreglos en textos como `[object Object]`.

Proteger contra inserción insegura de contenido.

El acceso a `localStorage` debe estar protegido por manejo de errores.

La recuperación automática debe funcionar cuando ambos HTML estén bajo el mismo origen. No asumir que será posible compartir almacenamiento entre orígenes diferentes.

Mantener controles accesibles por teclado y navegación libre.

El reinicio debe solicitar confirmación.

No modificar archivos externos a esta herramienta.

## 10. Verificaciones solicitadas

Revisa al menos estos escenarios:

1. Participante que completó únicamente el Caso A.
2. Participante que completó únicamente el Caso B.
3. Participante con ambos casos completados.
4. Participante que no realizó la actividad anterior.
5. Solicitud anterior vacía.
6. Estado anterior incompleto o malformado.
7. Recuperación automática al abrir.
8. Selección de diferentes tareas para delegar.
9. Cambio de caso y conservación de respuestas.
10. Construcción del prompt sin duplicar la solicitud ni la tarea.
11. Construcción con campos parcialmente vacíos.
12. Edición manual del prompt.
13. Regeneración confirmada y cancelada.
14. Copia de la versión final editada.
15. Recarga y restauración del trabajo.
16. Reporte y descarga Markdown.
17. Reinicio confirmado y cancelado.
18. Funcionamiento en pantallas de 390 px.
19. Funcionamiento sin recursos externos.
20. Protección ante datos de tipos inesperados.

Indica qué pruebas ejecutaste realmente y cuáles requieren revisión posterior.

## 11. Restricciones finales

No agregar pestañas.

No agregar ejercicios extensos.

No utilizar una plantilla de prompting rígida.

No ejecutar prompts.

No conectarse a servicios de IA.

No agregar evaluaciones automáticas.

No modificar las actividades 1 y 2.

No modificar Quarto, Git ni el sitio publicado.

**La experiencia debe ser sencilla: recuperar mi necesidad, decidir qué delegar, comunicarlo con precisión y revisar posibles ambigüedades.**

Entrega únicamente el HTML completo actualizado y un resumen breve de los cambios realizados.


