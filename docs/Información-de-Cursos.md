# Historias de Usuario

PETICIONES DE PABLO
## HU-01: Presentacion de cursos por videos  

*Titulo:* Presentacion de cursos por videos  
*Como:* Estudiante interesado en lo academico  
*Quiero:* Ver los videos que suben los profesores explicando de que trata su materia  
*Para:* Entender sus enfoques de manera clara  

### Criterios de aceptacion:

*Scenario: Acceso al material del curso*  
Given: El estudiante esta explorando la información de una electiva  
When: Hace clic en una seccion llamada "Presentación del docente o curso"  
Then: El sistema reproduce un video donde el profesor explica su materia y que van a hacer  

*Scenario: Interfaz para informacion*  
Given: El estudiante busca una alternativa al sistema actual (Banner)  
When: Navega por el nuevo sitio de información de cursos  
Then: El sistema presenta la informacion de manera intuitiva y visualmente atractiva  


## HU-02: Visualizacion de ofertas de electivas internacionales   

*Titulo:* Visualizacion de ofertas de electivas internacionales  
*Como:* Estudiante en porceso de intercambio  
*Quiero:* ver la lista de las electivas ofertadas por otras universidades en convenio  
*Para:* agilizar la busqueda entre los cursos extranjeros y los de ICESI  

### Criterios de aceptacion:

*Scenario: Consulta de materias en universidades en convenio*   
Given: Que el estudiante entra al modulo de movilidad internacional  
When: Selecciona una universidad extranjera de la lista  
Then: El sistema despliega los cursos disponibles en esa institucion que pueden ser tomados como electivas  

*Scenario: Identificacion de similitudes*   
Given: El estudiante visualiza la lista de cursos internacionales  
When: Compara la informacion de un curso extranjero con una electiva de ICESI  
Then: El sistema permite visualizar los objetivos de ambos para facilitar el tramite  

------------------------------------------------------------------------------

PETICIONES DE ROBIN
## HU-01: Filtros de busqueda de electivas  

*Titulo:* Filtros de busqueda de electivas  
*Como:* Estudiante de la universidad  
*Quiero:* Contar con una base de datos que permita realizar busquedas por contenido y horario  
*Para:* Encontrar electivas que se ajusten a mi disponibilidad academica  

### Criterios de aceptacion:

*Scenario: Busqueda efectiva por criterios especificos*  
Given: El estudiante esta en el buscador de cursos  
When: Ingresa un criterio de busqueda como "contenido" o un "horario"  
Then: el sistema muestra una lista de cursos filtrados que coinciden exactamente con los parametros que puso el usuario  

*Scenario: Visualizacion de una estructura organizada*  
Given: El estudiante tiene duda sobre la procedencia de un curso  
When: Selecciona una electiva del listado  
Then: El sistema muestra a que departamento pertenece el curso para futuras consultas  


## HU-02: Gestion y validacion de Syllabus  

*Titulo:* Gestion y validacion de Syllabus  
*Como:* Jefe de departamento  
*Quiero:* Un sistema que permita organizar, consultar y validar la informacion de los syllabus creados por los profesores  
*Para:* Que la informacion académica sea oficial y sea accesible para los estudiantes  

### Criterios de aceptacion:

*Scenario: Validacion exitosa de un nuevo syllabus*  
Given: Un profesor ha cargado el syllabus de su curso en el sistema  
When: El jefe de departamento revisa y le da en "Aprobar"  
Then: El sistema publica la informacion automaticamente para que sea visible para los estudiantes  

*Scenario: Agente inteligente para consultas*   
Given: El sistema cuenta con un agente inteligente integrado  
When: Un usuario realiza una pregunta compleja sobre el contenido de los syllabus  
Then: El agente inteligente procesa la base de datos y entrega una respuesta  


## Información de Cursos

# PETICIONES DE PABLO

## HU-01: Acceso simplificado al syllabus

*Título:* Acceso simplificado al syllabus  
*Yo, como:* estudiante de la Universidad Icesi  
*Quiero:* acceder fácilmente al syllabus oficial de una electiva desde una plataforma centralizada  
*Para:* consultar información académica detallada sin depender de sistemas externos confusos.

### Criterios de aceptación:

*Scenario: Consulta exitosa del syllabus*  
Given que el estudiante se encuentra consultando una electiva  
When selecciona la opción "Ver syllabus"  
Then el sistema muestra el documento oficial asociado al curso

*Scenario: Syllabus no disponible*  
Given que el estudiante consulta una electiva  
When el syllabus no ha sido publicado  
Then el sistema muestra un mensaje indicando que no está disponible

---

## HU-02: Consulta comparativa de cursos internacionales

*Título:* Consulta comparativa de cursos internacionales  
*Yo, como:* estudiante en proceso de intercambio académico  
*Quiero:* comparar electivas de universidades extranjeras con cursos de la Universidad Icesi  
*Para:* identificar similitudes académicas y agilizar mi proceso de homologación.

### Criterios de aceptación:

*Scenario: Comparación exitosa de cursos*  
Given que el estudiante selecciona una electiva internacional  
When solicita comparar su contenido con cursos de Icesi  
Then el sistema muestra los objetivos académicos de ambos cursos

*Scenario: Sin cursos comparables*  
Given que el estudiante consulta una electiva internacional  
When no existen similitudes registradas  
Then el sistema informa que no hay equivalencias disponibles


# PETICIONES DE ROBIN

## HU-01: Actualización de información académica de electivas

*Título:* Actualización de información académica de electivas  
*Yo, como:* profesor encargado de una electiva  
*Quiero:* actualizar la información registrada de mi curso  
*Para:* mantener vigente la información académica disponible para consulta estudiantil.

### Criterios de aceptación:

*Scenario: Actualización exitosa*  
Given que el profesor accede a su curso registrado  
When modifica la información y guarda los cambios  
Then el sistema actualiza la información y la envía nuevamente a revisión

*Scenario: Actualización incompleta*  
Given que el profesor está editando la información del curso  
When omite campos obligatorios  
Then el sistema muestra un mensaje indicando los datos faltantes

---

## HU-02: Consulta del estado de validación del syllabus

*Título:* Consulta del estado de validación del syllabus  
*Yo, como:* profesor encargado de una electiva  
*Quiero:* consultar el estado de revisión de la información registrada  
*Para:* conocer si fue aprobada o requiere ajustes.

### Criterios de aceptación:

*Scenario: Consulta de syllabus aprobado*  
Given que el profesor accede al sistema  
When consulta una electiva aprobada  
Then el sistema muestra el estado "Aprobado"

*Scenario: Consulta de syllabus rechazado*  
Given que el profesor accede al sistema  
When consulta una electiva rechazada  
Then el sistema muestra las observaciones registradas por el jefe de departamento
