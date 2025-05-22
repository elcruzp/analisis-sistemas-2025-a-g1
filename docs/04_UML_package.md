```mermaid
classDiagram
    class Auth {
        +login()
        +register()
        +jwtStrategy
    }

    class Usuarios {
        +createUser()
        +getUsers()
        +updateUser()
    }

    class Tutorias {
        +createTutoria()
        +getTutorias()
        +updateEstado()
    }

    class Comentarios {
        +addComentario()
        +getComentarios()
    }

    class Database {
        +Prisma
        +PostgreSQL
    }

    Auth -- Usuarios
    Usuarios -- Tutorias
    Tutorias -- Comentarios
    Database ..> Auth
    Database ..> Usuarios
    Database ..> Tutorias
    Database ..> Comentarios
