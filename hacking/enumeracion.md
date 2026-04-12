# Enumeración

## ¿Qué es enumeración?

Es el proceso de recolectar información del sistema objetivo.

Es el primer paso en cualquier proceso de hacking.

## ¿Por qué es importante?

Permite identificar:
- sistema operativo
- usuarios
- procesos activos
- servicios y puertos abiertos

Con esta información, un atacante puede encontrar posibles vulnerabilidades.

## Comandos usados

- uname -a = información básica del sistema
- cat /etc/os-release = información detallada del sistema
- cat /etc/passwd = usuarios
- ps aux = procesos activos
- ss -tuln = puertos abiertos
