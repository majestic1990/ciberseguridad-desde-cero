# Día 4 - Enumeración del sistema

## Análisis realizado

Ejecuté el comando `uname -a`, el cual me permitió identificar información básica del sistema, como el kernel y el nombre del equipo.

Luego utilicé `cat /etc/os-release`, donde pude ver de forma clara que el sistema operativo es Linux Mint versión 22.3.

Posteriormente ejecuté `cat /etc/passwd`, donde observé múltiples usuarios del sistema, incluyendo:
- root
- usuarios del sistema
- mi usuario (majestic)

Esto me permitió entender que no solo existen usuarios humanos, sino también usuarios del sistema.

## Procesos activos

Con el comando `ps aux` observé los procesos en ejecución.

Identifiqué múltiples procesos ejecutados por:
- root
- majestic

Un proceso que me llamó la atención fue uno relacionado con Python, lo cual podría ser relevante dependiendo del contexto.

## Puertos abiertos

Usando `ss -tuln` identifiqué puertos abiertos:

- 631 (CUPS - impresión)
- 53 (DNS)

Observé que los puertos aparecen duplicados, lo cual se debe a que están abiertos en diferentes protocolos (TCP y UDP).

## Reflexión de ciberseguridad

La enumeración es una fase crítica en hacking, ya que permite recolectar información del sistema antes de intentar cualquier ataque.

Un atacante usaría esta información para:
- identificar servicios vulnerables
- detectar usuarios
- analizar procesos sospechosos
