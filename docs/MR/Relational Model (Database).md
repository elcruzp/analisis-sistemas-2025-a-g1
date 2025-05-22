```mermaid
erDiagram
    USUARIO ||--o{ TUTORIA : "solicita"
    USUARIO ||--o{ TUTORIA : "imparte"
    USUARIO ||--o{ COMENTARIO : "escribe"
    TUTORIA ||--o{ COMENTARIO : "tiene"

    USUARIO {
        int id PK
        string nombre
        string email
        string contraseña
        enum rol
        datetime createdAt
    }

    TUTORIA {
        int id PK
        string titulo
        string descripcion
        datetime fecha
        enum estado
        int estudianteId FK
        int tutorId FK
        datetime createdAt
    }

    COMENTARIO {
        int id PK
        string contenido
        int autorId FK
        int tutoriaId FK
        datetime createdAt
    }