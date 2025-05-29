
# ***Reglas de negocio***

># ***Hechos:*** 
>>* El cliente siempre es atendido por un vendedor
>>* Cada empleado tiene su comisión por ventas de 1% de las ventas mensuales
>>*   El sistema acepta efectivo, débito, crédito, transferencia y billeteras virtuales
>>*   Para ventas por obra social, el sistema precarga datos de afiliación y receta, pero el vendedor confirma el pedido
>>* Los descuentos solo aplican a pagos en efectivo
>>* Se mostrará un resumen antes de confirmar la compra
>>* Por cada venta se registra al cliente
>>* Los clientes frecuentes pueden abrir cuenta corriente
>>* Los clientes tendrán descuentos en productos seleccionados
>>* El salario del empleado no se verá modificado si sus inasistencias están justificadas
>>* Los empleados recibirán 20% de descuento en transacciones efectuadas


># ***Restricciones:***
>>* No venderle a clientes que adeudan por más de 15 días
>>* No imprimir ticket si el pago no se realizó
>>* El empleado solo puede ver el pedido
>>* Clientes que hayan comprado por obra social no pueden abonar con tarjeta crédito
>>* El sistema no debe habilitar pago con tarjeta de crédito si no pasa el monto de 70.000
>>* Los clientes que no superen por lo menos 1 compra semanal durante los últimos 3 meses, no se les podrá abrir una cuenta corriente en el sistema
>>* No se venderán productos psicotrópicos a menos que se cuente con una receta
>>* Los productos con cadena de frío, deben retirarse en el local
>>* Los productos que hayan quedado pendientes, únicamente se retirarán con el comprobante

># ***Acciones Disparadoras:***
>>* Enviar el pedido al proveedor cuando la existencia llegue al stock de seguridad
>>*  Si es el primer día del mes, generar un informe de las ventas del mes anterior.
>>* si la venta es con obra social entonces se obtendrá un descuento dependiendo de la obra social que tenga el cliente
>>* Si el empleado llega a vender 60 productos vendidos al mes, entonces comenzará a acumular comisiones
>>* Si el empleado tiene más de 4 inasistencias entonces se le sacara su comisión del mes
>>* Si el cliente es frecuente entonces obtendrá un descuento especial del 10% en compras en efectivo


># ***Cálculos:***
>>* El total del sueldo se calcula con los días de asistencia más la comisión y las horas extras
>>*  La comisión se calculará por el 1% del total de las ventas mensuales
>>* El valor del producto se calcula en base al precio de lista más el porcentaje de ganancias (70%)
>>* El total de la caja del día se calcula sumando todas las ventas facturadas.
>>* Si el cliente desea abonar con tarjeta en más de 3 cuotas, se le agregará un recargo del 20% por cada cuota adicional
># ***Inferencias:***
>>* --
