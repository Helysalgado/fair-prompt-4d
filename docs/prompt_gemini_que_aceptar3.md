Revisa la versión actual de la aplicación **«¿Qué puedo aceptar de una respuesta de IA?»** (`ai_discernment_tool(3).html`).

La nueva dinámica de pistas, validación y retroalimentación me parece adecuada. **No quiero rediseñarla.** Necesito corregir tres problemas antes de aprobarla.

### 1. Corregir la consistencia científica

Verifica programáticamente los conteos a partir de las secuencias FASTA originales.

Los resultados correctos son:

| Secuencia | Longitud | A | T | C | G | GC |
|---|---:|---:|---:|---:|---:|---:|
| Seq_01 | 30 | 9 | 7 | 6 | 8 | 46.7 % |
| Seq_02 | 24 | 6 | 6 | 6 | 6 | 50 % |
| Seq_03 | 36 | 12 | 8 | 7 | 9 | 44.4 % |

Corrige los comentarios, los metadatos y especialmente los textos de retroalimentación que utilizan números anteriores.

Evita duplicar conteos numéricos en explicaciones escritas manualmente. Cuando sea posible, genera los detalles de la validación directamente desde los resultados calculados.

No alteres las secuencias para hacerlas coincidir con explicaciones incorrectas.

### 2. No anticipar las respuestas en la primera estación

En «Examinar» muestra únicamente los encabezados y las cadenas FASTA.

No muestres inicialmente las longitudes, los conteos de A/T/C/G ni los porcentajes GC.

Los resultados calculados podrán aparecer después, cuando el participante presione «Validar mi respuesta» en la estación «Contrastar».

Conserva las pistas opcionales, pero evita que revelen los resultados antes de que el participante intente verificarlos.

### 3. Corregir la retroalimentación de «Decidir»

Actualmente la aplicación evalúa la coherencia entre la clasificación y la acción elegidas por el participante.

Esto puede producir retroalimentación engañosa: una clasificación equivocada puede recibir un mensaje positivo si la acción coincide con ella.

Quiero que la orientación considere también la evidencia conocida del caso.

Por ejemplo:

- Una afirmación comprobable mediante el FASTA puede aceptarse después de contrastar el dato.
- Una interpretación no demostrada no debe convertirse en un hecho, aunque el participante la haya clasificado como respaldada.
- Una sugerencia metodológica puede considerarse útil sin presentarse como resultado científico.
- Una afirmación sin información suficiente puede mantenerse pendiente.

Evita aprobar automáticamente una decisión solo porque coincide con la clasificación seleccionada.

Como la aplicación no puede interpretar de forma fiable una justificación escrita libremente, no debe afirmar que ha evaluado su calidad. La retroalimentación automática debe limitarse a las clasificaciones, acciones y evidencias predefinidas.

### 4. Mantener el diseño pedagógico aprobado

Conserva:

- Las cuatro estaciones.
- Las cinco afirmaciones actuales.
- Los botones «Necesito una pista» y «Validar mi respuesta».
- La retroalimentación consistente, parcial o que invita a revisar.
- La posibilidad de corregir respuestas y validar nuevamente.
- El reporte Markdown.
- La persistencia local.
- La identidad visual del taller.
- La ausencia de calificaciones y puntuaciones.

### 5. Verificación técnica

Comprueba también que:

- Los datos del FASTA y las explicaciones coinciden.
- La retroalimentación no aparece antes de solicitarla.
- Cambiar una clasificación no conserva una validación anterior como si siguiera vigente.
- `localStorage` recupera únicamente campos y valores válidos.
- El reporte no presenta la retroalimentación automática como una verificación científica independiente.
- La aplicación funciona sin dependencias externas y puede integrarse en un iframe Quarto.

Entrega la versión HTML completa en Canvas.

**No cambies otras actividades ni la estructura del curso. No integres todavía en Quarto.**


