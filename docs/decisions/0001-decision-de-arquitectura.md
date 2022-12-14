# Decisión de Arquitectura Principal

* Status: proposed
* Date: 2022-11-05

Technical Story: Selección de estilo por eventos para cubrir arquitectura principal del proyecto

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para cubrir los requisitos de comunicación entre sensores IoT y notificación de eventos

## Considered Options

* Estilo por eventos
* Estilo por capas
* Estilo cliente-servidor

## Decision Outcome

Chosen option: "Estilo por eventos", because se adapta adecuadamente al diseno del sistema.

### Positive Consequences

* Porque se ajusta a las necesidades de la arquitectura
* Porque cumple con la funcionalidad de notificar eventos
* Porque reacciona a eventos que se generan de forma no voluntaria

### Negative Consequences

* Porque cuando se producen muchos eventos simultáneos pueden surgir colapsos

## Pros and Cons of the Options

### Estilo por eventos

* Good, because comunica eventos que surgen de forma no voluntaria.
* Good, because cumple con las partes de la arquitectura como un centro de Gestiones que seria el Gestor de Eventos, produce eventos y tiene un consumidor de eventos.
* Good, because es escalable y distribuida.
* Bad, because posibilidad de desborde.

### Estilo por capas

* Good, because aparentemente cumplía con los requisitos de diseño y cómo se comunicaban los diferentes componentes.
* Good, because facilita la estandarización.
* Bad, because es poco eficiente.
* Bad, because en caso de que se necesitase contactar con capas superiores no se podria.

### Estilo cliente-servidor

* Good, because se reduce el tráfico de red considerablemente. Idealmente, el cliente se comunica con el servidor utilizando un protocolo de alto nivel de abstracción como por ejemplo SQL.
* Bad, because el usuario final no debería tener relación bidireccional con el servidor.
* Bad, because es dependiente de una red de internet.
* Bad, because no permite hacer diferencias notables entre usuarios.

## Links

* 0008 Estilo Por Capas
* 0007 Estilo Por Eventos
* 0009 Estilo Por Cliente Servidor
