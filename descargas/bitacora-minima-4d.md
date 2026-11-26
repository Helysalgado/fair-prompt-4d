# Bitácora mínima de colaboración científica con IA

**Antes del prompt · ELIXIR México 2026**  
**Versión para participantes 1.1 · Presentación v20.2 · 26 de noviembre de 2026**

> Registra qué pediste, qué produjo la IA, qué comprobaste, qué decidiste y qué queda pendiente. Completa cada apartado cuando lo indique la instructora, con frases cortas. No leas los prompts de los retos posteriores antes de realizar P0. No adjuntes esta bitácora al chat durante los primeros retos.
>
> Distingue lo que la IA afirma haber hecho, la evidencia de ejecución y lo que comprobó una persona. Si algo no se comprobó, indica «pendiente» o «no se pudo determinar». No confundas una propuesta con un producto aceptado.

## Identificación

- **Equipo / integrantes:**
- **Fecha prevista:** 26/11/2026 (corregir si se realiza otro día).
- **Plataforma:**
- **Modelo:**
- **Versión y configuración, si se conocen:**
- **Tipo de chat:** nuevo / temporal / otro:
- **Memoria (si se conoce):** activa / desactivada / desconocida.
- **Contexto previo o archivos adicionales, si los hubo:**
- **Herramientas realmente utilizadas:**
- **Entrada:** `expresion_genica_caso_simulado.xlsx` (versión, si se conoce: ).
- **Referencia al chat o copia del historial (opcional):**

Materiales: https://helysalgado.github.io/fair-prompt-4d/

Si cambias de herramienta o modelo, anótalo en el paso correspondiente. No inventes identificadores de modelos ni configuraciones.

## Paso 1 · Necesidad — Reto 1 (Delegation)

**Encargo P0:**

> Tengo este Excel de expresión génica de cinco filas y tres condiciones. Voy a publicar un artículo y me piden que los datos sigan los principios FAIR. ¿Me ayudas a prepararlo?

Antes de ejecutar, marca tu apuesta (una o varias):

- [ ] A. Hará preguntas aclaratorias.
- [ ] B. Explicará FAIR y propondrá pasos generales.
- [ ] C. Producirá directamente una versión «FAIR» del Excel.

Abre un chat nuevo, adjunta únicamente el Excel y ejecuta P0.

- **¿Qué hizo realmente la IA?**
- **¿Quién decidió el alcance? ¿Coincidió con lo que entendiste del encargo?**

## Paso 2 · Vocabulario e incertidumbres

Si desconoces algún concepto (metadatos, FAIR, Zenodo, etc.), puedes pedir a la IA una explicación breve relacionada con el caso. Es opcional; no es una actividad adicional.

- **Concepto consultado y qué comprendí (opcional):**

Explora directamente las dos hojas del Excel. Identifica cuatro asuntos que requieren aclaración y registra los tres que consideres prioritarios.

| Asunto | Evidencia disponible (hoja/celda) | ¿Qué falta saber? |
|---|---|---|
| | | |
| | | |
| | | |

- **¿Detecté algún supuesto de la IA sin evidencia en P0?**

## Paso 3 · Especificación — preparación del reto 2

### A. Descomposición del problema o tarea en subtareas

Después de discutir la diapositiva 13, identifica qué podemos delegar y qué depende de una persona.

- **Una subtarea que podemos delegar a la IA y con qué límites:**
- **Una subtarea que requiere intervención humana y por qué:**

### B. Tarea seleccionada para el taller

Realizar un diagnóstico preliminar del Excel de expresión génica para identificar qué información falta y quién debe confirmarla. No estamos preparando todavía el depósito ni certificando FAIR.

### C. Especificación de la tarea

| Elemento | Especificación |
|---|---|
| Contexto | Excel del caso simulado; hojas `Expresion_genica` y `Notas_experimento`. |
| Resultado buscado | Diagnóstico preliminar. |
| Alcance: ¿qué asuntos revisar? | Recupera los del Paso 2 y la discusión del grupo. |
| Salida: ¿cómo queremos recibir el diagnóstico? | |
| Evidencia: ¿cómo localizar las observaciones? | |
| Restricciones: ¿qué no debe hacer la IA? | |

### D. Criterios de aceptación

Antes de ejecutar P5, escribe cómo sabrás si el diagnóstico cumple lo que necesitas. Registra al menos un criterio comprobable y, si hay tiempo, añade otros.

- **Criterio(s):**
- **¿Qué comprobaré personalmente?**

## Paso 4A · Colaboración — ejecución del reto 2

Revisa P5 cuando la instructora lo indique. Compáralo con tu especificación y tus criterios; úsalo tal cual o adáptalo sin ampliar el alcance acordado. Ejecútalo en el mismo chat.

**P5 — propuesta de instrucción (v20.2):**

> Con el Excel adjunto (hojas Expresion_genica y Notas_experimento), prepara un diagnóstico preliminar limitado a cuatro asuntos: (1) unidades y escala de los valores; (2) definición de las condiciones experimentales, incluido el significado de «prom.»; (3) información sobre réplicas; (4) valores faltantes: su identificación, significado y posibles causas que requieren confirmación. En particular, examina la celda D7, identificada durante nuestra exploración previa.
>
> Para cada asunto, entrega una fila con: lo observado y su ubicación (hoja y celda), lo que es inferencia, lo que falta confirmar, la acción siguiente, la persona o rol que lo confirmaría y el estado de evidencia (observado, inferido o por confirmar).
>
> Si encuentras otros asuntos, menciónalos aparte como hallazgos adicionales, sin ampliar el diagnóstico. No modifiques ni completes datos, no transformes valores y no declares cumplimiento FAIR. Termina con tres preguntas prioritarias para la investigadora.

- **Instrucción utilizada:** P5 oficial / adaptado.
- **Cambio y motivo (solo si adaptaste; conserva el texto exacto o su referencia):**
- **¿Qué produjo la IA? ¿Dónde queda el resultado?**
- **¿Qué información de P0 aprovechamos y qué cambió en alcance, contenido o evidencia?**

## Paso 4B · Verificación

### 1. Diagnóstico P5: comprobación humana

Abre el Excel original y comprueba dos celdas citadas por la IA. Si solo revisas una, registra una. No es una revisión completa.

| Hoja/celda | Afirmación de la IA | Contenido comprobado por el equipo / resultado |
|---|---|---|
| | | |
| | | |

- **Estado:** cumple en lo comprobado / parcial / requiere correcciones / sin revisión completa / pendiente.
- **Justificación, correcciones o asuntos no aceptados:**

### 2. Autorrevisión P6

Observa la demostración de la instructora; si la ejecutas, hazlo en el mismo chat después de P5.

> Audita tu diagnóstico anterior. Para cada afirmación indica si es un hecho observado en el archivo, una inferencia o un asunto por confirmar, y cuál requiere una fuente externa. Cuando algo no aparezca en el archivo, escribe «no está documentado en el archivo», no «no existe». Señala qué debería comprobarse y dónde. No marques nada como verificado: esa etiqueta solo la asigna una persona después de comprobarlo.

- **Modalidad:** demostración / ejecutado por el equipo / no realizado.
- **¿Detecté una clasificación incorrecta o una corrección que no corresponde al diagnóstico? ¿Qué evidencia tengo?**

### 3. Contraste con fuente primaria

Selecciona una afirmación de la IA que requiera
consultar una fuente externa al Excel.

- Afirmación de la IA:
- Fuente consultada (título y URL):
- Sección o pasaje relevante:
- ¿Qué dice realmente la fuente?
- Conclusión: respalda / contradice /
  no permite decidir / pendiente.
  
  
### 4. Semáforo

Registra una de las afirmaciones discutidas,
qué decisión o decisiones tomarías y por qué.

Puedes seleccionar más de una opción.

- Afirmación:
- Decisión:
  - [ ] Aceptar
  - [ ] Corregir
  - [ ] Consultar
  - [ ] Detener
- Evidencia o justificación:


### 5. Reto 3 · Discernment — nueva solicitud de análisis

La investigadora ahora quiere conocer cuánto cambia la expresión de los genes en las condiciones de estrés respecto al control. Es otra tarea con el mismo Excel, no un requisito FAIR. El ejercicio es exploratorio.

> Escribe un script en Python que calcule el fold change de Estrés A y Estrés B respecto al Control para cada gen del Excel, y muéstrame la tabla de resultados.

Ejecuta la instrucción en el mismo chat. No necesitas abrir una terminal.

| Qué revisar | Observación del equipo |
|---|---|
| ¿Qué hizo con D7? | |
| ¿Qué supuso sobre «prom.», unidades y escala? | |
| ¿Hay evidencia de ejecución? (sí / resultados sin evidencia / no se pudo determinar) | |
| ¿Comprobamos algún resultado numérico? ¿Cómo? | |

- **¿Es pertinente el cálculo con la información disponible? ¿Por qué?**
- **Decisión sobre el uso del resultado:**
- **Ubicación del script o tabla, si se conservaron:**

## Paso 5 · Registro y continuidad — Reto 4 (Diligence)

### A. Declaración de uso de IA

Pide primero un borrador en el mismo chat, sin adjuntar esta bitácora.

> Redacta un borrador de declaración de uso de IA para todas las actividades de este caso, desde el encargo inicial hasta los análisis exploratorios. Distingue lo incorporado, lo no adoptado, las verificaciones humanas y lo pendiente. No inventes lo que no esté documentado.

Compara el borrador con tus registros. Corrige directamente o comparte solo la información necesaria para que la IA lo revise. Estamos solicitando una declaración, no la generación de la bitácora.

- **¿Qué omitió, exageró o afirmó sin respaldo?**
- **Declaración corregida (un párrafo breve):**
- **Estado:** borrador / corregida pendiente de revisión / aceptada por el equipo.

### B. Entregable y pendientes

**Entregable previsto:** diagnóstico preliminar trazable, con bitácora y asuntos pendientes. Su estado depende de la revisión efectivamente realizada.

- **Estado real del diagnóstico:**

| Pendiente (registra dos prioritarios) | Quién debe confirmarlo |
|---|---|
| | |
| | |

- **Hallazgos adicionales, si los hubo (fuera del alcance de P5):**

### C. Decisiones y productos — base para dar continuidad

Registra al menos una decisión y un producto relevantes; añade filas cuando sea necesario. Puedes recuperar lo ya escrito, sin volver a redactar toda la bitácora. Conserva los estados históricos y no conviertas una propuesta de la IA en una decisión humana.

**D — Decisiones** (estados: propuesta / vigente / reemplazada / suspendida / por confirmar).

| ID | Decisión | Estado | Quién decidió | Origen (paso/evidencia) |
|---|---|---|---|---|
| D-01 | | | | |
| D-02 | | | | |
| D-03 | | | | |

**R — Resultados o productos** (estados: borrador / adoptado / no adoptado / exploratorio / auxiliar / por confirmar).

| ID | Producto | Estado | Quién revisó | Origen o ubicación |
|---|---|---|---|---|
| R-01 | | | | |
| R-02 | | | | |
| R-03 | | | | |

- **Última actualización (fecha y quién):**

## Cierre · Transferencia a mi trabajo

- **Un problema de mi trabajo al que aplicaría estas etapas y qué haría distinto al pedir, verificar o conservar lo que construya con IA:**

---

### Referencias y alcance de la plantilla

Las seis etapas son la propuesta metodológica del taller; Delegation, Description, Discernment y Diligence son capacidades transversales del marco AI Fluency. Los datos son ficticios. Esta bitácora no certifica FAIR ni constituye una implementación completa del marco de Cwik.

- Dakan, R., Feller, J. y Anthropic (2025). *AI Fluency: Framework & Foundations*. https://www.anthropic.com/ai-fluency
- Cwik, J. C. (2026). *Disclosure is not documentation*. https://doi.org/10.1186/s41073-026-00245-8
- Materiales de documentación: https://doi.org/10.17605/OSF.IO/A439J

Plantilla original: Heladia Salgado · Centro de Ciencias Genómicas, UNAM · taller «Antes del prompt» · CC BY 4.0. Adaptación prellenada con asistencia de ChatGPT; revisión y aprobación humana pendientes.
