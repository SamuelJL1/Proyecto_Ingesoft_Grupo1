# Metodo Dorfman y PESTLE

## Requerimiento funcionales:

### RF1 – Registro de solicitud de equivalencia por parte del estudiante

El estudiante registra una solicitud indicando el curso origen, curso destino y los documentos requeridos. Si faltan campos obligatorios o los documentos no cumplen el formato establecido, el sistema lo indica sin perder la información ya ingresada.

La brecha digital puede excluir a estudiantes con menor acceso tecnológico; fallos durante el registro pueden bloquear el inicio del proceso sin posibilidad de recuperar la información. Los datos personales recopilados están sujetos a la Ley 1581 de 2012; su manejo inadecuado constituye una violación directa al derecho de Habeas Data.

### RF1.1: Carga y validación de documentos de soporte

El estudiante adjunta los documentos que sustentan la equivalencia (syllabus, código del curso y balance académico) en formato PDF con un tamaño máximo de 5MB por archivo. Si el archivo no cumple estas condiciones, el sistema indica el motivo con un mensaje específico.

Exigir un formato estricto sin orientación clara puede excluir a estudiantes con menor acceso o conocimiento técnico, vulnerando su derecho a participar en el proceso. La inestabilidad del sistema durante la carga puede provocar pérdida de documentos y dejar la solicitud incompleta sin que el estudiante lo sepa.

### RF2: Consulta del estado de solicitudes por parte del estudiante

El estudiante consulta en cualquier momento el estado actual de su solicitud: enviada, en revisión, aprobada o rechazada. Si no tiene solicitudes registradas, el sistema lo indica. La falta de visibilidad sobre el estado de la solicitud incumple el principio de transparencia exigido por el MEN y genera desconfianza en el proceso institucional.

### RF3: Asignación automática de solicitudes en el flujo institucional

Al registrarse una solicitud, el sistema la asigna al primer responsable de la cadena (Dirección de Programa), siguiendo el flujo institucional hacia el Jefe de Departamento y finalmente Admisiones. Si no es posible identificar el departamento del curso destino, la solicitud queda en estado "Pendiente de Asignación" y se notifica a la Dirección de Programa para su resolución manual.

Una asignación incorrecta que no respete la jerarquía institucional invalida el proceso académico y puede generar decisiones sin respaldo institucional. Errores en los datos maestros del sistema (departamentos, cursos, responsables) pueden provocar asignaciones incorrectas que perjudiquen directamente al estudiante.

### RF4: Registro de decisión final de solicitudes por parte del Jefe de Departamento

El Jefe de Departamento registra la decisión final (aprobada o rechazada) junto con una justificación obligatoria. El sistema actualiza el estado de la solicitud y desencadena automáticamente la generación del certificado y las notificaciones correspondientes.

Omitir la justificación hace que la decisión no sea auditable, abriendo la puerta a arbitrariedad y exponiendo a la institución a conflictos legales. Una decisión sin justificación comprensible afecta directamente la trayectoria académica del estudiante sin darle elementos para apelarla.

### RF4.1: Almacenar decisiones con trazabilidad histórica

Cada decisión queda almacenada con fecha, responsable, estado y justificación. El historial es inmutable; cualquier modificación posterior genera una nueva entrada sin eliminar la anterior, garantizando trazabilidad completa del proceso.

Sin trazabilidad inmutable, el historial no puede usarse como evidencia válida en procesos de reclamación o auditoría institucional. La pérdida de registros por fallos del sistema afecta los derechos del estudiante y la credibilidad institucional del proceso.

### RF5: Consulta de historial de equivalencias previas por parte del Jefe de Departament

El Jefe de Departamento busca equivalencias previas por curso origen, curso destino o filtrando por estado (aprobadas o rechazadas), con el fin de reutilizar criterios en solicitudes similares y evitar reprocesos. Si no existen registros para el criterio ingresado, el sistema lo indica sin generar error.

No contar con historial consultable obliga a reprocesar solicitudes similares, generando inconsistencias en las decisiones y mayor carga administrativa innecesaria.

### RF6: Modificación justificada de decisiones previas con registro de cambios

El Jefe de Departamento puede modificar el estado o justificación de una equivalencia previamente registrada. El cambio queda registrado en el historial con fecha y responsable, sin eliminar la decisión anterior.

Modificar una decisión sin dejar rastro auditable puede afectar a un estudiante que ya actuó con base en el resultado anterior, y expone a la institución a disputas legales sin evidencia que las respalde.

### RF7: Análisis automático de Solicitudes mediante IA por nivel de cumplimiento académico

El sistema analiza la solicitud comparando créditos, objetivos y competencias del curso externo con los del curso destino. El resultado incluye una clasificación de viabilidad (Alto, Medio o Bajo cumplimiento) y una indicación explícita de qué criterios cumple y cuáles no, de forma que el Jefe de Departamento pueda tomar una decisión informada.

Un análisis automatizado sin explicabilidad incumple el principio de transparencia exigido por el MEN y puede generar desconfianza en los estudiantes sobre cómo son evaluados. El modelo puede replicar sesgos presentes en datos históricos, perpetuando decisiones desiguales de forma sistemática.

### RF8: Notificación automática al estudiante sobre cambios en el estado de su solicitud

Cada vez que el estado de una solicitud cambia, el sistema notifica automáticamente al estudiante indicando el nuevo estado y, cuando aplica, el motivo registrado por el Jefe de Departamento al tomar la decisión (por ejemplo, si fue aprobada porque los créditos y competencias son equivalentes, o rechazada por diferencia en objetivos de aprendizaje). Los fallos en el envío se gestionan con reintentos automáticos para garantizar que el estudiante reciba la información.

La falta de notificación oportuna puede llevar al estudiante a tomar decisiones académicas con información desactualizada; un fallo técnico sin reintento equivale a dejar al estudiante sin respuesta.

### RF9: Notificación automática de solicitudes pendientes al siguiente responsable en la cadena institucional

Cada vez que un responsable aprueba el paso de una solicitud al siguiente nivel, el sistema notifica automáticamente al receptor correspondiente en la cadena (Dirección de Programa → Jefe de Departamento → Admisiones), indicándole que tiene una solicitud pendiente de revisión. Si el envío falla, el sistema reintenta automáticamente y alerta a la Dirección de Programa en caso de fallo persistente para que la gestión no se detenga.

Un fallo de notificación sin manejo de errores puede paralizar completamente el flujo institucional sin que ningún responsable lo detecte a tiempo.

### RF10: Generación automática del certificado de decisión final
Al registrar el Jefe de Departamento la decisión final sobre una solicitud, el sistema genera automáticamente un certificado que contiene: nombre del estudiante, curso origen, universidad de origen, curso destino, créditos, decisión (aprobada o rechazada), motivo de la decisión, fecha y responsables del flujo institucional.

El certificado es la evidencia formal de la decisión; generarlo con información incompleta deja sin respaldo legal tanto al estudiante como a la institución.

### RF10.1: Distribución y respaldo del certificado de decisión final
Una vez generado el certificado, el sistema lo distribuye al estudiante, la Dirección de Programa y el Jefe de Departamento. Adicionalmente, guarda una copia de respaldo en el sistema para garantizar su disponibilidad ante futuras consultas o requerimientos legales. Si el envío falla, el sistema reintenta automáticamente.

Sin distribución automática, la notificación queda sujeta a procesos manuales que pueden omitirse, dejando al estudiante sin constancia oficial del resultado.

### RF11: Priorización automática de solicitudes por urgencia o tiempo de espera

La bandeja de la Dirección de Programa muestra las solicitudes ordenadas de más antigua a más reciente. Las solicitudes que el sistema identifica como urgentes (estudiante con fecha límite de matrícula próxima o que ya se encuentra en la universidad de destino) se destacan visualmente por encima de las demás.

No atender a tiempo una solicitud urgente puede comprometer la situación académica o migratoria del estudiante de forma irreversible. Si el sistema no detecta automáticamente las condiciones de urgencia, la priorización depende de criterio manual y puede ser inconsistente.

### RF12: Consulta de información académica de cursos internos por parte del estudiante en movilidad

El estudiante en movilidad consulta los cursos del área con su código, nombre, créditos, competencias y resultados de aprendizaje, con el fin de identificar qué curso interno podría ser equivalente al que cursó en el extranjero antes de iniciar una solicitud formal. Si no hay cursos registrados en el sistema, se indica al estudiante sin generar error.

Sin acceso a esta información, el estudiante enfrenta una asimetría de conocimiento frente a la institución que lo obliga a iniciar solicitudes a ciegas, aumentando la tasa de rechazos evitables.

---

## Entidades

### Actores:
- Estudiante
- Dirección de Programa
- Jefe de Departamento
- Admisiones

### Entidades del negocio:
- Solicitud de equivalencia
- Curso origen
- Curso destino
- Universidad externa
- Departamento
- Programa académico
- Documento de soporte
- Decisión
- Historial de decisiones
- Certificado de decisión
- Evaluación IA

--- 

## Subsistemas:

Subsistema de Gestión de Solicitudes

RF1 - RF1.1 - RF2 - RF12

Subsistema de Flujo de Aprobación:

RF3 - RF4 - RF4.1 - RF10 - RF10.1 - RF11

Subsistema de Base de Datos

RF5 - RF6

Subsistema de Inteligencia Artificial

RF7

Subsistema de Notificaciones

RF8 - RF9

---

# Solicitud de Equivalencia

---

## Registro de solicitud de equivalencia

| **Historia N°:** | 1 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Registrar una solicitud de equivalencia con la información del curso y documentos |
| **Para** | Iniciar formalmente el proceso de evaluación de equivalencia ante la institución |

**Scenario 1.1:** Registro exitoso con datos completos

| | |
|---|---|
| **Given** | El estudiante se encuentra en el formulario de solicitud |
| **When** | Ingresa curso origen, curso destino y adjunta documentos válidos |
| **Then** | El sistema guarda la solicitud correctamente |
| **And** | Muestra un mensaje de confirmación |

**Scenario 1.2:** Guardado de borrador sin envío

| | |
|---|---|
| **Given** | El estudiante se encuentra en el formulario de solicitud |
| **When** | Completa parcialmente el formulario y selecciona guardar borrador |
| **Then** | El sistema almacena la información ingresada en estado "borrador" |
| **And** | Permite al estudiante continuar el registro en una sesión posterior |

**Scenario 1.3:** Registro fallido por datos incompletos

| | |
|---|---|
| **Given** | El estudiante se encuentra en el formulario de solicitud |
| **When** | Omite información obligatoria e intenta continuar |
| **Then** | El sistema muestra un mensaje de error indicando los campos faltantes |
| **And** | No avanza al siguiente paso hasta que se completen |

**Scenario 1.4:** Registro fallido por documentos en formato inválido

| | |
|---|---|
| **Given** | El estudiante se encuentra en el formulario de solicitud |
| **When** | Adjunta documentos en un formato no permitido |
| **Then** | El sistema muestra un mensaje indicando el formato inválido |
| **And** | Solicita al estudiante cargar el archivo en el formato correcto |

---

## Enrutamiento automático por flujo institucional

| **Historia N°:** | 2 |
|---|---|
| **Yo como** | Direccion de Programa |
| **Quiero** | Que el sistema asigne automáticamente las solicitudes al responsable correspondiente siguiendo el flujo institucional |
| **Para** | Agilizar el proceso de evaluación y garantizar el orden correcto a las entidades respectivas |

**Scenario 2.1:** Asignación inicial a la Dirección de Programa

| | |
|---|---|
| **Given** | El estudiante ha enviado una solicitud con documentos válidos y completos |
| **When** | El sistema registra la nueva solicitud |
| **Then** | Asigna la solicitud a la Dirección de Programa correspondiente |
| **And** | Notifica a la Dirección de Programa |

**Scenario 2.2:** Paso de la Dirección de Programa al Jefe de Departamento

| | |
|---|---|
| **Given** | La Dirección de Programa ha revisado la solicitud |
| **When** | La Dirección de Programa aprueba el paso al siguiente nivel |
| **Then** | El sistema asigna la solicitud al Jefe de Departamento correspondiente |
| **And** | Notifica al Jefe de Departamento |

**Scenario 2.3:** Paso del Jefe de Departamento a Admisiones

| | |
|---|---|
| **Given** | El Jefe de Departamento ha registrado la decisión final |
| **When** | El sistema confirma la decisión |
| **Then** | El sistema notifica a Admisiones |
| **And** | Se cierra el flujo de revisión |

**Scenario 2.4:** Solicitud sin departamento identificado

| | |
|---|---|
| **Given** | El estudiante ha enviado una solicitud con documentos válidos y completos |
| **And** | El sistema no puede identificar el departamento del curso destino |
| **When** | Intenta asignar la solicitud |
| **Then** | La solicitud queda en estado "Pendiente de Asignación" |
| **And** | Se notifica a la Dirección de Programa para resolverlo manualmente |

---

## Clasificación automática de solicitudes por IA

| **Historia N°:** | 3 |
|---|---|
| **Yo como** | Jefe de Departamento |
| **Quiero** | Recibir una clasificación automática de las solicitudes |
| **Para** | Enfocar mi revisión en las solicitudes con mayor y menor viabilidad académica |

**Scenario 3.1:** Clasificación en alto cumplimiento

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El sistema ejecuta el análisis de IA |
| **And** | El curso cumple la mayoría de los criterios |
| **Then** | Clasifica la solicitud como "Alto cumplimiento" |

**Scenario 3.2:** Clasificación en medio cumplimiento

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El sistema ejecuta el análisis de IA |
| **And** | El curso cumple parcialmente los criterios |
| **Then** | Clasifica la solicitud como "Medio cumplimiento" |

**Scenario 3.3:** Clasificación en bajo cumplimiento

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El sistema ejecuta el análisis de IA |
| **And** | El curso no cumple los criterios |
| **Then** | Clasifica la solicitud como "Bajo cumplimiento" |

---

## Consulta de historial de equivalencias previas

| **Historia N°:** | 4 |
|---|---|
| **Yo como** | Jefe de Departamento |
| **Quiero** | Consultar equivalencias previamente aprobadas o rechazadas |
| **Para** | Evitar reprocesar solicitudes similares |

**Scenario 4.1:** Consulta exitosa de historial

| | |
|---|---|
| **Given** | El Jefe de Departamento está en el historial |
| **When** | Busca por curso origen o curso destino |
| **Then** | El sistema muestra las equivalencias previas |

**Scenario 4.2:** Consulta sin resultados

| | |
|---|---|
| **Given** | El Jefe de Departamento está en el historial |
| **When** | Busca un curso sin registros previos |
| **Then** | El sistema muestra un mensaje indicando que no hay resultados |

**Scenario 4.3:** Filtrar historial solo por equivalencias aprobadas

| | |
|---|---|
| **Given** | El Jefe de Departamento está en el historial |
| **When** | Aplica el filtro "aprobadas" |
| **Then** | El sistema muestra únicamente las equivalencias con decisión aprobada |

---

## Modificación de decisiones con registro de cambios

| **Historia N°:** | 5 |
|---|---|
| **Yo como** | Jefe de Departamento |
| **Quiero** | Modificar decisiones anteriores |
| **Para** | Mantener actualizados los criterios académicos |

**Scenario 5.1:** Actualización exitosa de decisión

| | |
|---|---|
| **Given** | Existe una equivalencia previamente registrada |
| **When** | El Jefe de Departamento modifica el estado de la decisión |
| **Then** | El sistema actualiza la información |
| **And** | Guarda el cambio en el historial con fecha y responsable |

**Scenario 5.2:** Intento de actualización sin permisos

| | |
|---|---|
| **Given** | Existe una equivalencia registrada |
| **And** | El usuario no es Jefe de Departamento |
| **When** | Intenta modificar la decisión |
| **Then** | El sistema bloquea la acción |
| **And** | Muestra un mensaje de acceso denegado |

---

## Notificación automática de cambios de estado

| **Historia N°:** | 6 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Recibir notificaciones sobre el estado de mi solicitud |
| **Para** | Conocer en tiempo real el avance de mi solicitud sin necesidad de consultarla manualmente |

**Scenario 6.1:** Notificación por cambio de estado

| | |
|---|---|
| **Given** | Existe una solicitud en proceso |
| **When** | El estado cambia (aprobada, rechazada o en revisión) |
| **Then** | El sistema envía una notificación al estudiante con el nuevo estado |

**Scenario 6.2:** Consulta manual del estado

| | |
|---|---|
| **Given** | El estudiante accede al sistema |
| **When** | Revisa sus solicitudes |
| **Then** | El sistema muestra el estado actualizado de cada una |

---

## Consulta de información académica de cursos internos

| **Historia N°:** | 7 |
|---|---|
| **Yo como** | Estudiante en movilidad |
| **Quiero** | Consultar la información detallada de los cursos del área |
| **Para** | Evaluar qué curso interno es equivalente antes de iniciar una solicitud formal |

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
| **Then** | El sistema muestra un mensaje indicando que no hay cursos disponibles |

---

## Registro de curso de universidad extranjera

| **Historia N°:** | 8 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Registrar un curso de una universidad extranjera |
| **Para** | Iniciar una propuesta de equivalencia |

**Scenario 8.1:** Registro exitoso del curso externo

| | |
|---|---|
| **Given** | El estudiante ingresa nombre del curso, universidad, créditos y descripción |
| **When** | Guarda el curso externo |
| **Then** | El sistema registra el curso asociado al estudiante |

**Scenario 8.2:** Registro fallido por datos obligatorios faltantes

| | |
|---|---|
| **Given** | El estudiante no ingresa nombre del curso, universidad o créditos |
| **When** | Intenta guardar |
| **Then** | El sistema bloquea el registro y solicita completar los campos obligatorios |

---

## Carga de documentos de soporte del curso externo

| **Historia N°:** | 9 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Adjuntar documentos del curso externo, como el syllabus, código del curso y mi balance académico |
| **Para** | Respaldar la solicitud con la documentación académica que justifica la equivalencia |

**Scenario 9.1:** Carga exitosa de archivo válido

| | |
|---|---|
| **Given** | El archivo es PDF y pesa menos de 5MB |
| **When** | El estudiante carga el documento |
| **Then** | El sistema guarda el archivo correctamente y lo vincula a la solicitud |

**Scenario 9.2:** Carga fallida por archivo inválido o de tamaño excedido

| | |
|---|---|
| **Given** | El archivo no es PDF o supera 5MB |
| **When** | El estudiante intenta cargarlo |
| **Then** | El sistema rechaza el archivo y muestra un mensaje indicando el motivo |

---

## Sugerencia preliminar de viabilidad mediante IA

| **Historia N°:** | 10 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Recibir una sugerencia preliminar de equivalencia |
| **Para** | Saber si mi propuesta tiene viabilidad antes de enviarla formalmente |

**Scenario 10.1:** Generación de sugerencia con información suficiente

| | |
|---|---|
| **Given** | El curso externo tiene créditos, descripción y syllabus adjunto |
| **When** | El estudiante solicita sugerencia |
| **Then** | El sistema genera una recomendación preliminar de equivalencia |

**Scenario 10.2:** Información insuficiente para generar sugerencia

| | |
|---|---|
| **Given** | El curso externo no cuenta con descripción o syllabus adjunto |
| **When** | El estudiante solicita sugerencia |
| **Then** | El sistema solicita completar la información faltante |

**Scenario 10.3:** Sugerencia basada en criterios de aprobación

| | |
|---|---|
| **Given** | El curso externo tiene créditos, descripción y syllabus adjunto |
| **When** | El sistema genera la recomendación preliminar |
| **Then** | La sugerencia incluye una clasificación (Alto / Medio / Bajo Cumplimiento) basada en similitud de créditos, objetivos y competencias con el curso destino |
| **And** | El sistema indica al estudiante los criterios que cumple y los que no |

**Scenario 10.4:** Sugerencia apoyada en historial de solicitudes previas

| | |
|---|---|
| **Given** | Existen solicitudes similares previamente aprobadas o rechazadas en el sistema |
| **When** | El estudiante solicita sugerencia |
| **Then** | El sistema incluye en la recomendación un aviso indicando si cursos similares fueron aprobados o rechazados anteriormente |

**Scenario 10.5:** Curso externo sin precedentes en el historial

| | |
|---|---|
| **Given** | No existen solicitudes similares previas en el sistema |
| **When** | El estudiante solicita sugerencia |
| **Then** | El sistema genera la sugerencia únicamente con base en los criterios académicos disponibles |
| **And** | Indica al estudiante que no hay precedentes registrados para ese curso |

---

## Envío formal de solicitud de equivalencia

| **Historia N°:** | 11 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Enviar mi solicitud de equivalencia |
| **Para** | Someter la solicitud al flujo institucional de evaluación |

**Scenario 11.1:** Envío exitoso de solicitud completa

| | |
|---|---|
| **Given** | El curso externo tiene documentos y sugerencia preliminar |
| **When** | El estudiante envía la solicitud |
| **Then** | El sistema registra la solicitud con estado "enviada" |

**Scenario 11.2:** Envío bloqueado por información incompleta

| | |
|---|---|
| **Given** | Faltan documentos o datos obligatorios |
| **When** | El estudiante intenta enviar la solicitud |
| **Then** | El sistema bloquea el envío y muestra un mensaje indicando los elementos faltantes |

---

## Seguimiento del estado de la solicitud

| **Historia N°:** | 12 |
|---|---|
| **Yo como** | Estudiante |
| **Quiero** | Consultar el estado de mi solicitud |
| **Para** | Conocer en qué etapa del proceso se encuentra mi solicitud en cualquier momento |

**Scenario 12.1:** Visualización de estado activo

| | |
|---|---|
| **Given** | Existe una solicitud registrada |
| **When** | El estudiante consulta su solicitud |
| **Then** | El sistema muestra uno de los estados: enviada, en revisión, aprobada o rechazada |

**Scenario 12.2:** Estudiante sin solicitudes registradas

| | |
|---|---|
| **Given** | El estudiante no ha enviado solicitudes |
| **When** | Accede al módulo de seguimiento |
| **Then** | El sistema muestra un mensaje indicando que no hay solicitudes registradas |

---

## Gestión de bandeja de solicitudes recibidas

| **Historia N°:** | 13 |
|---|---|
| **Yo como** | Dirección de Programa |
| **Quiero** | Revisar las solicitudes de equivalencia recibidas |
| **Para** | Gestionarlas y asignarlas al siguiente responsable |

**Scenario 13.1:** Visualización de solicitudes pendientes

| | |
|---|---|
| **Given** | Existen solicitudes con estado "enviada" |
| **When** | La Dirección de Programa accede al módulo |
| **Then** | El sistema muestra el listado de solicitudes pendientes |

**Scenario 13.2:** Bandeja sin solicitudes pendientes

| | |
|---|---|
| **Given** | No hay solicitudes registradas |
| **When** | La Dirección de Programa accede al módulo |
| **Then** | El sistema muestra un mensaje indicando que no hay solicitudes por gestionar |

---

## Registro de decisión final sobre la equivalencia

| **Historia N°:** | 14 |
|---|---|
| **Yo como** | Jefe de Departamento |
| **Quiero** | Aprobar o rechazar una equivalencia |
| **Para** | Formalizar el resultado de la evaluación con trazabilidad en el sistema |

**Scenario 14.1:** Aprobación de solicitud

| | |
|---|---|
| **Given** | La solicitud está en estado "en revisión" |
| **When** | El Jefe de Departamento aprueba la equivalencia |
| **Then** | El sistema cambia el estado a "aprobada" |

**Scenario 14.2:** Rechazo de solicitud

| | |
|---|---|
| **Given** | La solicitud está en estado "en revisión" |
| **When** | El Jefe de Departamento rechaza la equivalencia |
| **Then** | El sistema cambia el estado a "rechazada" |

---

## Generación automática del certificado de decisión

| **Historia N°:** | 15 |
|---|---|
| **Yo como** | Jefe de Departamento |
| **Quiero** | Que el sistema genere y distribuya automáticamente un certificado al registrar la decisión final |
| **Para** | Formalizar el resultado y garantizar que todas las entidades involucradas queden notificadas con respaldo oficial |

**Scenario 15.1:** Generación exitosa del certificado al aprobar

| | |
|---|---|
| **Given** | El Jefe de Departamento registra una decisión de aprobación |
| **When** | El sistema confirma la decisión |
| **Then** | Genera un certificado con el nombre del estudiante, curso origen, universidad de origen, curso destino, créditos, decisión, fecha y responsables del flujo |
| **And** | Envía el certificado al estudiante, la Dirección de Programa y el Jefe de Departamento |
| **And** | Guarda una copia de respaldo en el sistema |

**Scenario 15.2:** Generación exitosa del certificado al rechazar

| | |
|---|---|
| **Given** | El Jefe de Departamento registra una decisión de rechazo |
| **When** | El sistema confirma la decisión |
| **Then** | Genera un certificado indicando el rechazo de la solicitud junto con la justificación registrada |
| **And** | Envía el certificado al estudiante, la Dirección de Programa y el Jefe de Departamento |
| **And** | Guarda una copia de respaldo en el sistema |

---

## Priorización de solicitudes por urgencia y antigüedad

| **Historia N°:** | 16 |
|---|---|
| **Yo como** | Dirección de Programa |
| **Quiero** | Ver las solicitudes ordenadas por prioridad |
| **Para** | Atender primero los casos más urgentes o con mayor tiempo de espera |

**Scenario 16.1:** Priorización por fecha de envío

| | |
|---|---|
| **Given** | Existen solicitudes en la bandeja |
| **When** | La Dirección de Programa accede al módulo de solicitudes |
| **Then** | El sistema muestra las solicitudes ordenadas de la más antigua a la más reciente |

**Scenario 16.2:** Priorización por urgencia detectada por el sistema

| | |
|---|---|
| **Given** | El sistema identifica una solicitud como urgente (estudiante con fecha límite de matrícula próxima o que ya se encuentra en la universidad de destino) |
| **When** | La Dirección de Programa accede al módulo |
| **Then** | El sistema destaca visualmente las solicitudes urgentes por encima de las demás |


---
