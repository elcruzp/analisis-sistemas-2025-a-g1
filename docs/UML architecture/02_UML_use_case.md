```mermaid
graph LR

    Estudiante("👤 Estudiante")
    Tutor("👤 Tutor")
    Coordinador("👤 Coordinador Académico")

    subgraph "TUTORIA PLUS - Gestión de Tutorías"
        S1[Solicitar tutoría]
        S2[Visualizar tutorías agendadas]
        S3[Cancelar tutoría]

        T1[Gestionar agenda de tutorías]
        T2[Registrar avances de tutoría]

        C1[Revisar reportes]
        C2[Hacer seguimiento académico]
    end

    Estudiante --> S1
    Estudiante --> S2
    Estudiante --> S3

    Tutor --> T1
    Tutor --> T2

    Coordinador --> C1
    Coordinador --> C2
