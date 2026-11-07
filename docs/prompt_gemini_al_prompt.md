# Crear desde cero — De la solicitud al prompt

Actúa como diseñador instruccional y desarrollador de aplicaciones web educativas.

Construye desde cero una herramienta HTML autónoma para el taller:

**«Antes del prompt: pensar, delegar y verificar con IA en la investigación científica»**

Título: **De la solicitud al prompt**

Subtítulo: **Transforma una necesidad definida en instrucciones claras para una IA.**

## 1. Objetivo

Que el participante construya un prompt a partir de una solicitud previamente delimitada, distinguiendo:

- Qué quiere lograr.
- Qué tarea delegará a la IA.
- Qué información y restricciones debe proporcionar.
- Qué resultado espera.
- Cómo verificará ese resultado.

La actividad no debe ejecutar el prompt ni conectarse a modelos de IA.

Duración objetivo: 8–10 minutos.

No crear un cuestionario extenso ni enseñar una lista de definiciones.

## 2. Recuperar el trabajo anterior

La actividad anterior se llama «¿Qué falta por definir?» y guarda sus datos en `localStorage`.

Clave actual:

`que_falta_por_definir_state_v3`

Tiene dos casos:

- Caso A: análisis de secuencias FASTA.
- Caso B: desarrollo de una herramienta web.

El estado incluye `currentCase` y, dentro de `cases.A` y `cases.B`, los campos:

- `questions`: preguntas o decisiones identificadas.
- `revisedRequest`: solicitud reformulada.
- `pendingDecisions`: decisiones pendientes de confirmar.

Implementa un botón:

**«Recuperar mi solicitud anterior»**

Al pulsarlo:

1. Intenta leer el estado anterior únicamente si se encuentra disponible en el mismo origen.
2. Comprueba y normaliza los tipos de datos antes de utilizarlos.
3. Permite seleccionar el Caso A o el Caso B si existen datos de ambos.
4. Recupera la solicitud reformulada y muestra por separado las decisiones pendientes.
5. No interpretes como decisiones propias las pistas consultadas en la actividad anterior.
6. No sobrescribas silenciosamente un trabajo que la persona ya empezó en esta herramienta.

Si los datos no están disponibles, ofrece un campo para pegar o escribir una solicitud.

No consideres la importación como obligatoria. La aplicación debe funcionar de forma independiente.

## 3. Estructura: tres pasos y un Reporte

### Pestaña 1. Mi solicitud

Mostrar la solicitud recuperada o escrita.

Preguntar:

**«¿Qué vas a pedirle a la IA que haga con esta solicitud?»**

Es importante diferenciar el producto que se desea obtener.

En el Caso A podría ser realizar un análisis, proponer un procedimiento o escribir un script.

En el Caso B podría ser definir requisitos, diseñar un prototipo o implementar una aplicación.

No selecciones automáticamente una tarea por el participante.

Permite escribir la tarea concreta que desea delegar.

### Pestaña 2. Construir instrucciones

Presentar un formulario breve con cuatro campos:

**Contexto y objetivo**
¿Qué quieres lograr y con qué información cuentas?

**Tarea**
¿Qué acción específica quieres que realice la IA?

**Condiciones y límites**
¿Qué restricciones debe respetar? ¿Qué información no debe inventar? ¿Qué debe preguntar si falta algún dato esencial?

**Resultado y verificación**
¿Qué producto esperas, en qué formato y qué comprobaciones debería permitir?

No mostrar ejemplos que adelanten respuestas dentro de los campos.

Utilizar etiquetas e instrucciones breves.

Permitir navegar sin completar todos los campos.

### Pestaña 3. Revisar mi prompt

Reunir las respuestas anteriores en un borrador estructurado.

Mostrar una vista previa del prompt.

Condiciones:

- Utilizar exclusivamente el texto escrito o confirmado por la persona.
- No agregar requisitos, valores, métodos o datos científicos inventados.
- Distinguir las decisiones pendientes.
- Permitir editar el prompt completo antes de copiarlo.
- No reemplazar cambios manuales sin avisar.
- Evitar incluir campos vacíos como instrucciones engañosas.

Incluir:

**Copiar prompt**

Y una pregunta final:

«¿Hay alguna decisión pendiente que la IA podría interpretar incorrectamente?»

No evaluar automáticamente la calidad del prompt.

### Pestaña 4. Reporte

Disponible en cualquier momento.

Incluir:

- Caso o solicitud utilizada.
- Procedencia de la solicitud: importada o escrita manualmente.
- Tarea elegida para delegar.
- Contexto y objetivo.
- Condiciones y límites.
- Resultado y verificación.
- Prompt final editado.
- Decisiones pendientes y reflexión final.

Permitir descargar en Markdown.

El reporte visible y el archivo Markdown deben utilizar la misma información.

## 4. Principios pedagógicos

La herramienta debe enseñar mediante la experiencia la diferencia entre:

**Delegation:** decidir qué tarea resulta apropiado encomendar a la IA.

**Description:** proporcionar instrucciones suficientemente claras para realizar esa tarea.

No es necesario mostrar explicaciones extensas del marco AI Fluency 4D.

No calificar respuestas.

No producir prompts automáticamente mediante reglas que completen información faltante.

Sí se permite ensamblar en un único texto las respuestas que escribió el participante.

No conectar con servicios externos.

## 5. Diseño

Conservar la identidad visual de las otras actividades:

- Azul `#00314F`
- Dorado `#C9A227`
- Blanco `#FFFFFF`
- Gris claro `#F3F4F6`
- Texto oscuro `#1F2937`

Interfaz sencilla, académica, limpia y responsive.

No incluir logos institucionales.

Cuatro pestañas:

1. Mi solicitud.
2. Construir.
3. Revisar.
4. Reporte.

Si el participante cambia de caso o de solicitud, regresar a la primera pestaña sin perder silenciosamente su trabajo anterior.

## 6. Requisitos técnicos

Crear un único archivo:

`de_la_solicitud_al_prompt.html`

Con CSS y JavaScript embebidos.

Sin CDN, frameworks, bibliotecas externas ni llamadas a APIs.

Compatible con ejecución independiente e integración posterior en Quarto mediante iframe.

Usar una clave de `localStorage` propia para esta tercera actividad, diferente de las anteriores.

Validar defensivamente el estado importado y el estado propio.

Permitir usar la herramienta incluso cuando `localStorage` no esté disponible.

Implementar reinicio con confirmación.

Mantener controles accesibles por teclado, etiquetas claras y navegación libre.

No insertar texto de usuarios mediante `innerHTML` sin sanitización.

El botón de copiar debe copiar el contenido final editado, no un borrador anterior.

El Reporte Markdown debe registrar el texto final, sin atribuirle verificaciones que todavía no se realizaron.

## 7. Pruebas

Verifica:

1. Uso sin datos importados.
2. Importación válida del Caso A.
3. Importación válida del Caso B.
4. Estado importado incompleto o corrupto.
5. Navegación por las cuatro pestañas.
6. Construcción del borrador sin completar datos ausentes.
7. Edición manual del prompt sin pérdida de cambios.
8. Copia del texto final.
9. Persistencia tras recargar.
10. Reinicio confirmado y cancelado.
11. Reporte vacío, parcial y completo.
12. Correspondencia entre Reporte visible y Markdown.
13. Funcionamiento offline.
14. Presentación en pantallas de 390 px.

Distingue pruebas realmente ejecutadas de verificaciones por inspección.

## 8. Entrega

Genera el HTML completo de la nueva herramienta.

No modifiques Quarto, Git ni los HTML de actividades anteriores.

No publiques.

**Prioridad absoluta: una actividad corta, comprensible y útil, sin convertir la construcción del prompt en otro ejercicio largo de identificación de problemas.**


