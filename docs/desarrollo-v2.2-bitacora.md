# Desarrollo v2.2 — Bitácora mínima 4D

Registro de la integración local del cierre del desafío integrador FAIR. No forma parte del sitio publicado v1.4. La actividad «¿Qué puedo aceptar de una respuesta de IA?» no se modificó.

## Recorrido único

- La navegación tiene un solo menú «Taller»: tres actividades, caso, práctica guiada, verificación, Bitácora mínima 4D y tarjeta.
- `contenido/07-bitacora.qmd` aloja la aplicación. La plantilla extensa permanece en `descargas/` como recurso opcional.
- `contenido/05-practica.qmd` organiza la práctica por pasos, sin horarios por apartado, y explica los tres Markdown de apoyo.
- Se retiraron del recorrido las instrucciones de parejas, puesta en común y revisión entre participantes.
- `contenido/interactivos/explorador-fair.qmd` queda como nota de ruta, fuera del menú. El diagnóstico no se sustituye por el Explorador.
- `docs/diseno-pedagogico-v2.md` todavía describe la revisión por pares como pieza ajustable de un diseño anterior. El sitio ya no la incluye. No se reescribió ese documento.

## Integración anterior

- Aplicación: `interactivos/bitacora_minima_4d.html`. El HTML no se modificó.

## Pruebas

Automatizada: `node --check` del script, correcta. `quarto render`, 16/16 páginas. La copia en `_site/interactivos/` coincide con la fuente.

En navegador, sobre el HTML y dentro del iframe de la página Quarto:

- Las cinco estaciones conservan las respuestas al cambiar de estación.
- Las cinco ayudas opcionales inician cerradas.
- Hay una afirmación inicial y el máximo es tres; el botón se desactiva al llegar al límite.
- «Respaldado» o «Contradicho» sin comprobación independiente muestra una orientación. Esa orientación no es una verificación científica.
- «Comprobación independiente» sin evidencia muestra otra orientación. Ambas se actualizan al cambiar el método, el estado o la evidencia, y el Markdown registra la limitación metodológica.
- `localStorage` (`taller_ia_bitacora_minima_4d_v2_2_compact`) restaura estación y respuestas. Un JSON ilegible vuelve al estado inicial.
- Cancelar el reinicio conserva los datos. Confirmarlo deja una afirmación y un solo aviso, aunque el diálogo se abra dos veces.
- Copiar arma el Markdown visible. Si `execCommand("copy")` falla, el aviso indica usar la descarga. La descarga prepara `bitacora_minima_4d_2026-11-06.md`.
- A 390 px ni la página de cierre ni la bitácora dentro del iframe se desbordan. El iframe usa la regla de 85vh y 520 px.
- La página de cierre tiene un solo iframe. El enlace independiente usa `target="_blank"`.
- Los enlaces al caso, la práctica, la verificación, el marco 4D, el Excel, las plantillas, la bitácora y el Explorador responden 200.

## Defectos corregidos

Ninguno. No se cambió la aplicación.

## Pendientes

- No se comprobó el portapapeles del sistema con un clic confiable dentro del iframe.
- No se recorrió con lector de pantalla ni se midió el contraste.
- No hay una suite automatizada de pruebas de interfaz en el repositorio.
