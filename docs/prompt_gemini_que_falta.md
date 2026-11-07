# Crear desde cero — ¿Qué falta por definir?

Actúa como diseñador instruccional y desarrollador web especializado en herramientas educativas interactivas.

Construye **desde cero** una aplicación HTML autónoma para el taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica»**

Nombre de la herramienta:

**¿Qué falta por definir?**

Subtítulo:

**De una necesidad comprensible a una solicitud más precisa.**

No reutilices ni adaptes código de versiones anteriores del Explorador de vocabulario. Queremos una implementación nueva, sencilla y mantenible.

## 1. Objetivo pedagógico

Ayudar a identificar decisiones que deben aclararse antes de delegar una tarea a una IA.

La actividad debe demostrar que una solicitud puede entenderse y, sin embargo, admitir diferentes interpretaciones.

No es un examen de vocabulario ni una actividad para construir un prompt completo.

Duración: **5–8 minutos**.

Cada participante elige solamente uno de dos casos.

## 2. Casos

### Caso A — Analizar secuencias FASTA

Solicitud inicial:

«Tengo un archivo FASTA con secuencias de ADN y quiero calcular la frecuencia de nucleótidos».

Aspectos de referencia para diseñar las pistas, sin mostrarlos inicialmente:

- ¿El archivo contiene una o varias secuencias?
- ¿Se esperan conteos absolutos, porcentajes o ambos?
- ¿Cómo tratar caracteres ambiguos, como N?
- ¿Se calcularán resultados por secuencia o globales?
- ¿Cómo debe presentarse el resultado?

### Caso B — Desarrollar una herramienta web

Solicitud inicial:

«Quiero una aplicación web que permita cargar un archivo FASTA, analizar su contenido y descargar los resultados».

Aspectos de referencia para las pistas:

- ¿Qué tipos de archivo acepta?
- ¿Qué análisis debe realizar?
- ¿Qué debe ocurrir con entradas inválidas?
- ¿Cómo se visualizan y descargan los resultados?
- ¿Qué condiciones permiten comprobar que funciona?

Los casos deben ser independientes, pero conservar una temática común para que resulte clara la diferencia entre solicitar un análisis y solicitar el desarrollo de una herramienta.

## 3. Interfaz: tres pasos y un Reporte

Utiliza exactamente cuatro pestañas:

**1. Identificar**

Mostrar la solicitud inicial.

Preguntar:

«¿Qué necesitarías aclarar antes de realizar esta tarea?»

Permitir escribir hasta tres preguntas o decisiones pendientes.

No mostrar las respuestas de referencia.

**2. Explorar**

Mostrar las preguntas registradas por el participante.

Permitir consultar hasta tres pistas progresivas, una por una.

Las pistas deben orientar hacia aspectos relevantes, pero no presentarse como respuestas obligatorias.

Si la persona considera que falta algo, puede regresar y modificar sus preguntas.

Incluir definiciones breves de vocabulario técnico únicamente cuando aporten claridad.

No calificar ni comparar automáticamente las respuestas con una lista de respuestas esperadas.

**3. Reformular**

Mostrar:

- Solicitud inicial.
- Preguntas registradas.
- Pistas efectivamente consultadas.

Preguntar:

«¿Cómo describirías ahora tu solicitud para que otra persona o una IA comprenda mejor lo que necesitas?»

Ofrecer un campo editable.

Después preguntar:

«¿Qué decisiones siguen pendientes de confirmar?»

No generar automáticamente la solicitud revisada.

No introducir datos desconocidos como si fueran hechos.

**4. Reporte**

Mostrar exclusivamente lo que ocurrió en la actividad:

- Caso elegido.
- Solicitud inicial.
- Preguntas registradas.
- Pistas consultadas.
- Solicitud revisada.
- Decisiones pendientes.

Incluir botón:

**Descargar reporte (.md)**

El Markdown debe coincidir con el Reporte visible.

Permitir descargarlo aunque haya respuestas incompletas.

## 4. Principios pedagógicos

- Descubrimiento antes de explicación.
- Navegación libre.
- Ayuda disponible sin exigir respuestas correctas.
- Sin calificaciones ni porcentajes de acierto.
- Sin mapas, gráficas o actividades adicionales.
- No mostrar inicialmente los aspectos que deben descubrirse.
- No obligar a consultar las tres pistas.
- No exigir escribir una respuesta para navegar.
- Diferenciar claramente las preguntas propias de las sugerencias de la herramienta.
- No afirmar que consultar una pista equivale a confirmar una decisión.

**La herramienta debe ser muy breve. Evita incorporar subsecciones innecesarias.**

## 5. Diseño

Mantén la identidad visual del taller:

- Azul principal: `#00314F`
- Dorado: `#C9A227`
- Blanco: `#FFFFFF`
- Gris claro: `#F3F4F6`
- Texto oscuro: `#1F2937`

Diseño académico, claro y moderno.

No utilices logos oficiales de la UNAM.

Debe verse adecuadamente dentro de un iframe de Quarto y también como página independiente.

## 6. Requisitos técnicos

- Un solo archivo HTML.
- CSS embebido.
- JavaScript embebido.
- Sin Tailwind CDN.
- Sin React ni frameworks.
- Sin APIs externas.
- Funcionar completamente offline.
- Persistencia en `localStorage`.
- Estado independiente para cada caso.
- Restauración defensiva ante almacenamiento incompleto o ilegible.
- Reinicio con confirmación.
- Accesibilidad mediante teclado.
- Diseño responsive.
- Descarga Markdown sin bibliotecas externas.

Utiliza una clave nueva de almacenamiento.

Evita duplicar identificadores HTML.

No utilices `innerHTML` para insertar directamente respuestas escritas por los participantes sin escaparlas adecuadamente.

Mantén una única estructura de datos como fuente del Reporte visible y del Markdown.

## 7. Verificación

Antes de entregar, comprueba:

1. Estado inicial vacío.
2. Cambio entre los dos casos sin pérdida de respuestas.
3. Navegación entre las cuatro pestañas.
4. Guardado de preguntas.
5. Pistas progresivas.
6. Registro correcto de las pistas consultadas.
7. Reformulación.
8. Reporte incompleto.
9. Correspondencia entre Reporte y Markdown.
10. Restauración tras recargar.
11. Reinicio confirmado y cancelado.
12. Uso mediante teclado.
13. Funcionamiento sin conexión.
14. Presentación en pantallas pequeñas.

Distingue las pruebas ejecutadas realmente de las verificaciones que solo realizaste mediante inspección de código.

## 8. Entrega

Genera directamente el archivo completo:

`que_falta_por_definir.html`

No modifiques Quarto ni el repositorio Git.

No publiques.

No añadas funciones fuera del alcance definido.

**Criterio principal de éxito:** una persona debe poder comprender la actividad y recorrerla en 5–8 minutos, descubriendo por qué su solicitud inicial necesita mayor precisión.


