## Antes de realizar cambios a lo loco en un entorno de producción, un buen administrador debe investigar y fundamentar sus decisiones. La improvisación técnica suele derivar en fallos de seguridad críticos o en servidores inoperativos. Utilizad vuestro acceso a las bases de datos académicas [1] para dotar de base científica y metodológica a vuestro trabajo:

El estandar Syslog es el registro de las distribuciones Unix/linux.Para organizar el caos de mensajes que genera el sistema para ello usa dos variables que son Facility y Severity.

# Facility: Se encarga de definir la categoria o el origen del mensaje .Permite al administrador separar los logs por su procedencia.

# Severity: Es el indice de importancia que tiene cada registro guardado en el syslog y va del 7 que es un simple bug hasta
0 que es una emergencia que tenemos que solucionarlo lo antes posible 

 ## Además, responde a esto: ¿Por qué es una negligencia grave que el archivo /var/log/auth.log tenga permisos de lectura para usuarios no privilegiados?
Porque un usuario sin privilegio accediera a auth.log seria la posivilidad de que un usuario quiera entrar a nuestro servidor sin permiso remotamente y ese es el arcgivo log que guarda los intentos de acceso no permitidos lo que podria hacer que borrara las pruebas.

## ¿Qué información específica (como PIDs, nombres de usuario o direcciones IP) diferencia un intento fallido de conexión remota SSH de un simple fallo de contraseña de un usuario local frente a la pantalla?



