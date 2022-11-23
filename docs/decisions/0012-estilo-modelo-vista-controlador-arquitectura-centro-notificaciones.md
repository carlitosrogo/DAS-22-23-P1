# Estilo Modelo Vista Controlador Arquitectura Centro Notificaciones

* Status: accepted
* Date: 2022-11-22

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para nuestro centro de notificaciones para gestionar las notificaciones y eventos.

## Considered Options

* Estilo Modelo Vista Controlador

## Decision Outcome

Chosen option: "Estilo Modelo Vista Controlador", because se adpata mejor a las funcionalidades del paquete y requisitos que se indentificaron.

### Positive Consequences

* Porque se ajusta a las necesidades de la arquitectura
* Porque cumple con la funcionalidad de notificar eventos
* Porque reacciona a eventos que se generan de forma no voluntaria

### Negative Consequences

* Porque cuando se producen muchos eventos simultáneos pueden surgir colapsos

## Pros and Cons of the Options

### Estilo Modelo Vista Controlador

* Good, because comunica eventos que surgen de forma no voluntaria.
* Good, because cumple con las partes de la arquitectura como un centro de Gestiones que seria el Gestor de Eventos, produce eventos y tiene un consumidor de eventos.
* Good, because es escalable y distribuida.
* Bad, because posibilidad de desborde.
