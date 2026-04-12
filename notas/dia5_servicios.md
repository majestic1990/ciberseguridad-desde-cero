# Día 5 - Análisis de servicios

Primero ejecuté el comando `ss -tulnp`, el cual muestra los puertos abiertos, procesos y el PID (identificador de procesos).

Esto me permitió identificar qué procesos están usando los puertos.

Observé que el proceso `firefox-bin` estaba usando puertos dinámicos (ejemplo: 45788 y 36306), lo cual es normal para aplicaciones cliente.

También identifiqué puertos abiertos importantes:
- 631 → servicio de impresión (CUPS)
- 53 → servicio DNS

## Análisis

- Firefox corre como usuario, lo cual es correcto.
- El puerto 631 pertenece a un servicio del sistema, no al navegador.
- Si un servicio es vulnerable, un atacante podría:
  - robar información
  - ejecutar código
  - comprometer el sistema

## Comandos usados

- ss -tulnp = muestra puertos, procesos y PID
- lsof -i :631 = muestra qué proceso usa el puerto
- ps -fp PID = muestra información detallada del proceso
