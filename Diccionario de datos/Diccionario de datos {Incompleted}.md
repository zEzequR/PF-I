# Diccionario de datos

>**Medicamentos** = @IDMed + nombreMed + (descripción) + laboratorio + precioMedUnitario + stock
**Usuario** = @IDUser + nombreUsuario + contraseña + montoTotalendido + [tipoUsuario]
**Tipo de Usuario** = [administrador | empleado]
**Empleado** = @IDEmpleado + IDUsuario + nombre + apellido + sueldo + monto total vendido + asistencia
**Asistencia** = @IDAsistencia + IDEmpleado + fecha + (horaEntrada) + (horaSalida) + [estado]
**Estado** = [presente | ausente | tarde | licencia]
**Ventas** = @IDVta + IDEmpleado + IDCliente + [tipoVta] + DatosCliente + fechaVta + montoTotal + [tipoPago] + (cuotas)
**Tipo Venta** = [ particular | obraSocial]
**Obra Social** = @numAfiliado + nomObraSocial + fechaPrescripción + fechaVenta + matriculaMed + 1{productosRecetados}x
**TipoPago** = [efectivo | débito | crédito | transferencia | billetera virtual]
**Datos Cliente**= @IDCliente + nombreCliente + apellidoCliente + (email) + númTel + DNI + (DetallesPedidos) + (SaldoCtaCorriente)
**ticket** = DatosFarmacia + fechaHora + DatosCliente + detallesPedido
**DatosFarmacia** = nombreFarmacia + Direccion + teléfono
**Detalles Pedido** = 1{nombreMed + precio}x + montoFinal

