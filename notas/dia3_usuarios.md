Día 3 - Usuarios y privilegios

# Día 3 - Usuarios y privilegios en Linux

## ¿Qué vi?

Ejecuté el comando `whoami` para identificar el usuario actual.

Luego usé `id`, lo que me permitió ver:
- UID (identificador del usuario)
- GID (grupo)
- grupos asociados

Después ejecuté:
sudo -l

Con esto pude ver qué permisos tengo como usuario para ejecutar comandos con privilegios elevados.

También utilicé:
cat /etc/passwd | grep majestic

Aquí identifiqué:
- mi usuario
- mi directorio home
- mi shell

## ¿Qué no logré hacer?

Intenté ejecutar:
cat /etc/shadow

Pero obtuve un error de "permiso denegado".

## ¿Por qué ocurrió?

El archivo `/etc/shadow` contiene información sensible (contraseñas encriptadas) y solo puede ser accedido por el usuario root.

Esto demuestra que no todos los archivos pueden ser leídos por cualquier usuario.

## ¿Quién manda en el sistema?

El usuario root tiene control total sobre el sistema. Puede leer, modificar o ejecutar cualquier archivo.

## ¿Qué puede hacer cada usuario?

Cada usuario tiene permisos específicos definidos por el sistema. Esto sigue el principio de mínimo privilegio, donde cada usuario solo debe tener acceso a lo necesario.

Una mala configuración de permisos puede generar vulnerabilidades, como escalamiento de privilegios.

## ¿Cómo funciona sudo?

El comando `sudo` permite ejecutar comandos con privilegios elevados (como root), usando la autenticación del usuario actual.

## Conceptos adicionales

- `x` (ejecución): permite ejecutar archivos o scripts, lo cual puede ser peligroso si el archivo es malicioso.
- `-` = archivo
- `d` = directorio

## Comandos usados

- whoami = usuario actual
- id = información del usuario
- sudo -l = permisos de sudo
- cat = ver contenido
- grep = filtrar información
