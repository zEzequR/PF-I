# Caso de uso: Venta
>**Actores primarios:** Empleado y Administrador.
**Actores secundarios:** Base de datos, Cliente, Ticketera y Posnet.

# Precondiciones: 
- El sistema debe estar conectado a la base de datos.
- El empleado/administrador debe haber iniciado sesión en el sistema.
- La ticketera debe estar conectada al sistema.

# Camino básico:

>1)El administrador/empleado accede al módulo de venta.
2)El administrador/empleado selecciona la manera en la que se van a vender el/los medicamentos (particular/obra social).
3)El administrador/empleado busca y selecciona el/los medicamento/s a facturar por medio de una lista que puede ser filtrada por nombre comercial o droga.
4)El administrador/empleado pide los datos al cliente y selecciona el método a pagar.
5)Se registran todos los datos de la venta y del cliente en la base de datos y se imprime el ticket con los detalles de la venta.

# Camino alternativo:

>2.a.1) El administrador/empleado selecciona que la venta va a ser por particular.
2.b.1) El administrador/empleado selecciona que la venta va a ser por obra social.
2.b.2) El administrador/empleado completa los campos correspondientes con los datos de la receta para realizar el descuento en la venta:
- Nombre de la obra social
- Número de afiliado
- Fecha de prescripción
- Fecha de venta
- Matricula del medico
- Productos recetados
>4.a.1) El administrador/empleado selecciona el método de pago.
4.a.2) Dependiendo del tipo de pago se aplicarán descuentos (efectivo) o intereses al precio final y dependiendo el monto final de la compra algunos métodos de pago no estarán disponibles.
4.b.1) El administrador/empleado busca si ese cliente ya compró anteriormente y corrobora si es un cliente frecuente para aplicar descuentos exclusivos.
4.b.2) El administrador/empleado le pide los datos correspondientes al cliente:
- Nombre del cliente
- Apellido del cliente
- Email (opcional)
- Numero de telefono
- DNI
>5.a.1) No se pudo realizar la venta ni el registro debido a que hubo un error en la base de datos.
5.a.2) El cliente no cuenta con el saldo suficiente en la tarjeta o billetera virtual.
5.a.3) La venta pudo realizarse pero no se imprimió el ticket debido a una falla en la ticketera.

# Escenario de éxito:

> La venta pudo realizarse y el ticket se imprimió con todos los datos de la venta con éxito.

# Escenario de fracaso:

> La venta y los registros no pudieron realizarse correctamente debido a un error en la base de datos, el cliente no contaba con duplicado para los medicamentos controlados, no contaba con suficiente saldo para abonar la compra. El ticket con los detalles de la venta no se imprimió debido a una falla en la ticketera.

