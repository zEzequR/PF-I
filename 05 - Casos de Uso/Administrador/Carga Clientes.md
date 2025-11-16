# Caso de uso: Registro de cliente

> **Actores primarios:** Empleado.
> **Actores secundarios:** Base de datos, Cliente, Ticketera.

# Precondiciones:

- El empleado debe haber iniciado sesión en el sistema y estar atendiendo una venta sin receta.

# Camino básico:

> 1)El empleado, durante la atención de una venta sin receta, ofrece verbalmente al cliente dejar un medio de contacto (email o teléfono) para envío de comprobante y beneficios como cliente frecuente.

2)Si el cliente acepta, el empleado ingresa en el sistema los datos mínimos (dni, nombre y al menos email o teléfono).

3)El sistema valida formatos (email/teléfono), registra el cliente.

4)El sistema asocia la venta al cliente nuevo registrado.

# Camino alternativo:

2.a) El cliente rechaza dejar datos:
2.a.1) El empleado registra la venta a nombre de un cliente "anónimo".

2.b) La ticketera falla después de cobrar:
2.b.1) Si el cliente ya proporcionó contacto, el sistema encola envío del comprobante.
2.b.2) Si el cliente no había dejado contacto, el sistema solicita al empleado que intente obtener al menos email o teléfono; si el cliente se niega, registrar al cliente como "anónimo" y cancelar la impresión o envío del comprobante, sólo guardarla localmente.

3.a) Datos con formato inválido (email/teléfono mal formados): el sistema muestra error inline y el empleado corrige o confirma la corrección; no se guarda hasta validar.

3.b) El sistema rechaza la solicitud porque el cliente ya existe en el sistema.

4.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al eliminar. Intente nuevamente más tarde”.

Escenario de éxito:

> El empleado ofreció verbalmente la oferta, el cliente aceptó, los datos fueron validados y guardados y la venta quedó asociada al cliente; si la ticketera falla, se encoló el envío del comprobante al contacto proporcionado.

# Escenario de fracaso:

No se pudo registrar al cliente por rechazo del cliente, formatos inválidos no corregidos, cliente ya existente en el sistema o error de base de datos; la venta se completó pero a nombre de un cliente "anónimo", si la impresora falló y no hay contacto, la venta se realiza pero sin entregar ningún comprobante al cliente.