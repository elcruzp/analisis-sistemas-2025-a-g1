```mermaid
classDiagram
    class Usuario {
        +id: Int
        +nombre: String
        +email: String
        +contraseña: String
        +rol: Rol
        +createdAt: DateTime
        +tutoriasSolicitadas: Tutoria[]
        +tutoriasAsignadas: Tutoria[]
        +comentarios: Comentario[]
    }

    class Tutoria {
        +id: Int
        +titulo: String
        +descripcion: String
        +fecha: DateTime
        +estado: EstadoTutoria
        +createdAt: DateTime
        +estudiante: Usuario
        +tutor: Usuario
        +comentarios: Comentario[]
    }

    class Comentario {
        +id: Int
        +contenido: String
        +createdAt: DateTime
        +autor: Usuario
        +tutoria: Tutoria
    }

    class Rol {
        ESTUDIANTE
        TUTOR
        COORDINADOR
    }

    class EstadoTutoria {
        PENDIENTE
        CONFIRMADA
        COMPLETADA
        CANCELADA
    }

    Usuario "1" -- "*" Tutoria : solicita
    Usuario "1" -- "*" Tutoria : imparte
    Usuario "1" -- "*" Comentario : escribe
    Tutoria "1" -- "*" Comentario : contiene
