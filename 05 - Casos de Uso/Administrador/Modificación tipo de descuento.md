### **Caso de uso: Modificación de tipo de descuento**

**Actores primarios:** Administrador **Actores secundarios:** Base de datos

**Precondiciones:**

* El administrador debe haber iniciado sesión en el sistema.  
* El tipo de descuento debe existir en el sistema previamente.

**Camino básico:**

1. El administrador accede al módulo de gestión de descuentos. 2\) Selecciona la opción “Modificar tipo de descuento”. 3\) El administrador busca y selecciona el descuento a modificar por medio de una lista que puede ser filtrada por motivo o estado. 4\) El administrador cambia uno o más atributos del objeto tipo de descuento:  
* Motivo  
* Porcentaje  
* Fecha Inicio  
* Fecha Fin  
5. El administrador confirma la modificación. 6\) El sistema actualiza el descuento en la base de datos.

**Camino alternativo:**

3.a) El administrador no puede modificar el descuento porque la base de datos no puede obtener la lista para mostrar. 5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al modificar. Intente nuevamente más tarde”. 5.b) No se puede realizar la modificación porque los datos ingresados son inconsistentes (Fecha de fin menor a fecha de inicio o porcentaje fuera de rango).

**Escenario de éxito:**

El tipo de descuento se modifica correctamente y se actualiza en el sistema, aplicando los nuevos valores a futuras ventas.

**Escenario de fracaso:**

El descuento no se actualiza por ingresar datos inválidos (fechas incoherentes) o error en la conexión con la base de datos.

