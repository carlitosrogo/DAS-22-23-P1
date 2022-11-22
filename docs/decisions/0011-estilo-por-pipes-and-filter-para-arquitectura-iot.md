# Estilo por Pipes and Filter para Arquitectura IoT

* Status: rejected
* Date: 2022-11-22

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para la comunicación entre sensores IoT

## Considered Options

* Estilo por Pipes And Filter

## Decision Outcome

Chosen option: "Estilo por Pipes And Filter"

### Positive Consequences

* Porque se ajusta a las necesidades de la arquitectura
* Porque cumple con la funcionalidad de notificar eventos
* Porque reacciona a eventos que se generan de forma no voluntaria

### Negative Consequences

* Porque cuando se producen muchos eventos simultáneos pueden surgir colapsos

## Pros and Cons of the Options

### Estilo por Pipes And Filter

* Good, because comunica eventos que surgen de forma no voluntaria.
* Good, because cumple con las partes de la arquitectura como un centro de Gestiones que seria el Gestor de Eventos, produce eventos y tiene un consumidor de eventos.
* Good, because es escalable y distribuida.
* Bad, because posibilidad de desborde.
