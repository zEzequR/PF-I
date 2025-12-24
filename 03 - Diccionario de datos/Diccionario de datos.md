# Diccionario de datos
**Medicamento** = @codBarra + nombreMed + (descripción) + drogueria + precioMedUnitario + precioCosto + stock + stockMinimo + esControlado + [activo] 
**Usuario** = nombreUsuario + contraseña + [tipoUsuario] 
**Tipo de Usuario** = [administrador | empleado] 
**Empleado** = nombreEmpleado + legajo + sueldo + cuil + email + direccion + [rol] 
**Direccion** = calle + numero + localidad + provincia + cp 
**Asistencia** = fecha + (horaEntrada) + (horaSalida) + [estado] 
**Estado** = [presente | ausente | tarde | licencia] 
**Venta** = [tipoVta] + fechaVta + montoTotal + [tipoPago] + (cuotas) + estadoVenta + nroVta 
**Tipo Venta** = [ particular | obraSocial] 
**Obra Social** = nombreObrasocial + (descuentoGeneral) 
**Pago** = numTransaccion + [tipoPago] + monto + (cuotas) + fechaPago + estadoPago 
**Ticket** = DatosFarmacia + fechaHora + DatosCliente + nroTicket + EstadoTicket + pdfPath 
**Pedido** = numPedido + fechaPedido + estadoPedido + pathPdf + drogueria 
**Detalles Pedido** = numPedido + codBarra + nombreMedicamento + cantidad 
**Receta* = nroReceta + fechaPrescripcion + matriculaMedico + fechaValidez + pathImagen 
**Detalle Venta** = nroDetalleVenta + codBarra + nombreMedicamento + cantidad + precioUnitario + montoFinal 
**Tipo Descuento** = motivo + porcentaje + fechainicio + fechaFinal + activo 
**Cliente** = email + nombreCliente + numTel + DNI + SaldoCtaCorriente + tipoCliente + montoAcumulado + esFrecuente 
**Cobertura** = numAfiliado + descuento 
**Medico** = matriculaMed + nombreMedico + email + numTel 
**Drogueria** = nombre + direccion + email + numTel + canalPreferido + cuit 
**Detalle receta** = productosRecetados + indicaciones


| Nombre | Descripción | Tipo | Longitud | Dominio / Observaciones |
| :--- | :--- | :--- | :--- | :--- |
| codBarra | identificador único del medicamento | int | 50 | 0-9 |
| nombreMed | nombre del medicamento | str | 60 | A-Z |
| descripcion | descripción del medicamento | str | 200 | continuo |
| drogueria | nombre de la droguería | str | 60 | A-Z |
| precioMedUnitario | precio de venta del medicamento | float | 100 | 0-9 |
| precioCosto | precio de costo (compra a droguería) | float | 100 | 0-9 |
| stock | cantidad disponible actual | int | 10 | 0-9 |
| stockMinimo | cantidad mínima para alerta de reposición | int | 10 | 0-9 |
| esControlado | indica si requiere receta archivada | boolean | 1 | True / False |
| activo | indica si el registro está habilitado (baja lógica) | boolean | 1 | True / False |
| nombreUsuario | nombre del usuario para login | str | 15 | continuo |
| contraseña | clave de acceso del usuario | str | 20 | continuo |
| tipoUsuario | tipo de usuario (rol) | str | 10 | discreto [administrador \| empleado] |
| nombreEmpleado | nombre del empleado | str | 60 | A-Z |
| legajo | número de legajo del empleado | int | 10 | 0-9 |
| sueldo | salario del empleado | float | 100 | 0-9 |
| cuil | clave única de identificación laboral | str | 13 | 0-9 (formato XX-XXXXXXXX-X) |
| calle | calle de la dirección | str | 100 | A-Z, 0-9 |
| numero | altura/número de la dirección | int | 10 | 0-9 |
| cp | código postal | str | 10 | continuo (alfanumérico) |
| localidad | localidad o ciudad | str | 60 | A-Z |
| provincia | provincia o estado | str | 60 | A-Z |
| fecha | fecha de asistencia | date | 10 | continuo |
| horaEntrada | hora de ingreso | datetime | 13 | continuo |
| horaSalida | hora de salida | datetime | 13 | continuo |
| estadoAsistencia | estado de asistencia | str | 10 | discreto [presente \| ausente \| tarde \| licencia] |
| tipoVta | tipo de venta | str | 15 | discreto [particular \| obraSocial] |
| fechaVta | fecha de la venta | date | 10 | continuo |
| montoTotal | monto total de venta | float | 100 | 0-9 |
| tipoPago | método de pago | str | 20 | discreto [efectivo \| debito \| credito \| transf] |
| cuotas | cantidad de cuotas (si aplica) | int | 2 | 0-9 |
| estadoVenta | estado de la venta | str | 20 | continuo |
| nroVta | número de venta (PK) | int | 10 | 0-9 |
| nombreObraSocial | nombre de la obra social | str | 60 | A-Z |
| numTransaccion | número de transacción de pago | int | 10 | 0-9 |
| monto | monto del pago parcial o total | float | 100 | 0-9 |
| fechaPago | fecha del pago | date | 10 | continuo |
| estadoPago | estado del pago | str | 20 | continuo |
| DatosFarmacia | información legal de la farmacia | str | 200 | continuo |
| fechaHora | fecha y hora del ticket | datetime | 13 | continuo |
| DatosCliente | información del cliente impresa | str | 200 | continuo |
| nroTicket | número único del ticket | int | 10 | 0-9 |
| EstadoTicket | estado del ticket | str | 20 | continuo |
| pdfPath | ruta del archivo PDF (pedido/ticket) | str | 200 | continuo |
| precioUnitario | precio al momento de la venta (detalle) | float | 100 | 0-9 |
| montoFinal | subtotal del detalle (precio x cantidad) | float | 100 | 0-9 |
| numPedido | número del pedido a droguería | int | 10 | 0-9 |
| estadoPedido | estado del pedido | str | 20 | continuo |
| cantidad | cantidad de unidades (venta/pedido) | int | 5 | 1-9999 |
| nroReceta | número de receta (PK) | int | 10 | 0-9 |
| fechaValidez | fecha de vencimiento de receta | date | 10 | continuo |
| tipoReceta | tipo de receta | str | 20 | continuo |
| nroDetalleVenta | identificador del detalle de venta | int | 10 | 0-9 |
| motivo | motivo del descuento | str | 60 | A-Z |
| porcentaje | porcentaje aplicado (0.0 a 1.0) | float | 5 | 0-100 |
| fechainicio | inicio de vigencia del descuento | date | 10 | continuo |
| fechaFinal | fin de vigencia del descuento | date | 10 | continuo |
| email | email de contacto (cliente/prov/emp) | str | 40 | continuo (formato email) |
| nombreCliente | nombre completo del cliente | str | 60 | A-Z |
| numTel | teléfono de contacto | str | 20 | continuo |
| DNI | documento nacional de identidad | str | 10 | 0-9 |
| SaldoCtaCorriente | saldo deudor del cliente | float | 100 | 0-9 |
| tipoCliente | categoría del cliente | str | 20 | continuo |
| montoAcumulado | monto total comprado (para fidelización) | float | 100 | 0-9 |
| esFrecuente | indica si es cliente frecuente | boolean | 1 | True / False |
| numAfiliado | número de afiliado a obra social | str | 20 | continuo |
| descuento | valor del descuento específico | float | 5 | 0-100 |
| matriculaMed | matrícula profesional del médico | int | 8 | 0-9 |
| nombreMedico | nombre del médico | str | 60 | A-Z |
| canalPreferido | medio de contacto/envío droguería | str | 20 | discreto [email \| telefono \| web] |
| cuit | clave única de id. tributaria (droguería) | str | 13 | 0-9 (formato XX-XXXXXXXX-X) |
| fechaPrescripcion | fecha en que se recetó | date | 10 | continuo |
| productosRecetados | texto con medicamentos recetados | str | 400 | continuo |
