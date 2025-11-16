# Caso de uso: Carga de clientes frecuentes

> **Actores primarios:** Administrador
> **Actores secundarios:** Base de datos

# Precondiciones: 
- El administrador debe haber iniciado sesión en el sistema.
- El administrador debe contar con los datos necesarios del nuevo cliente (Nombre de cliente, Mail, Número de telefono y DNI).
- El cliente debe cumplir los requisitos para abrir cuenta corriente (mínimo 1 compra semanal en los últimos 3 meses y no tener deudas mayores a 15 días).

# Camino básico:
> 1)El usuario accede al módulo de gestión de clientes.
2)Selecciona la opción “Registrar cliente frecuente”.
3)El administrador ingresa la información requerida: 
- Nombre de cliente
- Mail
- Numero de telefono
- DNI
- Detalles de pedidos
- Saldo en cuenta
> 4)El administrador confirma los datos.
5)El sistema registra el saldo a pagar del cliente frecuente.


# Camino alternativo:

> 4.a) Si ya existe un usuario con el mismo DNI o número de teléfono, el sistema muestra: “Cliente ya registrado” y no guarda los datos.
5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al agregar nuevo Cliente. Intente nuevamente más tarde”.

# Escenario de éxito:

> El cliente queda registrado como frecuente y tiene activa su cuenta corriente en el sistema.

# Escenario de fracaso:

> El cliente no se registra por error de conexión, Número de teléfono o DNI duplicado.
