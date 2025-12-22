# **Caso de uso: Carga de tipo de descuento**

**Actores primarios:** Administrador **Actores secundarios:** Base de datos

# **Precondiciones:** 
El administrador debe haber iniciado sesión en el sistema.

# **Camino básico:**

1. El administrador accede al módulo de gestión de descuentos.  
2. Selecciona la opción "Agregar nuevo tipo de descuento".  
3. El administrador ingresa la información requerida:  
* Motivo  
* Porcentaje   
* Fecha Inicio  
* Fecha Fin  
4. El administrador confirma la operación presionando “Guardar”.  
5. El sistema valida que el porcentaje sea correcto y almacena los datos en la base de datos.

# **Camino alternativo:** 
4.a) Los campos obligatorios no están completos o el porcentaje no es válido (ej: mayor a 100). 5.a) Si hay un error de conexión con la base de datos, el sistema muestra el mensaje: “Error al guardar. Intente nuevamente más tarde”. 5.b) El sistema detecta que ya existe un descuento con el mismo motivo y muestra error.

# **Escenario de éxito:** 
El tipo de descuento queda registrado correctamente en la base de datos y queda disponible para su aplicación en ventas.

# **Escenario de fracaso:** 
El sistema no guarda el descuento por datos inválidos, duplicados o por fallo en la conexión con la base de datos.

