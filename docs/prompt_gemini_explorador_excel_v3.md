# Refinamiento de Explorador FAIR — Visualizaciones y Reporte

Trabaja sobre la versión más reciente de **Explorador FAIR**, que ya incluye las secciones Observar, Interpretar, Preguntar, Sintetizar y Reporte, y utiliza una paleta visual inspirada en los colores de la UNAM.

Quiero mejorar la experiencia de la sección **Reporte**, incluyendo una visualización útil cuando existan datos suficientes, y corregir algunos problemas de interacción y registro.

**No reconstruyas la aplicación desde cero. Conserva su diseño general, las actividades y los datos exactos del Excel simulado.**

## 1. Reporte con visualizaciones significativas

La sección Reporte debe presentar una síntesis visual y escrita del trabajo realizado.

En esta herramienta agrega una visualización titulada:

**¿Cómo clasifiqué los elementos que exploré?**

Implementa una gráfica de barras horizontal que muestre cuántos elementos fueron clasificados por el participante en cada categoría:

- Lo observo directamente en el archivo.
- Es una interpretación o hipótesis plausible.
- Necesito más información para afirmarlo.

### Requisitos de la gráfica

- Calcular las cantidades exclusivamente a partir de `appState.st2.items`.
- Contar únicamente los elementos que tengan una clasificación seleccionada.
- No contar celdas simplemente visitadas.
- No incluir ejemplos ni respuestas ficticias.
- Mostrar cantidades enteras y etiquetas legibles.
- Identificar el total de elementos clasificados.
- Utilizar azul UNAM, dorado y gris, con buen contraste.
- Incluir una alternativa textual accesible con las mismas cantidades.
- Mostrar un estado vacío cuando todavía no existan clasificaciones.
- Actualizar la gráfica automáticamente cuando cambien las respuestas.
- No usar librerías externas: implementarla mediante HTML/CSS o SVG sencillo.
- No presentar la gráfica como una calificación ni como evaluación de exactitud científica.

Debajo de la gráfica incluir esta aclaración:

«Esta visualización describe tus clasificaciones durante la exploración. No determina si son correctas ni evalúa el cumplimiento FAIR».

### Gráfica en el archivo Markdown

En el Markdown descargable incluye una tabla con las categorías y cantidades reales.

Si es posible, añade una representación textual sencilla de barras, compatible con Markdown.

No dependas de imágenes externas, bibliotecas gráficas ni archivos adicionales para que el reporte pueda interpretarse.

## 2. Corregir el apartado «Aspectos pendientes»

Actualmente el Reporte utiliza `appState.st1.q3` para mostrar aspectos pendientes, aunque ese campo corresponde a otra pregunta.

Corrige esta relación.

En la estación Sintetizar agrega una pregunta abierta:

**«¿Qué información o decisiones siguen pendientes después de tu exploración?»**

Guarda su respuesta en un campo independiente del estado.

La sección «Aspectos pendientes» debe utilizar exclusivamente esa respuesta.

Si no existe, mostrar «Sin respuesta».

No completar automáticamente ese apartado con metadatos ni incertidumbres previstas por el diseño.

## 3. Mejorar la exploración de las dos hojas

La estación Interpretar debe permitir seleccionar elementos de ambas hojas:

- `Expresion_genica`
- `Notas_experimento`

Actualmente utiliza una copia de la tabla visible. Revisa su comportamiento para que sea posible cambiar de hoja dentro de la propia estación Interpretar.

Los elementos seleccionados deben conservar correctamente:

- Hoja.
- Coordenada.
- Contenido literal.
- Observación registrada.
- Clasificación.
- Interpretación revisada.

No considerar que seleccionar una celda equivale a completar su análisis.

El estado inicial no debe tener ninguna celda preseleccionada.

## 4. Retroalimentación sin adelantar respuestas

Revisa todas las pistas y los textos de ayuda.

En particular, algunas pistas sobre réplicas y procesamiento explican directamente la conclusión antes de que el participante haya razonado.

Mantén esta progresión:

1. Pregunta neutral.
2. Primer intento.
3. Pista general para dirigir la observación.
4. Segunda pista más específica, si es necesaria.
5. Posibilidad de corregir.
6. Explicación contextual posterior.

No reveles las incertidumbres previstas en una lista inicial.

No impidas avanzar si la persona no respondió.

Para preguntas abiertas, proporciona orientación, no una evaluación automática basada en palabras clave.

Evita placeholders que anticipen las respuestas que el participante debe descubrir.

## 5. Registrar el proceso de exploración

Cuando se soliciten pistas, registra cuáles fueron consultadas.

Distingue, cuando exista información suficiente:

- Primera observación o interpretación.
- Pistas consultadas.
- Clasificación realizada.
- Interpretación revisada.

No inventes una primera respuesta si la persona no la registró.

Incluye estos datos en el Reporte cuando correspondan.

El número de elementos explorados debe representar aquellos en los que realmente se registró una observación o clasificación, no solamente celdas seleccionadas.

## 6. Diseño visual

Conserva la paleta:

- Azul: `#00314F`
- Dorado: `#C9A227`
- Blanco: `#FFFFFF`
- Gris claro: `#F3F4F6`
- Texto oscuro: `#1F2937`

La visualización debe integrarse naturalmente en la sección Reporte.

Mantén una estética académica, sobria y accesible. No agregues gráficos decorativos, indicadores de logro ni tableros de rendimiento.

## 7. Regla general para futuras herramientas

Establece en comentarios del código esta convención de diseño:

**El Reporte puede incorporar tablas, gráficas o resúmenes visuales cuando existan datos suficientes y una pregunta concreta que justifique la visualización.**

No todas las herramientas necesitan gráficas.

La visualización debe:

- Responder una pregunta útil.
- Basarse en datos efectivamente registrados.
- Indicar qué representa y qué no representa.
- Respetar la incertidumbre.
- Tener alternativa textual.
- No sustituir la reflexión del participante.

## 8. Pruebas

Revisa especialmente:

1. Abrir Reporte con todas las actividades vacías.
2. Clasificar un elemento y comprobar que la gráfica muestra una unidad.
3. Cambiar la clasificación y comprobar que la gráfica se actualiza.
4. Analizar varios elementos de ambas hojas.
5. Dejar elementos sin clasificación y confirmar que no se contabilizan.
6. Registrar y corregir interpretaciones.
7. Registrar información pendiente en el campo correspondiente.
8. Descargar el Markdown y comparar las cantidades con la gráfica visible.
9. Recargar la aplicación y conservar las respuestas.
10. Reiniciar la actividad y comprobar que la gráfica vuelve al estado vacío.
11. Verificar que la celda `D7` sigue vacía.
12. Comprobar la navegación mediante teclado.

No declares ejecutadas pruebas que solamente hayas considerado o inspeccionado en el código.

## 9. Restricciones técnicas

- Un único archivo HTML autónomo.
- CSS y JavaScript embebidos.
- Sin dependencias externas obligatorias.
- Funcional offline.
- Sin APIs ni modelos de IA.
- Sin backend.
- Sin tracking.
- Sin calificaciones.
- Sin modificar los datos originales.
- Sin generar conclusiones científicas automáticamente.

## Entrega

Devuélveme el HTML completo actualizado y un resumen breve de las mejoras.

Explica también cómo se calculan las cantidades de la gráfica, cómo se representan en Markdown y qué pruebas quedan pendientes.

No solicites confirmación antes de realizar la actualización.

