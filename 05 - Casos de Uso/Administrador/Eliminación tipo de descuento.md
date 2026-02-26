# **Caso de uso: Eliminación de tipo de descuento**

**Actores primarios:** Administrador **Actores secundarios:** Base de datos

# **Precondiciones:** 

* El administrador debe haber iniciado sesión en el sistema.   
* El tipo de descuento debe existir en el sistema previamente.

# **Camino básico:**

1. El administrador accede al módulo de gestión de descuentos. 2\) Selecciona la opción “Eliminar tipo de descuento”. 3\) El administrador busca y selecciona el descuento a eliminar por medio de una lista que puede ser filtrada por motivo o porcentaje. 4\) El administrador confirma la eliminación. 5\) El sistema realiza la baja lógica enviando el mensaje setActivo(false) al objeto, dejándolo inhabilitado para futuras operaciones.

# **Camino alternativo:**

3.a) El administrador no puede eliminar el descuento porque la base de datos no puede obtener los registros para mostrar en la lista. 5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al eliminar. Intente nuevamente más tarde”.

# **Escenario de éxito:**
El tipo de descuento se desactiva correctamente (pasa a estado inactivo) y deja de estar disponible en el sistema para nuevas ventas.

# **Escenario de fracaso:** 
El tipo de descuento permanece activo por un error de conexión

