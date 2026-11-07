# Revisión del proyecto «Antes del prompt» (fair-prompt-4d)

Fecha: 6 de noviembre de 2026 · Rama revisada: `feat/taller-interactivo-v2` (commit `d032db6`)
Alcance: lectura del repositorio. **No se modificó ningún archivo** salvo la creación de este reporte. No se ejecutó `quarto render` ni se abrieron las aplicaciones en un navegador.

---

## 1. De qué trata

Sitio Quarto del taller práctico de dos horas **«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica»** (Heladia Salgado, CCG-UNAM, CC BY 4.0), sesión «Instrucciones para modelos de lenguaje en tareas científicas» del programa ELIXIR-México 2026 (16–27 nov 2026).

La idea central: con IA producir es fácil; lo difícil es **saber qué pedir, qué delegar y cómo comprobar**. El taller propone una secuencia iterativa de **seis etapas** (Necesidad → Vocabulario → Especificación → Colaboración → Verificación → Registro), acompañada transversalmente por las cuatro competencias del marco **AI Fluency 4D** (Delegation, Description, Discernment, Diligence). El material se presenta, con cuidado explícito, como síntesis didáctica, no como método validado.

El **caso integrador** es un Excel simulado de expresión génica (5 genes de *E. coli* × 3 condiciones, dos hojas) al que le faltan deliberadamente unidades, definición de condiciones, réplicas, cepa, procesamiento y responsable, y que tiene una celda vacía. Las trampas didácticas están bien planteadas: `Estrés A (prom.)` ambiguo, celda vacía que no debe leerse como 0, y la coexistencia de `b0014` y `dnaK` (en K-12, b0014 es el locus de *dnaK*, con valores distintos en la tabla), que invita a no asumir equivalencias sin confirmar anotación.

**Productos de la sesión:** (1) un diagnóstico FAIR preliminar elaborado en el asistente del participante y (2) la Bitácora mínima 4D descargada en Markdown. Se insiste en que nada de esto certifica FAIR.

## 2. Recorrido actual (navegación de `_quarto.yml`)

| Bloque | Página | Tipo |
|---|---|---|
| — | `index.qmd` | Portada |
| Antes del taller | `00-preparacion` | Requisitos, prueba de 2 min, plan B en texto |
| Comprender el problema | `01-contexto`, `02-ejemplos`, `03-metodo` | Lectura |
| | `interactivos/que-falta-por-definir` | App (casos A FASTA / B web) |
| Construir una solicitud | `03b-estructura-prompt` | Siete componentes del prompt, P0 vs versión B |
| | `interactivos/de-la-solicitud-al-prompt` | App (constructor de hasta 3 versiones) |
| Evaluar respuestas | `interactivos/que-puedo-aceptar` | App de discernimiento con FASTA |
| Caso científico | `04-caso-fair`, `05-practica`, `06-verificacion` | Caso, práctica P0/P1/P5/P6, verificación con fuente primaria |
| | `07-bitacora` | App Bitácora mínima 4D (iframe) |
| Recursos | `tarjeta-practica`, `08-referencias` | Tarjeta imprimible, bibliografía [R1]–[R13] |

Fuera del menú pero renderizada: `interactivos/explorador-fair.qmd` (ahora solo «Nota de ruta»); el Explorador FAIR se enlaza directamente desde `04-caso-fair`.

### Piezas técnicas

- **Prompts como fuente única:** `contenido/_prompts/p0, p1, p5, p6.md`, incluidos con `{{< include >}}`. P2–P4 no son prompts sino decisiones del participante (especificación y delegación).
- **`_prompt-copy.html`:** añade cabecera y botón «Copiar» a cada `div.prompt`.
- **Cinco aplicaciones HTML autocontenidas** en `interactivos/` (sin dependencias externas por CDN), cada una con estado en `localStorage` y reporte Markdown descargable.
- **10 diagramas SVG** en `recursos/`; descargas: `.xlsx`, `.txt` equivalente y plantilla extensa de bitácora (`.docx`/`.md`).
- Tema: `cosmo` + `tema.scss` + `styles.css` (clases `.en-un-minuto`, `.destacado`, `.prompt`, `.respuesta-ia`, `.etiqueta-pagina`, `.autoevaluacion`).
- `docs/`: diseño pedagógico v2.0, registros de desarrollo v2.2 y ~25 prompts usados con Gemini para generar las aplicaciones.

## 3. Estado del repositorio

- `main` = `origin/main` en `24cb967` (sitio v1.4 publicado en GitHub Pages).
- La rama `feat/taller-interactivo-v2` lleva **3 commits** no fusionados y **no existe en el remoto** (no se ha hecho push).
- `docs/` completa está **sin versionar** (`git status: ?? docs/`).
- `_site/` está al día respecto a las fuentes (ninguna página más antigua que su `.qmd`; las cinco apps coinciden byte a byte con su copia en `_site/`). Las anclas internas usadas en los enlaces existen en el HTML generado.
- `privado-docente/` no está en la carpeta ni en el historial de Git. Bien.

## 4. Fortalezas

- **Honestidad epistémica consistente:** datos simulados, respuestas de IA simuladas, «no certifica FAIR», «no se ha hecho piloto», «pendiente, nunca verificado». Se repite sin volverse ruido.
- **Separación clara de autorrevisión (P6) y verificación independiente**, con una actividad obligatoria concreta y verificable (Wilkinson et al. 2016, Box 2, A1.1/A1.2/A2; Mons et al. 2017 como aclaración «FAIR ≠ Open»).
- **Escala de cuatro etiquetas** (observado / inferido / por confirmar / verificado) que conecta caso, práctica, tarjeta y bitácora.
- **Bibliografía comentada** que dice qué aporta cada fuente *y qué no*.
- Buen diseño de las trampas del Excel; plan B en texto para asistentes sin adjuntos.
- Registros de desarrollo (`docs/desarrollo-v2.2-*.md`) con pruebas hechas y pendientes declarados, en el mismo espíritu del taller.

## 5. Observaciones y posibles inconsistencias (sin corregir)

Ordenadas aproximadamente por relevancia.

1. **Rama no publicada ni respaldada.** Los tres commits de v2.2 solo existen localmente. El sitio en vivo sigue siendo v1.4 (lo que el diseño pide hasta una decisión explícita de publicar), pero hoy no hay copia remota del trabajo.
2. **`docs/` sin versionar.** Contiene el diseño pedagógico y los registros de pruebas. Habría que decidir qué se versiona; los prompts a Gemini (`prompt_gemini_*`, con variantes numeradas y un nombre con errata: `prompt_gemini_explirador_excel.md`) y los borradores `l.txt`, `s.txt`, `s2.txt` parecen material de trabajo.
3. **Los registros de desarrollo no coinciden con la navegación actual.** `desarrollo-v2.2-bitacora.md` dice que hay «un solo menú "Taller"» y `desarrollo-v2.2-discernimiento.md` describe un menú «Taller v2.2» con el Explorador como punto 4. El `_quarto.yml` actual tiene cinco menús («Comprender el problema», «Construir una solicitud», etc.) y el Explorador está fuera del menú.
4. **`diseno-pedagogico-v2.md` describe otro recorrido.** Propone «cinco desafíos», empezar observando con el Explorador antes de explicar, microactividades A–C, revisión entre pares y una agenda de 120 minutos. El sitio implementado sigue otra ruta (páginas 1–11, sin Explorador en el recorrido, sin pares). El propio registro v2.2 lo reconoce solo para la revisión por pares.
5. **P0 duplicado.** `03b-estructura-prompt.qmd` reescribe el texto de P0 en vez de incluir `_prompts/p0.md`, en contra de la regla de `CONTRIBUTING.md`. Ya figuraba como pendiente en el diseño v2.
6. **Formulario anónimo sin enlace.** `05-practica.qmd` pide responder «en el formulario de la sesión», pero no hay formulario ni enlace. También figuraba como pendiente.
7. **Sesgo hacia ChatGPT en una app.** `de_la_solicitud_al_prompt.html` y su página invitan a probar en ChatGPT (enlace fijo a chatgpt.com), mientras `00-preparacion` dice que cualquier asistente sirve.
8. **Etiquetas de página.** `01-contexto` y `03-metodo` llevan «Antes del taller», pero la portada indica recorrerlas durante el taller. Puede ser intencional (lectura previa recomendada), aunque confunde un poco.
9. **Restos de la agenda con horarios.** `recursos/agenda-practica.svg` (11:30–13:30) ya no se usa en ninguna página, pero se sigue copiando y publicando con `recursos/**`. `PROMPT_PARA_CURSOR.md` aún habla de «nueve páginas», de 120 minutos y del bloque 12:10–12:30, que contradicen el último commit («sin duraciones visibles»).
10. **README desactualizado para v2.2.** El historial termina en 1.4. La tabla de contenido no menciona que la bitácora ahora es una app ni que la plantilla pasó a ser opcional.
11. **Nomenclatura pendiente.** El diseño v2 plantea cambiar «etapas» por «recomendaciones flexibles». El sitio sigue usando «etapas». La decisión sigue abierta.
12. **Títulos de las apps.** Algunas aplicaciones generadas usan mayúsculas tipo inglés («Reporte de Construcción y Prueba», «Toma de Decisiones y Rigor», «Evidencia Primaria (FASTA)»), a diferencia del estilo del sitio. El `<title>` de la bitácora dice «Taller IA en la Investigación Científica», no «Antes del prompt».
13. **Referencias con fechas de 2026.** [R11] (Gupta, 10 jun 2026) y [R12] (Fowler, 21 may 2026) se declaran consultadas el 2 nov 2026. No las verifiqué en esta revisión.

## 6. Pendientes declarados por el propio proyecto

- No se ha hecho piloto con participantes ni evaluación de aprendizaje.
- No se ha probado el portapapeles dentro del iframe con un clic real, ni la accesibilidad con lector de pantalla, ni se ha medido el contraste.
- No hay pruebas automatizadas de interfaz.
- Hay que reconstruir las respuestas esperadas y las guías docentes, y mantenerlas fuera del repositorio.

## 7. Qué no verifiqué

- No ejecuté `quarto render` ni `quarto preview`, para no tocar `_site/`.
- No abrí las aplicaciones en un navegador ni revisé su lógica a fondo; solo estructura, estado y enlaces externos.
- No abrí las URLs de la bibliografía.
- No inspeccioné el `.xlsx` ni el `.docx` binarios; usé la versión `.txt`, que dice ser equivalente.
