# 📄 Requisitos del Sistema de Biblioteca

## 🎭 Entrevista simulada

**Pregunta:** ¿Cómo identifican a los estudiantes?  
**Respuesta:** Mediante carnet o número de matrícula.  

**Pregunta:** ¿Cómo registran préstamos?  
**Respuesta:** Manualmente en hojas o Excel.  

**Pregunta:** ¿Cómo manejan devoluciones?  
**Respuesta:** Se buscan registros manualmente.  

**Pregunta:** ¿Cómo gestionan multas?  
**Respuesta:** Se calculan manualmente.  

**Pregunta:** ¿Cómo controlan inventario?  
**Respuesta:** Con listas en Excel no actualizadas.  

---

## ⚙️ Requisitos Funcionales

RF-01: El sistema debe registrar estudiantes.  
RF-02: El sistema debe registrar libros.  
RF-03: El sistema debe registrar préstamos.  
RF-04: El sistema debe registrar devoluciones.  
RF-05: El sistema debe calcular multas automáticamente.  
RF-06: El sistema debe validar disponibilidad de libros.  
RF-07: El sistema debe permitir búsqueda de libros.  
RF-08: El sistema debe generar reportes.  
RF-09: El sistema debe gestionar usuarios.  
RF-10: El sistema debe bloquear usuarios con multas.  

---

## 🔒 Requisitos No Funcionales

RNF-01: El sistema debe ser fácil de usar.  
RNF-02: El sistema debe responder en menos de 2 segundos.  
RNF-03: El sistema debe proteger los datos de usuarios.  
RNF-04: El sistema debe tener disponibilidad continua.  
RNF-05: El sistema debe ser escalable.  

---

## 🧪 Escenarios Gherkin

Feature: Préstamo de libros  

Scenario: Registrar préstamo exitoso  
Given el estudiante está activo  
And el libro está disponible  
When el bibliotecario registra el préstamo  
Then el sistema guarda el préstamo  
And actualiza el libro como prestado  

---

Feature: Devolución de libro  

Scenario: Registrar devolución con retraso  
Given el préstamo está vencido  
When el bibliotecario registra la devolución  
Then el sistema calcula la multa  
And actualiza el estado del libro  

---

## 🤖 Validación (IA)

- Se detectó falta de automatización en el sistema actual  
- Se identificaron riesgos de errores humanos  
- Se definieron requisitos para evitar inconsistencias  