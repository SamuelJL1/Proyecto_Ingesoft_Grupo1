# Historias de Usuario

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
