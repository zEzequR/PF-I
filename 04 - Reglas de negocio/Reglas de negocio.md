
# ***Reglas de negocio***

># ***Hechos:*** 
>>* El cliente siempre es atendido por un vendedor.
>>* Para ventas por obra social, el sistema precarga datos de afiliación y receta, pero el vendedor confirma el pedido.
>>* Los descuentos solo aplican a pagos en efectivo.
>>* Se mostrará un resumen antes de confirmar la compra.
>>* Por cada venta se registra al cliente.
>>* Los clientes frecuentes pueden abrir cuenta corriente.
>>* Los clientes tendrán descuentos en productos seleccionados.
>>* El salario del empleado no se verá modificado si sus inasistencias están justificadas.
>>* Los empleados recibirán 20% de descuento en transacciones efectuadas.
>>* El empleado ofrecerá verbalmente al cliente, en ventas sin receta y siempre sin obligarlo, dejar un medio de contacto (email o teléfono) para recibir el comprobante en caso de fallo de impresión y/o acceder al programa de cliente frecuente con beneficios. Si el cliente acepta, el empleado registrará el dato y el consentimiento en el sistema. Si el cliente se niega, el empleado registrará la venta a nombre de un cliente "anónimo" ya precargado en el sistema.
>>* Todos los proveedores (droguerías) con los que trabaje la farmacia deberán estar registrados en el sistema con los datos de contacto necesarios para envíar el detalle de pedido.


># ***Restricciones:***
>>* No venderle a clientes frecuentes que deben ($80.000 o más).
>>* El empleado solo puede ver el pedido.
>>* Clientes que hayan comprado por obra social no pueden abonar con tarjeta crédito (más de un pago).
>>* Por políticas internas de la farmacia, los clientes no podrán abonar con tarjeta de crédito (más de una cuota) en montos inferiores a $50.000.
>>* Los clientes que no sean frecuentes, no se les podrá abrir una cuenta corriente en el sistema.
>>* No se venderán productos psicotrópicos a menos que se cuente con una receta.
>>* Los productos con cadena de frío, deben retirarse en el local.
>>* Los productos que hayan quedado pendientes, únicamente se retirarán con el comprobante.

># ***Acciones Disparadoras:***
>>* Enviar el pedido al proveedor cuando la existencia llegue al stock de seguridad.
>>* Si es el primer día del mes, generar un informe de las ventas del mes anterior.

># ***Cálculos:***
>>* El valor del producto se calcula en base al precio de lista más el porcentaje de ganancias (70%).
>>* El total de la caja del día se calcula sumando todas las ventas facturadas.
>>* Si el cliente desea abonar con tarjeta en más de 3 cuotas, se le agregará un recargo del 20% por cada cuota adicional.
>>* Los clientes frecuentes obtendrán un 10% de descuento en efectivo.
>>* Si la venta es con receta, debe contemplarse y calcular el/los descuento/s a los medicamentos recetados para el precio final.

># ***Inferencias:***
>>* Si el cliente es frecuente ($400.000 gastados en la farmacia) entonces accedera a beneficios exclusivos.

