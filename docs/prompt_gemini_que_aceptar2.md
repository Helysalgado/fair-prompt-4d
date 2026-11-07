Revisa la aplicación HTML que acabamos de desarrollar, «¿Qué puedo aceptar de una respuesta de IA?».

Quiero hacer un **ajuste pedagógico importante**: actualmente la respuesta simulada de IA parece contener demasiados errores, afirmaciones extremas y conclusiones científicas injustificadas.

El objetivo del ejercicio NO es enseñar que la IA siempre se equivoca. Queremos que los participantes aprendan a reconocer que una respuesta puede contener información correcta, recomendaciones útiles y algunas afirmaciones que necesitan comprobación.

### 1. Ajustar las afirmaciones

Conserva el caso FASTA de tres secuencias y las cuatro estaciones existentes.

Sustituye las cinco afirmaciones actuales por estas:

1. «El archivo contiene tres secuencias de ADN».
2. «La secuencia Seq_01 contiene 30 nucleótidos».
3. «La secuencia Seq_02 presenta un contenido GC del 50 %».
4. «Seq_03 es la secuencia más larga del archivo. Podría ser útil comparar su composición de nucleótidos con las otras secuencias».
5. «Las diferencias de longitud podrían estar relacionadas con las condiciones experimentales».

La mayoría son correctas o razonables. La última plantea una posible explicación que los datos no permiten confirmar.

### 2. Corregir los datos científicos

Los conteos correctos, obtenidos directamente de las cadenas FASTA actuales, son:

| Secuencia | Longitud | A | T | C | G |
|---|---:|---:|---:|---:|---:|
| Seq_01 | 30 | 8 | 7 | 7 | 8 |
| Seq_02 | 24 | 6 | 6 | 6 | 6 |
| Seq_03 | 36 | 10 | 8 | 8 | 10 |

Las tres tienen 50 % GC.

Verifica estos cálculos programáticamente a partir de las secuencias reales. No mantengas conteos manuales inconsistentes con los datos.

### 3. No revelar las respuestas

En la estación «Contrastar», actualmente aparece una «Pauta de orientación» que revela la clasificación correcta.

Esto elimina el razonamiento que esperamos del participante.

Sustituye esas pistas por preguntas orientadoras que no revelen la respuesta, por ejemplo:

- ¿Puedes comprobar esta afirmación directamente con el FASTA?
- ¿Qué operación necesitarías realizar?
- ¿La afirmación contiene más de una idea?
- ¿Qué parte está respaldada y qué parte necesitaría información adicional?
- ¿Es posible que una sugerencia sea razonable sin estar demostrada?

Las pistas deben ser contextuales y aparecer cuando el participante solicite ayuda.

### 4. Permitir afirmaciones parcialmente respaldadas

La afirmación 4 combina un dato comprobable con una sugerencia.

No obligues al participante a clasificar ambas partes como si fueran una sola conclusión indivisible.

Permite distinguir entre:

- Lo que puede comprobarse.
- Lo que constituye una sugerencia.
- Lo que requiere evidencia adicional.

La clasificación debe fomentar el razonamiento, no una única respuesta obligatoria.

### 5. Simplificar la experiencia

El ejercicio debe durar aproximadamente 20 minutos.

Evita términos innecesariamente especializados como «clasificación epistemológica» o «alucinación sistemática».

Utiliza preguntas como:

- ¿Qué afirma la IA?
- ¿Cómo lo comprobarías?
- ¿Qué evidencia tienes?
- ¿Qué harías con esta afirmación?

No exijas una justificación extensa para cada selección. Una explicación breve debe ser suficiente.

### 6. Mantener lo que ya funciona

Conserva:

- Las cuatro estaciones: Examinar, Contrastar, Decidir y Reporte.
- La identidad visual azul y dorado.
- El guardado local.
- La posibilidad de corregir decisiones.
- La exportación Markdown.
- La ausencia de calificaciones automáticas.

Al modificar las afirmaciones, revisa la persistencia para evitar que se recuperen clasificaciones de la versión anterior asociadas a afirmaciones diferentes.

### 7. Revisiones técnicas

Antes de mostrar la nueva versión:

- Comprueba los conteos reales a partir del FASTA.
- Asegura que las pistas no revelen las soluciones.
- Verifica que los textos del participante se muestren de forma segura.
- Revisa que la exportación refleje exactamente sus decisiones.
- No anuncies éxito al copiar si el portapapeles falla.
- Elimina la dependencia del CDN de Tailwind si queremos mantener la aplicación completamente autocontenida para Quarto.

### Resultado esperado

Presenta la aplicación HTML revisada en Gemini Canvas.

**No la integres todavía en Quarto. No cambies otras actividades del taller.**

El objetivo es que la aplicación enseñe a evaluar con criterio una respuesta de IA que es mayoritariamente útil, sin reducir Discernment a buscar errores deliberados.


