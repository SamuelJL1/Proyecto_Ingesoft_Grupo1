# COMPONENTE 1 – CATÁLOGO DE CURSOS

## HU1 – Ver lista de cursos
Yo como estudiante quiero ver la lista de cursos disponibles del área para conocer las opciones que puedo elegir.

**Feature:** Visualizar catálogo de cursos

- **Scenario:** Ver listado paginado de cursos  
  - **Given** que existen al menos 15 cursos activos registrados en el sistema  
  - **When** el estudiante accede al catálogo  
  - **Then** el sistema muestra la primera página con máximo 10 cursos  
  - **And** cada curso muestra código, nombre, créditos y área  
  - **And** los cursos están ordenados alfabéticamente por nombre  

- **Scenario:** Navegar entre páginas del catálogo  
  - **Given** que existen más de 10 cursos activos  
  - **When** el estudiante selecciona la página 2  
  - **Then** el sistema muestra los siguientes cursos sin repetir los anteriores  


## HU2 – Filtrar cursos
Yo como estudiante quiero filtrar cursos por temas o competencias para encontrar opciones alineadas con mis intereses.

**Feature:** Filtrar cursos por múltiples criterios

- **Scenario:** Filtrar por un criterio  
  - **Given** que el estudiante está viendo el catálogo completo  
  - **When** aplica filtro por área "Humanidades"  
  - **Then** el sistema muestra solo cursos del área Humanidades  

- **Scenario:** Filtrar por múltiples criterios combinados  
  - **Given** que el estudiante está viendo el catálogo  
  - **When** aplica filtro por área "Humanidades" y competencia "Pensamiento crítico"  
  - **Then** el sistema muestra únicamente cursos que cumplan ambos criterios  


## HU3 – Buscar cursos
Yo como estudiante quiero buscar cursos por nombre o palabra clave para encontrarlos rápidamente.

**Feature:** Buscar cursos

- **Scenario:** Búsqueda parcial case insensitive  
  - **Given** que existe un curso llamado "Introducción a la Programación"  
  - **When** el estudiante busca "prog"  
  - **Then** el sistema muestra el curso "Introducción a la Programación"  

- **Scenario:** Búsqueda sin coincidencias  
  - **Given** que el estudiante busca "astrofísica avanzada"  
  - **When** no existen cursos con esa palabra clave  
  - **Then** el sistema muestra mensaje de sin resultados  


## HU4 – Ver ficha de curso
Yo como estudiante quiero ver la ficha detallada de un curso para comprender su contenido antes de inscribirme.

**Feature:** Visualizar ficha completa del curso

- **Scenario:** Visualizar ficha de curso existente  
  - **Given** que el curso existe en el sistema  
  - **When** el estudiante accede a la ficha del curso  
  - **Then** el sistema muestra descripción, créditos, competencias, resultados de aprendizaje y prerrequisitos  

- **Scenario:** Acceso a curso inexistente  
  - **Given** que el curso no existe  
  - **When** el estudiante intenta acceder mediante URL directa  
  - **Then** el sistema muestra error 404  


## HU5 – Evaluar curso
Yo como estudiante quiero evaluar un curso que tomé para compartir mi experiencia.

**Feature:** Registrar evaluación de curso

- **Scenario:** Evaluar curso aprobado  
  - **Given** que el estudiante aprobó el curso con estado "finalizado"  
  - **When** envía una evaluación con calificación y comentario  
  - **Then** el sistema guarda la evaluación asociada al estudiante y al curso  

- **Scenario:** Intentar evaluar curso no finalizado  
  - **Given** que el estudiante está inscrito pero no ha finalizado el curso  
  - **When** intenta enviar evaluación  
  - **Then** el sistema bloquea la acción mostrando mensaje de restricción  


## HU6 – Editar o eliminar evaluación
Yo como estudiante quiero editar o eliminar mi evaluación para corregir mi retroalimentación.

**Feature:** Gestionar evaluación propia

- **Scenario:** Editar evaluación existente  
  - **Given** que el estudiante ya tiene una evaluación registrada  
  - **When** modifica la calificación o comentario  
  - **Then** el sistema actualiza la evaluación  

- **Scenario:** Eliminar evaluación  
  - **Given** que el estudiante tiene una evaluación registrada  
  - **When** selecciona eliminar evaluación  
  - **Then** el sistema elimina el registro permanentemente  


## HU7 – Ver evaluaciones de un curso
Yo como administrador quiero ver las evaluaciones de un curso para entender la percepción estudiantil.

**Feature:** Consultar evaluaciones por curso

- **Scenario:** Ver listado de evaluaciones  
  - **Given** que existen evaluaciones registradas para un curso  
  - **When** el administrador accede al módulo de evaluaciones  
  - **Then** el sistema muestra lista con calificación, comentario y fecha  

- **Scenario:** Curso sin evaluaciones  
  - **Given** que el curso no tiene evaluaciones  
  - **When** el administrador accede  
  - **Then** el sistema muestra mensaje de sin evaluaciones  


## HU8 – Ver métricas agregadas
Yo como administrador quiero ver métricas agregadas de evaluación para identificar tendencias.

**Feature:** Visualizar métricas de curso

- **Scenario:** Mostrar métricas disponibles  
  - **Given** que el curso tiene evaluaciones registradas  
  - **When** el administrador consulta métricas  
  - **Then** el sistema muestra promedio de calificación  
  - **And** total de evaluaciones  
  - **And** distribución de calificaciones  

- **Scenario:** Curso sin suficientes evaluaciones  
  - **Given** que el curso tiene menos de 3 evaluaciones  
  - **When** el administrador consulta métricas  
  - **Then** el sistema muestra mensaje de datos insuficientes  


## HU9 – Ver histórico de evaluaciones
Yo como administrador quiero consultar evaluaciones históricas para analizar la evolución de un curso.

**Feature:** Consultar histórico de evaluaciones

- **Scenario:** Ver histórico por periodo  
  - **Given** que existen evaluaciones en distintos semestres  
  - **When** el administrador filtra por semestre  
  - **Then** el sistema muestra evaluaciones del periodo seleccionado  

- **Scenario:** Periodo sin registros  
  - **Given** que no existen evaluaciones en el semestre seleccionado  
  - **When** el administrador consulta histórico  
  - **Then** el sistema muestra mensaje sin registros  


# COMPONENTE 2 – EQUIVALENCIAS INTERNACIONALES

## HU10 – Consultar cursos del área para equivalencias
Yo como estudiante en movilidad quiero consultar la información detallada de los cursos del área para compararlos con cursos externos.

**Feature:** Consultar cursos del área para equivalencias

- **Scenario:** Visualizar cursos con información académica completa  
  - **Given** que existen cursos registrados en el sistema  
  - **When** el estudiante accede al módulo de equivalencias  
  - **Then** el sistema muestra cursos con código, nombre, créditos, competencias y resultados de aprendizaje  

- **Scenario:** No existen cursos registrados  
  - **Given** que no existen cursos en el sistema  
  - **When** el estudiante accede al módulo  
  - **Then** el sistema muestra mensaje indicando que no hay cursos disponibles  


## HU11 – Registrar curso externo
Yo como estudiante quiero registrar un curso de una universidad extranjera para iniciar una propuesta de equivalencia.

**Feature:** Registrar curso extranjero

- **Scenario:** Registrar curso externo correctamente  
  - **Given** que el estudiante ingresa nombre del curso, universidad, créditos y descripción  
  - **When** guarda el curso externo  
  - **Then** el sistema registra el curso asociado al estudiante  

- **Scenario:** Intentar guardar con datos obligatorios faltantes  
  - **Given** que faltan nombre del curso o universidad o créditos  
  - **When** el estudiante intenta guardar  
  - **Then** el sistema bloquea el registro y solicita completar campos obligatorios  


## HU12 – Adjuntar documentos del curso externo
Yo como estudiante quiero adjuntar documentos del curso externo para sustentar la equivalencia.

**Feature:** Adjuntar documentos de soporte

- **Scenario:** Adjuntar archivo válido  
  - **Given** que el archivo es PDF y pesa menos de 5MB  
  - **When** el estudiante carga el documento  
  - **Then** el sistema guarda el archivo correctamente  

- **Scenario:** Archivo inválido o excede tamaño permitido  
  - **Given** que el archivo no es PDF o supera 5MB  
  - **When** el estudiante intenta cargarlo  
  - **Then** el sistema rechaza el archivo mostrando mensaje de error  


## HU13 – Obtener sugerencia preliminar de equivalencia
Yo como estudiante quiero recibir una sugerencia preliminar de equivalencia para saber si mi propuesta tiene viabilidad.

**Feature:** Generar sugerencia preliminar

- **Scenario:** Generar sugerencia con información suficiente  
  - **Given** que el curso externo tiene créditos, descripción y sílabo adjunto  
  - **When** el estudiante solicita sugerencia  
  - **Then** el sistema genera recomendación preliminar de equivalencia  

- **Scenario:** Información insuficiente para sugerencia  
  - **Given** que falta descripción o sílabo del curso externo  
  - **When** el estudiante solicita sugerencia  
  - **Then** el sistema solicita completar la información faltante  


## HU14 – Enviar solicitud formal de equivalencia
Yo como estudiante quiero enviar mi solicitud de equivalencia para revisión académica.

**Feature:** Enviar solicitud de equivalencia

- **Scenario:** Enviar solicitud completa  
  - **Given** que el curso externo tiene documentos y sugerencia preliminar  
  - **When** el estudiante envía la solicitud  
  - **Then** el sistema registra la solicitud con estado "enviada"  

- **Scenario:** Bloquear envío por información incompleta  
  - **Given** que faltan documentos o datos obligatorios  
  - **When** el estudiante intenta enviar la solicitud  
  - **Then** el sistema bloquea el envío y muestra mensaje de error  


## HU15 – Consultar estado de solicitud
Yo como estudiante quiero consultar el estado de mi solicitud para hacer seguimiento.

**Feature:** Ver estado de solicitud

- **Scenario:** Visualizar estado válido  
  - **Given** que existe una solicitud registrada  
  - **When** el estudiante consulta su solicitud  
  - **Then** el sistema muestra uno de los estados: enviada, en revisión, aprobada o rechazada  

- **Scenario:** Estudiante sin solicitudes  
  - **Given** que el estudiante no ha enviado solicitudes  
  - **When** accede al módulo  
  - **Then** el sistema muestra mensaje sin solicitudes  


## HU16 – Revisar solicitudes de equivalencia
Yo como administrador quiero revisar solicitudes de equivalencia para evaluarlas.

**Feature:** Consultar solicitudes pendientes

- **Scenario:** Ver solicitudes en revisión  
  - **Given** que existen solicitudes con estado "enviada"  
  - **When** el administrador accede al módulo  
  - **Then** el sistema muestra listado de solicitudes pendientes  

- **Scenario:** No existen solicitudes pendientes  
  - **Given** que no hay solicitudes registradas  
  - **When** el administrador accede al módulo  
  - **Then** el sistema muestra mensaje sin solicitudes  


## HU17 – Aprobar o rechazar equivalencia
Yo como administrador quiero aprobar o rechazar una equivalencia para registrar la decisión.

**Feature:** Decidir equivalencias

- **Scenario:** Aprobar solicitud  
  - **Given** que la solicitud está en estado "en revisión"  
  - **When** el administrador aprueba la equivalencia  
  - **Then** el sistema cambia el estado a "aprobada"  

- **Scenario:** Rechazar solicitud  
  - **Given** que la solicitud está en estado "en revisión"  
  - **When** el administrador rechaza la equivalencia  
  - **Then** el sistema cambia el estado a "rechazada"  


## HU18 – Consultar equivalencias previas
Yo como administrador quiero consultar equivalencias aprobadas previamente para reutilizar criterios.

**Feature:** Consultar historial de equivalencias

- **Scenario:** Ver equivalencias aprobadas  
  - **Given** que existen equivalencias aprobadas  
  - **When** el administrador consulta el historial  
  - **Then** el sistema muestra cursos origen y cursos equivalentes  

- **Scenario:** No existen equivalencias previas  
  - **Given** que no existen equivalencias aprobadas  
  - **When** el administrador consulta historial  
  - **Then** el sistema muestra mensaje sin registros  


# REPOSITORIO DE CURSOS

## HU19 – Crear curso
Yo como administrador quiero crear cursos en el sistema para mantener actualizado el catálogo.

**Feature:** Crear curso en el repositorio

- **Scenario:** Crear curso con permisos de administrador  
  - **Given** que el usuario tiene rol administrador  
  - **When** registra código, nombre, créditos y descripción  
  - **Then** el sistema crea el curso en el repositorio  

- **Scenario:** Usuario sin permisos intenta crear curso  
  - **Given** que el usuario no tiene rol administrador  
  - **When** intenta crear un curso  
  - **Then** el sistema bloquea la acción  


## HU20 – Editar curso
Yo como administrador quiero editar la información de un curso para mantenerla vigente.

**Feature:** Editar curso existente

- **Scenario:** Editar curso con permisos  
  - **Given** que el usuario tiene rol administrador y el curso existe  
  - **When** actualiza la información del curso  
  - **Then** el sistema guarda los cambios  

- **Scenario:** Usuario sin permisos intenta editar curso  
  - **Given** que el usuario no es administrador  
  - **When** intenta editar un curso  
  - **Then** el sistema bloquea la acción
 
  # Retroalimentaciones y gestión interna

## HU1 – Visualización de syllabus
Yo como jefe de departamento quiero visualizar el syllabus de un curso registrado para revisar sus objetivos de aprendizaje y contenidos.

**Feature:** Visualizar syllabus de un curso

- **Scenario:** Curso con syllabus completo  
  - **Given** que existe un curso registrado con los campos nombre, objetivos de aprendizaje y contenidos diligenciados  
  - **When** el jefe de departamento consulta el syllabus del curso  
  - **Then** el sistema muestra el nombre del curso  
  - **And** muestra los objetivos de aprendizaje  
  - **And** muestra los contenidos  

- **Scenario:** Curso sin syllabus completo  
  - **Given** que existe un curso registrado sin objetivos de aprendizaje o sin contenidos  
  - **When** el jefe de departamento consulta el syllabus del curso  
  - **Then** el sistema muestra un mensaje indicando que el syllabus está incompleto  


## HU2 – Registro de decisión sobre propuestas
Yo como jefe de departamento quiero registrar una decisión sobre una propuesta de materia para definir su estado dentro del proceso académico.

**Feature:** Gestionar decisiones de propuestas

- **Scenario:** Registro de decisión válida  
  - **Given** que existe una propuesta con los campos nombre, objetivos y créditos diligenciados  
  - **When** el jefe registra una decisión con valor “aprobado”, “rechazado” o “en revisión”  
  - **Then** el sistema guarda el estado seleccionado  
  - **And** registra la fecha de la decisión  

- **Scenario:** Registro con propuesta incompleta  
  - **Given** que existe una propuesta con campos obligatorios vacíos  
  - **When** el jefe intenta registrar una decisión  
  - **Then** el sistema no permite guardar la decisión  
  - **And** indica los campos obligatorios faltantes  


## HU3 – Selección de cursos para comparación
Yo como jefe de departamento quiero seleccionar exactamente dos cursos para realizar su comparación.

**Feature:** Seleccionar cursos para comparar

- **Scenario:** Selección válida de dos cursos  
  - **Given** que existen al menos dos cursos registrados en el sistema  
  - **When** el jefe selecciona dos cursos diferentes  
  - **Then** el sistema registra la selección de los dos cursos  

- **Scenario:** Selección inválida de cursos  
  - **Given** que existen cursos registrados en el sistema  
  - **When** el jefe selecciona menos o más de dos cursos  
  - **Then** el sistema no permite continuar con la comparación  


## HU4 – Comparación de cursos
Yo como jefe de departamento quiero comparar los objetivos de aprendizaje de dos cursos seleccionados para identificar diferencias entre ellos.

**Feature:** Comparar cursos

- **Scenario:** Comparación válida  
  - **Given** que hay dos cursos seleccionados  
  - **And** ambos tienen objetivos de aprendizaje registrados  
  - **When** el jefe realiza la comparación  
  - **Then** el sistema muestra los objetivos de aprendizaje de ambos cursos  

- **Scenario:** Comparación con información incompleta  
  - **Given** que hay dos cursos seleccionados  
  - **And** uno de los cursos no tiene objetivos de aprendizaje registrados  
  - **When** el jefe realiza la comparación  
  - **Then** el sistema indica que uno de los cursos no tiene información suficiente  


## HU5 – Registro de cursos
Yo como asistente del departamento quiero registrar un curso con sus datos básicos para mantener actualizada la información académica.

**Feature:** Registrar cursos

- **Scenario:** Registro válido de curso  
  - **Given** que el asistente está en el formulario de registro  
  - **When** ingresa nombre del curso (texto), créditos (entero mayor a 0) y programa académico existente  
  - **Then** el sistema guarda el curso  

- **Scenario:** Registro con datos inválidos  
  - **Given** que el asistente está en el formulario de registro  
  - **When** ingresa créditos iguales a 0 o deja campos obligatorios vacíos  
  - **Then** el sistema no guarda el curso  
  - **And** indica los errores en los campos  


## HU6 – Consulta de cursos
Yo como jefe de departamento quiero consultar los cursos registrados para acceder a su información básica.

**Feature:** Consultar cursos

- **Scenario:** Consulta con cursos existentes  
  - **Given** que existen cursos registrados en el sistema  
  - **When** el jefe consulta la lista de cursos  
  - **Then** el sistema muestra el nombre del curso y el programa académico de cada uno  

- **Scenario:** Consulta sin cursos  
  - **Given** que no existen cursos registrados en el sistema  
  - **When** el jefe consulta la lista de cursos  
  - **Then** el sistema indica que no hay cursos registrados  

#Ultimas historias de usuario con respecto a los nuevos requerimientos

# HU1 — Diligenciar encuesta de evaluación

## Título: Diligenciar encuesta de evaluación de asignatura

**Yo, como** estudiante  
**Quiero** diligenciar una encuesta de evaluación asociada a un curso y periodo académico cursado  
**Para** registrar mi opinión sobre la calidad de la asignatura y el desempeño académico.  

## Criterios de aceptación

### Scenario: Acceso exitoso a encuesta disponible
**Given** el estudiante ha cursado una asignatura en un periodo académico válido  
**When** accede al módulo de evaluación  
**Then** el sistema muestra la encuesta correspondiente al curso y periodo.  

### Scenario: Envío exitoso de encuesta diligenciada
**Given** el estudiante completó todas las preguntas y agregó un comentario obligatorio  
**When** selecciona enviar encuesta  
**Then** el sistema registra las respuestas y muestra confirmación de envío exitoso.  

---

# HU2 — Validar y enviar encuesta

## Título: Validación y envío definitivo de encuesta

**Yo, como** estudiante  
**Quiero** validar que mi encuesta esté completa antes de enviarla  
**Para** asegurar que mi evaluación sea registrada correctamente.  

## Criterios de aceptación

### Scenario: Validación exitosa
**Given** la encuesta tiene todas las respuestas completas y comentario válido  
**When** el estudiante selecciona validar y enviar  
**Then** el sistema cambia el estado a ENVIADA.  

### Scenario: Validación fallida por preguntas incompletas
**Given** existen preguntas sin responder  
**When** el estudiante intenta enviar la encuesta  
**Then** el sistema muestra mensaje indicando preguntas pendientes.  

---

# HU3 — Seleccionar anonimato

## Título: Selección de privacidad de encuesta

**Yo, como** estudiante  
**Quiero** decidir si mi encuesta será anónima o identificada  
**Para** controlar la privacidad de mi información.  

## Criterios de aceptación

### Scenario: Selección de envío anónimo
**Given** el estudiante diligenció la encuesta  
**When** activa la opción anónima  
**Then** el sistema registra la preferencia de anonimato.  

### Scenario: Selección de envío identificado
**Given** el estudiante diligenció la encuesta  
**When** desactiva la opción anónima  
**Then** el sistema asocia la identidad al envío.  

---

# HU4 — Consultar evaluaciones filtradas

## Título: Consulta de evaluaciones filtradas

**Yo, como** jefe de departamento  
**Quiero** consultar evaluaciones usando filtros  
**Para** revisar información específica de cursos y periodos.  

## Criterios de aceptación

### Scenario: Filtrado por estado
**Given** existen evaluaciones registradas  
**When** el jefe filtra por estado  
**Then** el sistema muestra solo evaluaciones coincidentes.  

### Scenario: Ocultamiento de identidad en anónimas
**Given** existe una evaluación anónima  
**When** el jefe visualiza resultados  
**Then** el sistema oculta identidad del estudiante.  

---

# HU5 — Vista filtrable de evaluaciones

## Título: Vista filtrable de evaluaciones institucionales

**Yo, como** jefe de departamento  
**Quiero** visualizar evaluaciones en una interfaz filtrable  
**Para** facilitar el control de calidad institucional.  

## Criterios de aceptación

### Scenario: Filtrado por curso y periodo
**Given** el jefe accede a la vista de evaluaciones  
**When** selecciona curso y periodo  
**Then** el sistema actualiza la lista filtrada.  

### Scenario: No existen resultados para filtros seleccionados
**Given** el jefe de departamento accede a la vista de evaluaciones  
**And** aplica filtros por curso, periodo y estado sin coincidencias  
**When** ejecuta la búsqueda  
**Then** el sistema muestra un mensaje indicando "No se encontraron evaluaciones para los filtros seleccionados".  

---

# HU6 — Rechazar validación con justificación

## Título: Rechazo de evaluación con justificación

**Yo, como** jefe de departamento  
**Quiero** rechazar evaluaciones pendientes con una justificación obligatoria  
**Para** dejar trazabilidad de mis decisiones.  

## Criterios de aceptación

### Scenario: Rechazo exitoso
**Given** una evaluación está en estado pendiente  
**When** el jefe registra motivo válido y rechaza  
**Then** el sistema actualiza estado a RECHAZADA.  

### Scenario: Rechazo fallido por justificación corta
**Given** el motivo tiene menos de 10 caracteres  
**When** intenta rechazar  
**Then** el sistema muestra error de validación.  

---

# HU7 — Generar reportes analíticos

## Título: Generación de reportes analíticos

**Yo, como** jefe de departamento  
**Quiero** generar reportes analíticos de retroalimentación  
**Para** identificar tendencias académicas.  

## Criterios de aceptación

### Scenario: Generación exitosa de reporte
**Given** existen evaluaciones consolidadas  
**When** el jefe solicita reporte  
**Then** el sistema genera métricas y comparaciones.  

### Scenario: Generación de reporte con datos insuficientes
**Given** no existen evaluaciones aprobadas o rechazadas para el curso seleccionado  
**When** el jefe solicita generar reporte  
**Then** el sistema informa que no hay datos suficientes para análisis.  

---

# HU8 — Registrar cierre de periodo académico

## Título: Registro de cierre académico

**Yo, como** sistema administrativo  
**Quiero** registrar el cierre de un periodo académico  
**Para** activar procesos automáticos institucionales.  

## Criterios de aceptación

### Scenario: Registro exitoso de cierre
**Given** el periodo está activo  
**When** se registra fecha de cierre  
**Then** el sistema marca el periodo como cerrado.  

### Scenario: Intento de cierre de periodo ya cerrado
**Given** el periodo académico ya se encuentra registrado como cerrado  
**When** el administrador intenta registrar nuevamente el cierre  
**Then** el sistema muestra mensaje indicando que el periodo ya fue cerrado previamente.  

---

# HU9 — Envío automático de reportes

## Título: Distribución automática de reportes

**Yo, como** sistema  
**Quiero** enviar automáticamente reportes a jefes de departamento  
**Para** garantizar entrega oportuna de información.  

## Criterios de aceptación

### Scenario: Envío automático exitoso
**Given** el periodo académico fue cerrado  
**When** se generan reportes  
**Then** el sistema los envía automáticamente.  

### Scenario: Fallo en envío automático de reportes
**Given** el sistema generó los reportes correctamente  
**And** ocurre un error en el envío al jefe de departamento  
**When** se intenta distribuir automáticamente  
**Then** el sistema registra el fallo y notifica que el envío no pudo completarse.  

---

# HU10 — Consultar histórico de reportes

## Título: Consulta histórica de reportes

**Yo, como** jefe de departamento  
**Quiero** consultar reportes históricos  
**Para** analizar evolución académica.  

## Criterios de aceptación

### Scenario: Consulta exitosa
**Given** existen reportes históricos  
**When** el jefe aplica filtros  
**Then** el sistema muestra reportes coincidentes.  

### Scenario: Consulta sin filtros opcionales
**Given** el jefe de departamento accede al histórico de reportes  
**When** consulta sin especificar curso ni periodo académico  
**Then** el sistema muestra todos los reportes disponibles asociados a su departamento.  

---

# HU11 — Comparar cursos con IA

## Título: Comparación inteligente de cursos

**Yo, como** jefe de departamento  
**Quiero** comparar cursos mediante inteligencia artificial  
**Para** identificar similitudes y oportunidades de mejora.  

## Criterios de aceptación

### Scenario: Comparación exitosa
**Given** dos cursos válidos seleccionados  
**When** el jefe ejecuta comparación  
**Then** el sistema muestra porcentaje de similitud y recomendación.  

### Scenario: Comparación fallida por cursos inválidos
**Given** uno o ambos cursos seleccionados no existen o no están validados  
**When** el jefe ejecuta la comparación  
**Then** el sistema muestra un mensaje indicando que la comparación no puede realizarse.  

---

# HU12 — Comentario obligatorio

## Título: Registro de comentario obligatorio

**Yo, como** estudiante  
**Quiero** ingresar un comentario obligatorio de mínimo 50 palabras  
**Para** aportar contexto cualitativo a mi evaluación.  

## Criterios de aceptación

### Scenario: Comentario válido
**Given** el comentario tiene al menos 50 palabras  
**When** el estudiante continúa  
**Then** el sistema permite seguir con el proceso.  

### Scenario: Comentario inválido
**Given** el comentario tiene menos de 50 palabras  
**When** intenta continuar  
**Then** el sistema bloquea avance y muestra mensaje de error.  
