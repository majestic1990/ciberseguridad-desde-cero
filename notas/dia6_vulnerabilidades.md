# Día 6 - Análisis de vulnerabilidades

Primero ejecuté el comando `ss -tulnp`, el cual muestra puertos, procesos y PID.

Luego identifiqué puertos importantes como:
- 53 → DNS
- 631 → CUPS

Posteriormente utilicé `ps -fp PID` para analizar procesos.

## ¿Qué servicio es?

El puerto 53 corresponde al servicio DNS (Domain Name System), encargado de resolver nombres de dominio.

También observé el proceso `ksmd`, el cual pertenece al kernel de Linux y no es un servicio de red.

## ¿Para qué sirve?

- DNS: traduce nombres de dominio a direcciones IP
- ksmd: optimiza el uso de memoria RAM en el sistema

## ¿Tiene vulnerabilidades?

Los servicios como DNS pueden tener vulnerabilidades dependiendo de la implementación.

El proceso ksmd también ha tenido investigaciones relacionadas con seguridad, especialmente en ataques avanzados de memoria.

## ¿Qué pasaría si es explotado?

- DNS vulnerable → redirección de tráfico, ataques MITM
- ksmd vulnerable → posible fuga de información o ataques de memoria
