# Caso de uso: Carga de medicamentos

>**Actores primarios:** Administrador
**Actores secundarios:** Base de datos

# Precondiciones: 
- El administrador debe haber iniciado sesión en el sistema.

# Camino básico:

1)El administrador accede al módulo de gestión de medicamentos.
2)Selecciona la opción "Agregar nuevo medicamento".
3)El administrador ingresa la información requerida: 
- Codigo de barra
- Nombre de medicamento
- Drogueria
- Controlado
- Precio unitario
- Stock
4)El administrador confirma la operación presionando “Guardar”.
5)El sistema almacena los datos en la base de datos.



# Camino alternativo:

>5.a) Los campos obligatorios no están completos y con formato incorrecto.
7.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al guardar. Intente nuevamente más tarde”.

# Escenario de éxito:

>El medicamento queda registrado correctamente en la base de datos y queda disponible para su venta.

# Escenario de fracaso:

>El sistema no guarda el medicamento por datos incompletos o por fallo en la conexión con la base de datos.
