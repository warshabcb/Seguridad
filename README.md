# Seguridad
Notas Generales


## Herramientas

### Nmap

- Escaneo de ping: Verifica si los hosts están activos.
  ``` nmap -sn <target> ```
- Escaneo de puertos: Identifica puertos abiertos en los hosts.
  ``` nmap -p 1-65535 <target> ```
  o puertos especificos
  ``` nmap -p 22,80,443 <target> ```
- Descubre qué servicios se están ejecutando en los puertos abiertos.
  ``` nmap -sV <target> ```
- Intenta identificar el sistema operativo del host. ``` nmap -O <target> ```
- Utiliza scripts de Nmap para una variedad de tareas de auditoría y detección. ``` nmap --script=<script-name> <target> ```
- El escaneo agresivo (-A) activa la detección de sistema operativo, versión de servicios, ejecución de script y traceroute: nmap -A <target>
- Muchos servicios utilizan UDP, y este escaneo puede revelar más sobre el objetivo.  ``` nmap -sU <target> ```
- Nmap ofrece varias técnicas para evadir firewalls y sistemas de detección de intrusos, como fragmentación de paquetes (-f) y el uso de tiempos específicos para evitar la detección de patrones (-T):
  ```
  nmap -f <target>  # Fragmentación de paquetes
  nmap -T4 <target>  # Ajusta la velocidad del escaneo (0 es más lento, 5 es más rápido)
  ```
- El escaneo SYN (-sS) es menos intrusivo y más difícil de detectar que un escaneo de conect completo: ``` nmap -sS <target> ```
- El Nmap Scripting Engine (NSE) es extremadamente poderoso para realizar una variedad de tareas, desde la detección avanzada hasta la explotación y la auditoría de seguridad:
  ``` nmap --script=<category> <target> ``` Puedes especificar categorías como ```default```, ```safe```, ```vuln```, ```exploit```, entre otras.
- Nmap puede generar resultados en varios formatos, útiles para el análisis posterior o la integración con otras herramientas:
  ```
  nmap -oX output.xml <target>  # Salida en XML
  nmap -oN output.nmap <target>  # Salida en formato normal
  nmap -oG output.gnmap <target>  # Salida en formato grepable
  ```
    
