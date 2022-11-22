# Estilo Modelo Vista Controlador Arquitectura Centro Notificaciones

* Status: accepted
* Date: 2022-11-22

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para nuestro centro de notificaciones para gestionar las notificaciones y eventos

## Considered Options

* Estilo Modelo Vista Controlador

## Decision Outcome

Chosen option: "Estilo Modelo Vista Controlador", because se adpata mejor a las funcionalidades del paquete y requisitos que se indentificaron.

### Positive Consequences

* Separación clara de las distintas partes del sistema (lógica, datos, y la interfaz).
* Buena seguridad para los datos almacenados ya que el usuario no interactua directamente con los datos, si no que pasa primeramente por un controlador.

### Negative Consequences

* La navegación por el código puede ser compleja al disponer de más componentes, lo que se traduce en un mayor número de archivos o unidades.
* Tener varias capas nos incrementa la complejidad del sistema.
* Agrega complejidad al sistema.

## Links

* 0013 Estilo Cliente-Servidor Arquitectura Centro de Notificaciones
