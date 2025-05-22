```mermaid
graph TD
    %% Actores
    Estudiante([Estudiante])
    Tutor([Tutor])
    Coordinador([Coordinador])

    %% Casos de uso - Estudiante
    Estudiante --> A1[Solicitar tutoría]
    Estudiante --> A2[Ver tutorías propias]
    Estudiante --> A3[Cancelar tutoría]
    Estudiante --> A4[Agregar comentario]

    %% Casos de uso - Tutor
    Tutor --> B1[Aceptar/rechazar tutoría]
    Tutor --> B2[Ver tutorías asignadas]
    Tutor --> B3[Cambiar estado de tutoría]
    Tutor --> B4[Agregar comentario]

    %% Casos de uso - Coordinador
    Coordinador --> C1[Gestionar usuarios]
    Coordinador --> C2[Ver reportes]
    Coordinador --> C3[Asignar tutores]

    %% Relaciones
    A2 --> D1[Ver tutorías]
    B2 --> D1

    A4 -.-> A1
