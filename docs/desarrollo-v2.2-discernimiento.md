# Desarrollo v2.2 — Discernimiento

Registro de la integración local de la actividad «¿Qué puedo aceptar de una respuesta de IA?». No forma parte del sitio publicado v1.4.

## Integración

- Aplicación: `interactivos/ai_discernment_tool.html`
- Página Quarto: `contenido/interactivos/que-puedo-aceptar.qmd`
- Registro de render: `_quarto.yml`
- Navegación de desarrollo, menú y barra lateral «Taller v2.2»:
  1. ¿Qué falta por definir?
  2. De la solicitud al prompt
  3. ¿Qué puedo aceptar de una respuesta de IA?
  4. Desafío integrador FAIR (`explorador-fair.qmd`)
- El menú «Taller FAIR» de la v1.4 permanece en la configuración. No se publicaron cambios.

El archivo de Descargas del 5 de noviembre es anterior al que ya estaba en `interactivos/`. No se sustituyó.

## Defectos y correcciones

Las secuencias y las cinco afirmaciones no se modificaron. El recálculo en JavaScript coincide con Seq_01 (30; A9 T7 C6 G8; GC 46.7 %), Seq_02 (24; A6 T6 C6 G6; GC 50 %) y Seq_03 (36; A12 T8 C7 G9; GC 44.4 %).

Correcciones aplicadas en la aplicación:

- Los controles generados de Contrastar y Decidir quedaron asociados a su etiqueta.
- Los botones declaran `type="button"` y la estación activa expone `aria-pressed`.
- La restauración de `localStorage` conserva los campos válidos de un estado incompleto y descarta tipos inválidos, sin convertirlos en `[object Object]`.
- Copiar el reporte intenta el portapapeles y, si falla, selecciona el texto visible sin anunciar un éxito falso.

## Pruebas

Automatizada: `node --check` del script, correcta. `quarto render`, 16/16 páginas.

En navegador, sobre el HTML y luego dentro de la página Quarto:

- Examinar muestra el FASTA y la respuesta simulada, sin los conteos calculados.
- Contrastar exige una clasificación para validar. La pista es opcional y no adelanta la retroalimentación.
- Cambiar la clasificación oculta la validación y la revisión de la decisión. Se puede volver a validar.
- La orientación de Decidir aparece al pulsar «Revisar mi decisión» y se oculta al cambiar la acción.
- La retroalimentación de Seq_01, Seq_02 y Seq_03 muestra las cifras recalculadas.
- El reporte visible coincide con el Markdown. La descarga prepara `Discernimiento_IA_2026-11-06.md`.
- Recarga, reinicio cancelado y reinicio confirmado, estado incompleto y JSON ilegible.
- A 390 px la página no se desborda; la barra de estaciones se desplaza.
- El iframe de Quarto carga las cuatro estaciones. El enlace independiente abre el HTML. La página Quarto no incluye las soluciones.

## Pendientes

- No se comprobó el portapapeles del sistema con un clic confiable dentro del iframe.
- No se midió el contraste con una herramienta de accesibilidad ni se recorrió con lector de pantalla.
- No hay una suite automatizada de pruebas de interfaz en el repositorio.
