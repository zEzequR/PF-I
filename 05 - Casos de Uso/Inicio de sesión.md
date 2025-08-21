# Caso de uso: Inicio de sesión

> **Actores primarios:** Administrador, empleado
> **Actores secundarios:** Base de datos
>**Precondiciones:** El sistema debe estar conectado a la red 


# Camino básico:

- El usuario ingresa al sistema.
- El usuario ingresa sus credenciales.
- El sistema verifica los datos ingresados.
- El sistema concede acceso y muestra la pantalla principal.

# Camino alternativo:

> 2.a) Si alguno de los campos está vacío, el sistema muestra un mensaje: "Debe completar todos los campos".
> 3.a) Las credenciales están vacías o son incorrectas.
 > 4.a) El sistema no logra la conexión con la base de datos, el sistema muestra un mensaje: "Error de conexión".
> 4.a.1) El usuario vuelve al inicio de sesión.

# Escenario de éxito:

> El usuario ingresa al sistema, sus credenciales son correctas, se conecta a la base de datos correctamente e ingresa al menú correspondiente(administrador-empleado).

# Escenario de fracaso:

> 1)Las credenciales son incorrectas y el usuario no puede ingresar al sistema.
> 2)Se produce un error de conexión a la base de datos y el sistema no puede validar sus credenciales ni continuar correctamente con su funcionamiento
