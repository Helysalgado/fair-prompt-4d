# Diseñar aplicación interactiva: Bitácora mínima 4D

Actúa como diseñador instruccional y desarrollador de aplicaciones educativas para investigadores científicos.

Necesito una aplicación web interactiva en **Gemini Canvas**, desarrollada en un único archivo HTML con CSS y JavaScript integrados.

Forma parte de la versión 2.2 del taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica».**

## 1. Contexto del taller

Los participantes han trabajado previamente en:

1. Identificar qué falta por definir antes de solicitar ayuda a una IA.
2. Construir y mejorar instrucciones mediante prompting.
3. Examinar respuestas de IA y comprobar afirmaciones.
4. Decidir qué aceptar, corregir o dejar pendiente.

La actividad final consiste en examinar un **Excel simulado de expresión génica**, realizar un diagnóstico FAIR preliminar con apoyo de IA y distinguir entre:

- Información observada directamente en el Excel.
- Inferencias que necesitan confirmación.
- Información que debe consultar el responsable del experimento.
- Recomendaciones que requieren verificar documentación externa.

No se pide modificar el dataset, completar metadatos faltantes ni certificar que cumple con FAIR.

Ahora necesitamos una herramienta de cierre que permita documentar la colaboración con IA utilizando el marco **AI Fluency 4D**:

- **Delegation:** qué tareas decidimos delegar a la IA.
- **Description:** cómo comunicamos lo que necesitábamos.
- **Discernment:** cómo evaluamos las respuestas.
- **Diligence:** cómo actuamos responsablemente y documentamos decisiones.

## 2. Objetivo pedagógico

Al terminar, cada participante debe poder responder:

**¿Qué hice con ayuda de IA, cómo evalué sus resultados y de qué me hago responsable?**

La aplicación debe producir una bitácora breve, comprensible y útil para documentar una actividad científica.

No buscamos una declaración genérica como «utilicé ChatGPT».

Tampoco una transcripción completa de la conversación.

Queremos un registro de las decisiones relevantes.

## 3. Organización de la aplicación

Diseña una interfaz con cinco estaciones o pestañas.

### Estación 1. Mi trabajo

Solicita:

- Nombre breve de la actividad.
- ¿Qué necesitaba resolver?
- ¿Qué resultado esperaba obtener?

Proporciona como contexto predeterminado el caso del Excel simulado de expresión génica, pero permite editar las respuestas.

No inventes información experimental.

### Estación 2. Qué delegué — Delegation

Pregunta:

- ¿Qué tareas encargué a la IA?
- ¿Qué decisiones mantuve bajo mi responsabilidad?
- ¿Qué decidí no delegar?

Incluye ejemplos breves como ayuda opcional, sin completar automáticamente las respuestas.

Por ejemplo, identificar posibles problemas de documentación puede delegarse parcialmente; confirmar el diseño experimental requiere evidencia o consultar al responsable.

### Estación 3. Cómo trabajé con la IA — Description

Pregunta:

- ¿Qué información proporcioné?
- ¿Qué instrucciones o restricciones fueron importantes?
- ¿Qué cambié después de revisar una respuesta?

Permite pegar un prompt representativo, pero aclara que no se requiere copiar toda la conversación.

No hagas obligatorio registrar un modelo o versión si el participante no dispone de ese dato.

### Estación 4. Qué comprobé — Discernment

Esta es la sección más importante.

Solicita registrar hasta tres afirmaciones o resultados relevantes.

Para cada uno, permite indicar:

- Afirmación o resultado.
- Fuente o evidencia consultada.
- Tipo de comprobación realizada.
- Resultado de esa comprobación.
- Estado: respaldado, contradicho, parcialmente respaldado o pendiente.

Distingue claramente entre:

1. Leer una respuesta de IA.
2. Pedirle a la IA que revise su respuesta.
3. Comprobar el resultado contra una fuente independiente.

No presentes los dos primeros como equivalentes al tercero.

Si alguien indica que consultó una fuente externa, solicita cuál fue y qué parte comprobó.

**No marques automáticamente ninguna comprobación como realizada.**

Si el participante no pudo verificar un dato, debe poder registrar «Pendiente» sin penalización.

### Estación 5. Responsabilidad y reporte — Diligence

Pregunta:

- ¿Qué incertidumbres permanecen?
- ¿Qué acciones se necesitan antes de utilizar o publicar el resultado?
- ¿Quién debe confirmar la información pendiente?
- ¿Qué cuidados se tuvieron con los datos, la privacidad o las fuentes?

Incluye un campo breve para una reflexión final:

**«¿Qué aprendí sobre colaborar responsablemente con IA?»**

Genera una vista previa de la bitácora y permite copiar o descargar el reporte en Markdown.

## 4. Retroalimentación orientadora

La aplicación debe proporcionar feedback útil, pero no calificaciones.

Cuando el participante deje una sección vacía o escriba una respuesta demasiado genérica, puede recibir preguntas orientadoras como:

- ¿Qué tarea concreta recibió la IA?
- ¿Qué decisión tomaste tú?
- ¿Qué dato del archivo respalda esta afirmación?
- ¿La fuente fue realmente consultada o sigue pendiente?
- ¿Quién puede confirmar el dato experimental?
- ¿Qué necesitarías comprobar antes de publicar?

La orientación debe ser opcional.

No utilices un modelo de IA ni pretendas evaluar semánticamente textos libres.

Puedes detectar campos vacíos y ofrecer orientación basada en reglas simples.

No inventes verificaciones, responsabilidades, referencias ni decisiones.

## 5. Diseño visual y experiencia de usuario

Usa la identidad visual del taller:

- Azul oscuro: `#00314F`.
- Dorado: `#C9A227`.
- Fondo blanco.
- Grises neutros.
- Tipografía legible.
- Interfaz profesional, limpia y adaptable.

Conserva la familia visual de las aplicaciones anteriores.

Requisitos técnicos:

- HTML, CSS y JavaScript autocontenidos.
- Sin frameworks externos ni CDN.
- Sin backend ni API.
- Guardado local en `localStorage`.
- Reinicio con confirmación.
- Navegación entre estaciones sin pérdida de información.
- Exportación de Markdown.
- Funcionar dentro de un iframe Quarto.
- Compatibilidad móvil.
- Etiquetas accesibles y navegación por teclado.
- Mostrar de manera segura cualquier texto escrito por el participante.
- Manejar estados guardados incompletos o inválidos.

## 6. Reporte final

El Markdown debe ser breve y contener:

1. Identificación de la actividad.
2. Necesidad y resultado esperado.
3. Delegation: tareas delegadas y decisiones humanas.
4. Description: instrucciones, contexto y cambios.
5. Discernment: afirmaciones examinadas, evidencias y estado.
6. Diligence: incertidumbres, responsables y siguientes acciones.
7. Reflexión final.

Debe quedar claramente identificado como un **registro del participante**, no como una validación automática del análisis científico.

No afirmar que el dataset cumple FAIR ni que las comprobaciones se realizaron si el participante no lo documentó.

## 7. Restricciones pedagógicas

Esta actividad representa el cierre del taller, no un nuevo módulo extenso.

Debe poder completarse aproximadamente en **8–10 minutos**, utilizando las decisiones y evidencias generadas durante el desafío FAIR.

Por lo tanto:

- No exigir respuestas largas.
- No repetir todo el diagnóstico FAIR.
- No obligar a completar cinco formularios extensos.
- No introducir nuevas tareas científicas.
- No enseñar nuevamente el marco 4D desde cero.
- No incluir puntuaciones, medallas ni certificaciones.
- Permitir respuestas parciales y registrar información pendiente.

La bitácora debe complementar el diagnóstico, no sustituirlo.

## 8. Entregable

Desarrolla la aplicación funcional en Gemini Canvas.

Nombre del archivo propuesto:

`bitacora_minima_4d.html`

Antes de finalizar, revisa la coherencia pedagógica, los estados de navegación, la persistencia, la exportación Markdown y la experiencia móvil.

**No generes páginas Quarto, no modifiques otras actividades ni publiques la aplicación. Primero quiero revisar el prototipo.**


