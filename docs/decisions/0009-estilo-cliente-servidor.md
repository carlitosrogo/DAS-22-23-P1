# Estilo cliente-servidor

* Status: rejected
* Date: 2022-11-22

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para cubrir los requisitos de comunicación entre sensores IoT y notificación de eventos

## Considered Options

* Estilo Cliente-Servidor

## Decision Outcome

Chosen option: "Estilo Cliente-Servidor"

### Positive Consequences

* se reduce el tráfico de red considerablemente. Idealmente, el cliente se comunica con el servidor utilizando un protocolo de alto nivel de abstracción como por ejemplo SQL.

### Negative Consequences

* el usuario final no debería tener relación bidireccional con el servidor.
* es dependiente de una red de internet.
* no permite hacer diferencias notables entre usuarios.

## Links

* 0001 Decision De Arquitectura
* 0008 Estilo Por Capas
* 0007 Estilo Por Eventos
