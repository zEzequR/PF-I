# Caso de uso: Modificación de proveedor
> **Actores primarios:** Administrador.  
> **Actores secundarios:** Base de datos, AuditLog.

# Precondiciones:
- El administrador debe haber iniciado sesión en el sistema con permisos para editar proveedores.  
- El proveedor a modificar debe existir en la base de datos.  

# Camino básico:
> 1)El administrador accede de Proveedores.
2)El administrador modifica los datos actuales del proveedor
3)El administrador confirma los datos.
4)El sistema actualiza el proveedor en la base de datos.

# Camino alternativo:
3.a) Si algún campo del laboratorio a modificar ya está asociado a otro, el sistema muestra: "Campo ya registrado” y no guarda los datos.
4.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al modificar al proveedor. Intente nuevamente más tarde”.

# Escenario de éxito:
> El administrador actualizó los datos del proveedor

# Escenario de fracaso:
> El laboratorio no se puede registrar por error de conexión
