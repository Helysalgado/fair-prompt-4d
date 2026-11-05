# Prompt para Cursor · transformar contenidos en sitio Quarto

Actúa como desarrollador de sitios docentes con Quarto. Este proyecto **ya tiene contenido redactado** en `index.qmd` y `contenido/*.qmd`; consérvalo como fuente editorial. Tu tarea es implementar, revisar y pulir el sitio, no resumir ni sustituir sus contenidos.

## Objetivo

Crear un sitio Quarto HTML con navegación intuitiva para el taller «Antes del prompt: pensar, delegar y verificar con IA en la investigación científica». El sitio es el **manual completo del participante**, y las futuras diapositivas serán solo una guía para la facilitación.

## Requisitos

1. Conservar las nueve páginas de `contenido/`, las seis etapas, el marco 4D y el orden pedagógico. Mantener los textos técnicos, referencias y matices de incertidumbre.
2. Partir de `_quarto.yml`; optimizar navegación, buscador, lectura móvil, contraste de color y accesibilidad. Identidad sobria con acentos azul y dorado (sin logos institucionales no autorizados).
3. Comprobar rutas a `recursos/*.svg`, Excel y plantillas de bitácora en `descargas/`, enlaces entre páginas y anclas internas. `_quarto.yml` ya limita el render a `index.qmd` y `contenido/*.qmd` y copia `descargas/` como recurso; no lo reviertas.
4. Preservar literalmente los prompts P0, P1, P5 y P6, con el flujo de **un solo chat**. Las etapas 3 y 4 son ejercicios de decisión del participante, no prompts adicionales obligatorios.
5. La práctica dura 120 minutos. No convertirla en un tutorial de programación ni prometer certificación FAIR.
6. Mantener visible que los datos son simulados y que la verificación externa debe hacerse de verdad, no mediante autorrevisión del modelo.
7. Nunca publicar ni enlazar `privado-docente/`. Antes de publicar en GitHub, verificar que ni la carpeta ni sus contenidos estén versionados públicamente; preferir reubicarlos fuera del repositorio.
8. Construir el sitio con Quarto, inspeccionar salida y corregir errores. Reportar qué verificaste, qué no y cómo ejecutar y publicar.
9. Proponer un sistema simple para que futuras diapositivas reutilicen títulos, actividades y diagramas, sin duplicar el texto del sitio.

## Entregables

- Sitio Quarto funcionando localmente con `quarto preview` y `quarto render`.
- `_quarto.yml` y recursos de estilo necesarios.
- README con comandos concretos y flujo recomendado para GitHub Pages.
- Lista de comprobaciones y pendientes sin inventar pruebas ni resultados.

No cambies el fondo pedagógico sin explicar el motivo y proponer el cambio para revisión.


## Actualización v1.1 · prompting integrado

Incluye `contenido/03b-estructura-prompt.qmd` en la navegación, inmediatamente después de `03-metodo.qmd`. Conserva explícitamente los siete componentes como recurso flexible, el carácter **opcional** del rol y la advertencia de que una cita producida por IA no equivale a verificación. En `05-practica.qmd`, la microactividad consume 5–7 minutos **dentro** del bloque de 12:10–12:30: no aumentes la duración total del taller. No conviertas esta incorporación en una séptima etapa. Mantén fuera del repositorio público los recursos docentes privados.
