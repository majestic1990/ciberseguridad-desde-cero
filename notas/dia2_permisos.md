# Día 2 - Permisos en Linux

## ¿Qué vi antes y después?

Inicialmente ejecuté el comando `ls -la`, el cual me permitió ver todos los archivos, incluyendo los ocultos (los que empiezan con `.`).

Observé que cada archivo tiene una estructura como:

-rw-rw-r--

Esto representa los permisos del archivo.

Luego creé un archivo con:
touch prueba.txt

Volví a ejecutar `ls -la` y vi el nuevo archivo con permisos por defecto.

Después ejecuté:
chmod 777 prueba.txt

Al revisar nuevamente, los permisos cambiaron a:

rwxrwxrwx

Esto significa que todos los usuarios (dueño, grupo y otros) tienen permisos de lectura, escritura y ejecución.

## ¿Qué cambié?

Modifiqué los permisos del archivo `prueba.txt`, pasando de permisos limitados a permisos totales.

## ¿Qué significan los permisos?

Los permisos indican qué acciones puede realizar cada tipo de usuario:

- Dueño
- Grupo
- Otros

Permisos:
- r = lectura
- w = escritura
- x = ejecución

## Comandos usados

- chmod = cambiar permisos
- 777 = dar permisos totales (rwx) a todos 

## Reflexión de ciberseguridad

El uso de `chmod 777` es peligroso porque permite que cualquier usuario modifique o ejecute el archivo.

Esto puede representar una vulnerabilidad, ya que un atacante podría aprovechar estos permisos para modificar archivos críticos o intentar escalar privilegios.
