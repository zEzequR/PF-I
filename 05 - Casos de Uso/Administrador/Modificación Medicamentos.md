# Caso de uso: Modificación de medicamentos

>**Actores primarios:** Administrador
**Actores secundarios:** Base de datos

# Precondiciones: 
- El sistema debe estar conectado a la base de datos.
- El administrador debe haber iniciado sesión en el sistema.
- El medicamento debe existir en el sistema previamente.

# Camino básico:
>1)El administrador accede al módulo de gestión de medicamentos.
2)Selecciona la opción “Modificar medicamento”.
3)El administrador busca y selecciona el medicamento a modificar por medio de una lista que puede ser filtrada por nombre, categoría o precio.
4)El administrador cambia uno o más atributos del objeto medicamento: 
- Codigo de barra
- Nombre de medicamento
- Descripción(duplicado requerido)
- Laboratorio
- Precio unitario
- Stock
>5)El administrador confirma la modificación.
6)El sistema elimina el registro del medicamento de la base de datos.

# Camino alternativo:

> 3.a) El administrador no puede modificar el medicamento porque la base de datos no puede obtener los medicamentos para mostrar en la lista.
5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al modificar. Intente nuevamente más tarde”.
5.b) No se puede realizar la modificación porque se intentó cambiar el código de barras.(No se pueden modificar, solo agregar).

# Escenario de éxito:

> El medicamento se modifica correctamente y se actualiza en el sistema

# Escenario de fracaso:

> El medicamento no se actualiza por editar campos o atributos primarios para el sistema (código de barra), error en la conexión con la base de datos.
