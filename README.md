# Antes del prompt · sitio Quarto del taller

Este repositorio contiene **contenido editorial listo para adaptar a un sitio Quarto**. No son diapositivas: se diseñó para que el sitio sea el recurso principal y una futura presentación sirva como guía de facilitación. Los capítulos `.qmd` son Markdown con un encabezado YAML mínimo y componentes nativos de Quarto.

## Publicable

- `index.qmd`: portada, propósito y navegación.
- `contenido/`: nueve páginas con fundamentos, situaciones críticas, metodología, caso FAIR, práctica, verificación, bitácora y fuentes.
- `recursos/`: siete SVG (cuatro originales, dos de ellos rehechos, y tres nuevos).
- `descargas/`: Excel ficticio para participantes y plantilla de bitácora (.docx y .md).
- `_quarto.yml`: configuración inicial de navegación y HTML. Se puede modificar en Cursor.

## No publicar

El ZIP privado separado contiene la carpeta `privado-docente/` con respuestas esperadas, guías de facilitación, la clave Excel y notas de la prueba de prompts. **No copiarla a `_site`, no incluirla en los recursos públicos y no publicarla en GitHub Pages.** Si el repositorio será público, lo más seguro es moverla fuera del repositorio antes de hacer commit.

## En Cursor / Quarto

1. Abrir esta carpeta como proyecto.
2. Revisar y ajustar `_quarto.yml`, títulos, estilo e imágenes; conservar las rutas relativas.
3. Tener Quarto instalado; ejecutar `quarto preview` para inspección y `quarto render` para construir el sitio.
4. Inspeccionar enlaces, callouts, tablas, SVG y descargas, también en móvil; publicar solo después de esa revisión.
5. Asegurar que no aparezcan contenidos de `privado-docente/` ni en el repositorio público ni en el sitio.

La transformación HTML **no fue ejecutada** como parte de este paquete. Los contenidos mantienen fechas, fuentes y la aclaración de que el piloto fue con IA, no con alumnado.

## Consistencia de la práctica

Se utilizan P0, P1, P5 y P6 en un chat continuo; la etapa 3 y 4 se realizan mediante especificación y decisiones humanas, y la 5 exige contraste en fuente primaria separado de la autorrevisión. Los datos son simulados y la meta es diagnosticar, no certificar FAIR.

## Registro AI Fluency 4D

- **Producto:** reorganización editorial de v1.6 en un paquete Markdown orientado a Quarto (22 de octubre de 2026).
- **Delegation:** IA reorganizó contenidos, redactó páginas de conexión, propuso navegación y verificó la estructura del paquete; responsabilidad de aprobación y publicación humana.
- **Description:** se usaron el documento maestro v1.6, la práctica y las decisiones pedagógicas del taller, evitando divulgar notas docentes.
- **Discernment:** verificaciones programáticas de presencia de archivos, vínculos relativos y estructura del ZIP; no se documenta prueba de render en Quarto ni piloto con participantes.
- **Diligence:** conserva fuentes, distingue archivos públicos y privados y evita atribuir certificación FAIR o validación pedagógica inexistentes.

## Novedades v1.1 (2 de noviembre de 2026)

- Nuevo capítulo `contenido/03b-estructura-prompt.qmd`: rol, contexto, objetivo, tarea, salida, restricciones y verificación; efectos esperados, límites y ejemplos progresivos.
- Actividad de prompting de **5–7 minutos dentro del bloque 12:10–12:30**, sin modificar la duración total.
- Se modificaron la navegación, la página de método, la práctica y la portada para integrar el capítulo sin crear una séptima etapa.
- **Trazabilidad 4D:** IA redactó y conectó el nuevo contenido (*Description*); propuso los efectos como hipótesis didácticas, no resultados de una prueba (*Discernment*); preservó la separación de materiales públicos y privados (*Diligence*); decisiones de aprobación y publicación a cargo de la persona docente (*Delegation*). No se ha documentado una nueva prueba piloto con participantes.

## Novedades v1.2 (2 de noviembre de 2026) · revisión editorial

- Revisión página por página con la autora; correcciones de coherencia (cinco *filas*, no cinco genes; «celda vacía»; nombres cortos de etapas unificados; restos de numeración del documento maestro eliminados; lenguaje para participantes en lugar de notas docentes).
- Diagramas: `combinar-tablas.svg` y `datos-y-metadatos.svg` rehechos (el segundo decía «4 filas»); nuevos `anatomia-prompt.svg`, `agenda-practica.svg` y `revisar-vs-verificar.svg`.
- Bitácora convertida a tablas (antes las líneas se fusionaban al renderizar) y alineada con la práctica; plantillas descargables.
- Duplicados eliminados (actividad obligatoria, cita del 80 %, «Si sobra tiempo», figuras repetidas).
- Referencias comprobadas en línea el 2 de noviembre de 2026; añadida [R13] Mons et al. (2017).
- `_quarto.yml`: render limitado a `index.qmd` y `contenido/*.qmd` (evita publicar `README.md` y `PROMPT_PARA_CURSOR.md`); autoría y licencia CC BY 4.0 en el pie.
- **Trazabilidad 4D:** IA propuso y aplicó cambios aprobados por la autora (*Delegation*/*Description*); fuentes verificadas abriendo las páginas, sin render de Quarto todavía (*Discernment*); separación público/privado preservada (*Diligence*).

## Novedades v1.3 (3 de noviembre de 2026) · diseño y preparación

- **Formato:** tema propio (`tema.scss`, paleta de los diagramas) sobre `cosmo`; tarjetas para prompts con botón «Copiar» (`_prompt-copy.html`), respuestas simuladas de la IA, frases destacadas, recuadro «En 1 minuto» y etiqueta Antes / Durante / Para profundizar con tiempo de lectura en cada página.
- **Nueva página `contenido/00-preparacion.qmd`:** requisitos (cuenta en un asistente que acepte archivos), prueba de 2 minutos, plan B con `descargas/expresion_genica_caso_simulado.txt`, privacidad y participación en línea.
- **Nueva `contenido/tarjeta-practica.qmd`:** guía imprimible de la sesión.
- **Prompts P0, P1, P5 y P6 en `contenido/_prompts/`:** una sola copia, incluida en la práctica y en la tarjeta con `{{< include >}}`. Para modificar un prompt, edita solo ese archivo.
- **Nuevos diagramas:** `vista-excel.svg`, `escala-evidencia.svg`, `un-solo-chat.svg`.
- **Práctica:** puesta en común tras P1, autoevaluación, prioridad a la verificación humana si falta tiempo, alternativa en línea para parejas y encuesta breve de cierre (el formulario debe crearse y compartirse en la sesión).
- Se redujeron advertencias repetidas sobre certificación FAIR.

## Construir y publicar

```bash
quarto preview          # vista previa local con recarga automática
quarto render           # construye el sitio en _site/ (no se versiona)
quarto publish gh-pages # publica en GitHub Pages (rama gh-pages)
```

La primera vez, `quarto publish gh-pages` crea la rama `gh-pages`; luego activa GitHub Pages en *Settings → Pages* con esa rama. Al publicar, descomenta `site-url` y `repo-url` en `_quarto.yml`.

**Trabaja en una copia local** (por ejemplo `~/proyectos/fair-prompt-4d`), no dentro de Google Drive: la sincronización de Drive interfiere con Git y con `quarto preview`.

Las contribuciones siguen [Conventional Commits](CONTRIBUTING.md).
