# Diagramas UML del Proyecto Final

## Sistema: Gestión de Préstamos de Biblioteca Universitaria

---

## 1. Diagrama de clases

```mermaid
classDiagram
    class Usuario {
        +int id
        +string nombre
        +string correo
        +string telefono
        +string estado
        +consultarCatalogo()
        +solicitarPrestamo()
    }

    class Bibliotecario {
        +int id
        +string nombre
        +registrarPrestamo()
        +registrarDevolucion()
        +gestionarMultas()
    }

    class Administrador {
        +crearUsuario()
        +gestionarRoles()
        +generarReportes()
    }

    class Libro {
        +int id
        +string titulo
        +string autor
        +string isbn
        +string categoria
    }

    class Ejemplar {
        +int id
        +string codigo
        +string estado
        +verificarDisponibilidad()
    }

    class Prestamo {
        +int id
        +date fechaPrestamo
        +date fechaLimite
        +string estado
        +calcularFechaLimite()
    }

    class Devolucion {
        +int id
        +date fechaDevolucion
        +registrarDevolucion()
    }

    class Multa {
        +int id
        +decimal monto
        +string estado
        +calcularMulta()
    }

    Usuario "1" --> "0..*" Prestamo
    Bibliotecario "1" --> "0..*" Prestamo
    Libro "1" --> "1..*" Ejemplar
    Ejemplar "1" --> "0..*" Prestamo
    Prestamo "1" --> "0..1" Devolucion
    Prestamo "1" --> "0..1" Multa
    Administrador --|> Bibliotecario
