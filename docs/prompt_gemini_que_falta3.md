# Ajuste final — ¿Qué falta por definir?

Trabaja sobre la versión actual de `qu_falta_por_definir(2).html`.

La estructura pedagógica ya está aprobada. Quiero realizar únicamente los siguientes ajustes antes de pasar la aplicación a revisión técnica.

## 1. No revelar el tema de las pistas

Actualmente aparecen títulos como:

- Pista 1: Interacción
- Pista 2: Validación
- Pista 3: Funcionalidades

Estos títulos anticipan los aspectos que el participante debe descubrir.

**Cambio solicitado:**

Antes de abrirlas, mostrar solamente:

- Pista 1
- Pista 2
- Pista 3
- Orientación adicional 1
- Orientación adicional 2

El tema específico de cada pista debe permanecer oculto hasta que la persona la consulte.

Conservar el contenido de las pistas, salvo los ajustes indicados más adelante.

## 2. Hacer progresiva la consulta

La persona debe poder consultar:

1. Pista 1.
2. Pista 2, después de consultar la primera.
3. Pista 3, después de consultar la segunda.

Las orientaciones adicionales serán opcionales y se habilitarán después de la tercera pista.

No obligues a consultar todas las pistas para avanzar a la siguiente pestaña.

Mantén la navegación libre.

Si el participante no sabe qué responder, puede escribir «No sé» y acceder a las pistas.

No evalúes las respuestas ni exijas que sean correctas.

## 3. Conservar el historial de consultas

Actualmente, al ocultar una pista se elimina del registro de pistas consultadas.

Corrige este comportamiento.

Distingue entre:

- **Pista consultada:** la persona ya abrió su contenido.
- **Pista visible:** el contenido está expandido en pantalla.

Una pista que se consultó debe permanecer registrada aunque su contenido se cierre.

Al recargar la página:

- Las pistas consultadas deben conservarse.
- La secuencia de desbloqueo debe restaurarse correctamente.
- El Reporte debe indicar las pistas efectivamente consultadas.
- Las pistas del Caso A no deben mezclarse con las del Caso B.

## 4. Refinar la orientación tecnológica del Caso B

La última orientación debe ayudar a distinguir entre:

**Qué necesita hacer la aplicación** y **cómo se implementará técnicamente**.

Utiliza una orientación como:

«Antes de elegir lenguajes, frameworks o servicios, piensa si la aplicación necesita funcionar sin conexión, procesar archivos grandes, almacenar información o permitir el acceso de varias personas. ¿Cuáles de estas necesidades están realmente definidas?»

No sugieras una arquitectura como única solución.

No conviertas la elección de tecnología en un requisito obligatorio para continuar.

## 5. Mantener el descubrimiento

Las pistas deben ayudar a reflexionar, no funcionar como una lista de respuestas correctas.

No agregues ejemplos en los campos de la primera pestaña.

No generes automáticamente las preguntas ni la solicitud reformulada.

En la pestaña «Reformular», distingue claramente las preguntas que escribió el participante de las orientaciones proporcionadas por la aplicación.

## 6. Conservar lo que ya funciona

No cambies:

- Las dos solicitudes iniciales.
- Las cuatro pestañas.
- El diseño azul y dorado.
- La selección de casos.
- El regreso automático a «1. Identificar» al cambiar de caso.
- Las respuestas independientes por caso.
- La descarga Markdown.
- El reinicio del caso activo.
- El funcionamiento autónomo sin conexión.

## 7. Verificación

Revisa especialmente estos escenarios:

1. Las pistas aparecen inicialmente con títulos neutrales.
2. La pista 2 no se puede abrir antes de la pista 1.
3. La pista 3 no se puede abrir antes de la pista 2.
4. Las orientaciones adicionales son opcionales.
5. Abrir y cerrar una pista no borra su historial.
6. El Reporte registra las pistas consultadas.
7. La descarga Markdown coincide con el Reporte.
8. Cambiar de caso regresa a la pestaña 1.
9. Cada caso conserva sus respuestas y pistas.
10. Recargar mantiene el progreso.
11. Reiniciar limpia solamente el caso seleccionado.
12. La herramienta funciona offline.

Distingue entre pruebas ejecutadas en navegador e inspección del código. No afirmes haber probado algo que no ejecutaste.

## Entregable

Devuelve el HTML completo actualizado.

No modifiques Quarto, Git ni otros archivos.

No publiques.

**No agregues funciones nuevas. El objetivo es cerrar esta versión con una experiencia sencilla, coherente y técnicamente verificable.**


