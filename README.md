# Seguridad
Notas Generales


## Herramientas

### Nmap

- Escaneo de ping: Verifica si los hosts están activos. ``` nmap -sn <target> ```
- Escaneo de puertos: Identifica puertos abiertos en los hosts. ``` nmap -p 1-65535 <target> ```
- Descubre qué servicios se están ejecutando en los puertos abiertos. ``` nmap -sV <target> ```
- Intenta identificar el sistema operativo del host. ``` nmap -O <target> ```
- Utiliza scripts de Nmap para una variedad de tareas de auditoría y detección. ``` nmap --script=<script-name> <target> ```
