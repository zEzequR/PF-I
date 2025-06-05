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

| Nombre              | Descripcion                                    | Tipo     | Longitud | Dominio                                                                       |
| ------------------- | ---------------------------------------------- | -------- | -------- | ----------------------------------------------------------------------------- |
| IDUser              | identificador unico de usuario                 | int      | 3        | 0-9                                                                           |
| nombreUsuario       | nombre del usuario                             | str      | 15       | Continuo                                                                      |
| contraseña          | clave de acceso del usuario                    | str      | 20       | Continuo                                                                      |
| tipoUsuario         | identificador para el administrador o empleado | int      | 1        | Discreto [0 / 1]                                                              |
| IDEmpleado          | identificador unico de empleado                | int      | 3        | 0-9                                                                           |
| nombre              | nombre del empleado                            | str      | 60       | a-Z                                                                           |
| apellido            | apellido del empleado                          | str      | 60       | a-Z                                                                           |
| sueldo              | sueldo del empleado                            | float    | 300      | 0-9                                                                           |
| monto total vendido | monto total de venta mensualmente              | float    | 300      | 0-9                                                                           |
| asistencia          | asistencia de los empleados                    | char     | 1        | Discreto [ P / A ]                                                            |
| IDAsistencia        | identificador unico de asistencia              | int      | 100      | 0-9                                                                           |
| fecha               | fecha actual para asistencia                   | date     | 8        | Continuo                                                                      |
| horaEntrada         | hora de entrada del empleado                   | datetime | 13       | Continuo                                                                      |
| horaSalida          | hora de salida del empleado                    | datetime | 13       | Continuo                                                                      |
| estado              | situacion del empleado                         | str      | 30       | Discreto [presente \| ausente \| tarde \| licencia]                           |
| IDVta               | identificador unico de venta                   | int      | 100      | 0-9                                                                           |
| IDCliente           | identificador unico de cliente                 | int      | 100      | 0-9                                                                           |
| tipoVta             | tipo de venta a realizar                       | int      | 2        | Discreto [0 / 1]                                                              |
| fechaVta            | fecha de la venta                              | date     | 10       | Continuo                                                                      |
| montoTotal          | monto total de la venta                        | float    | 100      | 0-9                                                                           |
| tipoPago            | distintos metodos de pago                      | str      | 5        | Dicreto [efectivo \| débito \| crédito \| transferencia \| billetera virtual] |
| cuotas              | cantidad de cuotas accesible                   | int      | 2        | 0-9                                                                           |
| numAfiliado         | identificador unico de cada afiliado           | str      | 20       | Continuo                                                                      |
| nomObraSocial       | nombre de obra social                          | str      | 60       | a-Z                                                                           |
| fechaPrescripción   | fecha en la que se realizo la receta           | date     | 8        | Continuo                                                                      |
| matriculaMed        | patente del medico                             | int      | 8        | 0-9                                                                           |
| productosRecetados  | medicamento recetados por el medico            | str      | 400      | Continuo                                                                      |
| nombreCliente       | nombre del cliente                             | str      | 60       | a-Z                                                                           |
| apellidoCliente     | apellido del cliente                           | str      | 60       | a-Z                                                                           |
| email               | email del cliente                              | str      | 40       | Continuo                                                                      |
| númTel              | numero de telefono del cliente                 | str      | 20       | Continuo                                                                      |
| DNI                 | numero de DNI del cliente                      | str      | 10       | Continuo                                                                      |
| SaldoCtaCorriente   | saldo adeudado del cliente                     | float    | 100      | 0-9                                                                           |
| fechaHora           | fecha y hora de la venta realizada             | datetime | 13       | Continuo                                                                      |
| nombreFarmacia      | nombre del local                               | str      | 60       | a-Z                                                                           |
| Direccion           | direccion del local                            | str      | 60       | Continuo                                                                      |
| teléfono            | numero de telefono del local                   | str      | 100      | Continuo                                                                      |
| nombreMed           | nombre del/los medicamento/s                   | str      | 60       | a-Z                                                                           |
| precio              | precio del/los medicamento/s                   | float    | 100      | 0-9                                                                           |
| montoFinal          | monto de venta de/los medicamento/s            | float    | 100      | 0-9                                                                           |