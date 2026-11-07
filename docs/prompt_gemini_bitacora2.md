Revisa la aplicación actual `bit_cora_m_nima_4d.html`, correspondiente a la Bitácora mínima 4D del taller v2.2.

La aplicación es pedagógicamente adecuada, pero resulta demasiado extensa para un ejercicio de cierre de 8–10 minutos.

**No la reconstruyas desde cero. Conserva su diseño visual, el marco 4D, la navegación, las ayudas opcionales, el guardado local y la exportación Markdown.**

Quiero que realices los siguientes ajustes:

### 1. Reducir la carga de escritura

Mantén las cinco estaciones, pero simplifica sus campos:

- **Mi actividad:** muestra el contexto del Excel FAIR simulado como información de referencia. Permite editar únicamente una descripción breve de lo que se hizo o de su objetivo.
- **Delegation:** dos campos: «Qué encargué a la IA» y «Qué decisiones mantuve bajo mi responsabilidad».
- **Description:** dos campos principales: «Qué contexto o instrucciones fueron importantes» y «Qué ajusté después de revisar la respuesta». Permite registrar la herramienta o un prompt como información opcional.
- **Discernment:** solicita una comprobación representativa. Permite agregar hasta dos más si el participante lo desea.
- **Diligence:** registra «Qué quedó pendiente», «Qué haría después y quién debe confirmarlo» y una reflexión final opcional.

El participante debe poder registrar decisiones reales en pocas frases.

### 2. Simplificar Discernment

Para cada afirmación solicita:

1. Qué afirmación examinó.
2. Cómo intentó comprobarla.
3. Qué evidencia encontró o qué quedó pendiente.
4. Su estado final.

Evita seis campos independientes por afirmación.

Conserva explícita la diferencia entre lectura, autorrevisión de IA y comprobación independiente.

Si alguien selecciona «Respaldado» sin registrar una comprobación independiente, muestra una advertencia orientadora y conserva la incertidumbre en el reporte. No declares que hubo verificación.

No exijas registrar tres afirmaciones.

### 3. Reducir las ayudas visuales

Muestra las preguntas orientadoras únicamente cuando el participante solicite ayuda.

No despliegues automáticamente listas de preguntas por cada campo vacío.

No utilices señales visuales que sugieran que una estación está completada solo porque contiene texto predeterminado.

### 4. Revisar ejemplos

Utiliza únicamente ejemplos compatibles con el Excel simulado del taller.

No supongas que existen columnas como `log2FC` si no forman parte de los datos confirmados.

Son ejemplos apropiados:

- Unidad de expresión no documentada.
- Número de réplicas pendiente de confirmar.
- Condiciones de estrés insuficientemente descritas.
- Una celda vacía cuyo significado se desconoce.

No inventes metadatos experimentales.

### 5. Corregir problemas técnicos

- Evita reinstalar escuchadores de eventos al reiniciar la aplicación.
- Asegura que el reinicio restaure visualmente todos los campos.
- Maneja estados de comprobación inconsistentes sin crear afirmaciones de verificación falsas.
- Comprueba que `localStorage` restaure únicamente datos válidos.
- Mejora el control del foco en el modal de reinicio.
- Explica brevemente que los datos se guardan en el navegador y pueden permanecer en un equipo compartido.
- Conserva la protección al mostrar texto del participante.
- Verifica que el reporte Markdown coincida con las respuestas visibles.

### 6. Objetivo final

La aplicación debe permitir elaborar una bitácora auténtica y breve, no repetir el diagnóstico FAIR.

El resultado esperado es un reporte que explique:

- Qué se delegó a la IA.
- Cómo se trabajó con ella.
- Qué se contrastó con evidencia.
- Qué decisiones o incertidumbres permanecen bajo responsabilidad humana.

No debe evaluar ni certificar la calidad científica del diagnóstico.

Entrega la versión HTML completa en Gemini Canvas. No la integres todavía en Quarto.


