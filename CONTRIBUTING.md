# Cómo contribuir

## Mensajes de commit

Este repositorio sigue [Conventional Commits 1.0.0](https://www.conventionalcommits.org/es/v1.0.0/):

```
<tipo>(<ámbito>): <resumen en imperativo>

<cuerpo opcional: qué y por qué>

<pie opcional>
```

| Tipo | Úsalo para | Ejemplo |
|---|---|---|
| `feat` | Contenido o función nueva | `feat(practica): agrega puesta en común tras P1` |
| `fix` | Corregir un error | `fix(recursos): corrige número de filas en datos-y-metadatos` |
| `docs` | README y guías del repositorio | `docs: explica cómo publicar en GitHub Pages` |
| `style` | Tema, CSS, tipografía | `style(tema): aumenta contraste de las tarjetas de prompt` |
| `refactor` | Reorganizar sin cambiar lo visible | `refactor(practica): extrae prompts a _prompts/` |
| `chore` | Configuración y mantenimiento | `chore: ignora carpeta _site` |
| `ci` | Publicación automática | `ci: publica el sitio con GitHub Actions` |

Reglas breves:

- Resumen en **imperativo** («agrega», «corrige»), en minúsculas, sin punto final y de 72 caracteres o menos.
- **Un cambio lógico por commit**: no mezcles una corrección de contenido con un cambio de estilo.
- Ámbitos sugeridos: `contenido`, `practica`, `bitacora`, `recursos`, `descargas`, `tema`, `sitio`, `referencias`.
- Si un cambio rompe algo para quien reutiliza el material (por ejemplo, cambiar el texto de P0–P6), indícalo con `!` (`feat(practica)!: ...`) y un pie `BREAKING CHANGE:`.

Para tener la plantilla en cada commit:

```bash
git config commit.template .gitmessage
```

## Reglas del contenido

- Los prompts P0, P1, P5 y P6 están **solo** en `contenido/_prompts/`. No los copies en otras páginas: inclúyelos con `{{< include _prompts/p0.md >}}`.
- **Nunca** agregues `privado-docente/` ni respuestas esperadas al repositorio.
- Antes de hacer commit, ejecuta `quarto render` y revisa que no haya advertencias.
