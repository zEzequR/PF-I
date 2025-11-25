# Diccionario de datos

>**Medicamento** = @codBarra + nombreMed + (descripción) + drogueria + precioMedUnitario + stock
**Usuario** = nombreUsuario + contraseña + [tipoUsuario]
**Tipo de Usuario** = [administrador | empleado]
**Empleado** = nombreEmpleado
**Asistencia** = fecha + (horaEntrada) + (horaSalida) + [estado]
**Estado** = [presente | ausente | tarde | licencia]
**Venta** = [tipoVta] + fechaVta + montoTotal + [tipoPago] + (cuotas) + estadoVenta + nroVta
**Tipo Venta** = [ particular | obraSocial]
**Obra Social** = nombreObrasocial
**Pago** = numTransaccion + [tipoPago] + monto + (cuotas) + fechaPago + estadoPago
**ticket** = DatosFarmacia + fechaHora + DatosCliente + nroTicket + EstadoTicket + pdfPath
**Detalles Pedido** = 1{nombreMed + precio}x + montoFinal + numPedido + estadoPedido + pathPdf + drogueria
**Receta** = nroReceta
**Detalle Venta** = montoFinal + nroDetalleVenta + precio
**Tipo Descuento** = motivo + porcentaje + fechainicio + fechaFinal + estado
**Cliente** = email + nombreCliente + numTel + DNI + SaldoCtaCorriente + tipoCliente + montoAcumulado
**Cobertura** = numAfiliado + descuento
**Medico** = matriculaMed + nombreMedico
**Drogueria** = nombre + direccion + email + numTel + formatoEnvio
**Detalle receta** = fechaPrescripcion + matriculaMedico + productosRecetados


| Nombre               | Descripción                                            | Tipo     | Longitud | Dominio / Observaciones                                                         |
|----------------------|--------------------------------------------------------|----------|----------|----------------------------------------------------------------------------------|
| codBarra             | identificador único del medicamento                    | int      | 50       | 0-9                                                                               |
| nombreMed            | nombre del medicamento                                 | str      | 60       | A-Z                                                                               |
| descripcion          | descripción del medicamento                            | str      | 200      | continuo                                                                          |
| drogueria            | nombre de la droguería                                 | str      | 60       | A-Z                                                                               |
| precioMedUnitario    | precio del medicamento                                 | float    | 100      | 0-9                                                                               |
| stock                | cantidad disponible                                    | int      | 10       | 0-9                                                                               |
| nombreUsuario        | nombre del usuario                                     | str      | 15       | continuo                                                                          |
| contraseña           | clave de acceso del usuario                            | str      | 20       | continuo                                                                          |
| tipoUsuario          | tipo de usuario                                        | str      | 10       | discreto [administrador \| empleado]                                             |
| nombreEmpleado       | nombre del empleado                                    | str      | 60       | A-Z                                                                               |
| fecha                | fecha de asistencia                                    | date     | 10       | continuo                                                                          |
| horaEntrada          | hora de ingreso                                        | datetime | 13       | continuo                                                                          |
| horaSalida          | hora de salida                                         | datetime | 13       | continuo                                                                          |
| estadoAsistencia     | estado de asistencia                                   | str      | 10       | discreto [presente \| ausente \| tarde \| licencia]                              |
| tipoVta              | tipo de venta                                          | str      | 15       | discreto [particular \| obraSocial]                                              |
| fechaVta             | fecha de la venta                                      | date     | 10       | continuo                                                                          |
| montoTotal           | monto total de venta                                   | float    | 100      | 0-9                                                                               |
| tipoPago             | método de pago                                         | str      | 20       | discreto [efectivo \| debito \| credito \| transferencia \| billetera virtual]   |
| cuotas               | cuotas de la venta                                     | int      | 2        | 0-9                                                                               |
| estadoVenta          | estado de la venta                                     | str      | 20       | continuo                                                                          |
| nroVta               | número de venta (PK)                                   | int      | 10       | 0-9                                                                               |
| nombreObraSocial     | nombre de la obra social                               | str      | 60       | A-Z                                                                               |
| numTransaccion       | número de transacción                                  | int      | 10       | 0-9                                                                               |
| monto                | monto de pago                                          | float    | 100      | 0-9                                                                               |
| fechaPago            | fecha del pago                                         | date     | 10       | continuo                                                                          |
| estadoPago           | estado del pago                                        | str      | 20       | continuo                                                                          |
| DatosFarmacia        | información de la farmacia                             | str      | 200      | continuo                                                                          |
| fechaHora            | fecha y hora del ticket                                | datetime | 13       | continuo                                                                          |
| DatosCliente         | información del cliente en el ticket                   | str      | 200      | continuo                                                                          |
| nroTicket            | número del ticket                                      | int      | 10       | 0-9                                                                               |
| EstadoTicket         | estado del ticket                                      | str      | 20       | continuo                                                                          |
| pdfPath              | ruta del archivo PDF                                   | str      | 200      | continuo                                                                          |
| precio               | precio unitario (pedido/detalle venta)                 | float    | 100      | 0-9                                                                               |
| montoFinal           | monto final del detalle                                | float    | 100      | 0-9                                                                               |
| numPedido            | número del pedido                                      | int      | 10       | 0-9                                                                               |
| estadoPedido         | estado del pedido                                      | str      | 20       | continuo                                                                          |
| pathPdf              | ruta del PDF del pedido                                | str      | 200      | continuo                                                                          |
| nroReceta            | número de receta (PK)                                  | int      | 10       | 0-9                                                                               |
| fechaValidez         | fecha de validez de receta                             | date     | 10       | continuo                                                                          |
| tipoReceta           | tipo de receta                                         | str      | 20       | continuo                                                                          |
| nroDetalleVenta      | número del detalle de venta                            | int      | 10       | 0-9                                                                               |
| motivo               | motivo del descuento                                   | str      | 60       | A-Z                                                                               |
| porcentaje           | porcentaje aplicado                                    | float    | 5        | 0-100                                                                             |
| fechainicio          | inicio del descuento                                   | date     | 10       | continuo                                                                          |
| fechaFinal           | fin del descuento                                      | date     | 10       | continuo                                                                          |
| estado               | estado del descuento                                   | str      | 20       | continuo                                                                          |
| email                | email del cliente                                      | str      | 40       | continuo                                                                          |
| nombreCliente        | nombre del cliente                                     | str      | 60       | A-Z                                                                               |
| numTel               | teléfono del cliente                                   | str      | 20       | continuo                                                                          |
| DNI                  | documento del cliente (PK)                             | str      | 10       | continuo                                                                          |
| SaldoCtaCorriente    | saldo pendiente del cliente                            | float    | 100      | 0-9                                                                               |
| tipoCliente          | tipo de cliente                                        | str      | 20       | continuo                                                                          |
| montoAcumulado       | monto acumulado del cliente                            | float    | 100      | 0-9                                                                               |
| numAfiliado          | número de afiliado                                     | str      | 20       | continuo                                                                          |
| descuento            | porcentaje de descuento aplicado                        | float    | 5        | 0-100                                                                             |
| matriculaMed         | matrícula del médico                                   | int      | 8        | 0-9                                                                               |
| nombreMedico         | nombre del médico                                      | str      | 60       | A-Z                                                                               |
| direccion            | dirección de la droguería                              | str      | 100      | continuo                                                                          |
| formatoEnvio         | tipo de envío que maneja la droguería                  | str      | 20       | continuo                                                                          |
| fechaPrescripcion    | fecha de prescripción                                  | date     | 10       | continuo                                                                          |
| productosRecetados   | productos incluidos en la receta                       | str      | 400      | continuo                                                                          |
