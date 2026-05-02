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
