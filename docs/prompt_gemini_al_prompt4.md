# Rediseño de la actividad 3 — Laboratorio de construcción y prueba de prompts

Actúa como diseñador instruccional especializado en alfabetización en IA y desarrollador de aplicaciones web educativas.

Trabaja sobre el archivo existente:

`de_la_solicitud_al_prompt(4).html`

**No crees una aplicación nueva desde cero.** Conserva su identidad visual, los casos existentes y las funcionalidades útiles, pero reorganiza la experiencia pedagógica según las siguientes instrucciones.

## 1. Contexto del taller

La herramienta forma parte del taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica».**

Los participantes ya realizaron dos actividades:

- Actividad 1: Explorador FAIR.
- Actividad 2: ¿Qué falta por definir?

Ahora trabajarán en la actividad 3:

**«De la solicitud al prompt»**

### Objetivo central

Aprender a **comunicarse con precisión, reducir la ambigüedad y observar cómo distintos elementos de una instrucción pueden influir en las respuestas de una IA**.

Queremos que los participantes experimenten, no que simplemente completen un formulario para obtener un prompt.

La herramienta debe funcionar como una guía para construir instrucciones y probarlas en ChatGPT.

No debe conectarse mediante API ni ejecutar automáticamente los prompts.

## 2. Nueva experiencia pedagógica

El participante deberá:

1. Elegir una necesidad y decidir qué tarea delegará a la IA.
2. Construir progresivamente su prompt.
3. Copiar distintas versiones y probarlas en ChatGPT.
4. Observar y registrar las diferencias entre respuestas.
5. Identificar qué ambigüedades permanecen.
6. Descargar un reporte de su proceso.

La actividad debe permitir experimentar sin obligar a completar todos los campos.

Duración orientativa: 10–15 minutos.

**Dos pruebas son suficientes para completar el ejercicio; una tercera será opcional.**

No exigir cuatro pruebas ni imponer un orden obligatorio para agregar elementos.

## 3. Mantener los casos actuales

Conservar exclusivamente estos dos casos por ahora.

### Caso A — Análisis FASTA

Solicitud de partida:

«Necesito analizar un archivo FASTA con varias secuencias de ADN para conocer la frecuencia de los nucleótidos. Quiero obtener resultados por secuencia y poder compararlos».

Opciones para delegar:

- Explicarme cómo realizar el análisis.
- Escribir un script para realizarlo.
- Analizar los datos que le proporcione.
- Revisar los resultados que ya obtuve.
- Otra tarea.

### Caso B — Aplicación web

Solicitud de partida:

«Necesito desarrollar una aplicación web que permita introducir secuencias de ADN en formato FASTA, realizar análisis básicos y descargar los resultados. La aplicación debe ser sencilla de utilizar y ayudar a identificar entradas incorrectas».

Opciones para delegar:

- Ayudarme a definir los requisitos de la aplicación.
- Diseñar un prototipo de la interfaz.
- Escribir el código de la aplicación.
- Revisar o mejorar una implementación existente.
- Otra tarea.

No modificar los textos de las solicitudes.

No incorporar todavía los casos sobre artículos científicos y búsqueda bibliográfica.

## 4. Nueva organización: cuatro pestañas

### Pestaña 1. ¿Qué voy a delegar?

Conservar esencialmente el funcionamiento actual.

Mostrar:

- Selector de Caso A o B.
- Solicitud de partida.
- Opciones de delegación correspondientes.
- Campo «Otra tarea» cuando aplique.

La persona debe elegir qué ayuda necesita de la IA.

No añadir nuevas preguntas.

No recuperar información de la actividad anterior.

No agregar botones de sincronización.

Al cambiar de caso, regresar a esta pestaña y conservar el trabajo independiente de cada caso.

### Pestaña 2. Construir y probar

**Esta será la pestaña principal de la herramienta.**

Actualmente los campos están en la pestaña 2 y el prompt ensamblado aparece en la pestaña 3.

Quiero que **ambos estén en la misma pestaña**.

El participante debe ver cómo cambia su prompt mientras agrega información.

#### A. Punto de partida

Mostrar la solicitud de partida y la tarea elegida.

Debajo, un texto breve:

«Comienza con estas instrucciones. Puedes copiarlas y probarlas en ChatGPT antes de agregar más detalles».

Esta será la primera versión del prompt.

No generar contenido adicional que el participante no haya proporcionado.

#### B. Construcción progresiva

Mantener tres componentes editables:

**Contexto y objetivo**

Pregunta orientadora:

«¿Qué información adicional necesita conocer la IA para comprender tu situación?»

**Condiciones y límites**

Pregunta orientadora:

«¿Qué debe respetar, qué no debe suponer y qué debería preguntarte si falta información esencial?»

**Resultado esperado y verificación**

Pregunta orientadora:

«¿Qué resultado necesitas, cómo debe presentarlo y cómo podrías comprobarlo?»

No repetir un campo independiente de «Tarea», porque esa decisión ya se tomó en la pestaña 1.

Si la persona necesita precisar la tarea elegida, ofrecer un campo breve y opcional para hacerlo.

Este detalle debe complementar o precisar la tarea, no sustituirla silenciosamente ni generar duplicaciones.

No colocar respuestas de ejemplo en los placeholders.

Los componentes pueden completarse en cualquier orden.

#### C. Prompt actualizado en la misma pestaña

Mostrar una sección claramente visible:

**«Tu prompt para probar»**

El texto debe actualizarse automáticamente cuando el participante:

- Seleccione una tarea.
- Agregue contexto.
- Agregue condiciones.
- Especifique el resultado esperado.
- Precise la tarea.

El prompt se construirá exclusivamente con la solicitud de partida, la selección del participante y los textos que este haya escrito.

No completar información ausente.

No añadir decisiones experimentales, técnicas o metodológicas no proporcionadas.

No incluir encabezados correspondientes a campos vacíos.

Evitar duplicaciones innecesarias.

Mostrar el prompt en un área de texto legible, con posibilidad de copiarlo.

Incluir junto a esta vista:

**«Copiar prompt»**

El botón debe copiar exactamente el texto mostrado.

No es necesario que la persona vaya a otra pestaña para copiarlo.

#### D. Probar en ChatGPT

Agregar un botón:

**«Abrir ChatGPT»**

Debe abrir `https://chatgpt.com/` en una pestaña nueva.

No enviar automáticamente el prompt.

No afirmar que el mensaje fue ejecutado ni que ChatGPT recibió el texto.

Mostrar esta instrucción breve:

«Copia tu prompt, abre ChatGPT y pégalo en una conversación nueva. Observa qué interpreta la IA y qué resultado entrega».

Para cada versión que se quiera comparar, recomendar una conversación nueva con el mismo modelo y los mismos archivos o información disponibles, en la medida de lo posible.

No transmitir datos de los participantes a servicios externos desde esta herramienta.

#### E. Guardar versiones para comparar

Añadir el botón:

**«Guardar esta versión»**

Al presionarlo:

- Guardar una copia exacta del prompt visible.
- Asignarle un identificador consecutivo: Versión 1, Versión 2, Versión 3.
- Registrar qué componentes estaban incorporados.
- Conservar el texto de manera inmutable respecto a las ediciones posteriores.
- Permitir volver a copiar una versión guardada.
- No afirmar que la versión fue probada en ChatGPT.

Limitar la dinámica principal a tres versiones para evitar una interfaz extensa.

Si el participante ya tiene tres versiones, no sobrescribir ninguna; explicar brevemente que puede continuar editando su prompt, pero el ejercicio de comparación utiliza un máximo de tres versiones guardadas.

Permitir borrar una versión únicamente mediante una acción explícita y con confirmación.

No registrar versiones automáticamente al editar.

### Pestaña 3. Comparar y reflexionar

Eliminar de esta pestaña el ensamblador del prompt.

El participante ya construyó y copió las versiones en la pestaña 2.

Ahora debe reflexionar sobre los resultados obtenidos en ChatGPT.

Mostrar las versiones guardadas con sus identificadores.

Permitir consultar el texto de cada versión sin modificarlo.

#### A. Registro breve de observaciones

Para cada versión guardada, mostrar un campo opcional:

**«¿Qué observaste en la respuesta de ChatGPT?»**

No pedir que pegue toda la respuesta del modelo.

La persona puede escribir una observación breve.

Las observaciones son declaraciones del participante, no verificaciones automáticas de la herramienta.

Si una versión todavía no se probó, debe poder dejar el campo vacío.

No marcar una versión como probada simplemente porque fue guardada.

#### B. Comparación reflexiva

Mostrar dos preguntas:

**1. ¿Qué diferencias observaste entre las respuestas y cuáles podrían relacionarse con los cambios en tus instrucciones?**

**2. ¿Qué ambigüedades permanecen o qué necesitarías aclarar antes de utilizar el resultado?**

Ambas preguntas deben admitir respuestas abiertas.

No proporcionar respuestas de referencia.

No calificar automáticamente.

No afirmar que una respuesta es mejor solo porque el prompt es más largo.

La aplicación no tiene acceso a las respuestas de ChatGPT y debe comunicar claramente esa limitación.

#### C. Precaución metodológica

Incluir una nota breve:

«Las respuestas de una IA pueden variar incluso con el mismo prompt. Esta comparación permite explorar posibles efectos de tus instrucciones, pero no demuestra por sí sola una relación causal».

No convertir la actividad en una explicación extensa de metodología experimental.

### Pestaña 4. Reporte

Conservar la descarga Markdown.

El Reporte deberá incluir:

- Caso seleccionado.
- Solicitud de partida proporcionada por el taller.
- Tarea elegida para delegar.
- Contexto, condiciones y resultado especificados.
- Versiones guardadas del prompt, con su texto exacto.
- Componentes utilizados en cada versión.
- Observaciones que registró el participante sobre cada prueba.
- Reflexión comparativa.
- Ambigüedades pendientes.
- Prompt actual, si es distinto de las versiones guardadas.

Distinguir claramente:

- Información proporcionada por el taller.
- Decisiones y textos escritos por el participante.
- Versiones guardadas.
- Observaciones declaradas por el participante.

No afirmar que se ejecutaron pruebas que la herramienta no puede comprobar.

El Reporte visible y el Markdown descargado deben basarse en una única fuente de datos y coincidir.

Debe poder descargarse aunque la actividad esté incompleta.

## 5. Eliminar funciones innecesarias

Eliminar el botón:

**«Regenerar desde mis respuestas»**

Y la lógica asociada que ya no sea necesaria.

Actualmente el prompt se ensambla automáticamente y el botón suele producir un resultado idéntico, por lo que confunde al usuario.

La nueva interacción debe ser más sencilla:

- Escribir.
- Ver cómo cambia el prompt.
- Copiar.
- Guardar versión.
- Probar en ChatGPT.
- Comparar.

No conservar controles duplicados que realicen esencialmente la misma operación.

## 6. Protección del trabajo

Mantener `localStorage` para conservar:

- Caso activo.
- Tarea seleccionada.
- Campos de construcción.
- Prompt actual.
- Versiones guardadas.
- Observaciones.
- Reflexiones.
- Pestaña activa.

Los datos de los casos A y B deben permanecer separados.

Al cambiar de caso:

- Regresar a la pestaña 1.
- Restaurar los datos existentes del caso seleccionado.
- No borrar las versiones del otro caso.

Si la persona recarga la página, debe recuperar su trabajo.

Validar defensivamente los datos restaurados.

No convertir objetos, números o arreglos en cadenas como `[object Object]`.

Si el almacenamiento falla, permitir continuar usando la herramienta durante la sesión.

El reinicio debe solicitar confirmación y aclarar si se eliminarán los datos de ambos casos.

## 7. Diseño de la pestaña principal

La pestaña 2 debe funcionar en escritorio y móvil.

En escritorio, utiliza una disposición de dos columnas cuando haya espacio suficiente:

- Izquierda: componentes editables.
- Derecha: prompt actualizado y botones para copiar, guardar y abrir ChatGPT.

En pantallas pequeñas, mostrar las secciones una debajo de otra.

Evitar que el área del prompt quede demasiado lejos de los campos que lo modifican.

Puedes utilizar un panel lateral con posición fija durante el desplazamiento en escritorio, siempre que no obstruya el contenido.

Mantener la identidad visual:

- Azul `#00314F`.
- Dorado `#C9A227`.
- Blanco y grises neutros.
- Tipografía legible.
- Sin logos institucionales.

No agregar animaciones innecesarias ni elementos visuales que distraigan del aprendizaje.

## 8. Requisitos técnicos

Entregar un único HTML completo y autónomo:

`de_la_solicitud_al_prompt.html`

Con CSS y JavaScript embebidos.

Sin frameworks, CDN ni dependencias externas.

Sin conexión con APIs de IA.

El único enlace externo de la actividad será el botón para abrir ChatGPT mediante una acción explícita del participante.

La herramienta debe seguir funcionando offline para construir, guardar versiones y generar reportes; abrir ChatGPT requerirá conexión.

Mantener controles accesibles, navegación por teclado, etiquetas claras y diseño responsive.

Sanitizar cualquier texto de usuario que se incorpore al DOM.

No sobrescribir versiones guardadas cuando cambien los campos.

No perder respuestas al cambiar de caso.

No crear commits ni modificar archivos de Quarto.

## 9. Pruebas solicitadas

Verifica los siguientes escenarios:

1. Seleccionar Caso A y una tarea.
2. Copiar el prompt base.
3. Agregar contexto y observar cómo cambia el prompt.
4. Agregar condiciones y observar cómo cambia.
5. Agregar resultado esperado.
6. Guardar Versión 1.
7. Modificar campos y guardar Versión 2.
8. Comprobar que la Versión 1 conserva su texto original.
9. Guardar Versión 3.
10. Intentar guardar una cuarta versión sin sobrescribir las anteriores.
11. Copiar una versión guardada.
12. Abrir ChatGPT en una nueva pestaña.
13. Registrar observaciones diferentes para dos versiones.
14. Dejar una versión sin probar.
15. Registrar reflexión comparativa.
16. Cambiar entre casos A y B.
17. Recargar y restaurar el trabajo.
18. Reiniciar con confirmación y cancelar el reinicio.
19. Generar Reporte con actividad parcial.
20. Comparar Reporte visible y Markdown.
21. Abrir la actividad en pantalla de 390 px.
22. Probar almacenamiento corrupto o incompleto.
23. Comprobar funcionamiento offline, salvo el enlace a ChatGPT.

Distingue las pruebas realmente ejecutadas de las verificadas únicamente mediante inspección del código.

## 10. Restricciones finales

No agregar nuevos casos todavía.

No agregar más pestañas.

No crear cuestionarios.

No evaluar automáticamente los prompts.

No generar respuestas simuladas de ChatGPT.

No incluir respuestas modelo que anticipen las decisiones del participante.

No hacer que la herramienta ejecute las instrucciones por el usuario.

No modificar las actividades anteriores.

No modificar Quarto.

No publicar.

## Entregable

Devuelve el HTML completo actualizado y una descripción breve de los cambios.

La experiencia debe enseñar una idea central:

**Una instrucción más precisa no es necesariamente una instrucción más larga. Su calidad depende de comunicar claramente la necesidad, la tarea, las condiciones y el resultado esperado, sin dejar decisiones importantes a interpretaciones arbitrarias.**

El participante debe descubrir esto mediante la construcción y comparación de sus propios prompts.


