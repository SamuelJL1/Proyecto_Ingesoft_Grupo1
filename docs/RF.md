# REQUERIMIENTOS FUNCIONALES - RETROALIMENTACIONES Y GESTIÓN INTERNA 

## RF1 – Visualizar syllabus de un curso

El sistema debe mostrar el nombre, los objetivos de aprendizaje y los contenidos de un curso seleccionado, siempre que estén disponibles. Si algún campo obligatorio está vacío, el sistema debe notificar que el syllabus está incompleto.

### PESTLE

* **Social/Político:** La visualización clara del syllabus permite que el jefe tenga insumos objetivos para decidir sobre propuestas y homologaciones.
* **Tecnológico:** Requiere un repositorio centralizado de cursos con campos estructurados.

<br>

## RF2 – Registrar decisión sobre propuesta de materia

El sistema debe permitir al jefe registrar el estado de una propuesta (aprobado, rechazado, en revisión) y almacenar la fecha de la decisión, validando que los campos nombre, objetivos y créditos de la propuesta estén completos. Si no lo están, debe impedir el guardado e indicar los campos faltantes.

### PESTLE

* **Legal/Político:** La trazabilidad de la decisión (quién, cuándo y qué se decidió) es esencial para llevar un control claro del proceso de preaprobación.
* **Económico:** Evita re-trabajo por decisiones informales no guardadas.

<br>

## RF3 – Seleccionar dos cursos para comparación

El sistema debe permitir la selección de exactamente dos cursos como paso previo a la comparación. Si el jefe selecciona menos o más de dos cursos, el sistema debe mostrar un mensaje y bloquear la continuación.

### PESTLE

* **Tecnológico/Social:** Establece una restricción lógica necesaria para evitar errores en la comparación (que podría ser asistida por IA).
* **Económico:** Reduce la probabilidad de decisiones equivocadas al forzar el formato de comparación uno a uno, que es más claro y rápido de interpretar.

<br>

## RF4 – Comparar objetivos de aprendizaje de dos cursos

El sistema debe mostrar los objetivos de aprendizaje de dos cursos seleccionados para facilitar su comparación. Si algún curso no tiene objetivos registrados, debe indicarlo sin impedir la visualización de los que sí existen.

### PESTLE

* **Social/Político:** La comparación directa de objetivos permite al jefe justificar si una nueva propuesta de materia va acorde con el objetivo general de los cursos, el cual es el pensamiento crítico.
* T**ecnológico:** Sienta la base para una futura funcionalidad de IA que evalúe la similitud entre los objetivos de dos cursos.

<br>

## RF5 – Registrar curso con datos básicos

El sistema debe permitir al asistente registrar un curso con nombre, créditos (número entero mayor a 0) y programa académico. Debe validar que los créditos sean positivos y que los campos obligatorios no estén vacíos, mostrando errores específicos si no se cumple.

### PESTLE

* **Tecnológico/Legal:** Alimenta el repositorio central con datos validados, que luego servirán para homologaciones y comparaciones. La validación fuerte previene datos inconsistentes que generarían errores en otros subsistemas.
* **Económico:** La carga de cursos por parte del asistente libera al jefe de otras tareas operativas.

<br>

## RF6 – Consultar lista de cursos registrados

El sistema debe mostrar una lista con el nombre y el programa académico de todos los cursos registrados, o un mensaje informativo si no existe ninguno.

### PESTLE

* **Social/Tecnológico:** Proporciona una vista base para cualquier operación (selección para comparar, revisión de syllabus, etc.), siendo la puerta de entrada a las demás funcionalidades.
* **Económico:** Reduce el tiempo de búsqueda de información dispersa en documentos o carpetas compartidas.