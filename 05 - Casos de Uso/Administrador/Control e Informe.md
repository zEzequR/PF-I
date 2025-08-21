# Caso de uso: Control e informe
>**Actores primarios:** Administrador.
**Actores secundarios:** Base de datos.

# Precondiciones: 
- El sistema debe estar conectado a la base de datos.
- El administrador debe haber iniciado sesión en el sistema.

# Camino básico:
> 1)El administrador accede al módulo de control y reportes.
2)El administrador selecciona el tipo de dato que quiere ver.
3)El sistema carga en una tabla todos los datos correspondientes.
4)El administrador selecciona los datos que quiere para guardarlos localmente en un PDF.

# Camino alternativo:

> 2.a.1) El administrador selecciona la opción para ver las ventas del mes.
2.a.2) El administrador selecciona la opción para ver el stock de los productos.
3.a.1) El administrador busca y selecciona el/los medicamento/s por medio de una lista que puede ser filtrada por año/mes/semana/dia.
3.a.2) El administrador no puede obtener el/los medicamento/s porque la base de datos no puede obtener los medicamentos para mostrar en la lista.
3.a.3) El sistema muestra los medicamentos en una tabla.
3.b.1) El administrador busca y selecciona el/los medicamento/s por medio de una lista que puede ser filtrada por nombre del producto, categoria, precio o laboratorio.
3.b.2) El administrador no puede obtener el/los medicamento/s porque la base de datos no puede obtener los medicamentos para mostrar en la lista.
3.b.3) El sistema muestra los medicamentos en una tabla.
4.a) El PDF no se pudo guardar localmente debido a un error al crearlo.

# Escenario de éxito:

> El administrador pudo generar el informe de ventas del mes o el próximo pedido de medicamentos.

# Escenario de fracaso:

> El administrador no pudo generar el informe de ventas o el pedido de medicamentos debido a un error en la base de datos, el PDF no se pudo generar debido a un error.
