# Decisión De Arquitectura Centro de Notificaciones

* Status: accepted
* Date: 2022-11-13

Technical Story: Selección de estilo de arquitectura secundaria para el centro de notificaciones

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para nuestro centro de notificaciones para gestionar las notificaciones y eventos

## Considered Options

* Estilo modelo vista controlador
* Estilo cliente-servidor

## Decision Outcome

Chosen option: "Estilo modelo vista controlador", because se adpata mejor a las funcionalidades del paquete y requisitos que se indentificaron.

### Positive Consequences

* Separación clara de las distintas partes del sistema (lógica, datos, y la interfaz).
* Buena seguridad para los datos almacenados ya que el usuario no interactua directamente con los datos, si no que pasa primeramente por un controlador.

### Negative Consequences

* La navegación por el código puede ser compleja al disponer de más componentes, lo que se traduce en un mayor número de archivos o unidades.
* Tener varias capas nos incrementa la complejidad del sistema.
* Agrega complejidad al sistema.

## Pros and Cons of the Options

### Estilo modelo vista controlador

Consiste en un patrón de diseño de software que se utiliza para separar en tres componentes los datos, la metodología y la interfaz gráfica de una aplicación.

* Good, because separación clara de dónde tiene que ir cada tipo de lógica, facilitando el mantenimiento y la escalabilidad de nuestra aplicación.
* Good, because sencillez para crear distintas representaciones de los mismos datos.
* Good, because reutilización de los componentes.
* Bad, because la separación de conceptos en capas agrega complejidad al sistema.
* Bad, because la cantidad de archivos a mantener y desarrollar se incrementa considerablemente

### Estilo cliente-servidor

En una arquitectura Cliente-Servidor existe un servidor y múltiples clientes que se conectan al servidor para recuperar todos los recursos necesarios para funcionar, en este sentido, el cliente solo es una capa para representar los datos y se detonan acciones para modificar el estado del servidor, mientras que el servidor es el que hace todo el trabajo pesado.

* Good, because los clientes tienen poca trascendencia en el esquema y sus necesidades de administración son menores.
* Good, because los recursos comunes a todos los usuarios se administran en el servidor. Así se evitan situaciones como la redundancia o inconsistencia de información en las bases de datos.
* Good, because al disponer de un mecanismo central de autenticación, las posibilidades de acceso indebido se reducen considerablemente.
* Good, because se pueden añadir o suprimir clientes sin que el funcionamiento de la red se vea afectado.
* Bad, because tanto la instalación como el mantenimiento son más elevados debido al perfil muy técnico del lado servidor.
* Bad, because toda la red está construida al rededor del servidor y si éste deja de funcionar o lo hace con un rendimiento inadecuado, afectará a toda la infraestructura.
