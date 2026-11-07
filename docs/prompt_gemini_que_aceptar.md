# Diseñar aplicación interactiva: ¿Qué puedo aceptar de una respuesta de IA?

Actúa como diseñador instruccional especializado en investigación científica, alfabetización en IA y desarrollo de aplicaciones educativas interactivas.

Necesito que desarrolles en **Gemini Canvas** una aplicación web educativa, en un único archivo HTML con CSS y JavaScript integrados.

La aplicación forma parte de la **versión 2.2** del taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica».**

## 1. Contexto pedagógico

El taller enseña a investigadores a colaborar con IA mediante las competencias **AI Fluency 4D**:

- Delegation: decidir qué delegar a la IA.
- Description: comunicar necesidades e instrucciones.
- Discernment: evaluar críticamente resultados.
- Diligence: actuar responsablemente y documentar decisiones.

Los participantes ya realizaron dos actividades:

1. **¿Qué falta por definir?** Aprendieron a detectar ambigüedades y decisiones pendientes en solicitudes científicas sencillas.
2. **De la solicitud al prompt.** Aprendieron a decidir qué delegar, construir instrucciones, probarlas en ChatGPT y comparar respuestas.

Ahora necesitamos practicar **Discernment**.

La actividad posterior será un desafío integrador sobre un Excel simulado de expresión génica, en el que aplicarán FAIR, 4D y prompting.

**Importante:** esta aplicación NO debe adelantar ni resolver el desafío FAIR. Usaremos un ejemplo sencillo de análisis de secuencias FASTA para practicar la verificación.

## 2. Objetivo

Que el participante aprenda a distinguir entre:

- Una afirmación respaldada por los datos disponibles.
- Una inferencia plausible que no está demostrada.
- Una afirmación que requiere información adicional.
- Una afirmación que necesita consultar una fuente externa.
- Una afirmación contradicha por la evidencia.

No se trata de evaluar si la respuesta de IA parece bien redactada, sino si puede aceptarse con base en evidencia.

La aplicación no debe calificar automáticamente al participante ni revelar inmediatamente las respuestas correctas.

## 3. Caso científico

Presenta un pequeño archivo FASTA ficticio con tres secuencias de ADN, claramente identificadas como datos simulados.

Las secuencias deben ser cortas y permitir contar nucleótidos manualmente.

Incluye una respuesta simulada de IA que contenga entre cinco y seis afirmaciones de diferente naturaleza:

- Un conteo correcto.
- Un conteo incorrecto.
- Una interpretación plausible pero no demostrada.
- Una afirmación que requiere información sobre el origen de las secuencias.
- Una recomendación que dependería de documentación externa.

Los conteos deben verificarse cuidadosamente al construir el ejemplo.

Identifica claramente la respuesta como **simulación didáctica**, no como una ejecución real de ChatGPT.

No inventes referencias científicas ni afirmes haber consultado fuentes externas.

## 4. Experiencia interactiva

Organiza la actividad en cuatro momentos, utilizando pestañas o estaciones:

### Estación 1. Examinar

El participante ve:

- El FASTA.
- La respuesta simulada de IA.
- Una pregunta inicial: «¿Qué afirmaciones aceptarías sin comprobar y por qué?».

No muestres todavía una clasificación resuelta.

### Estación 2. Contrastar

Presenta cada afirmación de manera individual.

Permite seleccionar una clasificación:

- Observada y respaldada.
- Inferida.
- Por confirmar.
- Requiere verificación externa.
- Contradicha por los datos.

Solicita una justificación breve.

Cuando una afirmación depende del FASTA, permite registrar qué secuencia o fragmento la respalda.

El participante debe poder corregir sus decisiones.

### Estación 3. Decidir

Para cada afirmación, solicita una acción:

- Aceptar.
- Corregir.
- Consultar una fuente.
- Consultar al responsable de los datos.
- Dejar pendiente.

Incluye una pregunta sobre el nivel de verificación:

«¿Cambiaría tu decisión si el resultado fuera a utilizarse en una publicación científica?».

Incluye también la reflexión:

«¿Pedirle a la IA que revise su respuesta equivale a verificarla?».

La retroalimentación debe ser orientadora y contextual, no una calificación ni una respuesta automática.

### Estación 4. Reporte

Genera un reporte visible en Markdown que incluya:

- Identificación del caso.
- Afirmaciones examinadas.
- Clasificación elegida por el participante.
- Evidencia o justificación registrada.
- Decisión tomada.
- Verificaciones pendientes.
- Reflexión final.

Permite copiar y descargar el reporte `.md`.

No declares que una fuente fue verificada si el participante no registró la evidencia real de esa comprobación.

## 5. Requisitos de experiencia de usuario

Usa la identidad visual que hemos empleado en el taller:

- Azul oscuro UNAM: `#00314F`.
- Dorado: `#C9A227`.
- Fondo blanco y grises neutros.
- Tipografía legible.
- Diseño sobrio, científico y profesional.

La aplicación debe:

- Funcionar en escritorio y móvil.
- Utilizar pestañas claras.
- Guardar el avance en `localStorage`.
- Permitir reiniciar con confirmación.
- Funcionar sin API, backend, cuentas ni conexión a un modelo.
- Ser compatible con un iframe dentro de Quarto.
- No utilizar frameworks externos ni recursos CDN.
- Mantener separadas las respuestas del participante y los datos de ejemplo.
- Renderizar cualquier texto escrito por el participante de forma segura, sin interpretarlo como HTML ejecutable.
- Contar con etiquetas accesibles, navegación por teclado y mensajes de estado comprensibles.

## 6. Criterios pedagógicos indispensables

La aplicación debe enseñar explícitamente que:

1. Una respuesta convincente no necesariamente es correcta.
2. La autorrevisión de un modelo no sustituye la verificación independiente.
3. La evidencia determina qué podemos aceptar, no la seguridad con que responde la IA.
4. No todas las afirmaciones requieren la misma profundidad de comprobación.
5. Cuando falta información, mejorar el prompt no necesariamente resuelve el problema.
6. «No está documentado» no equivale a «no existe».
7. Es válido dejar una afirmación pendiente.
8. Una persona puede utilizar una hoja de cálculo, un script, una fuente primaria o consultar a un experto en lugar de insistir en el chat.

No conviertas estas ideas en una conferencia dentro de la aplicación. Deben surgir de decisiones que toma el participante.

## 7. Alcance y restricciones

Esta aplicación es una actividad de aprendizaje de aproximadamente **20 minutos**.

No debe convertirse en un curso completo de FASTA, bioinformática ni principios FAIR.

No incluyas puntuaciones, medallas, porcentajes de aciertos ni certificaciones.

No introduzcas el Excel FAIR en este ejercicio: ese archivo se reserva para el desafío integrador final.

No generes automáticamente una justificación que el participante no haya escrito.

No registres como realizadas pruebas, consultas o verificaciones que no ocurrieron.

## 8. Entregable

Genera una aplicación completa, funcional y autocontenida en un solo HTML.

Incluye comentarios técnicos breves donde sean necesarios.

Antes de darla por terminada, revisa:

- Coherencia científica de las afirmaciones.
- Exactitud de los conteos FASTA.
- Funcionamiento de las estaciones.
- Persistencia del estado.
- Seguridad al mostrar texto escrito por el usuario.
- Correspondencia entre el reporte visible y el Markdown descargado.
- Comportamiento en pantallas pequeñas.

**Primero presenta la aplicación en Canvas para revisarla. No generes todavía archivos Quarto ni instrucciones para publicar.**


