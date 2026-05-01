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
