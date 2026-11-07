# Prompt de actualización para Gemini Canvas
## Explorador FAIR — Reporte final, identidad visual UNAM y mejoras pedagógicas

Actúa como **diseñador instruccional y desarrollador front-end especializado en aprendizaje activo, gestión de datos científicos, principios FAIR, accesibilidad y aplicaciones educativas interactivas**.

Estamos desarrollando una herramienta para el taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica»**

La aplicación se llama **Explorador FAIR** y ya existe una primera versión HTML funcional.

Quiero que actualices la aplicación existente, conservando el contenido científico, las dos hojas del Excel simulado y las funcionalidades útiles.

Esta solicitud reúne tres objetivos:

1. Incorporar una sección final independiente llamada **Reporte**, con un resumen completo y descarga Markdown.
2. Aplicar una identidad visual académica inspirada en los colores de la UNAM.
3. Corregir problemas pedagógicos y funcionales identificados en la primera versión.

**No crees una aplicación diferente. Mejora la versión existente y entrega el HTML completo actualizado.**

---

# 1. Organización general de la aplicación

Mantén cuatro estaciones de aprendizaje:

1. **Observar**
2. **Interpretar**
3. **Preguntar**
4. **Sintetizar**

Agrega una quinta sección:

5. **Reporte**

La sección Reporte es una síntesis del trabajo realizado, **no una actividad adicional que deba aprobarse**.

La navegación superior debe mostrar:

`Observar | Interpretar | Preguntar | Sintetizar | Reporte`

Características obligatorias:

- Navegación libre entre todas las secciones.
- Ninguna sección debe bloquearse por respuestas incompletas.
- Reporte debe poder abrirse desde el inicio.
- El estado de avance debe reflejar actividades realmente realizadas.
- No utilizar puntuaciones, notas, porcentajes de acierto, rankings ni medallas.
- Mantener las respuestas al cambiar de sección o recargar la página.
- Evitar que una falla en una actividad impida navegar a las demás.

La sección Sintetizar debe permitir revisar las conclusiones personales y formular una reflexión final.

La sección Reporte debe reunir todos los resultados registrados en las actividades anteriores.

---

# 2. Regla pedagógica central: descubrir antes de recibir la respuesta

**No reveles anticipadamente las respuestas que el participante debe descubrir.**

El objetivo es que una persona investigadora explore el archivo, identifique sus límites, reconozca incertidumbres y formule preguntas por sí misma.

No muestres al inicio:

- Las cuatro incertidumbres principales del caso.
- Una lista de problemas que debe encontrar.
- Las respuestas esperadas.
- Un diagnóstico FAIR elaborado.
- Conclusiones predeterminadas.
- Ejemplos dentro de los campos que contengan directamente la respuesta buscada.
- Opciones seleccionadas automáticamente.

Implementa retroalimentación progresiva:

**Observar → responder → recibir una pista si se necesita → revisar → comprender.**

Para cada desafío:

1. Presenta una pregunta neutral.
2. Permite el primer intento.
3. Ofrece una primera pista que oriente dónde mirar o qué comparar.
4. Si persiste la dificultad, ofrece una segunda pista más concreta.
5. Permite modificar la respuesta.
6. Después de un intento, ofrece una explicación contextual que pueda abrirse voluntariamente.
7. No bloquees el avance si alguien no consigue responder.

Las pistas no deben revelar directamente la conclusión.

Cuando una respuesta sea abierta o existan varias interpretaciones razonables, solicita evidencia y justificación. **No utilices palabras clave para simular una evaluación científica automática.**

Reconoce como válidas las respuestas que expresen incertidumbre bien fundamentada.

---

# 3. Mejorar la estación Interpretar

En la versión actual, la estación Interpretar anuncia directamente cuatro elementos del archivo:

- El encabezado `Estrés A (prom.)`.
- La celda `D7`.
- La anotación «Valores procesados».
- La anotación sobre réplicas.

Esto revela gran parte de las situaciones que queremos que el participante descubra.

## Nueva interacción

La estación debe comenzar con una consigna general:

**«Explora el archivo y selecciona un elemento que te genere alguna duda sobre su interpretación».**

Permite elegir una celda o una nota desde las hojas del Excel.

Después de la selección:

1. Mostrar el nombre de la hoja, la coordenada y el contenido literal.
2. Preguntar qué puede afirmarse directamente.
3. Preguntar si existe alguna interpretación que necesite confirmación.
4. Permitir registrar una justificación.
5. Ofrecer pistas graduales si se necesitan.
6. Permitir revisar la interpretación.
7. Guardar lo que la persona escribió.

Los elementos importantes del caso deben estar contemplados internamente para ofrecer retroalimentación contextual cuando se seleccionen, pero **no deben mostrarse como una lista inicial de problemas**.

Cuando la celda seleccionada no tenga retroalimentación específica, utiliza preguntas generales sobre evidencia, contexto y límites de interpretación.

No inventes una explicación particular para celdas que no la tengan.

## Revisión y corrección

Cuando exista una interpretación inicial y otra revisada, conserva ambas.

Distingue:

- Lo que el participante observó.
- Lo que interpretó.
- La evidencia indicada.
- La revisión que realizó.
- Lo que todavía necesita confirmar.

No presentes la revisión como una respuesta validada automáticamente.

---

# 4. Identidad visual inspirada en la UNAM

Actualiza la interfaz para utilizar una paleta académica consistente con las futuras herramientas interactivas del taller.

## Paleta principal

| Uso | Color | Código |
|---|---|---|
| Azul principal | Azul UNAM de referencia para el taller | `#00314F` |
| Acento | Dorado | `#C9A227` |
| Fondo de tarjetas | Blanco | `#FFFFFF` |
| Fondo secundario | Gris claro | `#F3F4F6` |
| Texto secundario | Gris medio | `#64748B` |
| Texto principal | Gris oscuro | `#1F2937` |

Se trata de una paleta de trabajo inspirada en la identidad universitaria, no de una declaración de colores institucionales oficiales.

## Colores funcionales

| Uso | Fondo | Texto sugerido |
|---|---|---|
| Información | `#DCEAF2` | `#00314F` |
| Confirmación | `#E8F3EA` | `#24613A` |
| Precaución o pista | `#FFF3D6` | `#835C10` |

Utiliza colores de texto que cumplan requisitos de contraste y legibilidad.

## Reglas de aplicación

- Azul oscuro para encabezado, títulos, navegación activa y botones principales.
- Dorado para detalles de identidad, separadores, acentos e indicadores discretos.
- Blanco y gris claro para fondos y áreas de trabajo.
- Verde suave para retroalimentación sustentada.
- Ámbar suave para pistas, incertidumbres y cuestiones pendientes.
- Azul suave para información contextual.

Evita grandes superficies doradas, fondos saturados, degradados llamativos, sombras excesivas o elementos infantiles.

**Nunca dependas solamente del color para comunicar un estado.** Acompáñalo de texto e iconos cuando corresponda.

No utilices el escudo ni logotipos oficiales de la UNAM.

## Variables CSS

Organiza la paleta utilizando variables CSS en `:root`, por ejemplo:

```css
:root {
  --unam-blue: #00314F;
  --unam-gold: #C9A227;

  --background: #F3F4F6;
  --surface: #FFFFFF;

  --text-primary: #1F2937;
  --text-secondary: #64748B;

  --info-bg: #DCEAF2;
  --info-text: #00314F;

  --success-bg: #E8F3EA;
  --success-text: #24613A;

  --warning-bg: #FFF3D6;
  --warning-text: #835C10;
}
```

Puedes añadir variantes más oscuras o claras cuando sean necesarias para estados hover, foco, bordes y contraste.

Mantén una estética científica, sobria, moderna y legible.

La tabla Excel debe continuar siendo el elemento visual protagonista.

---

# 5. Nueva sección final: Reporte

Incorpora una última sección independiente con el título:

# Reporte

Subtítulo:

**Mi exploración del dataset: observaciones, interpretaciones y preguntas pendientes**

Esta sección debe poder consultarse en cualquier momento, incluso cuando el participante todavía no haya contestado nada.

## Contenido obligatorio

Genera un resumen dinámico con las siguientes secciones.

### 1. Mi necesidad

Mostrar la necesidad que el participante escribió.

Si todavía no existe ese campo en las actividades, agrégalo en la estación Observar con una pregunta breve:

**«¿Qué necesitas lograr con estos datos?»**

No lo completes automáticamente.

### 2. Lo que observé en el archivo

Mostrar las observaciones registradas.

Cuando la persona haya asociado su observación con una celda, incluir:

- Hoja.
- Coordenada.
- Contenido literal consultado.
- Observación escrita.

No atribuir una observación a una celda que el participante no haya señalado.

### 3. Mis interpretaciones

Mostrar:

- Interpretación inicial.
- Evidencia indicada.
- Clasificación seleccionada.
- Interpretación revisada, cuando exista.
- Pistas consultadas, si se registraron.

No añadir respuestas modelo.

### 4. Mis incertidumbres prioritarias

Recuperar las incertidumbres identificadas durante la exploración.

No completar automáticamente con las cuatro incertidumbres previstas internamente.

### 5. Mis preguntas para continuar

Mostrar las preguntas formuladas por el participante.

Para cada pregunta:

- Elemento relacionado.
- Pregunta.
- Destinatario o fuente.
- Importancia.

### 6. Qué podría hacer con IA

Mostrar qué actividades considera delegables a una IA y cuáles requieren conocimiento experimental o consulta documental.

Esta distinción debe proceder de la respuesta real del participante.

### 7. Qué sigue pendiente

Mostrar únicamente los aspectos pendientes registrados.

**No introducir conclusiones fijas sobre metadatos, unidades, cepa, réplicas ni celdas vacías.**

### 8. Mi reflexión final

Mostrar la respuesta a:

**«Antes de pedir ayuda a una IA, ¿qué cambió en tu comprensión del problema?»**

## Tratamiento de información incompleta

Cuando algún apartado no tenga información registrada, mostrar:

**Sin respuesta**

No ocultar apartados ni completarlos automáticamente.

En el Reporte puede mostrarse una indicación discreta como:

«Esta sección todavía no tiene una respuesta registrada. Puedes regresar a la actividad correspondiente».

No presentar automáticamente el contenido faltante como una respuesta incorrecta.

---

# 6. Descarga Markdown

En la sección Reporte incorpora un botón principal:

**Descargar reporte (.md)**

Debe generar localmente:

`explorador-fair-reporte.md`

Mediante JavaScript del navegador, sin backend ni servicios externos.

El archivo debe contener:

```markdown
# Explorador FAIR — Reporte de exploración

**Taller:** Antes del prompt
**Caso:** Expresión génica simulada
**Fecha:** [fecha local]

## 1. Mi necesidad
[respuesta real]

## 2. Observaciones
- Hoja:
- Celda:
- Contenido observado:
- Mi observación:

## 3. Interpretaciones y revisiones
- Elemento:
- Interpretación inicial:
- Evidencia:
- Clasificación:
- Interpretación revisada:

## 4. Incertidumbres prioritarias
[respuestas reales]

## 5. Preguntas para continuar
- Elemento:
- Pregunta:
- Destinatario:
- Importancia:

## 6. Qué podría hacer con IA
[respuesta real]

## 7. Aspectos pendientes
[respuestas reales]

## 8. Reflexión final
[respuesta real]
```

Requisitos:

- El Markdown debe reflejar las respuestas reales.
- Debe coincidir con el contenido visible en Reporte.
- No debe incluir soluciones ni explicaciones como si fueran respuestas del participante.
- No debe afirmar que se realizó una verificación externa.
- Debe permitir descargar reportes incompletos.
- Debe utilizar «Sin respuesta» cuando falte información.
- Debe conservar las referencias a hojas y celdas que realmente fueron registradas.

---

# 7. Corregir problemas conocidos del HTML actual

Revisa y corrige expresamente:

### Error de referencia

En `downloadMarkdown()` existe una referencia incorrecta:

```javascript
appState.st1.ch1
```

Debe recuperarse la respuesta desde el estado correcto de la estación Interpretar.

Revisa también las demás referencias utilizadas para construir el reporte.

### Conclusiones fijas

La versión actual incluye una frase predeterminada en «Qué sigue pendiente»:

«Metadatos del experimento, confirmación de cepa de E. coli, definición de unidades y significado de la celda D7».

Elimina ese contenido como respuesta del participante.

Esa información puede permanecer como criterio interno pedagógico, pero no debe incorporarse al reporte si la persona no la escribió.

### Selección de celdas

Asegúrate de que:

- La celda seleccionada pueda registrarse como evidencia de una observación.
- La hoja y la coordenada se conserven correctamente.
- Seleccionar una celda no se interprete como haber completado una actividad.
- La selección siga funcionando con teclado.

### Estado y navegación

Revisa:

- Persistencia en `localStorage`.
- Actualización del Reporte al modificar respuestas.
- Recuperación del estado después de recargar.
- Reinicio completo mediante confirmación.
- Consistencia entre las cinco secciones de navegación.

No introduzcas datos ficticios adicionales.

---

# 8. Fidelidad al Excel

Conserva exactamente las dos hojas:

- `Expresion_genica`
- `Notas_experimento`

Mantén sus valores, encabezados y celdas vacías.

En particular:

- `Expresion_genica!D7` debe permanecer vacía.
- No interpretar «prom.» automáticamente.
- No afirmar que no existieron réplicas.
- No asignar unidades.
- No identificar la cepa de *E. coli*.
- No inventar procedimientos de normalización.
- No transformar una anotación parcial en un hecho experimental comprobado.

La aplicación representa un dataset simulado, no datos científicos reales.

---

# 9. Accesibilidad y comportamiento

Conserva e implementa:

- HTML semántico.
- Navegación completa mediante teclado.
- Foco visible.
- Botones accesibles.
- Etiquetas explícitas.
- `fieldset` y `legend` cuando correspondan.
- `aria-live` para retroalimentación.
- Contraste suficiente.
- Alternativas al uso exclusivo del mouse.
- Diseño responsive.
- Reporte accesible mediante navegación libre.
- Botones de descarga y reinicio funcionales.

Evita que los errores de JavaScript en una actividad deshabiliten la navegación general.

---

# 10. Restricciones técnicas

El resultado debe seguir siendo:

- Un único HTML autónomo.
- CSS embebido.
- JavaScript embebido.
- Sin React.
- Sin frameworks.
- Sin backend.
- Sin Node.
- Sin APIs externas.
- Sin login.
- Sin tracking.
- Sin dependencias externas obligatorias.
- Funcional sin conexión a internet.
- Con persistencia local transparente.
- Con descarga Markdown.
- Sin llamadas a modelos de IA.

No modifiques archivos de Quarto.

No generes documentos independientes adicionales.

---

# 11. Verificación funcional obligatoria

Antes de entregar, revisa los siguientes escenarios.

1. Abrir la aplicación por primera vez: ninguna respuesta aparece contestada.
2. Abrir Reporte sin completar actividades.
3. Escribir una necesidad y comprobar que aparece en Reporte.
4. Cambiar de estación y regresar sin perder respuestas.
5. Seleccionar una celda y registrar una observación vinculada a ella.
6. Introducir una interpretación y posteriormente corregirla.
7. Solicitar una pista sin revelar inmediatamente la solución.
8. Recargar la página y recuperar las respuestas.
9. Descargar un reporte parcialmente completado.
10. Verificar que el Markdown contiene las respuestas reales.
11. Verificar que no aparecen conclusiones científicas predefinidas.
12. Verificar que los campos incompletos dicen «Sin respuesta».
13. Reiniciar la aplicación y comprobar que se limpian las respuestas.
14. Navegar mediante teclado.
15. Comprobar la visualización de las dos hojas.
16. Verificar que la celda `D7` sigue vacía.
17. Comprobar que los botones funcionan sin conexión.
18. Confirmar que ninguna actividad asigna calificaciones.
19. Confirmar que el esquema visual utiliza los nuevos colores.
20. Confirmar que Reporte siempre está disponible.

Distingue pruebas ejecutadas realmente de verificaciones realizadas solo mediante inspección del código.

No afirmes que probaste el HTML en navegador si no lo hiciste.

---

# 12. Entregable final

Devuélveme:

1. **El HTML completo actualizado**, no parches ni fragmentos.
2. Un resumen breve de los cambios realizados.
3. Una explicación de la estructura de las cinco secciones.
4. Una lista de las variables CSS principales.
5. Una descripción de cómo funciona la exportación Markdown.
6. Las pruebas realmente ejecutadas y las que quedan pendientes.

No solicites confirmación antes de realizar los cambios.

## Principio final

**La herramienta debe ayudar a pensar, no sustituir el razonamiento de la persona.**

El participante debe descubrir las respuestas mediante la exploración, recibir orientación cuando la necesite y conservar en el Reporte un registro fiel de lo que realmente hizo, interpretó y decidió.

