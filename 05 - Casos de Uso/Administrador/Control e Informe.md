# Caso de uso: Control e informe
**Actores primarios:** Administrador.
**Actores secundarios:** Base de datos.

# Precondiciones: 
- El administrador debe haber iniciado sesión en el sistema.
- Los proveedores están registrados en el sistema con datos de contacto (email y/o WhatsApp) para los envíos de pedidos.

# Camino básico:
 1)El administrador accede al módulo de control y reportes.
2)El administrador selecciona el tipo de dato que quiere ver (ej.: ventas en deter fecha, productos con stock ≤ stock_min, listado completo de productos, etc).
3)El sistema carga en una tabla todos los datos correspondientes.
4)El administrador selecciona los datos que quiere para guardarlos y/o enviarlos en formato PDF.

# Camino alternativo:

 2.a.1) El administrador selecciona la opción para ver las ventas del mes.
2.a.2) El administrador selecciona la opción para ver el stock de los productos.
3.a.1) El administrador busca y selecciona el/los medicamento/s por medio de una lista que puede ser filtrada por año/mes/semana/dia.
3.a.2) El administrador no puede obtener el/los medicamento/s porque la base de datos no puede obtener los medicamentos para mostrar en la lista.
3.a.3) El sistema muestra los medicamentos en una tabla.
3.b.1) El administrador busca y selecciona el/los medicamento/s por medio de una lista que puede ser filtrada por nombre del producto, categoria, precio o laboratorio.
3.b.2) Si no existen productos que cumplan el filtro, el sistema muestra “Sin resultados”.
3.b.3) El administrador no puede obtener el/los medicamento/s porque la base de datos no puede obtener los medicamentos para mostrar en la lista.
3.b.4) El sistema muestra los medicamentos en una tabla.
4.a) El PDF no se pudo guardar y/o envíar debido a un error al crearlo.
4.b)El PDF se generó correctamente pero no se pudo envíar al proveedor debido a un error en el sistema de correos y/o controlador.

# Escenario de éxito:

 El administrador pudo generar el informe o el próximo pedido de medicamentos (y enviárselo al proveedor).

# Escenario de fracaso:

 El administrador no pudo generar el informe o el pedido de medicamentos debido a un error en la base de datos, el PDF no se pudo generar debido a un error o el PDF con el pedido no se pudo envíar al laboratorio debido a un error en el controlador y/o sistema de correos.
