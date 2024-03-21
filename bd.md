# Base de datos de proyecto integrador

## Entidades

### estudiantes
- id_estudiante *(PK)*
- nombres
- apellidos
- fecha_nacimiento

### padres_estudiantes
- id_padres *(PK)*
- nombres
- apelidos

### profesores
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
- id_ae
- id_estudiante *(FK)*
- id_asistencia *(FK)*
- presente

### calificaciones
- id_calificacion *(PK)*
- id_materia *(FK)*
- id_estudiante *(FK)*
- calificacion