# Historias de Usuario

PETICIONES DE PABLO
## HU-01: Presentacion de cursos por videos  

**Titulo:** Presentacion de cursos por videos  
**Como:** Estudiante interesado en lo academico  
**Quiero:** Ver los videos que suben los profesores explicando de que trata su materia  
**Para:** Entender sus enfoques de manera clara  

### Criterios de aceptacion:

**Scenario:** Acceso al material del curso  
**Given:** El estudiante esta explorando la información de una electiva  
**When:** Hace clic en una seccion llamada "Presentación del docente o curso"  
**Then:** El sistema reproduce un video donde el profesor explica su materia y que van a hacer  

**Scenario:** Interfaz para informacion  
**Given:** El estudiante busca una alternativa al sistema actual (Banner)  
**When:** Navega por el nuevo sitio de información de cursos  
**Then:** El sistema presenta la informacion de manera intuitiva y visualmente atractiva  

## RF derivado del HU-01

*RF1:* El sistema debe tener un reproductor de video que permita a los estudiantes ver las presentaciones de los docentes sobre sus cursos

*Analisis PESTLE RF:*

|  Dimension  |  Hallazgo   |  Argumentacion Etica  |
|-------------|-------------|-----------------------|
|T-Tecnologico | El contenido por video suele ser menos pesado para los estudiantes | Los videos no se conviertan en un factor de exclusión para estudiantes con limitacion |

---

## HU-02: Visualizacion de ofertas de electivas internacionales   

**Titulo:** Visualizacion de ofertas de electivas internacionales  
**Como:** Estudiante en porceso de intercambio  
**Quiero:** ver la lista de las electivas ofertadas por otras universidades en convenio  
**Para:** agilizar la busqueda entre los cursos extranjeros y los de ICESI  

### Criterios de aceptacion:

**Scenario:** Consulta de materias en universidades en convenio  
**Given:** Que el estudiante entra al modulo de movilidad internacional  
**When:** Selecciona una universidad extranjera de la lista  
**Then:** El sistema despliega los cursos disponibles en esa institucion que pueden ser tomados como electivas  

**Scenario:** Identificacion de similitudes   
**Given:** El estudiante visualiza la lista de cursos internacionales    
**When:** Compara la informacion de un curso extranjero con una electiva de ICESI    
**Then:** El sistema permite visualizar los objetivos de ambos para facilitar el tramite 

## RF derivado del HU-02

*RF2:* El sistema debe desplegar una lista de electivas de universidades extranjeras en convenio, detallando sus objetivos

*Analisis PESTLE RF:*

|  Dimension  |  Hallazgo   |  Argumentacion Etica  |
|-------------|-------------|-----------------------|
|P-Politico   | Los convenios internacionales estan sujetos a tratados diplomáticos | El sistema mostrara solo convenios activos para no generar falsas expectativas |
|L-Legal      | El intercambio de informacion de cursos debe cumplir con las leyes de proteccion de datos personales | El manejo de datos debe ser transparente para proteger la integridad del estudiante |
|A-Ambiental  | La digitalizacion del catalogo de electivas internacionales reduce el uso de folletos | El beneficio de eliminar el papel es positivo, siempre que se garantice que la información digital sea completa |

---

## HU-03: Busqueda de electivas disponibles    

**Titulo:** Busqueda de electivas disponibles    
**Como:** estudiante de ICESI    
**Quiero:** buscar electivas que se encuentren disponibles en la universidad    
**Para:** encontrar mas facilmente los cursos que se ajusten a mis intereses academicos


### Criterios de aceptacion:  

**Scenario:** Busqueda exitosa de una electiva      
**Given:** El estudiante esta en el sitio de electivas    
**When:** Escribe el nombre o una palabra clave relacionada con el curso    
**Then:** El sistema muestra las electivas que coinciden con la busqueda      

**Scenario:** Busqueda de una electiva sin resultados      
**Given:** El estudiante esta en el sitio de electivas      
**When:** Escribe una palabra para buscar un curso    
**Then:** El sistema muestra un mensaje indicando que no se encontraron resultados

---

## HU-04: Consulta de informacion general de una electiva    
**Titulo:** Consulta de informacion general de una electiva    
**Como:** Estudiante de ICESI    
**Quiero:** Consultar la informacion principal de una electiva    
**Para:** Conocer de manera rápida de que trata el curso antes de inscribirlo

### Criterios de aceptacion:    
**Scenario:** Visualizacion exitosa de la información del curso    
**Given:** Que el estudiante ingresa al sitio de electivas    
**When:** Selecciona una electiva de la lista    
**Then:** el sistema muestra la descripcion, objetivos, contenidos, departamento responsable y el profesor encargado    

**Scenario:** Información incompleta del curso    
**Given:** El estudiante selecciona una electiva    
**When:** La informacion del curso no está completa    
**Then:** El sistema muestra los datos disponibles    
**And:** Informa que falta información por actualizar

---

## HU-05: Acceso simplificado al syllabus

**Título:** Acceso simplificado al syllabus  
**Como:** estudiante de la Universidad Icesi  
**Quiero:** acceder fácilmente al syllabus oficial de una electiva desde una plataforma centralizada  
**Para:** consultar información académica detallada sin depender de sistemas externos confusos.

### Criterios de aceptación:

**Scenario:** Consulta exitosa del syllabus    
**Given:** que el estudiante se encuentra consultando una electiva  
**When:** selecciona la opción "Ver syllabus"  
**Then:** el sistema muestra el documento oficial asociado al curso

**Scenario:** Syllabus no disponible     
**Given:** que el estudiante consulta una electiva  
**When:** el syllabus no ha sido publicado  
**Then:** el sistema muestra un mensaje indicando que no está disponible

---

## HU-06: Consulta comparativa de cursos internacionales

**Título:** Consulta comparativa de cursos internacionales  
**Como:** estudiante en proceso de intercambio académico  
**Quiero:** comparar electivas de universidades extranjeras con cursos de la Universidad Icesi  
**Para:** identificar similitudes académicas y agilizar mi proceso de homologación.

### Criterios de aceptación:

**Scenario:** Comparación exitosa de cursos    
**Given:** que el estudiante selecciona una electiva internacional  
**When:** solicita comparar su contenido con cursos de Icesi  
**Then:** el sistema muestra los objetivos académicos de ambos cursos

**Scenario:** Sin cursos comparables
**Given:** que el estudiante consulta una electiva internacional  
**When:** no existen similitudes registradas  
**Then:** el sistema informa que no hay equivalencias disponibles

------------------------------------------------------------------------------

PETICIONES DE ROBIN
## HU-01: Filtros de busqueda de electivas  

**Titulo:** Filtros de busqueda de electivas  
**Como:** Estudiante de la universidad  
**Quiero:** Contar con una base de datos que permita realizar busquedas por contenido y horario  
**Para:** Encontrar electivas que se ajusten a mi disponibilidad academica  

### Criterios de aceptacion:

**Scenario:** Busqueda efectiva por criterios especificos    
**Given:** El estudiante esta en el buscador de cursos  
**When:** Ingresa un criterio de busqueda como "contenido" o un "horario"  
**Then:** el sistema muestra una lista de cursos filtrados que coinciden exactamente con los parametros que puso el usuario  

**Scenario:** Visualizacion de una estructura organizada  
**Given:** El estudiante tiene duda sobre la procedencia de un curso  
**When:** Selecciona una electiva del listado  
**Then:** El sistema muestra a que departamento pertenece el curso para futuras consultas  

## RF derivado del HU-01

*RF1:* El sistema debe permitir a los usuarios realizar busquedas de electivas filtrando por contenido, horario y departamento academico

*Analisis PESTLE RF:* 
NO APLICA

---

## HU-02: Gestion y validacion de Syllabus  

**Titulo:** Gestion y validacion de Syllabus  
**Como:** Jefe de departamento  
**Quiero:** Un sistema que permita organizar, consultar y validar la informacion de los syllabus creados por los profesores  
**Para:** Que la informacion académica sea oficial y sea accesible para los estudiantes  

### Criterios de aceptacion:

**Scenario:** Validacion exitosa de un nuevo syllabus*  
**Given:** Un profesor ha cargado el syllabus de su curso en el sistema  
**When:** El jefe de departamento revisa y le da en "Aprobar"  
**Then:** El sistema publica la informacion automaticamente para que sea visible para los estudiantes  

**Scenario:** Agente inteligente para consultas  
**Given:** El sistema cuenta con un agente inteligente integrado  
**When:** Un usuario realiza una pregunta compleja sobre el contenido de los syllabus  
**Then:** El agente inteligente procesa la base de datos y entrega una respuesta  

## RF derivado de HU-02:

*RF2:* El sistema debe proporcionar una interfaz para que el jefe de departamento consulte y apruebe los syllabus cargados por los profesores

*Analisis PESTLE RF:*

|  Dimension  |  Hallazgo  |  Argumentacion Etica  |
|-------------|------------|-----------------------|
|P-Politico   | El Ministerio de Educacion Nacional exige transparencia en la disponibilidad de los microcurriculos | Garantizar que el estudiante acceda a informacion oficial y aprobada para no inducir al error | 
|S-Social     | Existe una necesidad de estandarizar la calidad educativa entre los departamentos | Asegurarse que todos los estudiantes sin importar el departamento, reciban informacion con el mismo rigor de revision |

---

## HU-03: Visualizar departamento al que pertenece una electiva

**Titulo:** Visualizar departamento al que pertenece una electiva  
**Como:** Estudiante de la universidad  
**Quiero:** Identificar a que departamento pertenece cada electiva  
**Para:** Saber a donde dirigir las consultas o solicitudes relacionadas con el curso  

### Criterios de aceptacion:  

**Scenario:** Visualizacion del departamento de una electiva  
**Given:** El estudiante esta consultando la lista de las electivas  
**When:** Selecciona una electiva  
**Then:** el sistema muestra al departamento académico que pertenece el curso  

**Scenario:** Electiva sin departamento asignado  
**Given:** El estudiante esta consultando la lista de las electivas  
**When:** Selecciona un curso de electiva que no tiene departamento  
**Then:** El sistema informa en un mensaje indicando que la informacion del departamento esta pendiente por actualizar  

---

## HU-04: Consultar syllabus de una electiva  

**Titulo:** Consultar syllabus de una electiva  
**Como:** Estudiante de la universidad   
**Quiero:** Acceder de manera sencilla al syllabus de una electiva    
**Para:** Conocer la información detallada de los contenidos, objetivos, metodología y evaluación del curso

### Criterios de aceptacion:  
**Scenario:** Consulta exitosa del syllabus      
**Given:** El estudiante está visualizando la información de una electiva    
**When:** Selecciona la opcion de “Consultar syllabus”    
**Then:** El sistema muestra el syllabus del curso de forma clara y accesible    

**Scenario:** Syllabus no disponible   
**Given:** El estudiante intenta consultar el syllabus de una electiva  
**When:** El Syllabus no ha sido cargado o aprobado   
**Then:** El sistema informa que el syllabus aun no se encuentra disponible 

---

## HU-05: Actualización de información académica de electivas

**Título:** Actualización de información académica de electivas  
**Como:** profesor encargado de una electiva  
**Quiero:** actualizar la información registrada de mi curso  
**Para:** mantener vigente la información académica disponible para consulta estudiantil.

### Criterios de aceptación:

**Scenario:** Actualización exitosa      
**Given:** que el profesor accede a su curso registrado  
**When:** modifica la información y guarda los cambios  
**Then:** el sistema actualiza la información y la envía nuevamente a revisión

**Scenario:** Actualización incompleta  
**Given:** que el profesor está editando la información del curso  
**When:** omite campos obligatorios  
**Then:** el sistema muestra un mensaje indicando los datos faltantes

---

## HU-06: Consulta del estado de validación del syllabus

**Título:** Consulta del estado de validación del syllabus  
**Como:** profesor encargado de una electiva  
**Quiero:** consultar el estado de revisión de la información registrada  
**Para:** conocer si fue aprobada o requiere ajustes.

### Criterios de aceptación:

**Scenario:** Consulta de syllabus aprobado  
**Given:** que el profesor accede al sistema  
**When:** consulta una electiva aprobada  
**Then:** el sistema muestra el estado "Aprobado"

**Scenario:** Consulta de syllabus rechazado  
**Given:** que el profesor accede al sistema  
**When:** consulta una electiva rechazada  
**Then:** el sistema muestra las observaciones registradas por el jefe de departamento


# Requerimientos Funcionales
## RF DERIVADOS DE HU1
**RF1:** El sistema debe mostrar a los estudiantes el video de los profesor del curso
**Analisis PESTLE RF:** En caso de necesitarlo: Analisis de   PESTLE/ No aplica


Nota: Simplemente ponene #RF DERIVADOS DE HU2..HUN,
PERO siguen el mismo orden de numeros, a que me refiero que independientemente de que HU sea sigue el orden de numero de RF, es decir si HU2 y salen dos RF entonces RF2 Y RF3, ahora del HU3, sale uno entonces RF4.
