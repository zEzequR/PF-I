# Caso de uso: Carga de nuevos empleados

> *Actores primarios:* Administrador
> *Actores secundarios:* Base de datos

# Precondiciones:
- El administrador debe haber iniciado sesión en el sistema.
- El administrador debe contar con los datos necesarios del nuevo empleado.

# Camino básico:

> 1)El administrador accede al módulo de gestión de empleados.
2)Selecciona la opción “Agregar nuevo empleado”.
3)El administrador ingresa la información requerida: 
- Nombre de usuario
- Contraseña
- Monto total vendido
- Tipo de usuario(administrador | empleado) 
>4)El administrador confirma los datos.
5)El sistema agrega el nuevo empleado a la base de datos.


# Camino alternativo:

> 4.a) Si falta un dato obligatorio o hay un formato inválido, el sistema muestra un mensaje de error y solicita la corrección.
4.b) Si ya existe un usuario con el mismo nombre de usuario, el sistema muestra: “Empleado ya registrado” y no guarda los datos.
5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al agregar nuevo empleado. Intente nuevamente más tarde”.

# Escenario de éxito:

> El nuevo empleado queda registrado correctamente en la base de datos y puede iniciar sesión con sus credenciales.

# Escenario de fracaso:

> El empleado no se puede registrar por error de conexión, nombre de usuario duplicado

