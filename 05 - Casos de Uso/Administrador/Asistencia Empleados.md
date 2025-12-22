# Caso de uso: Asistencia de empleados
**Actores primarios:** Administrador
**Actores secundarios:** Base de datos

# Precondiciones: 
- El administrador debe haber iniciado sesión en el sistema.

# Camino básico:
1)El administrador accede al módulo de Asistencia.
2)El sistema muestra la lista de empleados.
3)El administrador selecciona a/los empleado/s al/los que desea registrar/les su asistencia/s.
4)El administrador completa los campos correspondientes de cada empleado:
- Fecha
- Hora de entrada y salida
- Estado(presente | ausente | tarde | licencia)

# Camino alternativo:

2.a) Se produce un error en la base de datos y el sistema no muestra a los empleados.
5.a) Si falta información obligatoria, el sistema muestra: “Complete todos los campos requeridos”.
5.b) Si hay un error de conexión, el sistema indica: “Error al guardar, intente nuevamente”.
5.b.1) Si no se carga la asistencia de todos los empleados, el sistema muestra: “Complete la asistencia de todos los empleados”.

# Escenario de éxito:

 La asistencia del día queda registrada y disponible para consultas.

# Escenario de fracaso:

 No se registra la asistencia por datos incompletos, error del sistema o falta de conexión.
