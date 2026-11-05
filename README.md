# Antes del prompt

**Pensar, delegar y verificar con IA en la investigación científica**

Sitio del taller práctico de dos horas que propone una ruta de seis etapas para trabajar con asistentes de IA sin perder el criterio científico, aplicada a un caso de datos de expresión génica y principios FAIR.

🌐 **Sitio:** <https://helysalgado.github.io/fair-prompt-4d/>

Autora: Heladia Salgado · Centro de Ciencias Genómicas, UNAM · Licencia [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es)

El taller forma parte del programa ELIXIR-México 2026 como sesión «Instrucciones para modelos de lenguaje en tareas científicas (*prompting*; ponencia y taller)».

## Contenido

| Bloque | Páginas |
|---|---|
| Antes del taller | `00-preparacion` (requisitos y prueba de 2 minutos) |
| Fundamentos | `01-contexto` · `02-ejemplos` · `03-metodo` · `03b-estructura-prompt` |
| Taller FAIR | `04-caso-fair` · `05-practica` · `06-verificacion` · `07-bitacora` · `tarjeta-practica` |
| Para profundizar | `08-referencias` |

## Estructura del repositorio

```
index.qmd              portada
contenido/             páginas del taller (.qmd)
contenido/_prompts/    P0, P1, P5 y P6: única copia, incluida con {{< include >}}
recursos/              diagramas SVG
descargas/             Excel simulado, versión en texto y plantillas de bitácora
_quarto.yml            configuración del sitio y navegación
tema.scss, styles.css  tema visual
_prompt-copy.html      botón «Copiar» de las tarjetas de prompt
```

## Construir y publicar

```bash
quarto preview           # vista previa local con recarga automática
quarto render            # construye el sitio en _site/ (no se versiona)
quarto publish gh-pages  # publica en GitHub Pages (rama gh-pages)
```

Trabaja en la copia local (`~/git-local-projects/fair-prompt-4d`), no dentro de Google Drive: la sincronización de Drive interfiere con Git y con `quarto preview`.

## Reglas del contenido

- Los datos del caso son **simulados**; el objetivo es diagnosticar, no certificar FAIR.
- Para cambiar un prompt, edita solo su archivo en `contenido/_prompts/`.
- El material docente privado (`privado-docente/`: respuestas esperadas, guías de facilitación) **no se versiona** y está excluido en `.gitignore`.
- Los mensajes de commit siguen [Conventional Commits](CONTRIBUTING.md).

## Historial de versiones

| Versión | Fecha | Cambios principales |
|---|---|---|
| 1.0 | 22 oct 2026 | Reorganización del documento maestro v1.6 en páginas para Quarto. |
| 1.1 | 2 nov 2026 | Capítulo «Del problema al prompt» y actividad de 5–7 minutos. |
| 1.2 | 2 nov 2026 | Revisión editorial página por página, diagramas corregidos, bitácora en tablas, referencias verificadas y [R13]. |
| 1.3 | 3 nov 2026 | Tema visual, página «Antes del taller», tarjeta de práctica, prompts como fuente única y tres diagramas nuevos. |
| 1.4 | 5 nov 2026 | Repositorio en GitHub con Conventional Commits y sitio publicado en GitHub Pages. |

## Uso de IA (AI Fluency 4D)

- **Delegation:** la IA reorganizó, redactó y revisó contenidos y diagramas; la aprobación y la publicación son responsabilidad de la autora.
- **Description:** se trabajó a partir del documento maestro, las decisiones pedagógicas del taller y revisiones página por página.
- **Discernment:** las fuentes se comprobaron abriendo las páginas (2 de noviembre de 2026) y el sitio se construyó y revisó visualmente; **no se ha realizado aún un piloto con participantes**.
- **Diligence:** se separan los materiales públicos de los privados y no se atribuyen certificación FAIR ni validación pedagógica inexistentes.
