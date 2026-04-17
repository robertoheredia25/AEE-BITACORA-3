## Fundamentos de Seguridad y Auditoría
## Reto de Investigación 1
# Antes de realizar cambios a lo loco en un entorno de producción, un buen administrador debe investigar y fundamentar sus decisiones. La improvisación técnica suele derivar en fallos de seguridad críticos o en servidores inoperativos. Utilizad vuestro acceso a las bases de datos académicas [1] para dotar de base científica y metodológica a vuestro trabajo:

El estandar Syslog es el registro de las distribuciones Unix/linux.Para organizar el caos de mensajes que genera el sistema para ello usa dos variables que son Facility y Severity.

# Facility: Se encarga de definir la categoria o el origen del mensaje .Permite al administrador separar los logs por su procedencia.

# Severity: Es el indice de importancia que tiene cada registro guardado en el syslog y va del 7 que es un simple bug hasta
0 que es una emergencia que tenemos que solucionarlo lo antes posible 

 ## Además, responde a esto: ¿Por qué es una negligencia grave que el archivo /var/log/auth.log tenga permisos de lectura para usuarios no privilegiados?
Porque un usuario sin privilegio accediera a auth.log seria la posivilidad de que un usuario quiera entrar a nuestro servidor sin permiso remotamente y ese es el arcgivo log que guarda los intentos de acceso no permitidos lo que podria hacer que borrara las pruebas.

## ¿Qué información específica (como PIDs, nombres de usuario o direcciones IP) diferencia un intento fallido de conexión remota SSH de un simple fallo de contraseña de un usuario local frente a la pantalla?

Si es un intento fallido de ssh te sañe sshd daemon que muestra que han intentado entrar al servidor atra vez de ssh otra cosa que lo canta todo es la dirrecion de ip de origen  y el pid corresponde con un sshd y no con un inicio de sesion local 

# Mensajes clave

Failed password for [usuario] from [IP] port [puerto] ssh2.
Invalid user [usuario] from [IP]... Intento de fuerza bruta
PAM [número] more authentication failures; logname= uid=0 euid=0 tty=:0 ruser=.... Inicio de sesion fallido por contraseña ejemplo

## Reto de Investigación 2
# Cumplimiento y Log Management. Busca en Dialnet o Semantic Scholar artículos sobre Log Management (Gestión centralizada de registros). A nivel empresarial y legal (piensa en el RGPD en España), ¿qué ventajas vitales ofrece enviar y custodiar los logs en un servidor externo seguro en lugar de mantenerlos dispersos e indefensos en la propia máquina que podría ser vulnerada?

La gestion centralizada o log management no es solo uan buena pratica tecnologica en el panorama actual en el mundo de la ciberseguirdad y normativas relacionadas es una necesidad critica. Tal y como señala la literatura academica e investigaciones indexadas en bases de datos como Dialnet la capacidad de recolectar corelacionar y proteger los log siendo su proposito primordial la seguridad.
Esto lo que hace es no tener los log dentro del equipo que pudieran hackear






