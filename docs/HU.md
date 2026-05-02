# ESPECIFICACIÓN DE HISTORIAS DE USUARIO (GHERKIN)

## COMPONENTE 1 – CATÁLOGO DE CURSOS

### HU1 – Ver lista de cursos
**Feature:** Visualizar catálogo de cursos

*   **Scenario:** Ver listado de cursos disponibles
    *   **Given** que el estudiante ingresa al catálogo
    *   **When** accede a la página principal de cursos
    *   **Then** el sistema muestra la lista de cursos disponibles

*   **Scenario:** Catálogo sin cursos disponibles
    *   **Given** que no existen cursos registrados
    *   **When** el estudiante accede al catálogo
    *   **Then** el sistema muestra un mensaje indicando que no hay cursos disponibles

---

### HU2 – Filtrar cursos
**Feature:** Filtrar cursos por criterios

*   **Scenario:** Filtrar por tema
    *   **Given** que el estudiante está viendo el catálogo
    *   **When** aplica un filtro por tema
    *   **Then** el sistema muestra solo los cursos que coinciden con el filtro

*   **Scenario:** Filtro sin resultados
    *   **Given** que el estudiante aplica un filtro
    *   **When** no existen cursos que coincidan
    *   **Then** el sistema muestra un mensaje de sin resultados

---

### HU3 – Buscar cursos
**Feature:** Buscar cursos por palabra clave

*   **Scenario:** Buscar por nombre
    *   **Given** que el estudiante está en el catálogo
    *   **When** ingresa una palabra clave
    *   **Then** el sistema muestra los cursos que coinciden con la búsqueda

*   **Scenario:** Búsqueda sin coincidencias
    *   **Given** que el estudiante realiza una búsqueda
    *   **When** no existen coincidencias
    *   **Then** el sistema muestra un mensaje de sin resultados

---

### HU4 – Ver ficha de curso
**Feature:** Visualizar detalle de curso

*   **Scenario:** Ver información detallada
    *   **Given** que el estudiante selecciona un curso
    *   **When** accede a la ficha del curso
    *   **Then** el sistema muestra la información detallada del curso

*   **Scenario:** Curso inexistente
    *   **Given** que el curso no existe
    *   **When** el estudiante intenta acceder a la ficha
    *   **Then** el sistema muestra un mensaje de error

---

### HU5 – Evaluar curso
**Feature:** Enviar evaluación de curso

*   **Scenario:** Enviar evaluación correctamente
    *   **Given** que el estudiante finalizó un curso
    *   **When** envía una evaluación
    *   **Then** el sistema guarda la evaluación

*   **Scenario:** Evaluación incompleta
    *   **Given** que el estudiante intenta enviar una evaluación incompleta
    *   **When** envía el formulario
    *   **Then** el sistema solicita completar los campos obligatorios

---

### HU6 – Editar o eliminar evaluación
**Feature:** Gestionar evaluación propia

*   **Scenario:** Editar evaluación
    *   **Given** que el estudiante ya envió una evaluación
    *   **When** la modifica y guarda cambios
    *   **Then** el sistema actualiza la evaluación

*   **Scenario:** Eliminar evaluación
    *   **Given** que el estudiante tiene una evaluación registrada
    *   **When** decide eliminarla
    *   **Then** el sistema elimina la evaluación

---

### HU7 – Ver evaluaciones de un curso
**Feature:** Consultar evaluaciones

*   **Scenario:** Ver evaluaciones disponibles
    *   **Given** que existen evaluaciones de un curso
    *   **When** el administrador accede al curso
    *   **Then** el sistema muestra las evaluaciones

*   **Scenario:** Curso sin evaluaciones
    *   **Given** que no existen evaluaciones
    *   **When** el administrador accede al curso
    *   **Then** el sistema muestra mensaje sin evaluaciones

---

### HU8 – Ver métricas agregadas
**Feature:** Visualizar métricas de evaluación

*   **Scenario:** Ver métricas
    *   **Given** que existen evaluaciones
    *   **When** el administrador consulta métricas
    *   **Then** el sistema muestra estadísticas agregadas

*   **Scenario:** Sin datos suficientes
    *   **Given** que no hay evaluaciones suficientes
    *   **When** el administrador consulta métricas
    *   **Then** el sistema muestra mensaje de datos insuficientes

---

### HU9 – Ver histórico de evaluaciones
**Feature:** Consultar histórico

*   **Scenario:** Consultar histórico
    *   **Given** que existen evaluaciones pasadas
    *   **When** el administrador consulta histórico
    *   **Then** el sistema muestra registros anteriores

*   **Scenario:** Sin histórico
    *   **Given** que no hay registros previos
    *   **When** el administrador consulta histórico
    *   **Then** el sistema muestra mensaje sin histórico

---

## COMPONENTE 2 – EQUIVALENCIAS INTERNACIONALES

### HU10 – Consultar cursos del área
**Feature:** Consultar cursos para equivalencias

*   **Scenario:** Ver cursos disponibles
    *   **Given** que el estudiante accede al módulo
    *   **When** consulta los cursos del área
    *   **Then** el sistema muestra la información de cursos

*   **Scenario:** Sin cursos registrados
    *   **Given** que no existen cursos
    *   **When** el estudiante consulta
    *   **Then** el sistema muestra mensaje sin cursos
