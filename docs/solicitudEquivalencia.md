# Metodo Dorfman

## Requerimiento funcionales:

RF1: Registrar solicitudes de equivalencia con documentos adjuntos por parte del estudiante

RF1.1: Adjuntar documentos (syllabus, contenidos, etc.)

RF2: Consultar estado de solicitudes

RF3: Asignar automáticamente la solicitud al responsable según el flujo oficial de tres niveles

RF4: Registrar decisiones (aprobado, rechazado, pendiente)

RF4.1: Almacenar decesiones con fecha, Responsable y Estado

RF5: Consultar equivalencias previamente aprobadas

RF6: Actualizar decisiones históricas

RF7: Analizar solicitudes automáticamente (IA)

RF7.1: Clasificar las solicitudes en alto cumplimiento, medio cumplimiento o bajo cumplimiento

RF8: Notificar cambios de estado al estudiante

RF9: Informar al respectivo responsable siguiendo en el flujo

RF10: Generar y distribuir certificados automáticos al registrar la decisión final

RF11: Priorizar solicitudes por fecha de envío y nivel de urgencia

RF12: Consultar información detallada de cursos internos para comparación con externos

---

## Entidades:

Actores:

- Estudiante

- Administrador del sistema

- Dirección de programa

- Jefe de departamento

- Entidades del negocio:

- Solicitud de equivalencia

- Curso origen

- Curso destino

- Departamento

- Programa académico

- Decisión

- Historial de decisiones

- Evaluación IA

--- 

## Subsistemas:

Subsistema de Gestión de Solicitudes

RF1 - RF1.1 - RF2 - RF12

Subsistema de Flujo de Aprobación:

RF3 - RF4 - RF4.1 - RF10 - RF11

Subsistema de Base de Datos

RF5 - RF6

Subsistema de Inteligencia Artificial

RF7 - RF7.1

Subsistema de Notificaciones

RF8 - RF9

---

# Solicitud de Equivalencia

---

## Historia de usuario 1

| **Historia N°:** | 1 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Registrar una solicitud de equivalencia con la información del curso y documentos |
| **Para** | Que mi curso sea evaluado por la universidad |

**Scenario 1.1:** Registro exitoso con datos completos

| | |
|---|---|
| **Given** | El estudiante se encuentra en el formulario de solicitud |
| **When** | Ingresa curso origen, curso destino y adjunta documentos válidos |
| **Then** | El sistema guarda la solicitud correctamente |
| **And** | Muestra un mensaje de confirmación |

**Scenario 1.2:** Registro fallido por datos incompletos

| | |
|---|---|
| **Given** | El estudiante se encuentra en el formulario de solicitud |
| **When** | Omite información obligatoria |
| **Then** | El sistema muestra un mensaje de error indicando campos faltantes |

**Scenario 1.3:** Registro fallido por documentos inválidos

| | |
|---|---|
| **Given** | El estudiante se encuentra en el formulario de solicitud |
| **When** | Adjunta documentos en formato no permitido |
| **Then** | El sistema muestra un mensaje indicando el formato inválido |

---

## Historia de usuario 2

| **Historia N°:** | 2 |
|---|---|
| **Yo como** | Asistente de Programa |
| **Quiero** | Que el sistema asigne automáticamente las solicitudes al responsable correspondiente siguiendo el flujo institucional |
| **Para** | Agilizar el proceso de evaluación y garantizar el orden correcto a las entidades respectivas |

**Scenario 2.1:** Asignación al Asistente de Programa según departamento

| | |
|---|---|
| **Given** | El Estudiante ha enviado una solicitud con documentos válidos y completos |
| **When** | El Sistema registra la nueva solicitud |
| **Then** | Asigna la solicitud al asistente de programa correspondiente |
| **And** | Se notifica al asistente |

**Scenario 2.2:** Paso del Asistente al Director de Programa

| | |
|---|---|
| **Given** | El Asistente de Programa ha revisado la solicitud |
| **When** | El Asistente de Programa aprueba la solicitud |
| **Then** | El Sistema asigna la solicitud al Director de programa correspondiente |
| **And** | Se notifica al Director |

**Scenario 2.3:** Paso del Director de Programa al Jefe de Departamento

| | |
|---|---|
| **Given** | El Director de Programa ha revisado la solicitud |
| **When** | El Director de Programa aprueba la solicitud |
| **Then** | El Sistema asigna la solicitud al Jefe de Departamento correspondiente |
| **And** | Se notifica al Jefe de Departamento |

**Scenario 2.4:** Paso del Jefe de Departamento a Admisiones

| | |
|---|---|
| **Given** | El Jefe de departamento ha revisado la solicitud |
| **When** | El Jefe de departamento realiza la decisión final |
| **Then** | El Sistema notifica a admisiones |
| **And** | Se cierra el flujo de revisión |

**Scenario 2.5:** Solicitud sin Departamento Identificado

| | |
|---|---|
| **Given** | El Estudiante ha enviado una solicitud con documentos válidos y completos |
| **And** | El Sistema no puede identificar el departamento del curso destino |
| **When** | Intenta asignar la solicitud |
| **Then** | La Solicitud queda en estado "Pendiente de Asignación" |
| **And** | Se notifica al asistente para resolverlo manualmente |

---

## Historia de usuario 3

| **Historia N°:** | 3 |
|---|---|
| **Yo como** | Jefe de departamento |
| **Quiero** | Recibir una clasificación automática de las solicitudes |
| **Para** | Priorizar y optimizar mi revisión |

**Scenario 3.1:** Clasificación en alto cumplimiento

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El sistema ejecuta el análisis de IA |
| **And** | El curso cumple la mayoría de los criterios |
| **Then** | Clasifica la solicitud como "alto" |

**Scenario 3.2:** Clasificación en medio cumplimiento

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El sistema ejecuta el análisis de IA |
| **And** | El curso cumple parcialmente los criterios |
| **Then** | Clasifica la solicitud como "medio" |

**Scenario 3.3:** Clasificación en bajo cumplimiento

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El sistema ejecuta el análisis de IA |
| **And** | El curso no cumple los criterios |
| **Then** | Clasifica la solicitud como "bajo" |

---

## Historia de usuario 4

| **Historia N°:** | 4 |
|---|---|
| **Yo como** | Jefe de departamento |
| **Quiero** | Consultar equivalencias previamente aprobadas o rechazadas |
| **Para** | Evitar reprocesar solicitudes similares |

**Scenario 4.1:** Consulta exitosa de historial

| | |
|---|---|
| **Given** | El jefe de departamento está en el historial |
| **When** | Busca por curso origen o curso destino |
| **Then** | El sistema muestra las equivalencias previas |

**Scenario 4.2:** Consulta sin resultados

| | |
|---|---|
| **Given** | El jefe de departamento está en el historial |
| **When** | Busca un curso sin registros previos |
| **Then** | El sistema muestra un mensaje indicando que no hay resultados |

**Scenario 4.3:** Filtrar historial solo por equivalencias aprobadas

| | |
|---|---|
| **Given** | El jefe de departamento está en el historial |
| **When** | Aplica el filtro "aprobadas" |
| **Then** | El sistema muestra únicamente las equivalencias con decisión aprobada |

---

## Historia de usuario 5

| **Historia N°:** | 5 |
|---|---|
| **Yo como** | Jefe de departamento |
| **Quiero** | Modificar decisiones anteriores |
| **Para** | Mantener actualizados los criterios académicos |

**Scenario 5.1:** Actualización exitosa de decisión

| | |
|---|---|
| **Given** | Existe una equivalencia previamente registrada |
| **When** | El Jefe modifica el estado de la decisión |
| **Then** | El sistema actualiza la información |
| **And** | Guarda el cambio en el historial |

**Scenario 5.2:** Intento de actualización sin permisos

| | |
|---|---|
| **Given** | Existe una equivalencia registrada |
| **And** | El usuario no es jefe de departamento |
| **When** | Intenta modificar la decisión |
| **Then** | El sistema bloquea la acción |
| **And** | Muestra un mensaje de acceso denegado |

---

## Historia de usuario 6

| **Historia N°:** | 6 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Recibir notificaciones sobre el estado de mi solicitud |
| **Para** | Estar informado del proceso |

**Scenario 6.1:** Notificación por cambio de estado

| | |
|---|---|
| **Given** | Existe una solicitud en proceso |
| **When** | El estado cambia (aprobado, rechazado o pendiente) |
| **Then** | El sistema envía una notificación al estudiante |

**Scenario 6.2:** Consulta manual del estado

| | |
|---|---|
| **Given** | El estudiante accede al sistema |
| **When** | Revisa sus solicitudes |
| **Then** | El sistema muestra el estado actualizado |

---

## Historia de usuario 7

| **Historia N°:** | 7 |
|---|---|
| **Yo como** | Estudiante en movilidad |
| **Quiero** | Consultar la información detallada de los cursos del área |
| **Para** | Compararlos con cursos externos |

**Scenario 7.1:** Visualizar cursos con información académica completa

| | |
|---|---|
| **Given** | Existen cursos registrados en el sistema |
| **When** | El estudiante accede al módulo de equivalencias |
| **Then** | El sistema muestra cursos con código, nombre, créditos, competencias y resultados de aprendizaje |

**Scenario 7.2:** No existen cursos registrados

| | |
|---|---|
| **Given** | No existen cursos en el sistema |
| **When** | El estudiante accede al módulo |
| **Then** | El sistema muestra mensaje indicando que no hay cursos disponibles |

---

## Historia de usuario 8

| **Historia N°:** | 8 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Registrar un curso de una universidad extranjera |
| **Para** | Iniciar una propuesta de equivalencia |

**Scenario 8.1:** Registrar curso externo correctamente

| | |
|---|---|
| **Given** | El Estudiante ingresa nombre del curso, universidad, créditos y descripción |
| **When** | Guarda el curso externo |
| **Then** | El Sistema registra el curso asociado al estudiante |

**Scenario 8.2:** Intentar guardar con datos obligatorios faltantes

| | |
|---|---|
| **Given** | El Estudiante no ingresa nombre del curso, universidad o créditos |
| **When** | El Estudiante intenta guardar |
| **Then** | El Sistema bloquea el registro y solicita completar campos obligatorios |

---

## Historia de usuario 9

| **Historia N°:** | 9 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Adjuntar documentos del curso externo, como el syllabus, código del curso y mi balance académico |
| **Para** | Sustentar la equivalencia |

**Scenario 9.1:** Adjuntar archivo válido

| | |
|---|---|
| **Given** | El Archivo es PDF y pesa menos de 5MB |
| **When** | El Estudiante carga el documento |
| **Then** | El Sistema guarda el archivo correctamente |

**Scenario 9.2:** Archivo inválido o excede tamaño permitido

| | |
|---|---|
| **Given** | El Archivo no es PDF o supera 5MB |
| **When** | El Estudiante intenta cargarlo |
| **Then** | El Sistema rechaza el archivo mostrando mensaje de error |

---

## Historia de usuario 10

| **Historia N°:** | 10 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Recibir una sugerencia preliminar de equivalencia |
| **Para** | Saber si mi propuesta tiene viabilidad |

**Scenario 10.1:** Generar sugerencia con información suficiente

| | |
|---|---|
| **Given** | El Curso externo tiene créditos, descripción y syllabus adjunto |
| **When** | El Estudiante solicita sugerencia |
| **Then** | El Sistema genera recomendación preliminar de equivalencia |

**Scenario 10.2:** Información insuficiente para sugerencia

| | |
|---|---|
| **Given** | El Curso externo no cuenta con descripción o syllabus adjunto |
| **When** | El Estudiante solicita sugerencia |
| **Then** | El Sistema solicita completar la información faltante |

**Scenario 10.3:** Sugerencia basada en criterios de aprobación

| | |
|---|---|
| **Given** | El Curso externo tiene créditos, descripción y syllabus adjunto |
| **When** | El Sistema genera la recomendación preliminar |
| **Then** | La Sugerencia incluye una clasificación (Alto / Medio / Bajo Cumplimiento) basada en similitud de créditos, objetivos y competencias con el curso destino |
| **And** | El Sistema indica al estudiante los criterios que cumple y los que no |

**Scenario 10.4:** Recomendación apoyada en historial de solicitudes previas

| | |
|---|---|
| **Given** | Existen solicitudes similares previamente aprobadas o rechazadas en el sistema |
| **When** | El Estudiante solicita sugerencia |
| **Then** | El Sistema incluye en la recomendación un aviso donde se indica si cursos similares fueron aprobados o rechazados anteriormente |

**Scenario 10.5:** Curso externo sin precedentes en el historial

| | |
|---|---|
| **Given** | No existen solicitudes similares previas en el sistema |
| **When** | El Estudiante solicita sugerencia |
| **Then** | El Sistema genera la sugerencia únicamente con base en los criterios académicos disponibles |
| **And** | Indica al estudiante que no hay precedentes registrados para ese curso |

---

## Historia de usuario 11

| **Historia N°:** | 11 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Enviar mi solicitud de equivalencia |
| **Para** | Revisión académica |

**Scenario 11.1:** Enviar solicitud completa

| | |
|---|---|
| **Given** | El curso externo tiene documentos y sugerencia preliminar |
| **When** | El estudiante envía la solicitud |
| **Then** | El sistema registra la solicitud con estado "enviada" |

**Scenario 11.2:** Bloquear envío por información incompleta

| | |
|---|---|
| **Given** | Faltan documentos o datos obligatorios |
| **When** | El estudiante intenta enviar la solicitud |
| **Then** | El sistema bloquea el envío y muestra mensaje de error |

---

## Historia de usuario 12

| **Historia N°:** | 12 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Consultar el estado de mi solicitud |
| **Para** | Hacer seguimiento |

**Scenario 12.1:** Visualizar estado válido

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El Estudiante consulta su solicitud |
| **Then** | El Sistema muestra uno de los estados: enviada, en revisión, aprobada o rechazada |

**Scenario 12.2:** Estudiante sin solicitudes

| | |
|---|---|
| **Given** | El Estudiante no ha enviado solicitudes |
| **When** | Accede al módulo |
| **Then** | El sistema muestra mensaje sin solicitudes |

---

## Historia de usuario 13

| **Historia N°:** | 13 |
|---|---|
| **Yo como** | Asistente de Programa |
| **Quiero** | Revisar solicitudes de equivalencia |
| **Para** | Gestionarlas y asignarlas al siguiente responsable |

**Scenario 13.1:** Ver solicitudes en revisión

| | |
|---|---|
| **Given** | Existen solicitudes con estado "enviada" |
| **When** | El Asistente de Programa accede al módulo |
| **Then** | El sistema muestra listado de solicitudes pendientes |

**Scenario 13.2:** No existen solicitudes pendientes

| | |
|---|---|
| **Given** | No hay solicitudes registradas |
| **When** | El Asistente de Programa accede al módulo |
| **Then** | El sistema muestra mensaje sin solicitudes |

---

## Historia de usuario 14

| **Historia N°:** | 14 |
|---|---|
| **Yo como** | Jefe de Departamento |
| **Quiero** | Aprobar o rechazar una equivalencia |
| **Para** | Registrar la decisión |

**Scenario 14.1:** Aprobar solicitud

| | |
|---|---|
| **Given** | La solicitud está en estado "en revisión" |
| **When** | El Jefe de Departamento aprueba la equivalencia |
| **Then** | El sistema cambia el estado a "aprobada" |

**Scenario 14.2:** Rechazar solicitud

| | |
|---|---|
| **Given** | La solicitud está en estado "en revisión" |
| **When** | El Jefe de Departamento rechaza la equivalencia |
| **Then** | El sistema cambia el estado a "rechazada" |

---

## Historia de usuario 15

| **Historia N°:** | 15 |
|---|---|
| **Yo como** | Jefe de Departamento |
| **Quiero** | Que el sistema genere y asigne de forma automática un certificado al registrar la decisión final |
| **Para** | Formalizar el resultado y garantizar que todas las entidades involucradas queden notificadas con respaldo oficial |

**Scenario 15.1:** Generación exitosa del certificado al aprobar

| | |
|---|---|
| **Given** | El Jefe de Departamento registra una decisión de aprobación |
| **When** | El Sistema confirma la decisión |
| **Then** | Genera un certificado con el nombre del estudiante, curso origen, universidad de origen, curso destino, créditos, decisión, fecha y responsables del flujo |
| **And** | Envía el certificado al estudiante, asistente de programa, director de programa y jefe de departamento |
| **And** | Guarda un backup o copia de seguridad en el sistema |

**Scenario 15.2:** Generación del certificado al rechazar

| | |
|---|---|
| **Given** | El Jefe de Departamento registra una decisión de rechazo |
| **When** | El Sistema confirma la decisión |
| **Then** | Genera un certificado indicando el rechazo de la solicitud junto con la justificación registrada |
| **And** | Envía el certificado al estudiante, asistente de programa, director de programa y jefe de departamento |
| **And** | Guarda un backup o copia de seguridad en el sistema |

---

## Historia de usuario 16

| **Historia N°:** | 16 |
|---|---|
| **Yo como** | Asistente de Programa |
| **Quiero** | Ver las solicitudes ordenadas por prioridad |
| **Para** | Atender primero los casos más urgentes o con mayor tiempo de espera |

**Scenario 16.1:** Priorización por fecha de envío

| | |
|---|---|
| **Given** | Existen solicitudes en la bandeja |
| **When** | El Asistente accede al módulo de solicitudes |
| **Then** | El Sistema muestra las solicitudes ordenadas de la más antigua hasta la más reciente |

**Scenario 16.2:** Priorización por emergencia declarada

| | |
|---|---|
| **Given** | El Sistema marcó la solicitud como urgente al momento en que el Estudiante la enviase (Urgente se refiere a que el Estudiante tiene fecha límite de matrícula próxima o que ocurrió un imprevisto donde el Estudiante ya se encuentra en la otra universidad) |
| **When** | El Asistente accede al módulo |
| **Then** | El Sistema destaca visualmente las solicitudes marcadas como urgentes por encima de las demás |

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
