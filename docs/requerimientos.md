# Requerimiento funcionales:

## RF1: Registrar solicitudes de equivalencia por parte del estudiante

### RF1.1: Adjuntar documentos (syllabus, contenidos, etc.)

| Dimensión           | Hallazgo dado por el equipo (corregido y ampliado)                                                                                                                                                                                                                                                                                                                                                    | Argumentación ética                                                                                                                                                                                                                                                          |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **P - Político**    | En el contexto colombiano, las universidades están sujetas a lineamientos internos y del Ministerio de Educación Nacional (MEN) que regulan los procesos académicos, incluyendo la gestión de solicitudes de equivalencia. Estos lineamientos buscan garantizar orden, transparencia y equidad en los procesos académicos, por lo que el sistema debe alinearse con dichas políticas institucionales. | Desde una perspectiva ética, es fundamental que el sistema respete las normas institucionales, ya que estas están diseñadas para garantizar procesos justos. Ignorar estas políticas podría generar decisiones arbitrarias que afecten a los estudiantes de manera desigual. |
| **E - Económico**   | El desarrollo e implementación del sistema de registro implica costos asociados al desarrollo de software, infraestructura tecnológica y mantenimiento. Además, el almacenamiento de solicitudes y documentos genera costos recurrentes en servidores.                                                                                                                                                | No es ético que la institución limite o dificulte el acceso al proceso de equivalencias por razones económicas. El sistema debe garantizar que todos los estudiantes puedan acceder al proceso sin barreras, independientemente de los costos internos de la institución.    |
| **S - Social**      | No todos los estudiantes tienen el mismo nivel de acceso a herramientas digitales o comprensión de plataformas tecnológicas. Esto puede generar dificultades en el uso del sistema para ciertos grupos, como estudiantes con menor alfabetización digital.                                                                                                                                            | Éticamente, el sistema debe ser inclusivo y accesible. Diseñar un sistema complejo o poco intuitivo puede excluir a ciertos estudiantes, generando desigualdad en el acceso a un derecho académico como lo es solicitar una equivalencia.                                    |
| **T - Tecnológico** | El sistema depende de la disponibilidad de internet, compatibilidad con dispositivos y estabilidad de la plataforma. Fallos técnicos pueden impedir que los estudiantes registren sus solicitudes correctamente.                                                                                                                                                                                      | Es responsabilidad ética de la institución garantizar que la tecnología funcione correctamente. Un fallo técnico que impida registrar una solicitud puede afectar directamente el futuro académico del estudiante.                                                           |
| **L - Legal**       | El sistema recopila datos personales del estudiante, los cuales están protegidos por la Ley 1581 de 2012 (Habeas Data), que regula el tratamiento de datos personales en Colombia.                                                                                                                                                                                                                    | El manejo de datos personales implica una responsabilidad ética importante. No basta con cumplir la ley; se debe garantizar que los datos no sean utilizados indebidamente ni expuestos a riesgos.                                                                           |
| **A - Ambiental**   | La digitalización del proceso elimina la necesidad de formularios físicos y reduce el uso de papel en comparación con procesos tradicionales.                                                                                                                                                                                                                                                         | Aunque el impacto ambiental es positivo, este beneficio no debe ser el único criterio para implementar el sistema. La prioridad ética debe ser el bienestar y la equidad para los estudiantes.                                                                               |
---

## RF2: Consultar estado de solicitudes

## RF3: Asignar automáticamente la solicitud al responsable según el departamento

| Dimensión           | Hallazgo                                                                                                                                                                                                                                               | Argumentación ética                                                                                                                                                                  |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **P - Político**    | Las universidades operan bajo estructuras organizacionales definidas (facultades, departamentos), y los procesos deben respetar estas jerarquías. La asignación automática debe alinearse con estas estructuras para garantizar validez institucional. | Éticamente, es importante respetar la estructura institucional, ya que esta define responsabilidades claras. Una mala asignación puede llevar a decisiones incorrectas o no válidas. |
| **E - Económico**   | La automatización reduce la carga administrativa y el tiempo invertido por el personal, optimizando recursos institucionales.                                                                                                                          | Aunque la eficiencia es importante, no es ético sacrificar la precisión del proceso por rapidez o ahorro económico.                                                                  |
| **S - Social**      | Los estudiantes suelen desconocer el flujo interno de sus solicitudes, lo que genera incertidumbre sobre quién está evaluando su caso.                                                                                                                 | La transparencia es clave para generar confianza. Éticamente, los estudiantes tienen derecho a saber cómo se gestiona su solicitud.                                                  |
| **T - Tecnológico** | La asignación depende de datos correctos en el sistema (departamentos, cursos, responsables). Errores en estos datos pueden provocar asignaciones incorrectas.                                                                                         | Un error técnico puede afectar directamente la evaluación de un estudiante. Éticamente, el sistema debe minimizar estos riesgos.                                                     |
| **L - Legal**       | Es necesario registrar quién es responsable de cada etapa del proceso para garantizar trazabilidad en caso de auditorías o reclamaciones.                                                                                                              | La trazabilidad no solo es legal, sino ética, ya que permite identificar responsabilidades y evitar decisiones arbitrarias.                                                          |
| **A - Ambiental**   | La automatización reduce procesos manuales y uso de recursos físicos.                                                                                                                                                                                  | El beneficio ambiental es positivo, pero secundario frente a la correcta gestión del proceso académico.                                                                              |

---

## RF4: Registrar decisiones (aprobado, rechazado, pendiente)

### RF4.1: Almacenar decesiones con fecha, Responsable y Estado

| Dimensión           | Hallazgo                                                                                                                                | Argumentación ética                                                                                                           |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **P - Político**    | Las decisiones académicas deben poder ser auditadas por entes internos o externos, siguiendo principios de transparencia institucional. | Éticamente, las decisiones deben ser justificables. La falta de registro abre la puerta a arbitrariedad.                      |
| **E - Económico**   | No registrar decisiones genera reprocesos, aumentando costos administrativos.                                                           | La ineficiencia afecta recursos institucionales, pero lo más importante es que puede afectar negativamente a los estudiantes. |
| **S - Social**      | Las decisiones impactan directamente la trayectoria académica del estudiante.                                                           | Es éticamente necesario que las decisiones sean claras, justificadas y comprensibles.                                         |
| **T - Tecnológico** | Se requiere almacenamiento confiable y seguro para preservar la información.                                                            | Perder información afecta derechos del estudiante y la credibilidad del sistema.                                              |
| **L - Legal**       | Las decisiones deben poder ser utilizadas como evidencia en procesos legales o reclamaciones.                                           | La falta de evidencia puede perjudicar tanto a la institución como al estudiante.                                             |
| **A - Ambiental**   | Digitalizar decisiones reduce uso de papel.                                                                                             | Beneficio positivo, pero no prioritario frente al impacto social.                                                             |

---

## RF5: Consultar equivalencias previamente aprobadas

## RF6: Actualizar decisiones históricas

| Dimensión           | Hallazgo                                                                                                             | Argumentación ética                                                                                                     |
| ------------------- | -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **P - Político**    | Las políticas académicas pueden cambiar con el tiempo, lo que puede requerir la actualización de decisiones pasadas. | Cambiar decisiones sin criterios claros puede generar injusticias y afectar la confianza en la institución.             |
| **E - Económico**   | Reprocesar decisiones implica costos administrativos adicionales.                                                    | No es ético priorizar el ahorro económico sobre la equidad en decisiones académicas.                                    |
| **S - Social**      | Cambiar una decisión puede afectar directamente a un estudiante que ya había recibido un resultado.                  | Esto puede percibirse como injusto, especialmente si el estudiante ya tomó decisiones basadas en el resultado anterior. |
| **T - Tecnológico** | Es necesario mantener un historial de cambios para garantizar trazabilidad.                                          | La transparencia es esencial para mantener la confianza en el sistema.                                                  |
| **L - Legal**       | Cambios deben ser auditables para evitar conflictos legales.                                                         | La falta de registro puede generar disputas legales.                                                                    |
| **A - Ambiental**   | Proceso digital reduce recursos físicos.                                                                             | Impacto positivo pero secundario.                                                                                       |

---

## RF7: Analizar solicitudes automáticamente (IA)

### RF7.1: Clasificar las solicitudes en alto cumplimiento, medio cumplimiento o bajo cumplimiento

| Dimensión           | Hallazgo                                                                                                                 | Argumentación ética                                                   |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------- |
| **P - Político**    | Aunque no hay regulación específica de IA, el MEN exige transparencia en decisiones académicas.                          | No es ético tomar decisiones sin posibilidad de explicación.          |
| **E - Económico**   | La IA implica costos de desarrollo, mantenimiento y actualización, aunque puede reducir costos operativos a largo plazo. | No es ético priorizar ahorro sobre justicia en decisiones académicas. |
| **S - Social**      | Puede generar desconfianza si los estudiantes no entienden cómo funciona.                                                | Las personas tienen derecho a entender cómo son evaluadas.            |
| **T - Tecnológico** | Puede replicar sesgos históricos en los datos.                                                                           | La tecnología no debe perpetuar desigualdades.                        |
| **L - Legal**       | Uso de datos personales regulado por Ley 1581.                                                                           | Protección de datos es un derecho fundamental.                        |
| **A - Ambiental**   | Consumo energético de sistemas de IA.                                                                                    | Impacto menor frente al impacto social.     

---

## RF8: Notificar cambios de estado al estudiante

## RF9: Informar al respectivo responsable siguiendo en el flujo

## RF10 – Visualizar syllabus de un curso

El sistema debe mostrar el nombre, los objetivos de aprendizaje y los contenidos de un curso seleccionado, siempre que estén disponibles. Si algún campo obligatorio está vacío, el sistema debe notificar que el syllabus está incompleto.

### PESTLE

* **Social/Político:** La visualización clara del syllabus permite que el jefe tenga insumos objetivos para decidir sobre propuestas y homologaciones.
* **Tecnológico:** Requiere un repositorio centralizado de cursos con campos estructurados.

<br>

## RF11 – Registrar decisión sobre propuesta de materia

El sistema debe permitir al jefe registrar el estado de una propuesta (aprobado, rechazado, en revisión) y almacenar la fecha de la decisión, validando que los campos nombre, objetivos y créditos de la propuesta estén completos. Si no lo están, debe impedir el guardado e indicar los campos faltantes.

### PESTLE

* **Legal/Político:** La trazabilidad de la decisión (quién, cuándo y qué se decidió) es esencial para llevar un control claro del proceso de preaprobación.
* **Económico:** Evita re-trabajo por decisiones informales no guardadas.

<br>

## RF12 – Seleccionar dos cursos para comparación

El sistema debe permitir la selección de exactamente dos cursos como paso previo a la comparación. Si el jefe selecciona menos o más de dos cursos, el sistema debe mostrar un mensaje y bloquear la continuación.

### PESTLE

* **Tecnológico/Social:** Establece una restricción lógica necesaria para evitar errores en la comparación (que podría ser asistida por IA).
* **Económico:** Reduce la probabilidad de decisiones equivocadas al forzar el formato de comparación uno a uno, que es más claro y rápido de interpretar.

<br>

## RF13 – Comparar objetivos de aprendizaje de dos cursos

El sistema debe mostrar los objetivos de aprendizaje de dos cursos seleccionados para facilitar su comparación. Si algún curso no tiene objetivos registrados, debe indicarlo sin impedir la visualización de los que sí existen.

### PESTLE

* **Social/Político:** La comparación directa de objetivos permite al jefe justificar si una nueva propuesta de materia va acorde con el objetivo general de los cursos, el cual es el pensamiento crítico.
* T**ecnológico:** Sienta la base para una futura funcionalidad de IA que evalúe la similitud entre los objetivos de dos cursos.

<br>

## RF14 – Registrar curso con datos básicos

El sistema debe permitir al asistente registrar un curso con nombre, créditos (número entero mayor a 0) y programa académico. Debe validar que los créditos sean positivos y que los campos obligatorios no estén vacíos, mostrando errores específicos si no se cumple.

### PESTLE

* **Tecnológico/Legal:** Alimenta el repositorio central con datos validados, que luego servirán para homologaciones y comparaciones. La validación fuerte previene datos inconsistentes que generarían errores en otros subsistemas.
* **Económico:** La carga de cursos por parte del asistente libera al jefe de otras tareas operativas.

<br>

## RF15 – Consultar lista de cursos registrados

El sistema debe mostrar una lista con el nombre y el programa académico de todos los cursos registrados, o un mensaje informativo si no existe ninguno.

### PESTLE

* **Social/Tecnológico:** Proporciona una vista base para cualquier operación (selección para comparar, revisión de syllabus, etc.), siendo la puerta de entrada a las demás funcionalidades.
* **Económico:** Reduce el tiempo de búsqueda de información dispersa en documentos o carpetas compartidas.

## RF16: El sistema debe tener un reproductor de video que permita a los estudiantes ver las presentaciones de los docentes sobre sus cursos

### Analisis PESTLE RF:

|  Dimension  |  Hallazgo   |  Argumentacion Etica  |
|-------------|-------------|-----------------------|
|T-Tecnologico | El contenido por video suele ser menos pesado para los estudiantes | Los videos no se conviertan en un factor de exclusión para estudiantes con limitacion |

---

## RF17: El sistema debe desplegar una lista de electivas de universidades extranjeras en convenio, detallando sus objetivos

### Analisis PESTLE RF:

|  Dimension  |  Hallazgo   |  Argumentacion Etica  |
|-------------|-------------|-----------------------|
|P-Politico   | Los convenios internacionales estan sujetos a tratados diplomáticos | El sistema mostrara solo convenios activos para no generar falsas expectativas |
|L-Legal      | El intercambio de informacion de cursos debe cumplir con las leyes de proteccion de datos personales | El manejo de datos debe ser transparente para proteger la integridad del estudiante |
|A-Ambiental  | La digitalizacion del catalogo de electivas internacionales reduce el uso de folletos | El beneficio de eliminar el papel es positivo, siempre que se garantice que la información digital sea completa |

---

## RF18: El sistema debe permitir la búsqueda de electivas disponibles por nombre o palabra clave.

### Analisis PESTLE RF:

|  Dimension      |  Hallazgo   |  Argumentacion Etica  |
|-----------------|-------------|-----------------------|
|S - Social   | Los estudiantes necesitan una forma sencilla de buscar electivas segun sus intereses academicos | El sistema debe facilitar el acceso equitativo a la información para que todos los estudiantes puedan encontrar cursos sin depender de terceros |  
|T - Tecnologico  | Se requiere un buscador funcional que permita consultar cursos por nombre una palabra clave | La herramienta debe ser facil e intuitiva de usar para no complicar el acceso a la informacion|  

---


## RF19: El sistema debe permitir consultar la descripcion, objetivos, contenidos, departamento responsable y profesor encargado de una electiva

|  Dimension      |  Hallazgo   |  Argumentacion Etica  |
|-----------------|-------------|-----------------------|
|S - Social   | El estudiante necesita información clara antes de inscribir una electiva | El sistema debe permitir una decisión académica informada |  
|T - Tecnológico  | La informacion del curso debe ser oficial y de confianza | No se debe brindar informacion incorrecta que afecte la inscripcion de un estudiante |  


## RF20: El sistema debe informar cuando la informacion de una electiva este incompleta

|  Dimension      |  Hallazgo   |  Argumentacion Etica  |
|-----------------|-------------|-----------------------|
|S - Social   | El estudiante puede confundirse si no sabe que la informacion está incompleta | El sistema debe ser transparente sobre los datos disponibles |  
|T - Tecnológico  | La plataforma debe manejar casos donde falten datos o informacion | El sistema debe mostrar mensajes claros y no dejar al estudiante sin contexto |  
---

## RF21: El sistema debe permitir a los estudiantes acceder al syllabus oficial de cada electiva desde una plataforma centralizada.  

### Analisis PESTLE RF: No aplica
---

## RF22: El sistema debe permitir seleccionar una electiva internacional para realizar comparación académica.  

### Analisis PESTLE RF: No aplica

---

## RF23: El sistema debe organizar la información de cada electiva en secciones definidas (objetivos, contenido, profesor, departamento).  

### Analisis PESTLE RF: No Aplica

---

## RF24: El sistema debe permitir a los usuarios realizar busquedas de electivas filtrando por contenido, horario y departamento academico

### Analisis PESTLE RF: NO APLICA

---

## RF25: El sistema debe proporcionar una interfaz para que el jefe de departamento consulte y apruebe los syllabus cargados por los profesores

### Analisis PESTLE RF:

|  Dimension  |  Hallazgo  |  Argumentacion Etica  |
|-------------|------------|-----------------------|
|P-Politico   | El Ministerio de Educacion Nacional exige transparencia en la disponibilidad de los microcurriculos | Garantizar que el estudiante acceda a informacion oficial y aprobada para no inducir al error | 
|S-Social     | Existe una necesidad de estandarizar la calidad educativa entre los departamentos | Asegurarse que todos los estudiantes sin importar el departamento, reciban informacion con el mismo rigor de revision |

---

## RF26: El sistema debe mostrar el departamento académico al que pertenece una electiva, o informar cuando esta información esté pendiente por actualizar

### Analisis PESTLE RF:

|  Dimension      |  Hallazgo   |  Argumentacion Etica  |
|-----------------|-------------|-----------------------|
|S - Social   | Los estudiantes necesitan saber a que departamento pertenece una electiva para dirigir correctamente sus consultas o solicitudes | El sistema debe facilitar el acceso claro a la informacion institucional y evitar confusiones en la comunicacion academica |  
|T - Tecnologico  | La plataforma debe mostrar el departamento asociado al curso y manejar el caso en que este dato no exista | El sistema debe informar claramente cuando la informacion esta pendiente, en lugar de dejar el campo vacio |  

---


## RF27: El sistema debe permitir consultar el syllabus de una electiva cuando esté disponible

### Analisis PESTLE RF:

|  Dimension      |  Hallazgo   |  Argumentacion Etica  |
|-----------------|-------------|-----------------------|
|S - Social   | Los estudiantes necesitan acceder fácilmente al syllabus para conocer contenidos, objetivos, metodologia y evaluacion del curso | El sistema debe facilitar el acceso equitativo a la informacion academica antes de que el estudiante tome decisiones sobre la electiva |    
|L - Legal    | El syllabus debe ser informacion oficial del curso | El sistema debe evitar mostrar informacion no aprobada o no validada como si fuera definitiva |  

---

## RF28: El sistema debe permitir a los profesores editar la información académica de las electivas asignadas.  

### Analisis PESTLE RF: No aplica
---

## RF29: El sistema debe permitir a los profesores consultar el estado de revisión de cada syllabus registrado.  

### Analisis PESTLE RF: No aplica
---

## RF30: El sistema debe organizar la información de cada electiva en secciones definidas (objetivos, contenido, profesor, departamento).  

### Analisis PESTLE RF: No Aplica

---

## RF31: El sistema debe permitir el acceso rápido a la información principal de cada electiva.  

### Analisis PESTLE RF:

|  Dimension  |  Hallazgo   |  Argumentacion Etica  |
|-------------|-------------|-----------------------|
|E-Economico | Reducir el tiempo de consulta mejora la eficiencia del estudiante en la toma de decisiones académicas | Se debe garantizar que el acceso rápido a la información no omita datos importantes que puedan afectar la decisión del estudiante |

---
