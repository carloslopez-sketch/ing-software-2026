# Arquitectura del Proyecto Final

## Sistema: Gestión de Préstamos de Biblioteca Universitaria

## 1. Objetivo de la arquitectura

El sistema permitirá gestionar préstamos, devoluciones, usuarios, libros, sanciones y disponibilidad de ejemplares dentro de la Biblioteca Central de la Universidad.

La arquitectura se diseña para separar responsabilidades, facilitar mantenimiento y permitir crecimiento futuro.

---

## 2. Arquitectura propuesta

Se utilizará una arquitectura por capas:

1. Capa de presentación
2. Capa de aplicación
3. Capa de dominio
4. Capa de infraestructura
5. Capa de base de datos

---

## 3. Diagrama de capas

```mermaid
flowchart TD
    A[Usuario / Bibliotecario / Administrador] --> B[Capa de Presentación]

    B --> C[Capa de Aplicación]

    C --> D[Capa de Dominio]

    D --> E[Capa de Infraestructura]

    E --> F[(Base de Datos)]

    C --> G[Servicios externos] G --> H[Notificaciones por correo]

+-----------------------------+
|        Usuarios             |
| Estudiante / Bibliotecario  |
+-------------+---------------+
              |
              v
+-----------------------------+
|   Capa de Presentación      |
|   Interfaz Web              |
+-------------+---------------+
              |
              v
+-----------------------------+
|   Capa de Aplicación        |
|   Casos de uso / API REST   |
+-------------+---------------+
              |
              v
+-----------------------------+
|   Capa de Dominio           |
|   Reglas del negocio        |
+-------------+---------------+
              |
              v
+-----------------------------+
|   Capa de Infraestructura   |
|   Repositorios / Servicios  |
+-------------+---------------+
              |
              v
+-----------------------------+
|        Base de Datos        |
|           MySQL             |
+-----------------------------+
