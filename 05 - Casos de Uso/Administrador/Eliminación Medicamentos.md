# Caso de uso: Eliminación de medicamentos

 **Actores primarios:** Administrador
**Actores secundarios:** Base de datos

# Precondiciones: 
- El administrador debe haber iniciado sesión en el sistema.
- El medicamento debe existir en el sistema previamente.

# Camino básico:

1)El administrador accede al módulo de gestión de medicamentos.
2)Selecciona la opción “Eliminar medicamento”.
3)El administrador busca y selecciona el medicamento a eliminar por medio de una lista que puede ser filtrada por nombre, categoría o precio.
4)El administrador confirma la eliminación.
5)El sistema elimina el registro del medicamento de la base de datos.


# Camino alternativo:

3.a) El administrador no puede eliminar el medicamento porque la base de datos no puede obtener los medicamentos para mostrar en la lista.
4.a) El sistema verifica que el medicamento no esté asociado a ventas pendientes o pedidos abiertos.
5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al eliminar. Intente nuevamente más tarde”.

# Escenario de éxito:

El medicamento se elimina correctamente y deja de existir en el sistema

# Escenario de fracaso:

El medicamento no se elimina porque está asociado a una venta, hubo un error de conexión en la base de datos y el administrador no puede seleccionar ni eliminar un producto.

