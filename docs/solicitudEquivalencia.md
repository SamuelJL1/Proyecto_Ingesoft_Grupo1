# Metodo Dorfman

## Requerimiento funcionales:

RF1: Registrar solicitudes de equivalencia por parte del estudiante

RF1.1: Adjuntar documentos (syllabus, contenidos, etc.)

RF2: Consultar estado de solicitudes

RF3: Asignar automáticamente la solicitud al responsable según el departamento

RF4: Registrar decisiones (aprobado, rechazado, pendiente)

RF4.1: Almacenar decesiones con fecha, Responsable y Estado

RF5: Consultar equivalencias previamente aprobadas

RF6: Actualizar decisiones históricas

RF7: Analizar solicitudes automáticamente (IA)

RF7.1: Clasificar las solicitudes en alto cumplimiento, medio cumplimiento o bajo cumplimiento

RF8: Notificar cambios de estado al estudiante

RF9: Informar al respectivo responsable siguiendo en el flujo

---

## Entidades:

Actores:

Estudiante

Asistente

Administrador del sistema

Director de programa

Jefe de departamento

Entidades del negocio:

Solicitud de equivalencia

Curso origen

Curso destino

Departamento

Programa académico

Decisión

Historial de decisiones

Evaluación IA

--- 

## Subsistemas:

Subsistema de Gestión de Solicitudes

RF1 - RF1.1 - RF2

Subsistema de Flujo de Aprobación:

RF3 - RF4

Subsistema de Base de Datos

Rf4.1 - RF5 - RF6

Subsistema de Inteligencia Artificial

RF7 - RF7.1

Subsistema de Notificaciones

RF8 - RF9

---

# Historias de Usuario

## Historia de usuario 1

**Título:** Registro de solicitud de equivalencia

**Historia:**
Yo, como estudiante, quiero registrar una solicitud de equivalencia con la información del curso y documentos, para que mi curso sea evaluado por la universidad.

**Criterios de aceptación:**

### Scenario: Registro exitoso con datos completos

**Given:** El estudiante se encuentra en el formulario de solicitud

**When:** Ingresa curso origen, curso destino y adjunta documentos válidos

**Then:** El sistema guarda la solicitud correctamente

**And:** Muestra un mensaje de confirmación

### Scenario: Registro fallido por datos incompletos

**Given:** El estudiante se encuentra en el formulario de solicitud

**When:** Omite información obligatoria

**Then:** El sistema muestra un mensaje de error indicando campos faltantes

### Scenario: Registro fallido por documentos inválidos

**Given:** El estudiante se encuentra en el formulario de solicitud

**When:** Adjunta documentos en formato no permitido

**Then:** El sistema muestra un mensaje indicando el formato inválido

---

## Historia de usuario 2

**Título:** Asignación automática de solicitudes

**Historia:**
Yo, como administrador del sistema, quiero asignar automáticamente las solicitudes al responsable correspondiente, para agilizar el proceso de evaluación.

**Criterios de aceptación:**

#### Scenario: Asignación correcta según departamento

**Given:** Existe una solicitud registrada

**When:** El sistema identifica el departamento del curso destino

**Then:** Asigna la solicitud al responsable correspondiente

### Scenario: Solicitud sin departamento identificado

**Given:** Existe una solicitud registrada

**And:** El sistema no puede identificar el departamento

**When:** Intenta asignarla

**Then:** La solicitud queda en estado pendiente de asignación

**And:** Se notifica al asistente

---

## Historia de usuario 3

**Título:** Evaluación preliminar con inteligencia artificial

**Historia:**
Yo, como jefe de departamento, quiero recibir una clasificación automática de las solicitudes, para priorizar y optimizar mi revisión.

**Criterios de aceptación:**

### Scenario: Clasificación en alto cumplimiento

**Given:** Existe una solicitud registrada

**When:** El sistema ejecuta el análisis de IA

**And:** El curso cumple la mayoría de criterios

**Then:** Clasifica la solicitud como "alto"


### Scenario: Clasificación en medio cumplimiento

**Given:** Existe una solicitud registrada

**When:** El sistema ejecuta el análisis de IA

**And:** El curso cumple parcialmente los criterios

**Then:** Clasifica la solicitud como "medio"


### Scenario: Clasificación en bajo cumplimiento

**Given:** Existe una solicitud registrada

**When:** El sistema ejecuta el análisis de IA

**And:** El curso no cumple los criterios

**Then:** Clasifica la solicitud como "bajo"


---

## Historia de usuario 4

**Título:** Consulta de equivalencias previas

**Historia:**
Yo, como jefe de departamento, quiero consultar equivalencias previamente aprobadas o rechazadas, para evitar reprocesar solicitudes similares.

**Criterios de aceptación:**

### Scenario: Consulta exitosa de historial

**Given:** El evaluador está en el sistema

**When:** Busca por curso origen o curso destino

**Then:** El sistema muestra las equivalencias previas


### Scenario: Consulta sin resultados

**Given:** El evaluador está en el sistema

**When:** Busca un curso sin registros previos

**Then:** El sistema muestra un mensaje indicando que no hay resultados


---

## Historia de usuario 5

**Título:** Actualización de decisiones históricas

**Historia:**
Yo, como jefe de departamento, quiero modificar decisiones anteriores, para mantener actualizados los criterios académicos.

**Criterios de aceptación:**

### Scenario: Actualización exitosa de decisión

**Given:** Existe una equivalencia previamente registrada

**When:** El jefe modifica el estado de la decisión

**Then:** El sistema actualiza la información

**And:** Guarda el cambio en el historial


### Scenario: Intento de actualización sin permisos

**Given:** Existe una equivalencia registrada

**And:** El usuario no es jefe de departamento

**When:** Intenta modificar la decisión

**Then:** El sistema bloquea la acción

**And:** Muestra un mensaje de acceso denegado


---

## Historia de usuario 6

**Título:** Notificación de cambios en solicitudes

**Historia:**
Yo, como estudiante, quiero recibir notificaciones sobre el estado de mi solicitud, para estar informado del proceso.

**Criterios de aceptación:**

### Scenario: Notificación por cambio de estado

**Given:** Existe una solicitud en proceso

**When:** El estado cambia (aprobado, rechazado o pendiente)

**Then:** El sistema envía una notificación al estudiante


### Scenario: Consulta manual del estado

**Given:** El estudiante accede al sistema

**When:** Revisa sus solicitudes

**Then:** El sistema muestra el estado actualizado

---
# Analisis PESTLE


## RF1 — Registrar solicitudes de equivalencia

| Dimensión           | Hallazgo dado por el equipo (corregido y ampliado)                                                                                                                                                                                                                                                                                                                                                    | Argumentación ética                                                                                                                                                                                                                                                          |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **P - Político**    | En el contexto colombiano, las universidades están sujetas a lineamientos internos y del Ministerio de Educación Nacional (MEN) que regulan los procesos académicos, incluyendo la gestión de solicitudes de equivalencia. Estos lineamientos buscan garantizar orden, transparencia y equidad en los procesos académicos, por lo que el sistema debe alinearse con dichas políticas institucionales. | Desde una perspectiva ética, es fundamental que el sistema respete las normas institucionales, ya que estas están diseñadas para garantizar procesos justos. Ignorar estas políticas podría generar decisiones arbitrarias que afecten a los estudiantes de manera desigual. |
| **E - Económico**   | El desarrollo e implementación del sistema de registro implica costos asociados al desarrollo de software, infraestructura tecnológica y mantenimiento. Además, el almacenamiento de solicitudes y documentos genera costos recurrentes en servidores.                                                                                                                                                | No es ético que la institución limite o dificulte el acceso al proceso de equivalencias por razones económicas. El sistema debe garantizar que todos los estudiantes puedan acceder al proceso sin barreras, independientemente de los costos internos de la institución.    |
| **S - Social**      | No todos los estudiantes tienen el mismo nivel de acceso a herramientas digitales o comprensión de plataformas tecnológicas. Esto puede generar dificultades en el uso del sistema para ciertos grupos, como estudiantes con menor alfabetización digital.                                                                                                                                            | Éticamente, el sistema debe ser inclusivo y accesible. Diseñar un sistema complejo o poco intuitivo puede excluir a ciertos estudiantes, generando desigualdad en el acceso a un derecho académico como lo es solicitar una equivalencia.                                    |
| **T - Tecnológico** | El sistema depende de la disponibilidad de internet, compatibilidad con dispositivos y estabilidad de la plataforma. Fallos técnicos pueden impedir que los estudiantes registren sus solicitudes correctamente.                                                                                                                                                                                      | Es responsabilidad ética de la institución garantizar que la tecnología funcione correctamente. Un fallo técnico que impida registrar una solicitud puede afectar directamente el futuro académico del estudiante.                                                           |
| **L - Legal**       | El sistema recopila datos personales del estudiante, los cuales están protegidos por la Ley 1581 de 2012 (Habeas Data), que regula el tratamiento de datos personales en Colombia.                                                                                                                                                                                                                    | El manejo de datos personales implica una responsabilidad ética importante. No basta con cumplir la ley; se debe garantizar que los datos no sean utilizados indebidamente ni expuestos a riesgos.                                                                           |
| **A - Ambiental**   | La digitalización del proceso elimina la necesidad de formularios físicos y reduce el uso de papel en comparación con procesos tradicionales.                                                                                                                                                                                                                                                         | Aunque el impacto ambiental es positivo, este beneficio no debe ser el único criterio para implementar el sistema. La prioridad ética debe ser el bienestar y la equidad para los estudiantes.                                                                               |

---

## RF3 — Asignación automática de solicitudes

| Dimensión           | Hallazgo                                                                                                                                                                                                                                               | Argumentación ética                                                                                                                                                                  |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **P - Político**    | Las universidades operan bajo estructuras organizacionales definidas (facultades, departamentos), y los procesos deben respetar estas jerarquías. La asignación automática debe alinearse con estas estructuras para garantizar validez institucional. | Éticamente, es importante respetar la estructura institucional, ya que esta define responsabilidades claras. Una mala asignación puede llevar a decisiones incorrectas o no válidas. |
| **E - Económico**   | La automatización reduce la carga administrativa y el tiempo invertido por el personal, optimizando recursos institucionales.                                                                                                                          | Aunque la eficiencia es importante, no es ético sacrificar la precisión del proceso por rapidez o ahorro económico.                                                                  |
| **S - Social**      | Los estudiantes suelen desconocer el flujo interno de sus solicitudes, lo que genera incertidumbre sobre quién está evaluando su caso.                                                                                                                 | La transparencia es clave para generar confianza. Éticamente, los estudiantes tienen derecho a saber cómo se gestiona su solicitud.                                                  |
| **T - Tecnológico** | La asignación depende de datos correctos en el sistema (departamentos, cursos, responsables). Errores en estos datos pueden provocar asignaciones incorrectas.                                                                                         | Un error técnico puede afectar directamente la evaluación de un estudiante. Éticamente, el sistema debe minimizar estos riesgos.                                                     |
| **L - Legal**       | Es necesario registrar quién es responsable de cada etapa del proceso para garantizar trazabilidad en caso de auditorías o reclamaciones.                                                                                                              | La trazabilidad no solo es legal, sino ética, ya que permite identificar responsabilidades y evitar decisiones arbitrarias.                                                          |
| **A - Ambiental**   | La automatización reduce procesos manuales y uso de recursos físicos.                                                                                                                                                                                  | El beneficio ambiental es positivo, pero secundario frente a la correcta gestión del proceso académico.                                                                              |

---

## RF4 — Registrar decisiones

| Dimensión           | Hallazgo                                                                                                                                | Argumentación ética                                                                                                           |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **P - Político**    | Las decisiones académicas deben poder ser auditadas por entes internos o externos, siguiendo principios de transparencia institucional. | Éticamente, las decisiones deben ser justificables. La falta de registro abre la puerta a arbitrariedad.                      |
| **E - Económico**   | No registrar decisiones genera reprocesos, aumentando costos administrativos.                                                           | La ineficiencia afecta recursos institucionales, pero lo más importante es que puede afectar negativamente a los estudiantes. |
| **S - Social**      | Las decisiones impactan directamente la trayectoria académica del estudiante.                                                           | Es éticamente necesario que las decisiones sean claras, justificadas y comprensibles.                                         |
| **T - Tecnológico** | Se requiere almacenamiento confiable y seguro para preservar la información.                                                            | Perder información afecta derechos del estudiante y la credibilidad del sistema.                                              |
| **L - Legal**       | Las decisiones deben poder ser utilizadas como evidencia en procesos legales o reclamaciones.                                           | La falta de evidencia puede perjudicar tanto a la institución como al estudiante.                                             |
| **A - Ambiental**   | Digitalizar decisiones reduce uso de papel.                                                                                             | Beneficio positivo, pero no prioritario frente al impacto social.                                                             |

---

## RF6 — Actualizar decisiones históricas

| Dimensión           | Hallazgo                                                                                                             | Argumentación ética                                                                                                     |
| ------------------- | -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **P - Político**    | Las políticas académicas pueden cambiar con el tiempo, lo que puede requerir la actualización de decisiones pasadas. | Cambiar decisiones sin criterios claros puede generar injusticias y afectar la confianza en la institución.             |
| **E - Económico**   | Reprocesar decisiones implica costos administrativos adicionales.                                                    | No es ético priorizar el ahorro económico sobre la equidad en decisiones académicas.                                    |
| **S - Social**      | Cambiar una decisión puede afectar directamente a un estudiante que ya había recibido un resultado.                  | Esto puede percibirse como injusto, especialmente si el estudiante ya tomó decisiones basadas en el resultado anterior. |
| **T - Tecnológico** | Es necesario mantener un historial de cambios para garantizar trazabilidad.                                          | La transparencia es esencial para mantener la confianza en el sistema.                                                  |
| **L - Legal**       | Cambios deben ser auditables para evitar conflictos legales.                                                         | La falta de registro puede generar disputas legales.                                                                    |
| **A - Ambiental**   | Proceso digital reduce recursos físicos.                                                                             | Impacto positivo pero secundario.                                                                                       |

---

## RF7 — Evaluación automática con IA

| Dimensión           | Hallazgo                                                                                                                 | Argumentación ética                                                   |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------- |
| **P - Político**    | Aunque no hay regulación específica de IA, el MEN exige transparencia en decisiones académicas.                          | No es ético tomar decisiones sin posibilidad de explicación.          |
| **E - Económico**   | La IA implica costos de desarrollo, mantenimiento y actualización, aunque puede reducir costos operativos a largo plazo. | No es ético priorizar ahorro sobre justicia en decisiones académicas. |
| **S - Social**      | Puede generar desconfianza si los estudiantes no entienden cómo funciona.                                                | Las personas tienen derecho a entender cómo son evaluadas.            |
| **T - Tecnológico** | Puede replicar sesgos históricos en los datos.                                                                           | La tecnología no debe perpetuar desigualdades.                        |
| **L - Legal**       | Uso de datos personales regulado por Ley 1581.                                                                           | Protección de datos es un derecho fundamental.                        |
| **A - Ambiental**   | Consumo energético de sistemas de IA.                                                                                    | Impacto menor frente al impacto social.                               |
