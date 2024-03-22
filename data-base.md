# Base de datos

---

## Entidades

### estudiantes
- id_estudiante *(PK)*
- nombres
- apellidos
- fecha_nacimiento
- direccion

### tutores_x_estudiantes
- id_tutor_estudiante *(PK)*
- cedula

### docentes
- id_profesor *(PK)*
- nombres
- apellidos
- cedula

### materias
- id_materia *(PK)*
- nombre

### secciones
- id_seccion *(PK)*
- anio
- categoria
- id_profesor *(FK)*

### asistencias
- id_asistencia *(PK)*
- id_materia *(FK)*
- id_seccion *(FK)*
- fecha 

### asistencia_x_estudiante
- id
- id_estudiante *(FK)*
- id_asistencia *(FK)*
- presente

### calificaciones
- id_calificacion *(PK)*
- id_materia *(FK)*
- id_estudiante *(FK)*
- calificacion

---

## Módelo de negocios

- Una _sección_ tiene un _tutor_ **(1:1)**
- Una _asistencia_ pertenece _materia_ **(1:N)**
- Una _asistencia_ es de una _seccion_ **(1:N)**
- Una _asistencia-x-estudiante_ hace referencia a un _estudiante_ **(1:N)**
- Una _asistencia-x-estudiante_ pertenece a una _asistencia_ **(1:N)**
- Una _calificación_ hace referencia a una _materia_ **(1:N)**
- Una _calificación_ hace referencia a un _estudiante_ **(1:N)**