# Modelo Relacional (Base de Datos)
![Relational_Model](Relational%20Model.png)

## Tablas y relaciones:

### USUARIO:

- Campos básicos de identificación y autenticación.

- Rol para control de acceso.

- Relaciones: Una a muchas con TUTORIA (como estudiante y como tutor) y COMENTARIO.

### TUTORIA:

- Datos de la sesión académica.

- Estados que definen el flujo del proceso.

- Claves foráneas a USUARIO (ambos roles).

### COMENTARIO:

- Contenido de la comunicación.

- Relaciones con USUARIO (autor) y TUTORIA (contexto).

### Normalización:

Todas las tablas están en 3FN (Tercera Forma Normal):

- Sin atributos repetidos.

- Sin dependencias transitivas.

- Claves primarias simples.

#### *Estos diagramas cubren completamente los requisitos UML solicitados y reflejan fielmente la implementación técnica del sistema. Cada diagrama muestra una perspectiva diferente de la arquitectura, desde la estructura estática (clases, paquetes) hasta el comportamiento dinámico (casos de uso, secuencia) y el modelo de datos subyacente.*