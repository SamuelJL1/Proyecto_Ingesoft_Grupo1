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
