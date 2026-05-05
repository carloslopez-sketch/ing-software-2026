# SRS - Sistema de Gestión de Biblioteca Universitaria

## 1. Dominio del proyecto

El proyecto final será un Sistema de Gestión de Biblioteca Universitaria.

El sistema permitirá administrar estudiantes, libros, ejemplares, préstamos, devoluciones, multas, búsquedas y reportes administrativos.

---

## 2. Objetivo general

Desarrollar un sistema web que permita automatizar el proceso de préstamos bibliotecarios, reduciendo errores manuales, mejorando el control de inventario y facilitando el acceso a la información.

---

## 3. Usuarios del sistema

- Estudiante
- Bibliotecario
- Administrador

---

## 4. Historias de usuario

US-01: Como estudiante quiero registrarme en el sistema para acceder a los servicios de la biblioteca.

US-02: Como estudiante quiero iniciar sesión para consultar mis préstamos y multas.

US-03: Como estudiante quiero buscar libros por título, autor o categoría para encontrar material rápidamente.

US-04: Como estudiante quiero ver la disponibilidad de un libro para saber si puedo solicitarlo.

US-05: Como estudiante quiero consultar mis préstamos activos para conocer mis fechas de devolución.

US-06: Como estudiante quiero consultar mis multas pendientes para saber cuánto debo pagar.

US-07: Como bibliotecario quiero registrar estudiantes para permitirles usar el servicio de préstamo.

US-08: Como bibliotecario quiero validar la matrícula de un estudiante antes de realizar un préstamo.

US-09: Como bibliotecario quiero registrar libros para mantener actualizado el inventario.

US-10: Como bibliotecario quiero registrar ejemplares de cada libro para controlar copias físicas.

US-11: Como bibliotecario quiero registrar préstamos para saber qué estudiante tiene cada libro.

US-12: Como bibliotecario quiero registrar devoluciones para actualizar el estado del ejemplar.

US-13: Como bibliotecario quiero ver préstamos vencidos para dar seguimiento a estudiantes atrasados.

US-14: Como bibliotecario quiero actualizar el estado de un libro como disponible, prestado, dañado o perdido.

US-15: Como sistema quiero validar automáticamente si un libro está disponible antes de prestarlo.

US-16: Como sistema quiero calcular automáticamente multas por días de retraso.

US-17: Como sistema quiero bloquear préstamos a estudiantes con multas pendientes.

US-18: Como sistema quiero guardar historial de préstamos para auditoría.

US-19: Como administrador quiero gestionar usuarios y roles para controlar permisos.

US-20: Como administrador quiero generar reportes de libros más prestados, multas y préstamos vencidos.

---

## 5. Requisitos no funcionales

RNF-01 Rendimiento:
El sistema debe responder a búsquedas de libros en menos de 2 segundos con hasta 10,000 registros.

RNF-02 Disponibilidad:
El sistema debe estar disponible al menos el 95% del tiempo durante horario académico.

RNF-03 Seguridad:
Las contraseñas deben almacenarse cifradas mediante hashing seguro.

RNF-04 Usabilidad:
Un bibliotecario debe poder registrar un préstamo en menos de 1 minuto.

RNF-05 Escalabilidad:
El sistema debe permitir registrar al menos 10,000 estudiantes y 50,000 libros sin degradación significativa.

RNF-06 Auditoría:
El sistema debe registrar acciones importantes como préstamos, devoluciones, bloqueos y pagos de multas.

RNF-07 Compatibilidad:
El sistema debe funcionar correctamente en navegadores modernos como Chrome, Firefox y Edge.

RNF-08 Respaldo:
La base de datos debe poder respaldarse al menos una vez al día.

---

## 6. Priorización MoSCoW

### Must

- US-02: Iniciar sesión.
- US-03: Buscar libros.
- US-04: Ver disponibilidad.
- US-08: Validar matrícula.
- US-09: Registrar libros.
- US-10: Registrar ejemplares.
- US-11: Registrar préstamos.
- US-12: Registrar devoluciones.
- US-15: Validar disponibilidad.
- US-16: Calcular multas.
- US-17: Bloquear préstamos con multas.

### Should

- US-01: Registro de estudiantes.
- US-05: Consultar préstamos activos.
- US-06: Consultar multas.
- US-13: Ver préstamos vencidos.
- US-14: Actualizar estado del libro.
- US-18: Guardar historial de préstamos.
- US-19: Gestionar usuarios y roles.

### Could

- US-20: Generar reportes administrativos.

### Won’t

- Aplicación móvil.
- Notificaciones por WhatsApp.
- Integración con pagos bancarios.
- Reserva de libros en línea.
