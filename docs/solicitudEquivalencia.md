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

Director de programa

Jefe de departamento

Sistema (con IA)


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
