# Estilo Cliente-Servidor Arq. Centro Notificaciones

* Status: rejected
* Date: 2022-11-22

## Considered Options

* Estilo Cliente-Servidor

## Decision Outcome

Chosen option: "Estilo Cliente-Servidor"

### Positive Consequences

* los clientes tienen poca trascendencia en el esquema y sus necesidades de administración son menores.
* los recursos comunes a todos los usuarios se administran en el servidor. Así se evitan situaciones como la redundancia o inconsistencia de información en las bases de datos.
* al disponer de un mecanismo central de autenticación, las posibilidades de acceso indebido se reducen considerablemente.
* se pueden añadir o suprimir clientes sin que el funcionamiento de la red se vea afectado.

### Negative Consequences

* toda la red está construida al rededor del servidor y si éste deja de funcionar o lo hace con un rendimiento inadecuado, afectará a toda la infraestructura.
* tanto la instalación como el mantenimiento son más elevados debido al perfil muy técnico del lado servidor.

## Pros and Cons of the Options

### Estilo Cliente-Servidor

En una arquitectura Cliente-Servidor existe un servidor y múltiples clientes que se conectan al servidor para recuperar todos los recursos necesarios para funcionar, en este sentido, el cliente solo es una capa para representar los datos y se detonan acciones para modificar el estado del servidor, mientras que el servidor es el que hace todo el trabajo pesado.

## Links

* 0003 Decisión De Arquitectura Centro de Notificaciones
* 0012 Estilo Modelo Vista Controlador Arquitectura Centro Notificaciones
