# Requerimientos Funcionales – Subsistema de Retroalimentación Estudiantil

---

**RF1 — El sistema debe permitir al estudiante diligenciar una encuesta de evaluación de la asignatura**  
El sistema debe permitir al estudiante acceder y diligenciar una encuesta de evaluación previamente generada por el sistema a partir de un banco de preguntas definido por el jefe de departamento, asociada a un curso y periodo académico cursado. Esta funcionalidad busca capturar las respuestas del formulario junto con un comentario obligatorio del estudiante, el cual podrá ser enviado de manera anónima o identificado según la preferencia seleccionada. Para cumplir con este resultado, el requerimiento tiene como entradas el identificador del estudiante (idEstudiante), el identificador del curso (idCurso), el periodo académico (periodoAcademico), las respuestas del formulario (respuestasEncuesta), el comentario obligatorio (comentarioEstudiante) y la preferencia de anonimato (anonimo), generando como salidas el identificador de la encuesta respondida (idEncuestaRespondida) y la confirmación de envío exitoso (envioRegistrado).  
En el ámbito **Legal**, este requerimiento implica el tratamiento de datos personales de estudiantes, especialmente por la opción de anonimato, por lo que debe cumplir normas de protección de datos. En el ámbito **Tecnológico**, requiere mecanismos seguros para el manejo de formularios dinámicos y almacenamiento de respuestas.

---

**RF2 — El sistema debe permitir al estudiante validar y enviar la encuesta diligenciada al jefe de departamento**  
El sistema debe permitir al estudiante validar que todas las preguntas de la encuesta hayan sido respondidas y que el comentario obligatorio cumpla con la longitud mínima antes de realizar el envío definitivo al jefe de departamento. Una vez enviada, la encuesta queda registrada para su revisión institucional sin posibilidad de edición posterior. Para cumplir con este resultado, el requerimiento utiliza como entradas el identificador de la encuesta respondida (idEncuestaRespondida) y las respuestas completas del formulario, generando como salida el estado ENVIADA que confirma su disponibilidad para revisión administrativa. En el ámbito **Tecnológico**, se requieren validaciones automáticas que garanticen la integridad del formulario antes del envío definitivo. En el ámbito **Legal**, es necesario asegurar la conservación íntegra de los registros enviados.

---

**RF3 — El sistema debe permitir al estudiante seleccionar el envío anónimo o identificado de la encuesta**  
El sistema debe permitir al estudiante definir si desea que su encuesta sea enviada de forma anónima o identificada antes de completar el envío definitivo. Esta funcionalidad asegura que la preferencia de privacidad quede registrada y aplicada al momento de mostrar la información al jefe de departamento durante la revisión. Para cumplir con este resultado, el requerimiento utiliza como entrada la preferencia de anonimato (anonimo) asociada al identificador de la encuesta respondida (idEncuestaRespondida), generando como salida la confirmación de registro de privacidad (privacidadRegistrada). En el ámbito **Legal**, se relaciona con la protección de identidad y confidencialidad de los estudiantes. En el ámbito **Social**, el anonimato influye en la participación y sinceridad de las respuestas.

---

**RF4 — El sistema debe permitir al jefe de departamento consultar evaluaciones filtradas**  
El sistema debe permitir al jefe de departamento visualizar evaluaciones mediante filtros por estado, curso y periodo académico, facilitando así la revisión institucional y el control de calidad. Esta funcionalidad permite recuperar una colección de registros que cumplen con los criterios establecidos, asegurando además que si una evaluación es anónima, la identidad del estudiante se oculte automáticamente. Para cumplir con este resultado, el requerimiento utiliza como entradas el identificador del jefe (idJefe), el estado de filtro, y opcionalmente el curso y el periodo académico, generando como salida una lista estructurada de evaluaciones (listaEvaluaciones). En el ámbito **Tecnológico**, implica el desarrollo de mecanismos de filtrado y visualización segura de información. En el ámbito **Legal**, se debe proteger la identidad en encuestas anónimas.

---

**RF5 — El sistema debe permitir al jefe de departamento revisar evaluaciones mediante una vista filtrable**  
El sistema debe proporcionar al jefe de departamento una vista filtrable de evaluaciones por estado, curso y periodo académico para facilitar la revisión institucional y el control de calidad. Esta funcionalidad permite recuperar una colección de registros que cumplen con los criterios aplicados, garantizando que cuando una evaluación es marcada como anónima, la identidad del estudiante se oculte automáticamente. Para cumplir con este resultado, el requerimiento utiliza como entradas el identificador del jefe (idJefe), un estado válido (estado), y opcionalmente el curso (idCurso) y periodo (periodoAcademico), generando como salida una lista estructurada (listaEvaluaciones). En el ámbito **Político**, se relaciona con la transparencia y control institucional del proceso de revisión. En el ámbito **Legal**, implica el manejo de información académica sensible.

---

**RF6 — El sistema debe permitir al jefe de departamento rechazar validación con justificación**  
El sistema debe permitir al jefe de departamento rechazar evaluaciones en estado pendiente registrando obligatoriamente una justificación detallada del rechazo. Esta funcionalidad asegura que cada decisión esté respaldada por un motivo trazable, incluyendo fecha, responsable y razón del rechazo. Para cumplir con este resultado, el requerimiento utiliza como entradas el idEvaluacion, el idJefe, el motivo con mínimo 10 caracteres y la fechaRechazo, generando como salida el estado actualizado del registro. En el ámbito **Legal**, exige trazabilidad del proceso. En el ámbito **Tecnológico**, requiere auditoría y almacenamiento histórico.

---

**RF7 — El sistema debe generar reportes analíticos de retroalimentación**  
El sistema debe consolidar evaluaciones aprobadas y rechazadas para generar reportes analíticos dirigidos a jefes de departamento, permitiendo identificar tendencias. Incluye métricas como promedio, tasa de participación, distribución de calificaciones y comparaciones históricas. Entradas: idCurso y periodo académico. Salida: conjunto de datos estructurados. En el ámbito **Tecnológico**, implica procesamiento y análisis de datos. En el ámbito **Legal**, requiere anonimización de la información.

---

**RF8 — El sistema debe registrar el cierre de un periodo académico**  
El sistema debe registrar la finalización oficial de un periodo académico para activar procesos automáticos de consolidación y reportes. Entradas: periodo académico (AAAA-S) y fecha de cierre. Salida: confirmación de cierre. En el ámbito **Legal**, se relaciona con el cumplimiento del calendario académico. En el ámbito **Tecnológico**, requiere automatización de procesos.

---

**RF9 — El sistema debe enviar automáticamente reportes al jefe de departamento**  
El sistema debe distribuir automáticamente los reportes analíticos al finalizar el periodo, registrando evidencia del envío. Entradas: idJefeDepartamento y validación del periodo cerrado. Salida: confirmación de envío con fecha. En el ámbito **Tecnológico**, implica automatización. En el ámbito **Legal**, requiere trazabilidad del envío.

---

**RF10 — El sistema debe permitir consultar histórico de reportes**  
El sistema debe permitir consultar reportes históricos por curso y periodo académico para análisis longitudinal. Entradas: idJefeDepartamento, curso y periodo opcionales. Salida: lista de reportes históricos. En el ámbito **Tecnológico**, implica almacenamiento e indexación. En el ámbito **Legal**, debe cumplir políticas de conservación de datos.

---

**RF11 — El sistema debe permitir comparar cursos con inteligencia artificial**  
El sistema debe permitir comparar cursos mediante inteligencia artificial para identificar similitudes en evaluaciones, contenidos y desempeño. Entradas: idCursoA e idCursoB. Salida: diagnóstico comparativo automatizado. En el ámbito **Tecnológico**, involucra IA. En el ámbito **Legal**, requiere protección de datos.

---

**RF12 — El sistema debe permitir enviar un comentario obligatorio para validación**  
El sistema debe exigir al estudiante el envío de un comentario obligatorio mínimo de 50 palabras como parte de la validación de la evaluación. Se valida la entrada comentarioEstudiante antes de continuar el flujo. En el ámbito **Tecnológico**, exige validaciones automáticas. En el ámbito **Social**, promueve participación reflexiva. En el ámbito **Legal**, respalda la trazabilidad y conservación de evidencia cualitativa.
