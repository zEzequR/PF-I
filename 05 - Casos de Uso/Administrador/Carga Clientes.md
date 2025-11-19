# Caso de uso: Registro de cliente

 **Actores primarios:** Empleado.
 **Actores secundarios:** Base de datos.

# Precondiciones:

- El empleado debe haber iniciado sesión en el sistema.

# Camino básico:

1)El empleado accede al módulo de gestión de clientes.

2) El empleado ingresa los datos del cliente (dni, nombre y al menos email o teléfono).

3) El sistema valida los formatos de email y/o teléfono.

4) El sistema registra el nuevo cliente.

5) El sistema muestra el mensaje: “Cliente registrado correctamente”.
   
# Camino alternativo:

3.a) Datos con formato inválido (email/teléfono mal formados): el sistema muestra error y el empleado corrige o confirma la corrección; no se guarda hasta validar.

3.b) El sistema rechaza la solicitud porque el cliente ya existe en el sistema.

4.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error. Intente nuevamente más tarde”.

Escenario de éxito:

 El empleado ingresa correctamente los datos, el sistema valida los formatos, verifica que el cliente no exista previamente y lo registra.
 Finalmente, muestra un mensaje de confirmación y el cliente queda disponible para futuras ventas o consultas.
# Escenario de fracaso:

El cliente no llega a registrarse porque los datos ingresados presentan formatos inválidos que no fueron corregidos, o porque el sistema detecta que el DNI o el teléfono ya existen registrados. También puede producirse un fallo de conexión con la base de datos que impida guardar la información
