# AEE. Bitácora III. Conexiones Empresariales
# Taller Técnico: Operación Escudo

## Fundamentos de Seguridad y Auditoría

### Reto de Investigación 1. Anatomía de Syslog
Syslog es un sistema de log que almacena mensajes y comandos, es la salida de un grupo de datos dados por el sistema de entradas de Jobs. Cualquier instalación debería de darnos el syslog cada cierto tiempo para comprobar si hay problemas. 
El syslog son:
- Todos los mensajes dados de macros WTL
- Todos los mensajes introducidos por comandos de LOG
- Log hard-copy
- Todos los mensajes dirigidos al syslog desde cualquier sitio

El sistema clasifica los eventos cruzando dos variables:
- **Facility (Facilidad)**:
    Los tipos de mensajes son:
    - auth
    - authpriv
    - cron
    - daemon
    - kern
    - lpr
    - mail
    - mark
    - news
    - security
    - syslog
    - user
    - uucp
    - localo-local7

- **Severity (Prioridad)**:
    Los niveles de la prioridad de la información son:
    - debug 
    - info 
    - notice 
    - warning 
    - warn 
    - err 
    - error 
    - crit 
    - alert 
    - emerg 
    - panic


[1]

Es una negligencia grave que el archivo _/var/log/auth.log_ tenga permisos de lectura para usuarios no privilegiados ya que tiene todos los registros de todos los accesos. Si cualquier usuario puede leerlo, un atacante podría obtener los nombre válidos del sistema para realizar ataques de fuerza bruta, facilitandole la entrada al sistema.

La información registrada para un intento fallido de conexión remota mostrará su IP externa, su SSHD y su PID, mientras que para un fallo de contrasella de un usuario local mostrará la terminal local TTY y el proceso de validación del sistema.

### Referencias
[1] M. B. Alonso Alegre Díez, "Gestión de Logs," Trabajo Fin de Máster, Universidad Internacional de La Rioja (UNIR), 2016. [En línea]. Disponible en: https://reunir.unir.net/bitstream/handle/123456789/3618/ALONSO-ALEGRE%20DIEZ%2C%20MARIA%20BEGO%C3%91A.pdf 