# ESPECIFICACIÓN TÉCNICA DE HISTORIAS DE USUARIO

## COMPONENTE 1 – CATÁLOGO DE CURSOS

### HU1 – Ver lista de cursos
**Historia de Usuario:**
> Yo como estudiante quiero ver la lista de cursos disponibles del área para conocer las opciones que puedo elegir.

**Feature:** Visualizar catálogo de cursos

*   **Scenario: Ver listado paginado de cursos**
    ```gherkin
    Given que existen al menos 15 cursos activos registrados en el sistema
    When el estudiante accede al catálogo
    Then el sistema muestra la primera página con máximo 10 cursos
    And cada curso muestra código, nombre, créditos y área
    And los cursos están ordenados alfabéticamente por nombre
    ```

*   **Scenario: Navegar entre páginas del catálogo**
    ```gherkin
    Given que existen más de 10 cursos activos
    When el estudiante selecciona la página 2
    Then el sistema muestra los siguientes cursos sin repetir los anteriores
    ```

---

### HU2 – Filtrar cursos
**Historia de Usuario:**
> Yo como estudiante quiero filtrar cursos por temas o competencias para encontrar opciones alineadas con mis intereses.

**Feature:** Filtrar cursos por múltiples criterios

*   **Scenario: Filtrar por un criterio**
    
```gherkin
    Given que el estudiante está viendo el catálogo completo
    When aplica filtro por área "Humanidades"
    Then el sistema muestra solo cursos del área Humanidades
    ```

*   **Scenario: Filtrar por múltiples criterios combinados**
    ```gherkin
    Given que el estudiante está viendo el catálogo
    When aplica filtro por área "Humanidades" y competencia "Pensamiento crítico"
    Then el sistema muestra únicamente cursos que cumplan ambos criterios
    ```

---

### HU3 – Buscar cursos
**Historia de Usuario:**
> Yo como estudiante quiero buscar cursos por nombre o palabra clave para encontrarlos rápidamente.

**Feature:** Buscar cursos

*   **Scenario: Búsqueda parcial case insensitive**
    ```gherkin
    Given que existe un curso llamado "Introducción a la Programación"
    When el estudiante busca "prog"
    Then el sistema muestra el curso "Introducción a la Programación"
    ```

*   **Scenario: Búsqueda sin coincidencias**
    ```gherkin
    Given que el estudiante busca "astrofísica avanzada"
    When no existen cursos con esa palabra clave
    Then el sistema muestra mensaje de sin resultados
    ```

---

### HU4 – Ver ficha de curso
**Historia de Usuario:**
> Yo como estudiante quiero ver la ficha detallada de un curso para comprender su contenido antes de inscribirme.

**Feature:** Visualizar ficha completa del curso

*   **Scenario: Visualizar ficha de curso existente**
    ```gherkin
    Given que el curso existe en el sistema
    When el estudiante accede a la ficha del curso
    Then el sistema muestra descripción, créditos, competencias, resultados de aprendizaje y prerrequisitos
    ```

*   **Scenario: Acceso a curso inexistente**
    ```gherkin
    Given que el curso no existe
    When el estudiante intenta acceder mediante URL directa
    Then el sistema muestra error 404
    ```

---

### HU5 – Evaluar curso
**Historia de Usuario:**
> Yo como estudiante quiero evaluar un curso que tomé para compartir mi experiencia.

**Feature:** Registrar evaluación de curso

*   **Scenario: Evaluar curso aprobado**
    ```gherkin
    Given que el estudiante aprobó el curso con estado "finalizado"
    When envía una evaluación con calificación y comentario
    Then el sistema guarda la evaluación asociada al estudiante y al curso
    ```

*   **Scenario: Intentar evaluar curso no finalizado**
    ```gherkin
    Given que el estudiante está inscrito pero no ha finalizado el curso
    When intenta enviar evaluación
    Then el sistema bloquea la acción mostrando mensaje de restricción
    ```

---

### HU6 – Editar o eliminar evaluación
**Historia de Usuario:**
> Yo como estudiante quiero editar o eliminar mi evaluación para corregir mi retroalimentación.

**Feature:** Gestionar evaluación propia

*   **Scenario: Editar evaluación existente**
    ```gherkin
    Given que el estudiante ya tiene una evaluación registrada
    When modifica la calificación o comentario
    Then el sistema actualiza la evaluación
    ```

*   **Scenario: Eliminar evaluación**
    ```gherkin
    Given que el estudiante tiene una evaluación registrada
    When selecciona eliminar evaluación
    Then el sistema elimina el registro permanentemente
    ```

---

### HU7 – Ver evaluaciones de un curso
**Historia de Usuario:**
> Yo como administrador quiero ver las evaluaciones de un curso para entender la percepción estudiantil.

**Feature:** Consultar evaluaciones por curso

*   **Scenario: Ver listado de evaluaciones**
    ```gherkin
    Given que existen evaluaciones registradas para un curso
    When el administrador accede al módulo de evaluaciones
    Then el sistema muestra lista con calificación, comentario y fecha
    ```

*   **Scenario: Curso sin evaluaciones**
    ```gherkin
    Given que el curso no tiene evaluaciones
    When el administrador accede
    Then el sistema muestra mensaje de sin evaluaciones
    ```

---

### HU8 – Ver métricas agregadas
**Historia de Usuario:**
> Yo como administrador quiero ver métricas agregadas de evaluación para identificar tendencias.

**Feature:** Visualizar métricas de curso

*   **Scenario: Mostrar métricas disponibles**
    ```gherkin
    Given que el curso tiene evaluaciones registradas
    When el administrador consulta métricas
    Then el sistema muestra promedio de calificación
    And total de evaluaciones
    And distribución de calificaciones
    ```

*   **Scenario: Curso sin suficientes evaluaciones**
    
```gherkin
    Given que el curso tiene menos de 3 evaluaciones
    When el administrador consulta métricas
    Then el sistema muestra mensaje de datos insuficientes
    ```

---

### HU9 – Ver histórico de evaluaciones
**Historia de Usuario:**
> Yo como administrador quiero consultar evaluaciones históricas para analizar la evolución de un curso.

**Feature:** Consultar histórico de evaluaciones

*   **Scenario: Ver histórico por periodo**
    ```gherkin
    Given que existen evaluaciones en distintos semestres
    When el administrador filtra por semestre
    Then el sistema muestra evaluaciones del periodo seleccionado
    ```

*   **Scenario: Periodo sin registros**
    ```gherkin
    Given que no existen evaluaciones en el semestre seleccionado
    When el administrador consulta histórico
    Then el sistema muestra mensaje sin registros
    ```

---

## COMPONENTE 2 – EQUIVALENCIAS INTERNACIONALES

### HU10 – Consultar cursos del área para equivalencias
**Historia de Usuario:**
> Yo como estudiante en movilidad quiero consultar la información detallada de los cursos del área para compararlos con cursos externos.

**Feature:** Consultar cursos del área para equivalencias

*   **Scenario: Visualizar cursos con información académica completa**
    ```gherkin
    Given que existen cursos registrados en el sistema
    When el estudiante accede al módulo de equivalencias
    Then el sistema muestra cursos con código, nombre, créditos, competencias y resultados de aprendizaje
    ```

*   **Scenario: No existen cursos registrados**
    
```gherkin
    Given que no existen cursos en el sistema
    When el estudiante accede al módulo
    Then el sistema muestra mensaje indicando que no hay cursos disponibles
    ```
