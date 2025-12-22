# Caso de uso: Eliminación de proveedor
 **Actores primarios:** Administrador.  
 **Actores secundarios:** Base de datos.

# Precondiciones:
- El administrador debe haber iniciado sesión en el sistema. 
- El proveedor a eliminar debe existir en la base de datos.  

# Camino básico:
1)El administrador accede de Proveedores.
2)Selecciona la opción “Eliminar proveedor".
3)El administrador busca y selecciona el proveedor a eliminar por medio de una lista que puede ser filtrada.
4)El administrador confirma la eliminación.
5)El sistema elimina el proveedor de la base de datos.

# Camino alternativo:
4.a) El sistema no puede eliminar al proveedor debido a que ya existen productos asociados.
5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al eliminar. Intente nuevamente más tarde”.

# Escenario de éxito:
El proveedor se elimina correctamente y deja de existir en el sistema

# Escenario de fracaso:
El proveedor no se elimina porque está asociado a un/os medicamentos y/o hubo un error de conexión en la base de datos.
