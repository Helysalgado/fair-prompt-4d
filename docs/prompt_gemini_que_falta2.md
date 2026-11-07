# Ajustes pedagógicos y de navegación — ¿Qué falta por definir?

Modifica la aplicación HTML existente `qu_falta_por_definir.html`.

No crees una aplicación nueva ni cambies su estructura general.

Conserva las cuatro pestañas, los dos casos, el diseño azul/dorado, la persistencia local y el Reporte Markdown.

## A. Mejorar el Caso B: aplicación web

Reformula las pistas del Caso B para explorar cinco dimensiones:

1. **Interacción:** cómo ingresará información el usuario (archivo, caja de texto u otra modalidad).
2. **Validación:** qué deberá verificar la aplicación antes de procesar una secuencia.
3. **Funcionalidades:** qué análisis realizará realmente.
4. **Resultados:** cómo se visualizarán y descargarán.
5. **Tecnología y funcionamiento:** qué necesidades podrían influir en utilizar procesamiento local en el navegador o un servicio de servidor.

No afirmes que una arquitectura tecnológica específica sea obligatoria.

No presentes las decisiones de implementación como requisitos que siempre deban resolverse antes de iniciar.

El propósito es que el participante distinga entre lo que necesita que haga la aplicación y cómo podría construirse.

## B. Corregir el cambio de caso

Cuando el participante cambie del Caso A al Caso B o viceversa:

- Activar automáticamente la pestaña `1. Identificar`.
- Actualizar la pestaña visible y su estado accesible.
- Mostrar la solicitud inicial correspondiente al nuevo caso.
- Restaurar las respuestas anteriores de ese caso.
- Conservar intactas las respuestas del caso que acaba de abandonar.
- Guardar correctamente caso y pestaña activa en `localStorage`.

Al recargar, restaurar el caso y la pestaña donde estaba trabajando la persona.

## C. Evitar adelantar respuestas

En la pestaña `1. Identificar`, elimina los ejemplos de los campos de respuesta.

Utiliza únicamente placeholders neutrales.

En la pestaña `2. Explorar`, no muestres desde el inicio las cinco dimensiones del problema como títulos descriptivos.

Las pistas deben ser progresivas:

- Primera pista: orientación amplia.
- Segunda pista: explorar otra dimensión de la tarea.
- Tercera pista: ayudar a distinguir decisiones que afectan el resultado.
- Orientaciones adicionales, si existen, solo como material opcional.

No deben funcionar como una lista de respuestas esperadas.

Distingue entre:

- Preguntas formuladas por el participante.
- Pistas consultadas.
- Decisiones que todavía no están confirmadas.

No infieras automáticamente que consultar una pista equivale a haber tomado una decisión.

## D. Asegurar el descubrimiento

Primero debe aparecer la solicitud inicial y un espacio para reflexionar.

Después del primer intento, el participante puede consultar las pistas.

Si no sabe qué escribir, puede registrar «No sé» y acceder a la ayuda.

No evalúes respuestas automáticamente.

No completes ni reformules automáticamente la solicitud.

## E. Reporte y persistencia

Mantén el Reporte visible y el Markdown sincronizados.

Conserva por caso:

- Preguntas propias.
- Pistas consultadas.
- Solicitud revisada.
- Decisiones pendientes.

Al reiniciar, limpia los datos del caso activo y regresa a la pestaña 1.

Revisa que la restauración desde `localStorage` sea defensiva ante estados incompletos o incompatibles.

## F. Pruebas

Verifica específicamente:

1. Cambiar de caso desde el Reporte regresa a Identificar.
2. Las respuestas del Caso A no aparecen en el Caso B.
3. Regresar a un caso recupera sus respuestas.
4. Recargar restaura caso y pestaña.
5. Las pistas permanecen ocultas inicialmente.
6. Los placeholders no contienen respuestas.
7. Las pistas consultadas aparecen en el Reporte.
8. El Markdown coincide con el Reporte.
9. Reiniciar afecta únicamente el caso activo.
10. El HTML funciona sin conexión.

Si no puedes ejecutar pruebas reales en navegador, indícalo expresamente.

Entrega el HTML actualizado completo. No modifiques Quarto ni publiques.

