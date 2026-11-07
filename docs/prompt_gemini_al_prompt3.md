# Ajuste pedagógico — De la solicitud al prompt

Trabaja sobre la versión más reciente del archivo `de_la_solicitud_al_prompt.html`.

No crees una aplicación nueva. Conserva la estructura y las funcionalidades existentes.

## 1. Objetivo del ajuste

La actividad forma parte del taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica».**

Su objetivo principal es enseñar a los participantes a **comunicarse con precisión y reducir la ambigüedad al dar instrucciones a una IA**.

Actualmente, las solicitudes de referencia de los casos A y B están demasiado detalladas. Ya contienen muchas decisiones sobre entradas, operaciones, restricciones y resultados.

Esto reduce las oportunidades de aprendizaje, porque el participante podría limitarse a distribuir información existente entre los campos del prompt.

Queremos utilizar solicitudes intermedias: suficientemente claras para comprender la necesidad, pero con espacio para decidir qué delegar y cómo comunicarlo.

## 2. Sustituir las solicitudes de referencia

### Caso A — Análisis FASTA

Sustituye la solicitud actual por este texto exacto:

«Necesito analizar un archivo FASTA con varias secuencias de ADN para conocer la frecuencia de los nucleótidos. Quiero obtener resultados por secuencia y poder compararlos».

### Caso B — Aplicación web

Sustituye la solicitud actual por este texto exacto:

«Necesito desarrollar una aplicación web que permita introducir secuencias de ADN en formato FASTA, realizar análisis básicos y descargar los resultados. La aplicación debe ser sencilla de utilizar y ayudar a identificar entradas incorrectas».

Estos textos deben estar definidos directamente en el código HTML/JavaScript.

No deben depender de datos guardados en la actividad 2.

No deben presentarse como respuestas escritas por el participante.

Utiliza el encabezado:

**«Solicitud de partida»**

Debajo, una indicación breve:

«Esta solicitud ya expresa una necesidad. Tu tarea es decidir qué pedirle a la IA y cómo comunicarlo con precisión».

No incorporar automáticamente más detalles sobre datos, métodos, tecnologías o formatos.

## 3. Conservar la primera pestaña

Título:

**1. ¿Qué voy a delegar?**

Mantener:

- Selector de Caso A o Caso B.
- Solicitud de partida correspondiente.
- Pregunta «¿Qué quieres que haga la IA con esta solicitud?».
- Opciones de delegación específicas para cada caso.
- Opción «Otra tarea».

No agregar preguntas nuevas a esta pestaña.

Eliminar cualquier botón de importación, recuperación o sincronización con la actividad 2, si todavía existe.

La primera pestaña debe ser breve y permitir tomar una decisión concreta.

## 4. Ajustar la segunda pestaña

Título:

**2. Construir mis instrucciones**

Conservar los campos:

- Contexto y objetivo.
- Tarea.
- Condiciones y límites.
- Resultado y verificación.

Explicar brevemente que estos componentes sirven para reducir las interpretaciones posibles de una solicitud.

No son una fórmula rígida ni es obligatorio llenarlos todos.

La tarea seleccionada en la primera pestaña debe aprovecharse automáticamente, sin obligar a escribirla nuevamente.

El participante puede añadir detalles específicos cuando lo necesite.

No mostrar ejemplos que resuelvan las decisiones del participante.

### Información todavía no definida

Es importante transmitir que **comunicarse con precisión no significa tener todas las respuestas**.

Si falta información esencial, el participante puede indicar que la IA debe preguntar antes de proceder.

Incorpora esta idea de forma breve en la ayuda del campo «Condiciones y límites»:

«Indica qué debe respetar la IA, qué no debe suponer y qué debería preguntarte si falta información esencial».

No agregues otro campo ni una nueva actividad para esto.

## 5. Conservar la tercera pestaña

Título:

**3. Revisar mi prompt**

El prompt ensamblado debe incluir solamente:

- La solicitud de partida del caso elegido.
- La tarea seleccionada por el participante.
- El contexto adicional que haya escrito.
- Sus condiciones y límites.
- El resultado y los criterios de verificación que haya indicado.

No inventar información para completar campos vacíos.

Evitar duplicar la tarea seleccionada cuando se haya detallado posteriormente.

Conservar el prompt editable y el botón «Copiar prompt».

Si pulsa «Regenerar desde mis respuestas» después de editar manualmente el prompt, solicitar confirmación antes de sustituirlo.

Conservar las dos preguntas de revisión:

1. ¿Qué partes de tus instrucciones podrían interpretarse de más de una manera?
2. ¿Qué necesitas aclarar o confirmar antes de delegar la tarea?

No responder estas preguntas automáticamente.

## 6. Persistencia y casos

La actividad debe conservar sus propios datos en `localStorage`, de manera independiente.

Al cambiar de caso:

- Mostrar la solicitud de partida correspondiente.
- Restaurar las respuestas de ese caso.
- Regresar a la primera pestaña.
- No mezclar información entre A y B.

Al recargar, restaurar el caso activo, la pestaña y el trabajo escrito.

**Importante:** si existen datos guardados de versiones anteriores, las solicitudes antiguas no deben reemplazar los nuevos textos fijos. Las solicitudes de partida deben obtenerse siempre de las constantes actuales del código.

No eliminar silenciosamente las respuestas o los prompts manuales que ya existan.

## 7. Reporte

Conservar la cuarta pestaña y la descarga Markdown.

Utilizar la expresión **«Solicitud de partida»** para identificar el texto proporcionado por el taller.

Distinguirlo de las decisiones y respuestas del participante.

El reporte debe incluir el prompt final, las ambigüedades identificadas y las aclaraciones pendientes.

El Reporte visible y el Markdown descargado deben coincidir.

## 8. Conservar el diseño y comportamiento

No modificar:

- Los colores azul `#00314F` y dorado `#C9A227`.
- Las cuatro pestañas.
- La navegación libre.
- Las opciones de delegación de cada caso.
- La edición y copia del prompt.
- El Reporte Markdown.
- El reinicio con confirmación.
- El funcionamiento offline y responsive.

No añadir puntuaciones, evaluaciones automáticas ni nuevas actividades.

No modificar Quarto, Git, las actividades anteriores ni el sitio publicado.

## 9. Verificación

Comprueba que:

1. Ambos casos muestran exactamente las nuevas solicitudes.
2. Ningún texto antiguo almacenado sustituye las solicitudes fijas.
3. Las opciones de delegación corresponden al caso seleccionado.
4. La solicitud de partida aparece en el prompt ensamblado.
5. La tarea seleccionada se incorpora sin duplicaciones innecesarias.
6. Los campos vacíos no producen instrucciones inventadas.
7. Se conservan las ediciones manuales.
8. Cambiar de caso no pierde respuestas.
9. Recargar restaura el trabajo.
10. El Reporte y el Markdown coinciden.
11. La aplicación funciona sin conexión.
12. La interfaz es utilizable en pantallas móviles.

Indica cuáles pruebas ejecutaste realmente y cuáles están pendientes.

## Entregable

Devuelve el HTML completo actualizado y un resumen breve de los cambios.

**No amplíes el alcance. Este ajuste consiste en utilizar solicitudes intermedias y mantener el aprendizaje centrado en decidir qué delegar y comunicarse con precisión para reducir ambigüedades.**


