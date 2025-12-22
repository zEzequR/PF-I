### **Caso de uso: Eliminación de tipo de descuento**

**Actores primarios:** Administrador **Actores secundarios:** Base de datos

**Precondiciones:** 

* El administrador debe haber iniciado sesión en el sistema.   
* El tipo de descuento debe existir en el sistema previamente.

**Camino básico:**

1. El administrador accede al módulo de gestión de descuentos. 2\) Selecciona la opción “Eliminar tipo de descuento”. 3\) El administrador busca y selecciona el descuento a eliminar por medio de una lista que puede ser filtrada por motivo o porcentaje. 4\) El administrador confirma la eliminación. 5\) El sistema da de baja el registro del descuento en la base de datos (baja lógica).

**Camino alternativo:**

3.a) El administrador no puede eliminar el descuento porque la base de datos no puede obtener los registros para mostrar en la lista. 4.a) El sistema verifica que el tipo de descuento no esté asociado a ventas históricas para no romper la integridad de los informes. 5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al eliminar. Intente nuevamente más tarde”.

**Escenario de éxito:** El tipo de descuento se elimina (o desactiva) correctamente y deja de estar disponible en el sistema para nuevas ventas.

**Escenario de fracaso:** El tipo de descuento no se elimina porque está asociado a ventas previas, hubo un error de conexión en la base de datos y el administrador no puede seleccionar ni eliminar el registro.

