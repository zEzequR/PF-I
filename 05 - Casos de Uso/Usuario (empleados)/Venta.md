# Caso de uso: Venta


**Actores primarios:** Empleado y Administrador.
**Actores secundarios:** Base de datos, Cliente, Ticketera y Posnet, Sistema de recetas / obra social y Sistema de correos

# Precondiciones:

- El empleado/administrador debe haber iniciado sesión en el sistema.
- La ticketera debe estar conectada al sistema.

# Camino básico:

1)El administrador/empleado accede al módulo de venta.
2)El administrador/empleado selecciona o crea el cliente (o marca “Cliente anónimo”)
3)El administrador/empleado selecciona la manera en la que se van a vender el/los medicamentos (con receta/sin receta).
4)El administrador/empleado busca y selecciona el/los medicamento/s a facturar por medio de una lista que puede ser filtrada por nombre comercial o droga.
5)El administrador/empleado pide los datos al cliente y selecciona el método a pagar.
6)Se registran todos los datos de la venta y del cliente en la base de datos y se imprime el ticket con los detalles de la venta.

# Camino alternativo:

2.a.1) Si el cliente no está en el sistema, el empleado solicita datos mínimos:

- Nombre del cliente

- Email (opcional, recomendado para comprobante)

- Número de teléfono (opcional, recomendado para comprobante)

- DNI (Obligatorio)

3.a.1) El administrador/empleado selecciona que la venta es con Receta.
3.b.1) El administrador/empleado selecciona que la venta es Particular.
3.c.1) El administrador/empleado selecciona que la venta es por Obra Social.
3.c.2) El administrador/empleado completa los campos correspondientes con los datos de la receta/afiliación para tramitar cobertura o reintegro:

- Nombre de la obra social

- Número de afiliado

- Fecha de prescripción

- Fecha de venta

- Matrícula del médico

- Productos recetados

5.a.1) Dependiendo del tipo de pago se aplicarán descuentos (efectivo y promociones aplicables) o intereses al precio final según las reglas de recargo por cuotas; además, algunos métodos pueden quedar deshabilitados por políticas (obra social no se permiten cuotas).

5.a.1) Error en la base de datos (p. ej. fallo transaccional): la operación finaliza con error; se devuelve mensaje al empleado y no se persiste la venta. (Si el pago ya fue procesado, seguir procedimientos de conciliación/refund).
5.a.2) Pago rechazado por saldo insuficiente o tarjeta denegada y la venta no se completa.
5.a.3) La venta se registra y el pago se confirma, pero la impresión falla: la venta queda registrada; el empleado solicita email/teléfono al cliente (si no lo tenía) y el sistema envía el ticket por correo/wsp.

# Escenario de éxito:

La venta se registra correctamente, el pago queda confirmado, el stock se actualiza y el ticket se imprime o se envía por mail/WhatsApp si la ticketera falló y se obtuvo contacto del cliente.

# Escenario de fracaso:

La venta no pudo registrarse debido a: validación fallida de receta o afiliación (cuando corresponde), pago rechazado, o error crítico en la base de datos. Si la impresión falla después del cobro y no se obtuvo contacto del cliente, la venta queda registrada y se documenta la incidencia y se notifica al administrador para el seguimiento.
