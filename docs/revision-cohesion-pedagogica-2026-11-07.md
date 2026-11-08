# Revisión de cohesión y pedagogía del taller «Antes del prompt»

**Fecha:** 7 de noviembre de 2026
**Estado revisado:** rama `feat/taller-interactivo-v2`, commit `0237643` (publicado en `gh-pages` el 7 nov 2026, 00:51)
**Alcance:** todas las páginas del recorrido, los prompts P0–P6, la plantilla de bitácora, la tarjeta de práctica y el texto visible de las cinco aplicaciones. El sitio se renderizó completo (17 páginas) sin avisos y sin enlaces internos rotos.
**Qué no se hizo:** no se modificó ningún archivo salvo este reporte; no se probaron los prompts con una IA; no se recorrieron las aplicaciones con el ratón ni con lector de pantalla.

Este reporte complementa `revision-proyecto-2026-11-06.md`, que describía el estado anterior a la reorganización del 6 de noviembre.

---

## 1. Resumen

La **idea del taller es clara, valiosa y está bien expresada**: con IA, producir es fácil; lo difícil es saber qué pedir, qué delegar y cómo comprobar. Tras la reorganización, el recorrido tiene un **hilo conductor visible**: las seis etapas, las cuatro competencias 4D, las cuatro etiquetas de evidencia y la bitácora aparecen con los mismos nombres de la portada a la práctica. La práctica guiada es ahora la pieza que integra todo.

Los riesgos principales ya no son de contenido sino de **diseño de la sesión**:

1. **Tiempo.** La sesión dura dos horas y el recorrido completo, estimado con prudencia, pasa de 140 minutos (sección 4.1).
2. **Cambio de caso sin explicación.** Las tres actividades usan secuencias FASTA o una aplicación web; el resto usa el Excel FAIR. Nadie le dice al participante por qué.
3. **Respuestas adelantadas que quedan.** Tres lugares todavía revelan lo que el participante debe descubrir.
4. **La especificación «la escribes tú» está demasiado resuelta.** El modelo aparece cuatro veces antes de que el participante escriba la suya.
5. **«¿Qué puedo aceptar?» no se actualizó** con el formato y el vocabulario del resto.
6. **Los prompts P1, P5 y P6 no se han vuelto a probar** con una IA desde que se reescribieron.

---

## 2. La idea del taller

### Lo que funciona

- **Tesis nítida y repetida con coherencia.** «La IA puede hacerlo. ¿Tú sabes qué hizo, por qué lo hizo y cómo comprobarlo?» abre la portada, cierra la práctica y es fácil de recordar.
- **Título y subtítulo alineados.** «Antes del prompt» + «Qué pedir, qué delegar y cómo comprobar lo que hace la IA en investigación» corresponden a las tres preguntas de la tesis.
- **El malentendido del título está atendido.** `01-contexto` aclara que «antes del prompt» no significa esperar para usar la IA, sino comprender la tarea antes de delegarla.
- **Honestidad epistémica constante:** datos simulados, respuestas simuladas, «no certifica FAIR», «síntesis didáctica, no método validado», «falta volver a probar los prompts». Es coherente con lo que el taller enseña y le da credibilidad.
- **El caso es un buen vehículo.** El Excel tiene trampas reales y graduadas (`prom.`, celda vacía, `b0014`/`dnaK`, «valores procesados») que obligan a distinguir lo observado de lo supuesto.

### Lo que puede mejorar

- **Tres frases destacadas compiten.** La portada tiene una y `01-contexto` dos («Cuando producir resultados se vuelve más fácil…» y «No se trata de hacer el trabajo antes que la IA…»). Las tres dicen variantes de la misma idea. Conviene que haya **una sola frase canónica**, la de la portada, y que `01` la desarrolle en lugar de reformularla.
- **La portada dice «ponencia y taller»** (nombre de la sesión en el programa), pero el sitio no distingue qué parte es ponencia. Si la sesión tiene una exposición inicial, convendría decir qué páginas la acompañan.

---

## 3. Cohesión del recorrido

### Mapa actual

| Bloque | Página | Etapas | Caso que usa | Papel |
|---|---|---|---|---|
| Inicio | Portada | — | — | Tesis, objetivo, aprendizajes, alcance, ruta |
| Antes | `00-preparacion` | — | Excel (prueba) | Requisitos y prueba del asistente |
| Comprender | `01-contexto` | — | Excel (mención) | Por qué; infografía de actividades |
| Comprender | `02-ejemplos` | — | Tres situaciones | Vocabulario y fallas típicas |
| Comprender | `03-metodo` | 1–6 | Excel (ejemplos 4D) | Método y 4D |
| Comprender | ¿Qué falta por definir? | 1–3 | **FASTA / app web** | Precisar una solicitud |
| Construir | `03b-estructura-prompt` | 4 | Excel (P0 vs. B) | Componentes del prompt |
| Construir | De la solicitud al prompt | 4 | **FASTA / app web** | Construir y probar prompts |
| Evaluar | ¿Qué puedo aceptar? | 5 | **FASTA** | Discernir afirmaciones |
| Caso | `04-caso-fair` | (prepara 1–3) | Excel | Encargo, datos, FAIR, producto |
| Caso | `05-practica` | 1–6 | Excel | Práctica integral con IA y verificación |
| Cierre | `07-bitacora` (fuera del menú) | 6 | Excel | Revisión final del registro |

### Hilos que sí conectan

- **Etapas:** se presentan en `03`, se practican parcialmente en las actividades (cada paso dice su etapa) y completas en `05`.
- **4D:** definidas en `03` con ejemplos del Excel, usadas como lista de revisión en `03b` y marcadas en cada paso de `05` y en la bitácora.
- **Etiquetas de evidencia** (observado, inferido, por confirmar, verificado): unificadas en prompts, diagramas, práctica, tarjeta y bitácora.
- **Bitácora:** una plantilla con una sección por paso; los recuadros «Para tu bitácora» de `05` corresponden a esas secciones.
- **Verificación:** integrada en el paso 4 de la práctica; el diagrama «Un solo chat, dos actores» ya la mostraba ahí.

### Rupturas de cohesión

1. **El cambio de caso no está explicado (alta).** Las tres actividades interactivas usan FASTA o una aplicación web, entre dos páginas que usan el Excel (`03b` y `04`). El participante pasa Excel → FASTA → Excel → FASTA → FASTA → Excel. Puede ser una decisión pedagógica buena (practicar la habilidad en un problema sencillo y luego transferirla), pero **ninguna página lo dice**. Basta con una frase en la portada y en la primera actividad: *«Las actividades usan otro caso a propósito: practicas cada habilidad en un problema sencillo antes de aplicarla al caso FAIR.»*
2. **Los reportes de las actividades casi no se usan después (media).** `05` los ofrece en una caja plegable «por si te sirven», pero ningún paso los pide. Como tratan otro caso, su valor en la práctica es bajo. O se integran explícitamente (por ejemplo, en el paso 3: «retoma cómo reformulaste la solicitud en la actividad»), o se dejan como registro personal sin mencionarlos en `05`.
3. **«Comprender el problema» y «Caso» se pisan (baja).** `04` vuelve a plantear el encargo y la ambigüedad de «seguir FAIR», que ya se vieron en `02` (ejemplo 3) y `03b`. Ahora está bien conectado («Ya conoces este archivo…»), pero el participante encuentra el Excel en cuatro páginas antes de la práctica.
4. **La numeración P0, P1, P5, P6 es heredada (media).** El salto se explica con «P2–P4 no son prompts», pero es una explicación de algo que no debería necesitarla. Renumerar (P0–P3) o nombrar los prompts por su función (Encargo, Vocabulario, Diagnóstico, Autorrevisión) haría el recorrido más claro. Es un cambio importante para quien reutiliza el material, según `CONTRIBUTING.md`.

---

## 4. Pedagogía

### Lo que está bien resuelto

- **Activar antes de explicar.** Los ejemplos de `02` piden pensar antes de abrir la respuesta, `04` pide anotar tres cosas antes de mostrar la lista y la verificación pide llegar a una conclusión antes de abrir Mons et al.
- **Ejemplo resuelto, luego práctica.** `03b` muestra P0 frente a la versión B, y la práctica pide construir la propia especificación.
- **Metacognición y registro.** La bitácora por pasos obliga a anotar en el momento, no a reconstruir al final.
- **Transferencia.** «Para pensar» en `03b` (tabla con citas, extracción de artículos, redacción, script) lleva la habilidad fuera del caso FAIR.
- **Evaluación formativa.** Autoevaluación en `05` y lista de revisión en `07`, con criterios observables.

### 4.1 Tiempo y carga (alta)

La sesión dura dos horas. Una estimación prudente del recorrido completo:

| Bloque | Minutos estimados |
|---|---|
| Introducción, tres ejemplos y método (`01`–`03`) | 25 |
| ¿Qué falta por definir? | 10 |
| Del problema al prompt (`03b`) | 10 |
| De la solicitud al prompt (incluye probar en la IA) | 15 |
| ¿Qué puedo aceptar? | 10 |
| Caso de estudio (`04`) | 10 |
| Práctica: P0, P1, especificación, P5, P6, verificación y bitácora | 50–60 |
| **Total** | **≈ 130–140** |

Sin contar tiempos muertos (esperar respuestas de la IA, problemas de cuenta, participantes en línea). El diseño v2 protegía la verificación y definía qué recortar primero; **esa decisión ya no está escrita en ningún lado**. Recomendaciones:

- Decidir qué páginas son **lectura previa** (por ejemplo `01` y `03`) y no se recorren en la sesión.
- Marcar en la portada qué actividades son **imprescindibles** y cuáles **opcionales** si falta tiempo (candidatas a opcionales: «De la solicitud al prompt» completa, el Explorador FAIR, «Para pensar», la ampliación).
- Mantener la regla de prioridad de la verificación, que ya está en `05`, y extenderla a la sesión completa en una guía docente (privada).

### 4.2 La especificación propia está demasiado resuelta (alta)

`05` dice «la escribes tú», pero antes de escribirla el participante ya vio el modelo cuatro veces:

1. La versión B de `03b`, que es casi la especificación más P5.
2. La lista de la parte A en el paso 3, que ya trae los contenidos (resultado: diagnóstico documental; alcance: unidades, condiciones, réplicas y celda vacía; límites…).
3. El ejemplo plegable del paso 3.
4. El texto de P5, que repite alcance y restricciones.

El riesgo es que la especificación se vuelva copiar y no decidir. Opciones:
- En el paso 3, **convertir la lista A en preguntas** («¿Qué resultado buscas? ¿Qué dejas fuera? ¿Qué cuenta como evidencia?») y dejar las respuestas solo en el ejemplo plegable.
- Usar en `03b` como ejemplo resuelto **otro caso** (por ejemplo FASTA, que ya trabajaron en las actividades), para que el Excel quede «fresco» para la práctica.
- Aligerar P5 para que no repita lo que dice la especificación pegada.

### 4.3 Respuestas que todavía se adelantan (alta)

| Dónde | Qué adelanta | Sugerencia |
|---|---|---|
| `02-ejemplos`, recuadro inicial | Nombra las tres fallas («tarea indefinida», «cita real que no respalda la afirmación», «metadatos inventados») antes de los ejemplos, que ahora tienen títulos neutros y respuestas plegables | Cambiar por algo como «Tres situaciones para analizar antes de ver qué falló» |
| `02-ejemplos`, tabla de conceptos, fila FAIR | «FAIR no equivale a "abierto"» es la conclusión de la verificación obligatoria | Dejar «no equivale a un formato particular ni a un sí/no universal» |
| `04-caso-fair`, recuadro inicial | Enumera unidades, condiciones, réplicas y celda vacía antes de pedir «anota tres cosas que no puedes saber» | Decir «un diagnóstico de lo que falta saber» y nombrar los cuatro asuntos solo en «Qué vas a producir» |

### 4.4 El 4D se presenta en muchas tablas (baja)

Hay tablas 4D en `03-metodo`, `03b`, `05`, `07`, la tarjeta y la plantilla. Cada una tiene un propósito distinto (definir, revisar un prompt, ubicar en la práctica, registrar), así que no es repetición literal, pero la sensación puede ser de saturación. Si hubiera que recortar, la de `07` es la más prescindible: la plantilla ya trae la competencia en cada sección.

### 4.5 Facilitación

El sitio es un buen manual para el participante, pero **no hay guía docente** en el repositorio (por diseño: `privado-docente/` está excluido). Para una sesión de dos horas con participantes en línea, la guía es imprescindible: tiempos, qué recortar, respuestas esperadas de P5 y de la verificación, y qué hacer si la IA no responde o no acepta archivos. Conviene confirmar que existe y está al día con la v2.2.

---

## 5. Integración de las actividades

| Actividad | Integración con el recorrido | Observaciones |
|---|---|---|
| ¿Qué falta por definir? | **Buena.** Cada paso indica su etapa; conecta con el ejemplo 1 y con `03b` | Caso distinto del Excel sin explicar |
| De la solicitud al prompt | **Buena.** Equivalencia de bloques con los siete componentes; sin ChatGPT | Probar en la IA consume tiempo |
| ¿Qué puedo aceptar? | **Débil.** La página no se actualizó | Ver abajo |
| Explorador FAIR | Opcional, enlazado desde `04` para observar el Excel | Duplica abrir el Excel; útil si alguien no tiene programa de hojas de cálculo |
| Bitácora (app) | Retirada del recorrido | El archivo se sigue publicando sin enlaces |

**«¿Qué puedo aceptar?» necesita la misma revisión que las otras dos páginas de actividad (media):**
- Repite el título en negritas debajo del encabezado.
- No tiene sección «Para qué sirve» ni dice su etapa (5, Verificación) ni su competencia en inglés y español.
- No conecta con lo anterior ni con lo siguiente (el caso de estudio).
- Usa «pendiente» como decisión («Aceptar / Corregir / Dejar pendiente»), mientras que en la práctica «pendiente» es solo la conclusión de una verificación no hecha. Es aceptable porque aquí es una *acción*, pero conviene decirlo o usar «Dejar por confirmar».

**Tono de las aplicaciones (baja):** el Explorador FAIR y «¿Qué puedo aceptar?» mezclan *usted* («Seleccione», «su criterio») con el *tú* del sitio, y algunos títulos usan mayúsculas al estilo inglés («Toma de Decisiones y Rigor»). La de discernimiento muestra «Taller v2.2» en la cabecera.

---

## 6. Consistencia terminológica

- **«Pendiente» frente a «por confirmar»:** quedan restos en `03b` («marca esos datos como pendientes» en la tabla «Qué cambia…») y en la versión B («lo que requiere consulta externa»). Conviene usar las etiquetas unificadas también en el ejemplo resuelto.
- **P0 está duplicado:** `03b` lo escribe a mano en lugar de incluir `_prompts/p0.md`. Si se cambia P0, puede quedar distinto en las dos páginas.
- **Etiquetas de página:** `01`, `03` y `04` dicen «Antes o durante el taller». Si se decide qué es lectura previa (4.1), las etiquetas deberían reflejarlo.

---

## 7. Pendientes técnicos y de repositorio

- **Publicación y `main` desincronizados (alta).** `gh-pages` se publicó el 7 nov 00:51 desde la rama de trabajo, pero `main` sigue en `24cb967` (v1.4). El código del sitio en vivo no está en la rama principal. Conviene fusionar la rama en `main`.
- **Analítica de visitas sin aviso (media).** Se añadió Cloudflare Web Analytics. La sección «Privacidad y uso responsable» de `00-preparacion` no lo menciona. Aunque Cloudflare no usa cookies, por transparencia conviene una línea en esa sección o en el pie.
- **Prompts sin volver a probar (alta).** `08-referencias` lo declara. Correr la práctica completa en al menos dos asistentes antes del 26 de noviembre.
- **Documentos obsoletos:** `docs/desarrollo-v2.2-*.md` describen una navegación anterior; `PROMPT_PARA_CURSOR.md` habla de nueve páginas y 120 minutos; el README no tiene la v2.2 en el historial.
- **Archivos huérfanos publicados:** `recursos/agenda-practica.svg` y `interactivos/bitacora_minima_4d.html` se copian al sitio sin que ninguna página los enlace.
- **`Claude outputs/`** sigue en la carpeta, sin versionar, con una copia de la plantilla de bitácora.

---

## 8. Recomendaciones priorizadas

### Alta (antes de la sesión)

1. Definir la **ruta mínima de dos horas**: lectura previa, imprescindibles y opcionales; marcarla en la portada.
2. **Explicar el cambio de caso** (FASTA → Excel) en la portada y en la primera actividad.
3. Quitar las **tres respuestas adelantadas** de la sección 4.3.
4. **Reducir el modelo de especificación** en el paso 3 (preguntas en lugar de respuestas) o cambiar el caso del ejemplo resuelto de `03b`.
5. **Probar P0–P6** en dos asistentes y actualizar «Estado del material».
6. **Fusionar la rama en `main`.**

### Media

7. Actualizar la página **«¿Qué puedo aceptar?»** al formato de las otras actividades.
8. Decidir el papel de los **reportes de las actividades** en la práctica.
9. Considerar **renumerar los prompts** o nombrarlos por función.
10. Mencionar la **analítica** en la sección de privacidad.

### Baja

11. Una sola **frase destacada** canónica.
12. Unificar el **tono (tú)** y las mayúsculas en las aplicaciones.
13. Incluir P0 desde `_prompts/` en `03b`.
14. Limpiar documentos obsoletos y archivos huérfanos; actualizar el historial del README.

---

## 9. Conclusión

El taller tiene una idea fuerte y ahora un recorrido que la sostiene de principio a fin: el participante entiende el problema, aprende a delimitar, practica con casos sencillos y aplica todo a un caso realista, registrando y verificando por su cuenta. Lo que queda por resolver es sobre todo **cuánto cabe en dos horas** y **cuánto se le deja descubrir al participante**: son las dos decisiones que más pueden cambiar la experiencia real de la sesión, y conviene tomarlas antes de pulir más el contenido.
