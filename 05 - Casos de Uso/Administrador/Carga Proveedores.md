# Caso de uso: Carga de proveedores
>**Actores primarios:** Administrador.
**Actores secundarios:** Base de datos.

# Precondiciones: 
- El administrador debe haber iniciado sesión en el sistema.

# Camino básico:
> 1)El administrador accede de Proveedores.
2)El administrador ingresa los datos del proveedor:

- nombre

- email

- número de teléfono

- formato de envío preferido

3)El administrador confirma los datos.
4)El sistema agrega el nuevo proveedor a la base de datos.

# Camino alternativo:

3.a) Si falta un dato obligatorio o hay un formato inválido, el sistema muestra un mensaje de error y solicita la corrección.
3.b) Si ya existe el laboratorio a cargar, el sistema muestra: "Proveedor ya registrado” y no guarda los datos.
4.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al agregar al proveedor. Intente nuevamente más tarde”.

# Escenario de éxito:

> El proveedor queda registrado correctamente en la base de datos y ya se dispone para enviar detalles de pedidos.

# Escenario de fracaso:

> El laboratorio no se puede registrar por error de conexión
