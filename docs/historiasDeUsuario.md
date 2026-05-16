# Historias de Usuario

## Solicitud de equivalencia

### Historia 1

**Título:** Registro de solicitud de equivalencia

**Historia:**
Yo, como estudiante, quiero registrar una solicitud de equivalencia con la información del curso y documentos, para que mi curso sea evaluado por la universidad.

**Criterios de aceptación:**

#### Scenario: Registro exitoso con datos completos

**Given:** El estudiante se encuentra en el formulario de solicitud

**When:** Ingresa curso origen, curso destino y adjunta documentos válidos

**Then:** El sistema guarda la solicitud correctamente

**And:** Muestra un mensaje de confirmación

#### Scenario: Registro fallido por datos incompletos

**Given:** El estudiante se encuentra en el formulario de solicitud

**When:** Omite información obligatoria

**Then:** El sistema muestra un mensaje de error indicando campos faltantes

#### Scenario: Registro fallido por documentos inválidos

**Given:** El estudiante se encuentra en el formulario de solicitud
**When:** Adjunta documentos en formato no permitido
**Then:** El sistema muestra un mensaje indicando el formato inválido

---

### Historia de usuario 2

**Título:** Asignación automática de solicitudes

**Historia:**
Yo, como administrador del sistema, quiero asignar automáticamente las solicitudes al responsable correspondiente, para agilizar el proceso de evaluación.

**Criterios de aceptación:**

#### Scenario: Asignación correcta según departamento

**Given:** Existe una solicitud registrada

**When:** El sistema identifica el departamento del curso destino

**Then:** Asigna la solicitud al responsable correspondiente

#### Scenario: Solicitud sin departamento identificado

**Given:** Existe una solicitud registrada

**And:** El sistema no puede identificar el departamento

**When:** Intenta asignarla

**Then:** La solicitud queda en estado pendiente de asignación

**And:** Se notifica al asistente

---

### Historia de usuario 3

**Título:** Evaluación preliminar con inteligencia artificial

**Historia:**
Yo, como jefe de departamento, quiero recibir una clasificación automática de las solicitudes, para priorizar y optimizar mi revisión.

**Criterios de aceptación:**

#### Scenario: Clasificación en alto cumplimiento

**Given:** Existe una solicitud registrada

**When:** El sistema ejecuta el análisis de IA

**And:** El curso cumple la mayoría de criterios

**Then:** Clasifica la solicitud como "alto"

#### Scenario: Clasificación en medio cumplimiento

**Given:** Existe una solicitud registrada

**When:** El sistema ejecuta el análisis de IA

**And:** El curso cumple parcialmente los criterios

**Then:** Clasifica la solicitud como "medio"


#### Scenario: Clasificación en bajo cumplimiento

**Given:** Existe una solicitud registrada

**When:** El sistema ejecuta el análisis de IA

**And:** El curso no cumple los criterios

**Then:** Clasifica la solicitud como "bajo"


---

### Historia de usuario 4

**Título:** Consulta de equivalencias previas

**Historia:**
Yo, como jefe de departamento, quiero consultar equivalencias previamente aprobadas o rechazadas, para evitar reprocesar solicitudes similares.

**Criterios de aceptación:**

#### Scenario: Consulta exitosa de historial

**Given:** El evaluador está en el sistema

**When:** Busca por curso origen o curso destino

**Then:** El sistema muestra las equivalencias previas


#### Scenario: Consulta sin resultados

**Given:** El evaluador está en el sistema

**When:** Busca un curso sin registros previos

**Then:** El sistema muestra un mensaje indicando que no hay resultados


---

### Historia de usuario 5

**Título:** Actualización de decisiones históricas

**Historia:**
Yo, como jefe de departamento, quiero modificar decisiones anteriores, para mantener actualizados los criterios académicos.

**Criterios de aceptación:**

#### Scenario: Actualización exitosa de decisión

**Given:** Existe una equivalencia previamente registrada

**When:** El jefe modifica el estado de la decisión

**Then:** El sistema actualiza la información

**And:** Guarda el cambio en el historial


#### Scenario: Intento de actualización sin permisos

**Given:** Existe una equivalencia registrada

**And:** El usuario no es jefe de departamento

**When:** Intenta modificar la decisión

**Then:** El sistema bloquea la acción

**And:** Muestra un mensaje de acceso denegado


---

### Historia de usuario 6

**Título:** Notificación de cambios en solicitudes

**Historia:**
Yo, como estudiante, quiero recibir notificaciones sobre el estado de mi solicitud, para estar informado del proceso.

**Criterios de aceptación:**

#### Scenario: Notificación por cambio de estado

**Given:** Existe una solicitud en proceso

**When:** El estado cambia (aprobado, rechazado o pendiente)

**Then:** El sistema envía una notificación al estudiante


#### Scenario: Consulta manual del estado

**Given:** El estudiante accede al sistema

**When:** Revisa sus solicitudes

**Then:** El sistema muestra el estado actualizado


### Historia de usuario 7
Yo como estudiante en movilidad quiero consultar la información detallada de los cursos del área para compararlos con cursos externos.

**Feature:** Consultar cursos del área para equivalencias

- #### Scenario: Visualizar cursos con información académica completa  
  - **Given** que existen cursos registrados en el sistema  
  - **When** el estudiante accede al módulo de equivalencias  
  - **Then** el sistema muestra cursos con código, nombre, créditos, competencias y resultados de aprendizaje  

- #### Scenario: No existen cursos registrados  
  - **Given** que no existen cursos en el sistema  
  - **When** el estudiante accede al módulo  
  - **Then** el sistema muestra mensaje indicando que no hay cursos disponibles  


### Historia de usuario 8
Yo como estudiante quiero registrar un curso de una universidad extranjera para iniciar una propuesta de equivalencia.

**Feature:** Registrar curso extranjero

 #### Scenario: Registrar curso externo correctamente  
  - **Given** que el estudiante ingresa nombre del curso, universidad, créditos y descripción  
  - **When** guarda el curso externo  
  - **Then** el sistema registra el curso asociado al estudiante  

- #### Scenario: Intentar guardar con datos obligatorios faltantes  
  - **Given** que faltan nombre del curso o universidad o créditos  
  - **When** el estudiante intenta guardar  
  - **Then** el sistema bloquea el registro y solicita completar campos obligatorios  


### Historia de usuario 9
Yo como estudiante quiero adjuntar documentos del curso externo para sustentar la equivalencia.

**Feature:** Adjuntar documentos de soporte

- #### Scenario: Adjuntar archivo válido  
  - **Given** que el archivo es PDF y pesa menos de 5MB  
  - **When** el estudiante carga el documento  
  - **Then** el sistema guarda el archivo correctamente  

  #### Scenario: Archivo inválido o excede tamaño permitido  
  - **Given** que el archivo no es PDF o supera 5MB  
  - **When** el estudiante intenta cargarlo  
  - **Then** el sistema rechaza el archivo mostrando mensaje de error  


### Historia de usuario 10
Yo como estudiante quiero recibir una sugerencia preliminar de equivalencia para saber si mi propuesta tiene viabilidad.

**Feature:** Generar sugerencia preliminar

- #### Scenario: Generar sugerencia con información suficiente  
  - **Given** que el curso externo tiene créditos, descripción y sílabo adjunto  
  - **When** el estudiante solicita sugerencia  
  - **Then** el sistema genera recomendación preliminar de equivalencia  

- #### Scenario: Información insuficiente para sugerencia  
  - **Given** que falta descripción o sílabo del curso externo  
  - **When** el estudiante solicita sugerencia  
  - **Then** el sistema solicita completar la información faltante  


### Historia de usuario 11
Yo como estudiante quiero enviar mi solicitud de equivalencia para revisión académica.

**Feature:** Enviar solicitud de equivalencia

  #### Scenario: Enviar solicitud completa  
  - **Given** que el curso externo tiene documentos y sugerencia preliminar  
  - **When** el estudiante envía la solicitud  
  - **Then** el sistema registra la solicitud con estado "enviada"  

  #### Scenario: Bloquear envío por información incompleta  
  - **Given** que faltan documentos o datos obligatorios  
  - **When** el estudiante intenta enviar la solicitud  
  - **Then** el sistema bloquea el envío y muestra mensaje de error  


### Historia de usuario 12
Yo como estudiante quiero consultar el estado de mi solicitud para hacer seguimiento.

**Feature:** Ver estado de solicitud

- #### Scenario: Visualizar estado válido  
  - **Given** que existe una solicitud registrada  
  - **When** el estudiante consulta su solicitud  
  - **Then** el sistema muestra uno de los estados: enviada, en revisión, aprobada o rechazada  

- #### Scenario: Estudiante sin solicitudes  
  - **Given** que el estudiante no ha enviado solicitudes  
  - **When** accede al módulo  
  - **Then** el sistema muestra mensaje sin solicitudes  


### Historia de usuario 13
Yo como administrador quiero revisar solicitudes de equivalencia para evaluarlas.

**Feature:** Consultar solicitudes pendientes

- #### Scenario: Ver solicitudes en revisión  
  - **Given** que existen solicitudes con estado "enviada"  
  - **When** el administrador accede al módulo  
  - **Then** el sistema muestra listado de solicitudes pendientes  

- #### Scenario: No existen solicitudes pendientes  
  - **Given** que no hay solicitudes registradas  
  - **When** el administrador accede al módulo  
  - **Then** el sistema muestra mensaje sin solicitudes  


### Historia de usuario 14
Yo como administrador quiero aprobar o rechazar una equivalencia para registrar la decisión.

**Feature:** Decidir equivalencias

- #### Scenario: Aprobar solicitud  
  - **Given** que la solicitud está en estado "en revisión"  
  - **When** el administrador aprueba la equivalencia  
  - **Then** el sistema cambia el estado a "aprobada"  

- #### Scenario: Rechazar solicitud  
  - **Given** que la solicitud está en estado "en revisión"  
  - **When** el administrador rechaza la equivalencia  
  - **Then** el sistema cambia el estado a "rechazada"  


### Historia de usuario 15
Yo como administrador quiero consultar equivalencias aprobadas previamente para reutilizar criterios.

**Feature:** Consultar historial de equivalencias

- #### Scenario: Ver equivalencias aprobadas  
  - **Given** que existen equivalencias aprobadas  
  - **When** el administrador consulta el historial  
  - **Then** el sistema muestra cursos origen y cursos equivalentes  

- #### Scenario: No existen equivalencias previas  
  - **Given** que no existen equivalencias aprobadas  
  - **When** el administrador consulta historial  
  - **Then** el sistema muestra mensaje sin registros  

## Gestion de Retro-Alimentacion

### Historia de usuario 16
Yo como estudiante quiero evaluar un curso que tomé para compartir mi experiencia.

**Feature:** Registrar evaluación de curso

- #### Scenario: Evaluar curso aprobado  
  - **Given** que el estudiante aprobó el curso con estado "finalizado"  
  - **When** envía una evaluación con calificación y comentario  
  - **Then** el sistema guarda la evaluación asociada al estudiante y al curso  

- #### Scenario: Intentar evaluar curso no finalizado  
  - **Given** que el estudiante está inscrito pero no ha finalizado el curso  
  - **When** intenta enviar evaluación  
  - **Then** el sistema bloquea la acción mostrando mensaje de restricción  


### Historia de usuario 17
Yo como estudiante quiero editar o eliminar mi evaluación para corregir mi retroalimentación.

**Feature:** Gestionar evaluación propia

- #### Scenario: Editar evaluación existente  
  - **Given** que el estudiante ya tiene una evaluación registrada  
  - **When** modifica la calificación o comentario  
  - **Then** el sistema actualiza la evaluación  

- #### Scenario: Eliminar evaluación  
  - **Given** que el estudiante tiene una evaluación registrada  
  - **When** selecciona eliminar evaluación  
  - **Then** el sistema elimina el registro permanentemente  


### Historia de usuario 18
Yo como administrador quiero ver las evaluaciones de un curso para entender la percepción estudiantil.

**Feature:** Consultar evaluaciones por curso

- #### Scenario: Ver listado de evaluaciones  
  - **Given** que existen evaluaciones registradas para un curso  
  - **When** el administrador accede al módulo de evaluaciones  
  - **Then** el sistema muestra lista con calificación, comentario y fecha  

- #### Scenario: Curso sin evaluaciones  
  - **Given** que el curso no tiene evaluaciones  
  - **When** el administrador accede  
  - **Then** el sistema muestra mensaje de sin evaluaciones  


### Historia de usuario 19
Yo como administrador quiero ver métricas agregadas de evaluación para identificar tendencias.

**Feature:** Visualizar métricas de curso

#### Scenario: Mostrar métricas disponibles  
  - **Given** que el curso tiene evaluaciones registradas  
  - **When** el administrador consulta métricas  
  - **Then** el sistema muestra promedio de calificación  
  - **And** total de evaluaciones  
  - **And** distribución de calificaciones  

- #### Scenario: Curso sin suficientes evaluaciones  
  - **Given** que el curso tiene menos de 3 evaluaciones  
  - **When** el administrador consulta métricas  
  - **Then** el sistema muestra mensaje de datos insuficientes  


### Historia de usuario 20
Yo como administrador quiero consultar evaluaciones históricas para analizar la evolución de un curso.

**Feature:** Consultar histórico de evaluaciones

- #### Scenario: Ver histórico por periodo  
  - **Given** que existen evaluaciones en distintos semestres  
  - **When** el administrador filtra por semestre  
  - **Then** el sistema muestra evaluaciones del periodo seleccionado  

- #### Scenario: Periodo sin registros  
  - **Given** que no existen evaluaciones en el semestre seleccionado  
  - **When** el administrador consulta histórico  
  - **Then** el sistema muestra mensaje sin registros  

## Gestion de Informacion

### Historia de usuario 21
Yo como administrador quiero crear cursos en el sistema para mantener actualizado el catálogo.

**Feature:** Crear curso en el repositorio

- #### Scenario: Crear curso con permisos de administrador  
  - **Given** que el usuario tiene rol administrador  
  - **When** registra código, nombre, créditos y descripción  
  - **Then** el sistema crea el curso en el repositorio  

- #### Scenario: Usuario sin permisos intenta crear curso  
  - **Given** que el usuario no tiene rol administrador  
  - **When** intenta crear un curso  
  - **Then** el sistema bloquea la acción  

### Historia de usuario 22
Yo como administrador quiero editar la información de un curso para mantenerla vigente.

**Feature:** Editar curso existente

- #### Scenario: Editar curso con permisos  
  - **Given** que el usuario tiene rol administrador y el curso existe  
  - **When** actualiza la información del curso  
  - **Then** el sistema guarda los cambios  

- #### Scenario: Usuario sin permisos intenta editar curso  
  - **Given** que el usuario no es administrador  
  - **When** intenta editar un curso  
  - **Then** el sistema bloquea la acción
 

### Historia de usuario 23
Yo como jefe de departamento quiero visualizar el syllabus de un curso registrado para revisar sus objetivos de aprendizaje y contenidos.

**Feature:** Visualizar syllabus de un curso

- #### Scenario: Curso con syllabus completo  
  - **Given** que existe un curso registrado con los campos nombre, objetivos de aprendizaje y contenidos diligenciados  
  - **When** el jefe de departamento consulta el syllabus del curso  
  - **Then** el sistema muestra el nombre del curso  
  - **And** muestra los objetivos de aprendizaje  
  - **And** muestra los contenidos  

- #### Scenario: Curso sin syllabus completo  
  - **Given** que existe un curso registrado sin objetivos de aprendizaje o sin contenidos  
  - **When** el jefe de departamento consulta el syllabus del curso  
  - **Then** el sistema muestra un mensaje indicando que el syllabus está incompleto  


### Historia de usuario 24
Yo como jefe de departamento quiero registrar una decisión sobre una propuesta de materia para definir su estado dentro del proceso académico.

**Feature:** Gestionar decisiones de propuestas

- #### Scenario: Registro de decisión válida  
  - **Given** que existe una propuesta con los campos nombre, objetivos y créditos diligenciados  
  - **When** el jefe registra una decisión con valor “aprobado”, “rechazado” o “en revisión”  
  - **Then** el sistema guarda el estado seleccionado  
  - **And** registra la fecha de la decisión  

- #### Scenario: Registro con propuesta incompleta  
  - **Given** que existe una propuesta con campos obligatorios vacíos  
  - **When** el jefe intenta registrar una decisión  
  - **Then** el sistema no permite guardar la decisión  
  - **And** indica los campos obligatorios faltantes  


### Historia de usuario 25
Yo como jefe de departamento quiero seleccionar exactamente dos cursos para realizar su comparación.

**Feature:** Seleccionar cursos para comparar

- #### Scenario: Selección válida de dos cursos  
  - **Given** que existen al menos dos cursos registrados en el sistema  
  - **When** el jefe selecciona dos cursos diferentes  
  - **Then** el sistema registra la selección de los dos cursos  

- #### Scenario: Selección inválida de cursos  
  - **Given** que existen cursos registrados en el sistema  
  - **When** el jefe selecciona menos o más de dos cursos  
  - **Then** el sistema no permite continuar con la comparación  


### Historia de usuario 26
Yo como jefe de departamento quiero comparar los objetivos de aprendizaje de dos cursos seleccionados para identificar diferencias entre ellos.

**Feature:** Comparar cursos

- #### Scenario: Comparación válida  
  - **Given** que hay dos cursos seleccionados  
  - **And** ambos tienen objetivos de aprendizaje registrados  
  - **When** el jefe realiza la comparación  
  - **Then** el sistema muestra los objetivos de aprendizaje de ambos cursos  

- #### Scenario:* Comparación con información incompleta  
  - **Given** que hay dos cursos seleccionados  
  - **And** uno de los cursos no tiene objetivos de aprendizaje registrados  
  - **When** el jefe realiza la comparación  
  - **Then** el sistema indica que uno de los cursos no tiene información suficiente  


### Historia de usuario 27
Yo como asistente del departamento quiero registrar un curso con sus datos básicos para mantener actualizada la información académica.

**Feature:** Registrar cursos

- #### Scenario: Registro válido de curso  
  - **Given** que el asistente está en el formulario de registro  
  - **When** ingresa nombre del curso (texto), créditos (entero mayor a 0) y programa académico existente  
  - **Then** el sistema guarda el curso  

- #### Scenario: Registro con datos inválidos  
  - **Given** que el asistente está en el formulario de registro  
  - **When** ingresa créditos iguales a 0 o deja campos obligatorios vacíos  
  - **Then** el sistema no guarda el curso  
  - **And** indica los errores en los campos  


### Historia de usuario 28
Yo como jefe de departamento quiero consultar los cursos registrados para acceder a su información básica.

**Feature:** Consultar cursos

- #### Scenario: Consulta con cursos existentes  
  - **Given** que existen cursos registrados en el sistema  
  - **When** el jefe consulta la lista de cursos  
  - **Then** el sistema muestra el nombre del curso y el programa académico de cada uno  

- #### Scenario: Consulta sin cursos  
  - **Given** que no existen cursos registrados en el sistema  
  - **When** el jefe consulta la lista de cursos  
  - **Then** el sistema indica que no hay cursos registrados  


### Historia de usuario 29
Yo como estudiante quiero ver la lista de cursos disponibles del área para conocer las opciones que puedo elegir.

**Feature:** Visualizar catálogo de cursos

- #### Scenario: Ver listado paginado de cursos  
  - **Given** que existen al menos 15 cursos activos registrados en el sistema  
  - **When** el estudiante accede al catálogo  
  - **Then** el sistema muestra la primera página con máximo 10 cursos  
  - **And** cada curso muestra código, nombre, créditos y área  
  - **And** los cursos están ordenados alfabéticamente por nombre  

- #### Scenario: Navegar entre páginas del catálogo  
  - **Given** que existen más de 10 cursos activos  
  - **When** el estudiante selecciona la página 2  
  - **Then** el sistema muestra los siguientes cursos sin repetir los anteriores  


### Historia de usuario 30
Yo como estudiante quiero filtrar cursos por temas o competencias para encontrar opciones alineadas con mis intereses.

**Feature:** Filtrar cursos por múltiples criterios

- #### Scenario: Filtrar por un criterio  
  - **Given** que el estudiante está viendo el catálogo completo  
  - **When** aplica filtro por área "Humanidades"  
  - **Then** el sistema muestra solo cursos del área Humanidades  

- #### Scenario: Filtrar por múltiples criterios combinados  
  - **Given** que el estudiante está viendo el catálogo  
  - **When** aplica filtro por área "Humanidades" y competencia "Pensamiento crítico"  
  - **Then** el sistema muestra únicamente cursos que cumplan ambos criterios  


### Historia de usuario 31
Yo como estudiante quiero buscar cursos por nombre o palabra clave para encontrarlos rápidamente.

**Feature:** Buscar cursos

- #### Scenario: Búsqueda parcial case insensitive  
  - **Given** que existe un curso llamado "Introducción a la Programación"  
  - **When** el estudiante busca "prog"  
  - **Then** el sistema muestra el curso "Introducción a la Programación"  

- #### Scenario: Búsqueda sin coincidencias  
  - **Given** que el estudiante busca "astrofísica avanzada"  
  - **When** no existen cursos con esa palabra clave  
  - **Then** el sistema muestra mensaje de sin resultados  


### Historia de usuario 32
Yo como estudiante quiero ver la ficha detallada de un curso para comprender su contenido antes de inscribirme.

**Feature:** Visualizar ficha completa del curso

- #### Scenario: Visualizar ficha de curso existente  
  - **Given** que el curso existe en el sistema  
  - **When** el estudiante accede a la ficha del curso  
  - **Then** el sistema muestra descripción, créditos, competencias, resultados de aprendizaje y prerrequisitos  

- #### Scenario:** Acceso a curso inexistente  
  - **Given** que el curso no existe  
  - **When** el estudiante intenta acceder mediante URL directa  
  - **Then** el sistema muestra error 404

## Información de Cursos
| Título de la Historia de Usuario 33 |  Visualización de videos explicativos de cursos |
|---|---|
| **Yo, como** | Estudiante |
| **Quiero** | Visualizar videos informativos publicados por los docentes sobre sus cursos |
| **Para** | Comprender el enfoque de las materias antes de seleccionarlas |

---

# Criterios de Aceptación (Formato Gherkin)

## Scenario: Reproducción de video del curso
**Given** el módulo de la información de electiva con un video cargado  
**When** el usuario selecciona la sección "Presentación del curso"  
**Then** el sistema reproduce un video informativo del docente sobre la materia  

---

## Scenario: Disponibilidad del video
**Given** el estudiante accede a la información de una electiva  
**When** el curso tiene un video de presentación disponible  
**Then** el sistema muestra un reproductor de video accesible desde la página del curso  

---

## Scenario: Video no disponible
**Given** el estudiante accede a la información de una electiva  
**When** el curso no tiene un video de presentación disponible  
**Then** el sistema muestra un mensaje indicando que el curso no cuenta con un video informativo  


---
| Título de la Historia de Usuario 34 | Visualización de ofertas de electivas internacionales |
|---|---|
| Yo, como | Estudiante |
| Quiero | Ver la lista de las electivas ofertadas por otras universidades en convenio |
| Para | Explorar oportunidades académicas internacionales |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Consulta de cursos internacionales
Given el estudiante accede al de módulo matricular electivas  
When selecciona una universidad en convenio  
Then el sistema muestra la lista de electivas disponibles de esa institución  

### Scenario: Visualización de información del curso
Given el estudiante consulta una electiva internacional  
When selecciona un curso de la lista  
Then el sistema presenta información académica del curso, incluyendo nombre, descripción y objetivos  

### Scenario: Ausencia de electivas disponibles
Given el estudiante selecciona una universidad en convenio  
When la institución no tiene electivas disponibles  
Then el sistema muestra un mensaje indicando que no existen cursos ofertados actualmente  

---

| Título de la Historia de Usuario 35 | Búsqueda de electivas disponibles |
|---|---|
| Yo, como | Estudiante |
| Quiero | Buscar electivas que se encuentren disponibles en la universidad |
| Para | Encontrar más fácilmente los cursos que se ajusten a mis intereses académicos |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Búsqueda exitosa de una electiva
Given El estudiante está en el sitio de electivas  
When Escribe el nombre o una palabra clave relacionada con el curso  
Then El sistema muestra las electivas que coinciden con la búsqueda  

### Scenario: Búsqueda de una electiva sin resultados
Given El estudiante está en el sitio de electivas  
When Escribe una palabra para buscar un curso  
Then El sistema muestra un mensaje indicando que no se encontraron resultados  

---

| Título de la Historia de Usuario 36 | Consulta de información general de una electiva |
|---|---|
| Yo, como | Estudiante de ICESI |
| Quiero | Consultar la información principal de una electiva |
| Para | Conocer de manera rápida de qué trata el curso antes de inscribirlo |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Visualización exitosa de la información del curso
Given El estudiante ingresa al sitio de electivas  
When Selecciona una electiva de la lista  
Then El sistema muestra la descripción, objetivos, contenidos, departamento responsable y el profesor encargado  

### Scenario: Información incompleta del curso
Given El estudiante selecciona una electiva  
When La información del curso no está completa  
Then El sistema muestra los datos disponibles  
And Informa que falta información por actualizar 

---

# Historia de Usuario 37

| Título de la Historia de Usuario 37 | Acceso simplificado al syllabus |
|---|---|
| Yo, como | Estudiante de la Universidad Icesi |
| Quiero | acceder a un resumen syllabus de una electiva directamente en su descripción |
| Para | Consultar información académica detallada sin depender de sistemas externos confusos |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Consulta del syllabus de una electiva
Given el estudiante está consultando la información de una electiva  
When selecciona la opción "Ver syllabus"  
Then el sistema muestra el syllabus oficial asociado al curso con el objetivo, enfoque y porcentajes de la electiva  

### Scenario: Syllabus no disponible
Given el estudiante consulta la información de una electiva  
When el curso no tiene un syllabus publicado  
Then el sistema muestra un mensaje indicando que el syllabus no se encuentra disponible  

---



| Título de la Historia de Usuario 38 | Filtros de búsqueda de electivas |
|---|---|
| Yo, como | Estudiante |
| Quiero | filtrar electivas al buscar por contenido u horario |
| Para | Encontrar electivas que se ajusten a mi disponibilidad académica |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Búsqueda efectiva por criterios específicos
Given El estudiante está en el buscador de cursos  
When Ingresa un criterio de búsqueda como "contenido" o un "horario"  
Then El sistema muestra una lista de cursos filtrados que coinciden con los parámetros ingresados  

### Scenario: Visualización de una estructura organizada
Given El estudiante tiene duda sobre la procedencia de un curso  
When Selecciona una electiva del listado  
Then El sistema muestra a qué departamento pertenece el curso para futuras consultas  

---

| Título de la Historia de Usuario 39 | Gestión y validación de Syllabus |
|---|---|
| Yo, como | Planeador Academico |
| Quiero | Un sistema que permite organizar, consultar y validar la información de los syllabus creados por los profesores |
| Para | Que la información académica sea oficial y accesible para los estudiantes |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Validación exitosa de un nuevo syllabus
Given Un profesor ha cargado el syllabus de su curso en el sistema  
When El jefe de departamento revisa y da clic en "Aprobar"  
Then El sistema publica la información automáticamente para que sea visible para los estudiantes  

### Scenario: Consulta de syllabus aprobados
Given un syllabus ha sido aprobado  
When un estudiante consulta la información de una electiva  
Then el sistema muestra el syllabus oficial publicado  

### Scenario: Rechazo de un syllabus con observaciones
Given el jefe de departamento revisa un syllabus registrado  
When identifica información incompleta o incorrecta  
Then el sistema permite rechazar el syllabus y registrar observaciones para el profesor  

---

| Título de la Historia de Usuario 40 | Visualizar departamento al que pertenece una electiva |
|---|---|
| Yo, como | Estudiante |
| Quiero | Identificar a qué departamento pertenece cada electiva |
| Para | Saber a dónde dirigir las consultas o solicitudes relacionadas con el curso |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Visualización del departamento de una electiva
Given El estudiante está consultando la lista de las electivas  
When Selecciona una electiva  
Then El sistema muestra el departamento académico al que pertenece el curso  

### Scenario: Electiva sin departamento asignado
Given El estudiante está consultando la lista de las electivas  
When Selecciona un curso de electiva que no tiene departamento asignado  
Then El sistema informa en un mensaje indicando que la información del departamento está pendiente por actualizar  

### Scenario: Consulta del departamento desde la información del curso
Given el estudiante está visualizando la información detallada de una electiva  
When revisa los datos académicos del curso  
Then el sistema muestra el nombre del departamento académico responsable  

---

| Título de la Historia de Usuario 41 | Actualización de información académica de electivas |
|---|---|
| Yo, como | Profesor |
| Quiero | Actualizar la información registrada de mi curso |
| Para | Mantener actualizada la información académica disponible para consulta estudiantil |

## Criterios de Aceptación (Formato Gherkin)

### Scenario: Actualización de información de una electiva
Given el profesor accede a la información de una electiva registrada  
When modifica la información académica y selecciona la opción "Guardar cambios"  
Then el sistema actualiza la información y la envía al proceso de revisión académica  

### Scenario: Validación de campos obligatorios
Given el profesor está editando la información de una electiva  
When intenta guardar el formulario con campos obligatorios vacíos  
Then el sistema muestra un mensaje indicando los campos pendientes por completar  

### Scenario: Confirmación de actualización enviada
Given el profesor actualiza la información de una electiva correctamente  
When el sistema registra los cambios  
Then el sistema muestra un mensaje confirmando que la información fue enviada a revisión  
