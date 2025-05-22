```mermaid
sequenceDiagram
    participant Estudiante
    participant Frontend
    participant Backend
    participant BaseDatos

    Estudiante ->> Frontend: Completa formulario de tutoría
    Frontend ->> Backend: POST /tutorias (datos tutoría)
    Backend ->> BaseDatos: Validar datos (estudiante, tutor)
    BaseDatos -->> Backend: Datos válidos
    Backend ->> BaseDatos: Crear registro de tutoría
    BaseDatos -->> Backend: Tutoría creada (ID 123)
    Backend -->> Frontend: Respuesta éxito (201 Created)
    Frontend -->> Estudiante: Confirmación y detalles